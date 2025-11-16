---
aliases:
  - Verrouillage de compte
  - Account Lockout
  - Verrouillage de compte utilisateur
  - User Account Lockout
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Verrouillage de Compte (Account Lockout)

## 📥 Définition en une phrase
> Le [[AccountLockout|verrouillage de compte]] est une [[SecurityControl|mesure de sécurité]] qui désactive temporairement ou définitivement l'accès à un [[Account|compte utilisateur]] après un nombre spécifié de tentatives de [[Login|connexion]] infructueuses.

## 🧠 Concepts Clés / Piliers
*   **Mécanisme de Défense**: Une [[SecurityControl|mesure de sécurité]] fondamentale pour contrer les [[PasswordAttacks|attaques de mots de passe]] automatisées, telles que les [[BruteForceAttack|attaques par force brute]] et les tentatives répétées de [[PasswordCracking|cassage de mot de passe]] sur les [[Account|comptes utilisateurs]].
*   **[[FailedLoginThreshold|Seuil de Tentatives Échouées]]**: Un nombre prédéfini de tentatives de [[Login|connexion]] incorrectes (ex: 3, 5, 10) qui, une fois atteint, déclenche le [[AccountLockout|verrouillage du compte]]. Ce seuil doit être finement réglé pour équilibrer [[Security|sécurité]] et [[User|convivialité]].
*   **[[LockoutDuration|Durée du Verrouillage]]**: La période pendant laquelle un [[Account|compte]] reste verrouillé. Elle peut être temporaire (ex: 30 minutes) avec déverrouillage automatique, ou permanente nécessitant une intervention [[CentralizedAdministration|administrative]].
*   **[[AttemptCounterReset|Réinitialisation du Compteur]]**: Le processus par lequel le décompte des tentatives de [[Login|connexion]] échouées est remis à zéro, soit après un laps de temps prédéfini sans activité, soit après une [[Login|connexion]] réussie.
*   **Risque de [[DenialOfService|Déni de Service]]**: Une [[NetworkConfiguration|mauvaise configuration]] des politiques de [[AccountLockout|verrouillage de compte]] peut être exploitée par un [[ThreatActor|acteur de menace]] pour provoquer un [[DenialOfService|déni de service]] en verrouillant intentionnellement de nombreux [[Account|comptes]] légitimes, empêchant les [[User|utilisateurs]] légitimes d'accéder aux [[Resource|ressources]].

## 💡 Importance en Cybersécurité
> Le [[AccountLockout|verrouillage de compte]] est une composante critique de la [[Authentication|stratégie d'authentification]] et de la [[Security|sécurité]] des [[System|systèmes]]. Sa mise en œuvre protège directement contre les [[PasswordAttacks|attaques de mots de passe]] automatisées en rendant inefficaces les tactiques comme le [[BruteForceAttack|force brute]] et, dans une moindre mesure, le [[CredentialStuffing|bourrage d'identifiants]]. En imposant un délai ou une intervention pour déverrouiller un [[Account|compte]], il augmente considérablement le coût et le temps nécessaires pour un [[ThreatActor|attaquant]] cherchant un [[UnauthorizedAccess|accès non autorisé]] ou une [[AccountTakeover|prise de contrôle de compte]]. Cependant, il doit être associé à d'autres [[SecurityControl|contrôles de sécurité]] tels que la [[MultiFactorAuthentication|MFA]] et une [[StrongPasswordPolicy|politique de mots de passe forts]] pour une protection complète, et sa [[NetworkConfiguration|configuration]] doit être gérée avec attention pour éviter les vecteurs de [[DenialOfService|déni de service]].

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[DenialOfService|Déni de Service]]
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[Password|Mot de passe]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[Login|Connexion]]
*   [[ConfigurationManagement|Gestion de la Configuration]]
*   [[ThreatActor|Acteur de menace]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]