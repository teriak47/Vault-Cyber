---
aliases:
  - Contrôle d'Accès
  - Access Control
  - DAC
  - MAC
  - RBAC
  - ABAC
archetype: defense
type: Prévention
technologie:
  - IAM
  - SSO
  - MFA
  - ACL
  - LDAP
  - Kerberos
cssclasses:
  - max
tags:
  - access-control
  - gestion-acces
  - authentification
  - authentification/mfa
  - identification
  - autorisation
  - securite/responsabilite
  - modele/dac
  - modele/mac
  - modele/rbac
  - modele/abac
  - principe/moindre-privilege
  - principe/besoin-en-connaitre
  - single-sign-on
  - gestion-acces/privilegies
  - microsoft/active-directory
  - protocole/ldap
  - listes-controle-acces
  - pare-feu
  - detection/ids
  - detection/ips
  - vpn
  - politique
---

# Access Control

> [!goal] Objectif de Sécurité
> L'objectif du **Contrôle d'Accès** est de réguler qui ou quoi peut visualiser, utiliser ou accéder à une ressource particulière dans un environnement informatique. Il vise à minimiser les risques de sécurité en garantissant que seuls les utilisateurs, systèmes ou services autorisés ont accès aux ressources dont ils ont besoin, protégeant ainsi les données sensibles contre le vol, la corruption ou l'exfiltration.

## 🛡️ Mécanisme de Protection (Prevent)

Le contrôle d'accès est un processus fondamental de sécurité qui s'appuie sur deux principes clés : l'**authentification** et l'**autorisation**.

*   **Principes de Fonctionnement** :
    *   **Identification** : Processus par lequel un utilisateur ou un système déclare son identité (ex: nom d'utilisateur, ID).
    *   **Authentification** : Vérification de l'identité déclarée par des identifiants (ex: mots de passe, scans biométriques, jetons de sécurité, codes PIN). L'**authentification multifacteur (MFA)** ajoute une couche de sécurité supplémentaire en exigeant plusieurs méthodes de vérification.
    *   **Autorisation** : Après authentification, détermination du niveau d'accès approprié pour l'utilisateur en fonction des politiques de contrôle d'accès définies. Ce processus applique le *principe du moindre privilège* et le *besoin d'en connaître*.
    *   **Responsabilité (Accountability)** : Traçabilité des activités de chaque compte pour assurer la non-répudiation.

*   **Modèles de Contrôle d'Accès** :
    Différents modèles encadrent la manière dont les autorisations sont définies et appliquées.

    *   **Discretionary Access Control (DAC)** :
        *   **Fonctionnement** : Le propriétaire d'une ressource (fichier, base de données) a la discrétion de décider qui peut y accéder et quelles actions peuvent être effectuées (lecture, écriture, exécution).
        *   **Caractéristiques clés** : Flexible, facile à implémenter dans de petits environnements. Utilise souvent des *listes de contrôle d'accès (ACL)*.
        *   **Implémentation typique** : Permissions de fichiers et dossiers dans les systèmes d'exploitation (ex: NTFS sous Windows).

    *   **Mandatory Access Control (MAC)** :
        *   **Fonctionnement** : Le MAC applique un contrôle d'accès basé sur des étiquettes de sécurité et des classifications prédéfinies, plutôt que sur la discrétion des utilisateurs. L'accès est "obligatoire" et ne peut être modifié par le propriétaire de la ressource.
        *   **Caractéristiques clés** : Très restrictif, contrôle centralisé par un administrateur de sécurité. Les ressources et les utilisateurs sont classifiés (ex: "Top Secret", "Secret", "Confidentiel").
        *   **Implémentation typique** : Systèmes militaires ou gouvernementaux où la confidentialité est critique.

    *   **Role-Based Access Control (RBAC)** :
        *   **Fonctionnement** : Les autorisations d'accès sont attribuées aux utilisateurs en fonction de leurs rôles au sein de l'organisation. Un rôle est une collection de permissions requises pour exécuter un ensemble de tâches.
        *   **Caractéristiques clés** : Simplifie la gestion des accès dans les grandes entreprises avec des rôles structurés. Facile à administrer et moins sujet aux erreurs.
        *   **Implémentation typique** : Largement utilisé dans les entreprises, les systèmes de gestion d'identité et d'accès (IAM).

    *   **Attribute-Based Access Control (ABAC)** :
        *   **Fonctionnement** : L'accès est déterminé dynamiquement par un ensemble d'attributs (du sujet, de l'objet, de l'environnement, de l'action). Les règles ABAC utilisent un format "si-alors-sinon".
        *   **Caractéristiques clés** : Offre une granularité et une flexibilité élevées, idéale pour les environnements dynamiques, modernes et basés sur le cloud.
        *   **Implémentation typique** : Environnements cloud, microservices, architectures Zero Trust.

*   **Implémentations Techniques Générales** :
    Les systèmes de contrôle d'accès s'appuyant sur diverses technologies :
    *   **Services d'annuaire** (ex: Active Directory, LDAP) pour gérer les identités et les groupes d'utilisateurs.
    *   **Listes de contrôle d'accès (ACL)** sur les systèmes de fichiers, les routeurs ou les pare-feu.
    *   **Systèmes de gestion d'identité et d'accès (IAM)** qui intègrent l'authentification et l'autorisation.
    *   **Single Sign-On (SSO)** et **Authentification Multifacteur (MFA)**.
    *   **VPNs** pour l'accès à distance sécurisé.
    *   **Pare-feu** et **systèmes de détection/prévention d'intrusion (IDS/IPS)** pour le contrôle d'accès réseau.
    *   **Gestion des Accès Privilégiés (PAM)** pour les comptes à privilèges élevés.

## 🚨 Stratégie de Détection (Detect)

La surveillance des tentatives d'accès et des violations de politiques est cruciale pour détecter les contournements ou les abus du contrôle d'accès.

*   **Logs à surveiller** :
    *   **Journaux d'accès** : Enregistrent toutes les tentatives d'accès aux ressources, y compris l'heure, l'adresse IP du client, le nom d'utilisateur, la ressource demandée et le résultat (succès/échec).
        *   Journaux de serveurs web (Apache, Nginx)
        *   Journaux d'applications (requêtes API, requêtes de données, activités de session)
        *   Journaux système (Linux `/var/log/secure`, Observateur d'événements Windows)
        *   Journaux de bases de données (tentatives de connexion, requêtes)
        *   Journaux de pare-feu (tentatives d'intrusion, violations de politique)
    *   **Journaux d'audit** : Documentent les modifications numériques apportées au système, telles que les mises à jour de permissions par un administrateur.

*   **Règle SIEM suggérée** :
    Les systèmes SIEM (Security Information and Event Management) agrègent et corrèlent les logs pour identifier les activités suspectes.

```sql
// Détection de tentatives de connexion échouées répétées suivies d'un succès (Brute-Force ou Credential Stuffing)
SELECT
  user_id,
  source_ip,
  COUNT(DISTINCT event_id) AS failed_attempts,
  MIN(event_timestamp) AS first_failed,
  MAX(event_timestamp) AS last_failed,
  MAX(CASE WHEN event_type = 'successful_login' THEN event_timestamp END) AS successful_login_time
FROM
  access_logs
WHERE
  event_type IN ('failed_login', 'successful_login')
  AND event_timestamp BETWEEN NOW() - INTERVAL '5 minutes' AND NOW()
GROUP BY
  user_id, source_ip
HAVING
  failed_attempts >= 5 -- Seuil configurable
  AND successful_login_time IS NOT NULL
  AND successful_login_time > last_failed
// Alerte : Tentatives multiples d'échec de connexion suivies d'une connexion réussie pour user_id depuis source_ip.

// Détection d'accès à des ressources sensibles en dehors des heures ouvrables ou depuis des localisations inhabituelles
SELECT
  user_id,
  resource_accessed,
  access_time,
  source_ip,
  location
FROM
  access_logs
WHERE
  resource_sensitivity = 'high'
  AND (TIME(access_time) NOT BETWEEN '09:00:00' AND '17:00:00' OR DAY_OF_WEEK(access_time) IN ('Saturday', 'Sunday'))
  AND NOT EXISTS (SELECT 1 FROM whitelisted_locations WHERE whitelisted_locations.ip = access_logs.source_ip)
// Alerte : Accès à une ressource hautement sensible en dehors des heures normales ou depuis une adresse IP non approuvée.

// Détection de modification non autorisée de permissions
SELECT
  admin_user,
  action_type,
  target_user_or_resource,
  change_details,
  event_timestamp
FROM
  audit_logs
WHERE
  action_type IN ('permission_change', 'role_assignment')
  AND change_status = 'success'
  AND admin_user NOT IN (SELECT authorized_admin_for_changes FROM security_policy_roles)
// Alerte : Modification de permissions effectuée par un administrateur non autorisé pour ce type de changement.
```

## ⚔️ Contournement Connu (Evasion)

> [!warning] Faiblesses
> Les mécanismes de contrôle d'accès, bien que fondamentaux, présentent des vulnérabilités qui peuvent être exploitées par des attaquants.
*   **Contournement de l'authentification** :
    *   *Attaques par mot de passe* : Attaques par force brute, dictionnaire, *credential stuffing*, *password spraying* ou *phishing* peuvent compromettre les informations d'identification.
    *   *Faiblesses du MFA* : Les attaques de type *man-in-the-middle* (MitM) ou la fatigue des notifications push peuvent contourner le MFA.
    *   *Identifiants par défaut* : L'utilisation de mots de passe ou d'identifiants par défaut sur des systèmes non patchés.
*   **Contournement de l'autorisation (Broken Access Control)** :
    *   *Violation du principe du moindre privilège* : Accès accordé au-delà des besoins réels de l'utilisateur.
    *   *Référence d'objet directe non sécurisée (IDOR)* : Modification d'un paramètre URL ou d'une ID unique pour accéder à des informations d'un autre utilisateur ou ressource.
    *   *Forçage de navigation (Force Browsing)* : Accès direct à des URL d'administration ou à des pages authentifiées sans privilèges suffisants.
    *   *Manipulation de métadonnées* : Altération de jetons JWT, de cookies ou de champs cachés pour élever les privilèges.
    *   *Misconfigurations* : Erreurs de configuration dans les politiques de contrôle d'accès, les serveurs ou les API (ex: CORS misconfiguration).
    *   *Défauts de gestion de session* : Sessions non sécurisées pouvant être détournées.
*   **Contournements physiques** :
    *   *Tailgating / Piggybacking* : Un attaquant suit de près un employé autorisé pour entrer dans une zone sécurisée.
    *   *Cartes d'accès volées ou clonées* : Utilisation de cartes d'accès compromises, surtout si elles utilisent des technologies non chiffrées.
    *   *Portes ouvertes ou sabotage mécanique* : Portes laissées ouvertes intentionnellement ou par inadvertance, ou serrures altérées.
*   **Exploitation de vulnérabilités logicielles** :
    *   Failles de sécurité dans le système de contrôle d'accès lui-même (ex: buffer overflows, injections de code).
    *   Logiciels d'accès non mis à jour ou obsolètes, laissant des vulnérabilités exploitables.

## 🔗 Notes Connexes
*   **Contre l'attaque** : PrivilegeEscalation (conceptuel)
*   **Implémenté par** : IdentityAndAccessManagement (conceptuel)