---
aliases:
  - Identifiant
  - Informations d'identification
  - Login credential
  - Authentification credential
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Identifiant (Credential)

## 📥 Définition en une phrase
> Un [[Credential|identifiant]] est un ensemble d'informations ou de preuves utilisées pour vérifier l'[[UserIdentity|identité]] d'un [[User|utilisateur]], d'un [[System|système]] ou d'une [[SoftwareApplication|application]] afin d'accorder ou de refuser l'[[AccessControl|accès]] à une [[Resource|ressource]].

## 🧠 Concepts Clés / Piliers
*   **Composition**: Les [[Credential|identifiants]] peuvent inclure un [[Username|nom d'utilisateur]] et un [[Password|mot de passe]], des [[DigitalSignature|signatures numériques]], des [[Biometric|données biométriques]] (empreintes digitales, reconnaissance faciale), des jetons de sécurité ou des [[DigitalCertificate|certificats numériques]].
*   **[[Authentication|Authentification]]**: Le processus par lequel le [[System|système]] vérifie les [[Credential|identifiants]] pour confirmer l'[[UserIdentity|identité]] déclarée de l'[[User|utilisateur]]. C'est la première étape avant d'accorder l'accès.
*   **Protection**: La [[Security|sécurité]] des [[Credential|identifiants]] est primordiale et repose sur l'utilisation de [[StrongPassword|mots de passe forts]], la [[MultiFactorAuthentication|MFA]], et des pratiques de [[SecureStorage|stockage sécurisé]] pour prévenir les [[UnauthorizedAccess|accès non autorisés]].

## 💡 Importance en Cybersécurité
> Les [[Credential|identifiants]] sont la première ligne de [[Security|défense]] pour protéger les [[System|systèmes]] et les [[Data|données]]. Leur compromission est une voie majeure pour les [[Attack|attaques]] telles que le [[CredentialStuffing|bourrage d'identifiants]], l'[[AccountTakeover|prise de contrôle de compte]] et l'[[UnauthorizedAccess|accès non autorisé]], rendant leur gestion et leur protection fondamentales pour la [[Cybersecurity|cybersécurité]] d'une [[Enterprise|entreprise]].

## 🔗 Notes Connexes
*   [[Authentication]]
*   [[Authorization]]
*   [[Password]]
*   [[Username]]
*   [[MultiFactorAuthentication|MFA]]
*   [[StrongPassword|Mots de passe forts]]
*   [[PasswordManager|Gestionnaire de Mots de Passe]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[IdentityAndAccessManagement|IAM]]
*   [[Account|Compte]]
*   [[Login]]
*   [[Biometric|Biométrie]]
*   [[SecureStorage|Stockage Sécurisé]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]