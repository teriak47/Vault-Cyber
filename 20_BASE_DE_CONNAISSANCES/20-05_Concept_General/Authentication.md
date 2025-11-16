---
tags:
aliases:
  - Authentification
  - Authentication
  - Vérification d'identité
  - Login
  - Connexion
  - Sign-in
  - Log-in
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Authentification

## 📥 Définition en une phrase
> Processus de vérification de l'[[UserIdentity|identité]] déclarée d'un [[User|utilisateur]], d'un [[System|système]] ou d'une [[Enterprise|entité]], en comparant des preuves fournies à des informations stockées.

## 🧠 Concepts Clés / Piliers
*   **[[Identification]]**: L'[[User|entité]] déclare son [[UserIdentity|identité]], souvent via un [[Credential|identifiant]] unique (ex: [[Username|nom d'utilisateur]], [[InternetProtocol|adresse IP]]). C'est la première étape où l'entité prétend être une identité spécifique.
*   **Preuve ([[Credential|Credentials]])**: L'[[User|entité]] fournit un ou plusieurs [[Authentication|facteurs d'authentification]] pour étayer son [[Identification|identification]]. Ces preuves peuvent inclure des [[Password|mots de passe]], des informations [[Biometric|biométriques]] (empreinte digitale, reconnaissance faciale) ou des [[DigitalCertificate|certificats numériques]].
*   **Vérification**: Le [[System|système]] compare les preuves fournies par l'[[User|entité]] aux informations d'[[UserIdentity|identité]] enregistrées et fiables. Si les preuves correspondent, l'[[UserIdentity|identité]] est confirmée et l'[[User|utilisateur]] ou le [[System|système]] est authentifié.
*   **Facteurs d'[[Authentication|authentification]]**: Les catégories de preuves utilisées pour vérifier une [[UserIdentity|identité]] :
    *   **Ce que vous savez ([[KnowledgeFactor|Knowledge Factor]])**: Basé sur une connaissance secrète (ex: [[Password|mot de passe]], code PIN, réponses à des questions secrètes).
    *   **Ce que vous avez ([[PossessionFactor|Possession Factor]])**: Basé sur la possession d'un objet physique ou virtuel (ex: [[SecurityToken|jeton de sécurité]], [[DigitalCertificate|certificat numérique]], [[AuthenticationApplication|application d'authentification]] mobile).
    *   **Ce que vous êtes ([[InherenceFactor|Inherence Factor]])**: Basé sur une caractéristique [[Biometric|biométrique]] unique (ex: empreinte digitale, reconnaissance faciale ou vocale).
    *   **Où vous êtes ([[LocationFactor|Location Factor]])**: Basé sur des informations de [[LocationData|localisation]] (ex: [[InternetProtocol|adresse IP]] source, géolocalisation GPS).
    *   **Ce que vous faites ([[ActionFactor|Action Factor]])**: Basé sur un [[UserBehavior|comportement]] spécifique (ex: schéma de frappe, démarche).

## 💡 Importance en Cybersécurité
L'[[Authentication|authentification]] est une pierre angulaire de la [[Cybersecurity|cybersécurité]], agissant comme la première ligne de défense contre l'[[UnauthorizedAccess|accès non autorisé]] aux [[Resource|ressources]] et [[System|systèmes]]. Elle assure que seules les [[UserIdentity|identités]] légitimes peuvent interagir avec les [[System|systèmes]] d'[[Enterprise|entreprise]] ou personnels, protégeant ainsi la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[Data|données]]. Sans une [[Authentication|authentification]] robuste, les [[System|systèmes]] sont vulnérables à des [[Attack|attaques]] telles que le [[BruteForceAttack|cassage de mots de passe]], le [[CredentialStuffing|bourrage d'identifiants]], le [[Phishing|hameçonnage]] et les [[ReplayAttack|attaques par rejeu]], menant potentiellement à la [[DataBreach|violation de données]] ou à la [[SystemCompromise|compromission de système]]. En mettant en œuvre des [[Authentication|mécanismes d'authentification]] forts, tels que l'[[MultiFactorAuthentication|MFA]] et des [[StrongPasswordPolicy|politiques de mots de passe robustes]], les [[Enterprise|organisations]] peuvent significativement réduire leur [[AttackSurface|surface d'attaque]] et renforcer leur posture de [[Security|sécurité]].

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'accès]]
*   [[Authorization|Autorisation]]
*   [[BiometricAuthentication|Authentification biométrique]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[Credential|Identifiant]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[ManInTheMiddle|Attaque de l'homme du milieu]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[Password|Mot de passe]]
*   [[PasswordCracking|Cassage de mots de passe]]
*   [[PasswordHashing|Hachage et salage des mots de passe]]
*   [[Phishing|Hameçonnage]]
*   [[ReplayAttack|Attaque par rejeu]]
*   [[SecurityAudit|Audit de sécurité]]
*   [[SingleSignOn|Authentification Unique (SSO)]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]
*   [[TwoFactorAuthentication|Authentification à deux facteurs (2FA)]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[UserIdentity|Identité Utilisateur]]