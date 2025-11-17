---
tags:
  - vulnerabilite
aliases:
  - Réutilisation de mot de passe
  - Password Re-use
archetype: vulnerabilite
cve: 
cvss_score: 
cssclasses:
  - max
---

# Réutilisation de Mot de Passe

## 📥 Définition et Impact
> La réutilisation de mot de passe est une [[Vulnerability|vulnérabilité]] non technique où un [[User|utilisateur]] emploie le même [[Password|mot de passe]] ou une variante très similaire pour plusieurs [[Account|comptes]] sur différents [[OnlineServices|services en ligne]] ou [[System|systèmes]]. L'impact principal est l'augmentation significative du risque de [[AccountTakeover|prise de contrôle de compte]] : si un [[Password|mot de passe]] est compromis sur un service (par exemple, lors d'une [[DataBreach|fuite de données]]), un [[ThreatActor|acteur de menace]] peut utiliser ces [[Credential|identifiants]] pour accéder à d'autres [[Account|comptes]] du même [[User|utilisateur]].

## 📝 Détails Techniques
* **Vecteur d'attaque principal**: Facilite l'exploitation via des [[PasswordAttacks|attaques de mots de passe]] telles que le [[CredentialStuffing|bourrage d'identifiants]], les [[BruteForceAttack|attaques par force brute]] et les [[DictionaryAttack|attaques par dictionnaire]].
* **Composant affecté**: Les [[Account|comptes]] [[User|utilisateurs]] à travers divers [[OnlineServices|services en ligne]] et [[Enterprise|entreprises]], où le [[Password|mot de passe]] réutilisé est en vigueur.
* **Type de faiblesse**: [[CommonWeaknessEnumeration|CWE-255]] - Credentials Management. Cette faiblesse découle principalement de [[HumanError|l'erreur humaine]] et d'un manque de [[SecurityAwareness|sensibilisation à la sécurité]], plutôt que d'un défaut logiciel.

## 🛡️ Correctifs et Contournements
*   **Utilisation de [[StrongPassword|mots de passe forts]] et uniques**: Chaque [[Account|compte]] doit avoir un [[Password|mot de passe]] unique et complexe, résistant aux [[PasswordCracking|cassages de mot de passe]].
*   **[[PasswordManager|Gestionnaire de mots de passe]]**: Encourager l'utilisation d'un [[PasswordManager|gestionnaire de mots de passe]] pour générer et stocker des [[StrongPassword|mots de passe forts]] et uniques pour chaque service.
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]**: Activer la [[MultiFactorAuthentication|MFA]] sur tous les services qui le permettent. Cela ajoute une couche de [[Security|sécurité]] même si un [[Password|mot de passe]] est compromis.
*   **[[StrongPasswordPolicy|Politique de mots de passe forts]]**: Implémenter et appliquer des [[StrongPasswordPolicy|politiques de mots de passe forts]] exigeant une complexité minimale, une longueur suffisante et interdisant la réutilisation des anciens [[Password|mots de passe]].
*   **[[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|Sensibilisation des utilisateurs]]**: Organiser des sessions de [[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|sensibilisation des utilisateurs]] pour éduquer sur les risques liés à la réutilisation des [[Password|mots de passe]].

## 🔍 Comment la détecter ?
La réutilisation de [[Password|mots de passe]] n'est pas directement "détectable" en soi, mais ses conséquences peuvent être identifiées:
*   **Surveillance des [[Log|journaux]] d'[[Authentication|authentification]]**: Rechercher des schémas d'[[Login|connexions]] échouées ou réussies suspectes, provenant d'adresses [[InternetProtocol|IP]] inattendues, ou multiples tentatives d'[[Authentication|authentification]] sur différents [[Account|comptes]] ou services avec les mêmes [[Credential|identifiants]] (signe de [[CredentialStuffing|bourrage d'identifiants]]).
*   **[[SecurityInformationAndEventManagement|SIEM]]**: Utiliser des systèmes [[SecurityInformationAndEventManagement|SIEM]] pour corréler les événements d'[[Authentication|authentification]] et alerter sur les activités anormales qui pourraient indiquer une exploitation de la réutilisation de [[Password|mots de passe]].
*   **[[ThreatIntelligence|Renseignement sur les menaces]]**: Surveiller les bases de données de [[ThreatIntelligence|renseignements sur les menaces]] et les services qui signalent les [[Credential|identifiants]] compromis pour vérifier si les [[Credential|identifiants]] de l'[[Enterprise|entreprise]] ou des [[User|utilisateurs]] ont été divulgués.
*   **Analyse du [[NetworkTrafficAnalysis|trafic réseau]]**: Identifier des tentatives de [[CredentialStuffing|bourrage d'identifiants]] ou d'[[BruteForceAttack|attaques par force brute]] qui pourraient exploiter des [[Password|mots de passe]] réutilisés.

## 🔗 Notes Connexes
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[DictionaryAttack|Attaque par dictionnaire]]
*   [[PasswordManager|Gestionnaire de mots de passe]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs]]
*   [[StrongPasswordPolicy|Politique de mots de passe forts]]
*   [[SecurityAwareness|Sensibilisation à la sécurité]]
*   [[HumanError|Erreur humaine]]