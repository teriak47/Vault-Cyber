---
aliases:
  - Compte
  - User Account
  - Login Account
  - account
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Compte (Account)

## 📥 Définition en une phrase
> Un [[Account|compte]] est un ensemble d'identifiants et d'[[Authorization|autorisations]] permettant à un utilisateur d'accéder à un [[System|système]] informatique ou un [[OnlineServices|service en ligne]].

## 🧠 Concepts Clés / Piliers
*   **Identification et Authentification**: Le [[Account|compte]] est le point central pour l'[[Authentication|authentification]] de l'[[UserIdentity|identité d'un utilisateur]], typiquement via un [[Username|nom d'utilisateur]] et un [[Password|mot de passe]]. C'est le processus de vérification que l'utilisateur est bien celui qu'il prétend être.
*   **Autorisation et Accès**: Une fois authentifié, les [[Authorization|autorisations]] associées au [[Account|compte]] déterminent quels [[Resource|ressources]] (fichiers, applications, services) l'[[UserIdentity|utilisateur]] est permis d'accéder, de consulter ou de modifier.
*   **Gestion du Profil**: Chaque [[Account|compte]] est souvent lié à un [[Profile|profil]] qui stocke les préférences de l'[[UserIdentity|utilisateur]], ses [[PersonalData|données personnelles]] et d'autres configurations spécifiques au [[Account|compte]], permettant une expérience personnalisée.

## 💡 Importance en Cybersécurité
> Les [[Account|comptes]] sont des points d'entrée critiques pour les [[System|systèmes]] et [[OnlineServices|services en ligne]]. Leur [[Security|sécurité]] est fondamentale pour préserver la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] (la [[CIATriad|Triade CIA]]) des [[Data|données]] et [[Resource|ressources]]. Les [[ThreatActor|acteurs de menace]] ciblent fréquemment les [[Account|comptes]] via des [[Attack|attaques]] telles que l'[[AccountTakeover|ATO]], le [[BruteForceAttack|cassage de mots de passe]], le [[CredentialStuffing|bourrage d'identifiants]] ou le [[Phishing|hameçonnage]]. Une [[StrongPasswordPolicy|politique de mots de passe forts]], l'[[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] et des [[SecurityControl|contrôles de sécurité]] robustes sont essentiels pour prévenir l'[[UnauthorizedAccess|accès non autorisé]] et la [[SystemCompromise|compromission du système]].

## 🔗 Notes Connexes
*   [[UserIdentity|Identité utilisateur]]
*   [[Username|Nom d'utilisateur]]
*   [[Password|Mot de passe]]
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[Credential|Identifiants]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[AccountLockout|Verrouillage de compte]]
*   [[AccessControl|Contrôle d'accès]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[PasswordManager|Gestionnaire de Mots de Passe]]
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[SecurityAwareness|Sensibilisation à la Sécurité]]
*   [[System|Système]]
*   [[OnlineServices|Services en ligne]]
*   [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles]]
*   [[Profile|Profil utilisateur]]