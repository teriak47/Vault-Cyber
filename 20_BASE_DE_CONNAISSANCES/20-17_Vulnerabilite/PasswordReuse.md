---
tags:
  - vulnerabilite
  - vulnerabilite/mot-de-passe/reutilisation
  - gestion/mot-de-passe
  - securite/sensibilisation-utilisateur
aliases:
  - Réutilisation de mot de passe
  - Password Re-use
archetype: vulnerabilite
cve: ""
cvss_score: ""
cssclasses:
  - max
---

# Réutilisation de Mot de Passe

> [!info] Vulnérabilité Comportementale
> **Nature** : La réutilisation de mot de passe n'est pas une vulnérabilité logicielle avec un score CVSS traditionnel. Elle découle d'une erreur humaine et d'un manque de sensibilisation à la sécurité.
> *L'impact est [[Risk|significatif]] car elle augmente le risque de prise de contrôle de compte suite à une fuite de données sur un autre service.*

## 📥 Description Technique
La réutilisation de mot de passe est une [[Vulnerability|vulnérabilité]] non technique où un utilisateur emploie le même mot de passe ou une variante très similaire pour plusieurs comptes sur différents [[OnlineServices|services en ligne]] ou systèmes. L'impact principal est l'augmentation significative du risque de [[AccountTakeover|prise de contrôle de compte]] : si un mot de passe est compromis sur un service (par exemple, lors d'une [[DataBreach|fuite de données]]), un [[ThreatActor|acteur de menace]] peut utiliser ces identifiants pour accéder à d'autres comptes du même utilisateur.

Le [[AttackVector|vecteur d'attaque]] principal facilite l'[[Exploitation|exploitation]] via des [[PasswordAttacks|attaques de mots de passe]] telles que le [[CredentialStuffing|bourrage d'identifiants]], les [[BruteForceAttack|attaques par force brute]] et les [[DictionaryAttack|attaques par dictionnaire]]. Les comptes utilisateurs à travers divers [[OnlineServices|services en ligne]] et entreprises, où le mot de passe réutilisé est en vigueur, sont les composants affectés. Cette faiblesse est classifiée comme CWE-255 - Credentials Management et découle principalement de [[HumanError|l'erreur humaine]] et d'un manque de [[SecurityAwareness|sensibilisation à la sécurité]], plutôt que d'un défaut logiciel.

## 💥 Exploitabilité
*   **POC Public** : Oui (concepts et outils existants)
*   **Facilité d'exploitation** : Facile
*   **Prérequis** : Obtention d'un mot de passe (via [[DataBreach|fuite de données]], [[Phishing|hameçonnage]], etc.)

L'exploitation est facilitée par la disponibilité de listes d'identifiants compromis (souvent appelées "combo lists") sur des marchés noirs ou des forums, permettant des [[Automation|attaques automatisées]] de type bourrage d'identifiants.

## 🛡️ Patch & Mitigation

### Correctif Officiel
Pour cette vulnérabilité non technique, il n'existe pas de "version corrigée" logicielle. Les correctifs sont des changements de comportement et des implémentations de [[SecurityPolicy|politiques de sécurité]].

### Contournement (Workaround)
Si le patch n'est pas possible :
*   **Utilisation de [[StrongPassword|mots de passe forts]] et uniques**: Chaque compte doit avoir un mot de passe unique et complexe, résistant aux [[PasswordCracking|cassages de mot de passe]].
*   **[[PasswordManager|Gestionnaire de mots de passe]]**: Encourager l'utilisation d'un [[PasswordManager|gestionnaire de mots de passe]] pour générer et stocker des mots de passe forts et uniques pour chaque [[Service|service]].
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]**: Activer la [[MultiFactorAuthentication|MFA]] sur tous les services qui le permettent. Cela ajoute une [[Security|couche de sécurité]] même si un mot de passe est compromis.
*   **[[StrongPasswordPolicy|Politique de mots de passe forts]]**: Implémenter et appliquer des [[StrongPasswordPolicy|politiques de mots de passe forts]] exigeant une complexité minimale, une longueur suffisante et interdisant la réutilisation des anciens mots de passe.
*   **[[UserAwarenessTraining|Sensibilisation des utilisateurs]]**: Organiser des sessions de [[UserAwarenessTraining|sensibilisation des utilisateurs]] pour éduquer sur les risques liés à la réutilisation des mots de passe.

## 🔍 Détection
La réutilisation de mots de passe n'est pas directement "détectable" en soi, mais ses conséquences peuvent être identifiées:
*   **Surveillance des [[Log|journaux]] d'[[Authentication|authentification]]**: Rechercher des schémas de connexions échouées ou réussies suspectes, provenant d'adresses IP inattendues, ou multiples tentatives d'authentification sur différents comptes ou services avec les mêmes identifiants (signe de bourrage d'identifiants).
*   **[[SecurityInformationAndEventManagement|SIEM]]**: Utiliser des systèmes [[SecurityInformationAndEventManagement|SIEM]] pour corréler les événements d'authentification et alerter sur les activités anormales qui pourraient indiquer une exploitation de la réutilisation de mots de passe.
*   **[[ThreatIntelligence|Renseignement sur les menaces]]**: Surveiller les bases de données de [[ThreatIntelligence|renseignement sur les menaces]] et les services qui signalent les identifiants compromis pour vérifier si les identifiants de l'entreprise ou des utilisateurs ont été divulgués.
*   **[[NetworkTrafficAnalysis|Analyse du trafic réseau]]**: Identifier des tentatives de bourrage d'identifiants ou d'attaques par force brute qui pourraient exploiter des mots de passe réutilisés.

## 🔗 Références
*   MITRE ATT&CK T1110 : Brute Force
*   MITRE ATT&CK T1110.004 : Credential Stuffing