---
tags:
  - securite/multifacteur
  - authentification/biometrie
  - authentification
  - authentification/facteurs
aliases:
  - MFA
  - Multi-Factor Authentication
  - Authentification Multi-Facteurs
source:
  - 
cssclasses:
  - max
---

# Authentification Multi-Facteurs (MFA)

## 📥 Définition en une phrase
> L'Authentification Multi-Facteurs (MFA) est une méthode de vérification d'identité qui exige qu'un utilisateur fournisse deux ou plusieurs facteurs de vérification distincts pour accéder à un compte, un système ou une application.

## 🧠 Concepts Clés / Fonctionnement
*   **Facteurs d'authentification** : La MFA combine au moins deux des trois catégories de facteurs :
    *   **Ce que vous savez** (Knowledge Factor) : Un secret que seul l'utilisateur est censé connaître (ex: mot de passe, code PIN, réponse à une question secrète).
    *   **Ce que vous avez** (Possession Factor) : Un objet physique ou numérique que seul l'utilisateur possède (ex: smartphone pour TOTP, clé de sécurité U2F/FIDO2, carte à puce, jeton logiciel).
    *   **Ce que vous êtes** (Inherence Factor) : Une caractéristique biométrique unique à l'utilisateur (ex: empreinte digitale, reconnaissance faciale, scan rétinien).
*   **Renforcement de la sécurité** : En exigeant plusieurs types de preuves, la MFA réduit considérablement le risque d'accès non autorisé, car même si un facteur est compromis (ex: vol de mot de passe), l'attaquant ne pourra pas se connecter sans les autres facteurs.
*   **Méthodes courantes** :
    *   **OTP (One-Time Password)** : Codes à usage unique, générés par des applications (TOTP - Time-based OTP), envoyés par SMS ou email (bien que les SMS soient moins sécurisés).
    *   **Clés de sécurité physiques (FIDO/U2F)** : Dispositifs matériels qui offrent une authentification forte basée sur la cryptographie, résistante au [[Phishing|hameçonnage]].
    *   **Biométrie** : Intégrée aux appareils modernes (ex: Touch ID, Face ID).
*   **Adaptive MFA** : Peut ajuster les exigences d'authentification en fonction du contexte (localisation, appareil, heure, comportement de l'utilisateur).

## 🛡️ Risques / Menaces Associés
*   [[Phishing|Hameçonnage]] : Certaines formes de MFA (notamment par SMS) peuvent être contournées par des attaques de phishing sophistiquées ou des attaques de l'homme du milieu (AiTM).
*   [[SIMSwapping|Swap de carte SIM]] : Les attaquants peuvent détourner un numéro de téléphone pour recevoir des codes OTP par SMS.
*   [[SocialEngineering|Ingénierie Sociale]] : Les attaquants peuvent manipuler les utilisateurs pour qu'ils approuvent des requêtes MFA frauduleuses.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Privilégier les méthodes robustes** : Favoriser les clés de sécurité physiques (FIDO2/WebAuthn) ou les applications d'authentification (TOTP) plutôt que les SMS ou les emails pour les OTP.
*   **Sensibilisation des utilisateurs** : Former les utilisateurs à identifier les tentatives de [[SocialEngineering|hameçonnage]] et à ne pas approuver les requêtes MFA non sollicitées.
*   **Politiques MFA strictes** : Appliquer la MFA sur tous les comptes critiques et encourager son utilisation partout où c'est possible.
*   **Backup Codes** : Fournir des codes de secours à usage unique pour la récupération de compte en cas de perte du facteur secondaire.
*   [[LeastPrivilege|Principe du moindre privilège]] : Appliquer la MFA de manière conditionnelle ou adaptative en fonction du niveau de risque et de la sensibilité des ressources.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[SingleSignOn|Authentification Unique (SSO)]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[ZeroTrust|Confiance Zéro]]