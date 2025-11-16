---
tags:
  - concept/general
  - securite/authentification
  - authentification/a-deux-facteurs
  - securite/acces
  - biometrie
  - methode/securite
aliases:
  - Authentification à deux facteurs
  - 2FA
  - TFA
  - Two-Factor Authentication
  - Authentification à double facteur
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Authentification à Deux Facteurs (2FA)

## 📥 Définition en une phrase
> Une méthode de [[Security|sécurité]] qui exige la présentation de deux facteurs d'[[Authentication|authentification]] distincts, issus de catégories différentes, afin de vérifier l'[[UserIdentity|identité d'un utilisateur]] et d'ajouter une couche de [[Security|protection]] supplémentaire au-delà d'un simple [[Password|mot de passe]].

## 🧠 Concepts Clés / Piliers
*   **Catégories de Facteurs**: La 2FA repose sur l'utilisation de deux éléments provenant de différentes catégories d'[[Authentication|authentification]] :
    *   **Ce que vous savez**: Informations connues uniquement par l'[[User|utilisateur]], telles qu'un [[Password|mot de passe]] ou un code [[PIN|PIN]].
    *   **Ce que vous avez**: Un objet physique ou un jeton en possession de l'[[User|utilisateur]], comme un [[Smartphone|smartphone]] générant des codes, une [[HardwareSecurityKey|clé de sécurité matérielle]] (ex: FIDO U2F), ou un [[TimeBasedOneTimePassword|jeton OTP]].
    *   **Ce que vous êtes**: Une caractéristique [[Biometric|biométrique]] unique de l'[[User|utilisateur]], telle qu'une [[Fingerprint|empreinte digitale]] ou la [[FacialRecognition|reconnaissance faciale]].
*   **Indépendance des Facteurs**: Pour être considérée comme 2FA, les deux facteurs doivent impérativement provenir de *catégories différentes* (par exemple, un [[Password|mot de passe]] (savoir) et un code [[TimeBasedOneTimePassword|TOTP]] sur [[Smartphone|smartphone]] (avoir)).
*   **Processus d'Authentification**: Le processus implique généralement l'entrée du premier facteur (souvent le [[Password|mot de passe]]), suivie d'une demande pour le second facteur, qui doit être fourni ou validé, souvent dans un délai limité ou via un [[WirelessDevices|dispositif]] dédié.
*   **Implémentations Courantes**: Les méthodes courantes incluent l'utilisation de codes [[TimeBasedOneTimePassword|TOTP]] générés par des applications d'[[Authentication|authentification]], des codes envoyés par SMS, l'utilisation de [[HardwareSecurityKey|clés de sécurité matérielles]], ou l'approbation via une [[SoftwareApplication|application mobile]] spécifique.

## 💡 Importance en Cybersécurité
> L'[[TwoFactorAuthentication|authentification à deux facteurs]] est cruciale car elle augmente significativement la [[Security|sécurité]] des [[Account|comptes d'utilisateur]] en ajoutant une couche de [[DefenseInDepth|défense en profondeur]]. Elle réduit considérablement le [[RiskManagement|risque]] d'[[AccountTakeover|prise de contrôle de compte]] et d'[[UnauthorizedAccess|accès non autorisé]], même si le [[Password|mot de passe]] principal est [[SystemCompromise|compromis]] via des [[AttackVector|vecteurs d'attaque]] comme le [[Phishing|hameçonnage]], le [[CredentialStuffing|bourrage d'identifiants]] ou la [[PasswordSpraying|diffusion de mot de passe]]. C'est une mesure essentielle pour la [[DataProtection|protection des données sensibles]] et la [[Security|sécurité]] des [[OnlineServices|services en ligne]].

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs]]
*   [[Biometric|Biométrie]]
*   [[Password|Mot de passe]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[Security|Sécurité]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès]]
*   [[ZeroTrust|Zéro Confiance]]