---
tags:
  - account-lockout
  - strong-password
  - authentification
  - credential
  - multi-factor-authentication
aliases:
  - Compte
  - User Account
  - Login Account
source:
  - null
cssclasses:
  - max
---

# Compte (Account)

## 📥 Définition en une phrase
> Un [[Account|compte]] est un ensemble d'[[Credential|identifiants]] et de [[Authorization|permissions]] permettant à un [[UserIdentity|utilisateur]] d'accéder à un [[System|système]] informatique ou un [[OnlineServices|service en ligne]].

## 🧠 Concepts Clés / Fonctionnement
*   **[[Authentication|Authentification]]**: Le processus de vérification de l'identité déclarée d'un utilisateur, généralement via un [[Username|nom d'utilisateur]] et un [[Password|mot de passe]].
*   **[[Authorization|Autorisation]]**: Une fois authentifié, l'[[System|système]] détermine quels [[Resource|ressources]] (nouveau) l'utilisateur est autorisé à consulter ou modifier en fonction de son [[Account|compte]].
*   **[[Credential|Identifiants]]**: Les informations, comme les [[Username|noms d'utilisateur]] et les [[Password|mots de passe]], utilisées pour prouver l'identité de l'utilisateur.
*   **[[Profile|Profil]]**: Ensemble des données, préférences et configurations associées à un [[Account|compte]] d'utilisateur.

## 🛡️ Risques / Menaces Associés
*   [[AccountTakeover|Prise de contrôle de compte]] (ATO) : Un attaquant obtient un accès non autorisé à un [[Account|compte]] légitime.
*   [[BruteForceAttack|Attaque par force brute]] : Tentatives répétées de deviner les [[Password|mots de passe]] ou [[Credential|identifiants]] d'un [[Account|compte]].
*   [[CredentialStuffing|Bourrage d'identifiants]] : Utilisation massive de [[Credential|identifiants]] volés (souvent issus de [[DataBreach|fuites de données]]) pour accéder à d'autres [[OnlineServices|services en ligne]].
*   [[Phishing|Hameçonnage]] : Ingénierie sociale pour inciter les utilisateurs à divulguer leurs [[Credential|identifiants]] de [[Account|compte]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser des [[StrongPassword|mots de passe forts]] et uniques pour chaque [[Account|compte]].
*   Activer l'[[MultiFactorAuthentication|authentification multi-facteurs]] (MFA) chaque fois que possible.
*   Mettre en œuvre des politiques de [[AccountLockout|verrouillage de compte]] après un certain nombre de tentatives de connexion échouées.
*   Appliquer des [[AccessControl|contrôles d'accès]] stricts basés sur le principe du moindre privilège.
*   Utiliser un [[PasswordManager|gestionnaire de mots de passe]] pour gérer et stocker les [[Credential|identifiants]] de manière sécurisée.

## 🔗 Notes Connexes
*   [[UserIdentity|Identité utilisateur]]
*   [[PrivilegeEscalation|Escalade de Privilèges]]
*   [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles]]
*   [[SecurityAwareness|Sensibilisation à la Sécurité]]