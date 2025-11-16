---
aliases:
  - Identity and Access Management
  - IAM
  - Gestion des Identités et des Accès
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Gestion des Identités et des Accès (IAM)

## 📥 Définition en une phrase
> La Gestion des Identités et des Accès ([[IdentityAndAccessManagement|IAM]]) est un cadre de politiques, de processus et de technologies qui permet de gérer les [[Identity|identités]] numériques et de contrôler l'[[AccessControl|accès]] des [[User|utilisateurs]] et des entités aux [[Resource|ressources]] d'une [[Enterprise|entreprise]].

## 🧠 Concepts Clés / Piliers
*   **[[Identification|Identification]]**: Le processus par lequel un [[User|utilisateur]] ou un [[System|système]] se déclare à un [[System|système]], souvent via un nom d'[[Account|utilisateur]].
*   **[[Authentication|Authentification]]**: Le processus de validation de l'identité déclarée par un [[User|utilisateur]], confirmant qu'il est bien celui qu'il prétend être (par exemple, via un [[Password|mot de passe]], [[MultiFactorAuthentication|MFA]] ou [[Biometric|biométrie]]).
*   **[[Authorization|Autorisation]]**: La détermination des [[Resource|ressources]] et des actions qu'un [[User|utilisateur]] authentifié est autorisé à effectuer, souvent gérée par des [[AccessControl|modèles de contrôle d'accès]] comme le [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles (RBAC)]].
*   **Gestion du cycle de vie des identités**: L'ensemble des processus de [[Provisioning|provisionnement]] (création), de mise à jour et de [[Deprovisioning|déprovisionnement]] (suppression) des [[Account|comptes]] [[User|utilisateur]] et de leurs [[Identity|identités]] tout au long de leur existence dans l'[[Enterprise|entreprise]].
*   **[[SingleSignOn|Authentification Unique (SSO)]]**: Un mécanisme permettant à un [[User|utilisateur]] de s'authentifier une seule fois pour accéder à plusieurs [[SoftwareApplication|applications]] et [[System|systèmes]] sans avoir à se reconnecter.

## 💡 Importance en Cybersécurité
> L'[[IdentityAndAccessManagement|IAM]] est un pilier fondamental de la [[Cybersecurity|cybersécurité]] car il garantit que seules les bonnes personnes (ou entités) ont le bon [[AccessControl|accès]] aux bonnes [[Resource|ressources]] au bon moment, en adhérant au [[PrincipleOfLeastPrivilege|principe du moindre privilège]]. Une gestion robuste de l'[[IdentityAndAccessManagement|IAM]] est cruciale pour réduire la [[AttackSurface|surface d'attaque]], prévenir les [[UnauthorizedAccess|accès non autorisés]], minimiser les [[InsiderThreat|menaces internes]], et assurer la [[Compliance|conformité]] aux réglementations sur la protection des [[PersonalData|données]]. C'est une composante essentielle d'une stratégie de [[ZeroTrust|Modèle Zero Trust]].

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'accès]]
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles]]
*   [[PrivilegedAccessManagement|Gestion des Accès Privilégiés (PAM)]]
*   [[SingleSignOn|Authentification Unique (SSO)]]
*   [[ZeroTrust|Modèle Zero Trust]]
*   [[IdentityGovernance|Gouvernance des Identités]]
*   [[Compliance|Conformité]]