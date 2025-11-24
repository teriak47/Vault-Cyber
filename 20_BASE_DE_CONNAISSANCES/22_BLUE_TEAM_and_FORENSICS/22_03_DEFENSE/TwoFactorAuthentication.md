---
aliases:
  - Authentification à Deux Facteurs
  - Authentification forte
  - 2FA
  - MFA
  - Two-Factor Authentication
  - Multi-Factor Authentication
archetype: defense
type: Prévention
technologie:
  - Authentication
  - Identity & Access Management (IAM)
cssclasses:
  - max
tags:
  - authentification/multi-facteur
  - gestion-identite/acces
  - securite/mecanisme-defense
  - attaque/contournement-mfa
  - detection/authentification
---

# Two-Factor Authentication

> [!goal] Objectif de Sécurité
> Réduire considérablement le risque d'accès non autorisé aux comptes utilisateurs en exigeant une vérification d'identité supplémentaire au-delà du simple mot de passe, même si ce dernier est compromis. Cela prévient les attaques par *credential stuffing*, *brute force* et certaines formes de *phishing*.

## 🛡️ Mécanisme de Protection (Prevent)
L'authentification à deux facteurs (2FA) est une méthode d'authentification de sécurité qui exige deux formes d'identification distinctes avant d'accorder l'accès à un compte ou à un système. Elle est basée sur la combinaison de deux des trois "facteurs" suivants : "quelque chose que vous savez" (connaissance), "quelque chose que vous avez" (possession) et "quelque chose que vous êtes" (inhérence).

*   **Fonctionnement** :
    1.  **Premier facteur (Connaissance)** : L'utilisateur fournit généralement un mot de passe ou un code PIN.
    2.  **Deuxième facteur (Possession ou Inhérence)** : Après la vérification du premier facteur, le système demande une vérification supplémentaire.
        *   **Facteurs de Possession** (quelque chose que vous avez) :
            *   **Codes SMS/Email** : Un code unique est envoyé par SMS ou email au périphérique enregistré de l'utilisateur.
            *   **Applications TOTP (Time-based One-Time Password)** : Des applications comme Google Authenticator ou Authy génèrent des codes à usage unique qui changent toutes les 30 à 60 secondes.
            *   **Notifications Push** : Une notification est envoyée à un appareil mobile, demandant à l'utilisateur d'approuver ou de refuser la tentative de connexion.
            *   **Clés de sécurité matérielles (FIDO U2F/WebAuthn)** : Des dispositifs physiques comme les clés YubiKey qui s'insèrent dans un port USB ou se connectent via NFC/Bluetooth, nécessitant une interaction physique (toucher le bouton) pour l'authentification.
        *   **Facteurs d'Inhérence** (quelque chose que vous êtes) :
            *   **Biométrie** : Empreintes digitales, reconnaissance faciale ou balayage de l'iris.

*   **Configuration clé** :
    *   **Politique d'adoption** : Imposer le 2FA pour tous les comptes sensibles et encourager/forcer son utilisation pour tous les utilisateurs.
    *   **Types de 2FA prioritaires** : Préférer les méthodes basées sur la possession forte (clés de sécurité matérielles, applications TOTP) aux méthodes plus vulnérables (SMS).
    *   **Gestion des appareils de confiance** : Permettre aux utilisateurs de marquer des appareils comme "de confiance" pour réduire la fréquence des demandes 2FA sur ces appareils, tout en maintenant la sécurité.
    *   **Procédures de récupération de compte** : Mettre en place des processus robustes pour la récupération de compte en cas de perte du deuxième facteur, pour éviter les verrous légitimes.

## 🚨 Stratégie de Détection (Detect)
La surveillance des tentatives d'authentification 2FA peut révéler des activités suspectes et des tentatives de contournement.

*   **Logs à surveiller** :
    *   **Journaux d'authentification des systèmes/applications** : `Auth.log`, `Security Event Logs (Event ID 4624/4625 - Windows)`, journaux d'audit des services d'identité (Azure AD, Okta, Duo).
    *   **Journaux des serveurs d'authentification 2FA** : Logs des services de fourniture de codes TOTP, SMS ou notifications push.
    *   **Journaux de gestion des identités** : Modifications des méthodes 2FA enregistrées, réinitialisations de 2FA.

*   **Règle SIEM suggérée** :
```sql
// Détection de tentatives multiples d'authentification 2FA échouées pour un même utilisateur
SELECT COUNT(*) AS failed_2fa_attempts, user_id, source_ip
FROM authentication_logs
WHERE event_type = '2FA_failure'
  AND timestamp > NOW() - INTERVAL '5 minutes'
GROUP BY user_id, source_ip
HAVING failed_2fa_attempts > 5; // Seuil configurable

// Détection de l'enregistrement ou de la modification d'un nouveau deuxième facteur de manière inhabituelle
SELECT *
FROM identity_management_logs
WHERE event_type IN ('2FA_method_added', '2FA_method_changed', '2FA_reset')
  AND user_id IN (SELECT user_id FROM behavioral_analytics WHERE score > high_risk_threshold);
```

## ⚔️ Contournement Connu (Evasion)
> [!warning] Faiblesses
> Bien que le 2FA renforce considérablement la sécurité, il n'est pas infaillible et peut être contourné par des attaquants sophistiqués.
*   **Phishing de codes 2FA** : Les attaquants peuvent créer de fausses pages de connexion qui capturent à la fois les identifiants et le code 2FA en temps réel, puis les utilisent rapidement pour se connecter au compte légitime avant que le code n'expire.
*   **SIM Swapping / Permutation de carte SIM** : Un attaquant convainc l'opérateur téléphonique de la victime de transférer son numéro de téléphone vers une carte SIM contrôlée par l'attaquant, interceptant ainsi les codes 2FA envoyés par SMS.
*   **MFA Fatigue Attacks (Attaques par fatigue MFA)** : L'attaquant envoie de nombreuses requêtes de notification push 2FA à la victime, espérant qu'elle finira par approuver involontairement l'une d'elles par lassitude ou erreur.
*   **Malware (Maliciel)** : Certains malwares peuvent contourner le 2FA en accédant directement à la session authentifiée sur l'appareil de la victime ou en interceptant les codes 2FA.
*   **Attaques de l'homme du milieu (MitM)** : Un attaquant peut intercepter et relayer les requêtes d'authentification entre l'utilisateur et le service, y compris les informations 2FA, surtout si la connexion n'est pas sécurisée (HTTP au lieu de HTTPS).
*   **Vulnérabilités dans l'implémentation du 2FA** : Une mauvaise configuration ou des failles dans le déploiement du 2FA par le fournisseur de services peuvent permettre le contournement. Par exemple, des flux de récupération de compte faibles.

## 🔗 Notes Connexes
*   **Contre l'attaque** : CredentialStuffing
*   **Contre l'attaque** : PhishingAttack
*   **Implémenté par** : IdentityAccessManagementSystem