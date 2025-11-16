---
tags:
  - attaque
aliases:
  - Diffusion de Mot de Passe
  - Password Spreading
  - Password Spraying
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Password Spraying (Diffusion de Mot de Passe)

## 📥 Définition
> Le [[PasswordSpraying|Password Spraying]] est une [[Attack|attaque]] de type [[PasswordAttacks|cassage de mot de passe]] visant à obtenir un [[UnauthorizedAccess|accès non autorisé]] en testant un petit nombre de [[Password|mots de passe]] très courants sur un grand nombre de [[Account|comptes d'utilisateurs]]. Cette méthode est conçue pour éviter les [[AccountLockout|verrouillages de compte]] et rester [[AnomalyDetection|indétectée]].

## 🎯 Vecteurs d'Attaque
*   **[[OnlineServices|Services en ligne]]**: Cible les [[Login|formulaires de connexion]] d'applications web ou de [[Cloud|services cloud]].
*   **[[CorporateNetwork|Réseaux d'entreprise]]**: Utilise des [[Protocol|protocoles]] d'authentification réseau (ex: [[SecureShell|SSH]], RDP, [[FileTransferProtocol|FTP]]) pour tester des identifiants sur de multiples systèmes.
*   **Listes d'[[Username|utilisateurs]]**: Les attaquants s'appuient souvent sur des listes de noms d'utilisateurs légitimes collectées via des techniques de [[Reconnaissance|reconnaissance]].

## 💥 Impacts Potentiels
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[SystemCompromise|Compromission de compte]]
*   [[DataTheft|Vol de données]] (incluant les [[Credential|identifiants]])
*   [[DataBreach|Fuite de données]]
*   [[FinancialLoss|Pertes financières]]
*   [[ReputationalDamage|Atteinte à la réputation]]

## 📝 Exemple concret
> Un [[ThreatActor|attaquant]] cible une [[Enterprise|entreprise]] et collecte 10 000 [[Username|noms d'utilisateurs]] valides. Au lieu de tenter des milliers de [[Password|mots de passe]] différents sur un seul compte (ce qui déclencherait un [[AccountLockout|verrouillage de compte]]), l'attaquant choisit un [[Password|mot de passe]] courant comme "Bienvenue2024!" et l'essaie sur chacun des 10 000 comptes. S'il ne trouve aucune correspondance, il répète le processus avec un autre mot de passe courant comme "MonMotDePasse!", puis un autre. Cette approche minimise les échecs par compte, rendant l'[[Attack|attaque]] plus difficile à détecter par les systèmes de [[AccountLockout|verrouillage de compte]] traditionnels.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]: Rend l'[[Attack|attaque]] inefficace même si un [[Password|mot de passe]] est découvert.
    *   [[StrongPasswordPolicy|Politiques de Mots de Passe Forts]]: Exiger des mots de passe longs, complexes et uniques pour rendre les [[PasswordAttacks|attaques par dictionnaire]] et le spraying moins efficaces.
    *   [[AccountLockoutPolicy|Politiques de Verrouillage de Compte]]: Bien que ciblées par le spraying, des seuils de verrouillage bien configurés restent une [[SecurityControl|mesure de sécurité]] essentielle.
    *   [[UserAwarenessTraining|Sensibilisation des utilisateurs]]: Éduquer sur les dangers des [[PasswordReuse|réutilisations de mot de passe]] et l'importance des [[StrongPassword|mots de passe forts]].
*   **Détection** :
    *   [[SecurityInformationAndEventManagement|SIEM]]: Permet d'agréger et d'analyser les [[Log|journaux]] d'authentification pour identifier les modèles anormaux (ex: une même [[Password|tentative de mot de passe]] sur de multiples comptes).
    *   [[AnomalyDetection|Détection d'anomalies]]: Surveiller les tentatives de [[Login|connexion]] pour des schémas inhabituels de volume, de source [[InternetProtocolAddressBlocks|IP]] ou de [[LocationData|localisation géographique]].
    *   [[SecurityMonitoring|Surveillance de sécurité]]: Examiner les [[Log|logs]] des [[Server|serveurs]] d'authentification pour des échecs d'authentification dispersés.
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]]: Avoir une stratégie claire pour réagir en cas de [[SystemCompromise|compromission de compte]] détectée suite à une attaque.

## 🔗 Notes Connexes
*   [[BruteForceAttack|Attaque par Force Brute]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[PasswordPolicy|Politique de Mot de Passe]]
*   [[Authentication|Authentification]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès]]
*   [[ThreatActor|Acteur de menace]]