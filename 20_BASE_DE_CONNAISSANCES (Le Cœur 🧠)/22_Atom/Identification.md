---
tags:
  - identification
  - securite/gestion-identifiants
  - gouvernance/separation-taches
  - authentification
  - autorisation
  - gestion-identites/controle-acces
aliases:
  - Identification
  - Déclaration d'identité
cssclasses:
  - max
---

# Identification

## 📥 Définition en une phrase
> L'identification est le processus par lequel une entité (utilisateur, système) déclare son identité au sein d'un système ou d'un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Première étape** : Il s'agit de la phase initiale dans le processus d'[[AccessControl|contrôle d'accès]], précédant l'[[Authentication|authentification]] et l'[[Authorization|autorisation]].
*   **Déclaration d'identité** : Une entité présente un identifiant unique (nom d'utilisateur, adresse email, numéro de carte, etc.) pour se faire reconnaître par le système.
*   **Unicité** : L'identifiant doit être unique au sein du domaine du système pour permettre une distinction claire entre les différentes entités.
*   **Non-vérification** : L'identification ne prouve pas que l'entité est bien celle qu'elle prétend être ; elle ne fait que déclarer une identité. La preuve de l'identité est fournie par l'[[Authentication|authentification]].

## 🛡️ Risques / Menaces Associés
*   [[IdentityTheft|Usurpation d'identité]] : Une entité malveillante utilise les identifiants d'une autre entité.
*   [[SocialEngineering|Ingénierie Sociale]] : Tentatives d'obtenir frauduleusement des identifiants (ex: via le [[Phishing|hameçonnage]]).
*   Divulgation d'[[SensitiveData|informations sensibles]] : Les identifiants peuvent révéler des informations personnelles s'ils ne sont pas bien gérés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[StrongPasswordPolicy|Politiques de mots de passe robustes]] : Bien que principalement pour l'authentification, des identifiants non-triviaux et des politiques d'[[AccountLockout|verrouillage de compte]] aident à protéger l'identifiant.
*   [[AccessControlList|Gestion des comptes]] et des identifiants uniques : Assurer l'unicité et la bonne gestion du cycle de vie des identifiants.
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] : Renforce l'authentification qui suit l'identification, rendant plus difficile l'usurpation d'identité même si l'identifiant est compromis.
*   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] : Limiter les droits associés à un identifiant au strict nécessaire.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[AccessControl|Contrôle d'accès]]
*   [[IdentityAndAccessManagement|Gestion des identités et des accès (IAM)]]