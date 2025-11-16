---
tags:
aliases:
  - Sauvegarde
  - Backup
  - Sauvegardes
  - Data Backup
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sauvegarde (Backup)

## 📥 Définition en une phrase
> Une [[Backup|sauvegarde]] est une copie de [[Data|données]] informatiques, conservée séparément des [[Data|données]] originales, permettant de les [[BackupAndRecovery|restaurer]] en cas de [[DataCorruption|perte]], de corruption ou de destruction.

## 🧠 Concepts Clés / Piliers
*   **Types de Sauvegarde**: Différentes stratégies pour copier les [[Data|données]].
    *   **[[FullBackup|Complète]]**: Copie l'intégralité des [[Data|données]] sélectionnées.
    *   **[[IncrementalBackup|Incrémentielle]]**: Copie uniquement les [[Data|données]] modifiées depuis la dernière [[Backup|sauvegarde]] (complète ou incrémentielle).
    *   **[[DifferentialBackup|Différentielle]]**: Copie toutes les [[Data|données]] modifiées depuis la dernière [[FullBackup|sauvegarde complète]].
*   **Processus de [[BackupAndRecovery|Restauration]]**: Action de récupérer les [[Data|données]] à partir d'une [[Backup|sauvegarde]] pour les rendre de nouveau accessibles et utilisables.
*   **[[3-2-1Rule|Règle du 3-2-1]]**: Une pratique fondamentale pour assurer la résilience des [[Backup|sauvegardes]], préconisant d'avoir au moins **3** copies des [[Data|données]], sur **2** types de médias différents, avec **1** copie conservée [[OffsiteStorage|hors site]].
*   **Objectifs de Récupération**: Mesures cruciales définissant la tolérance aux pertes et aux interruptions.
    *   **[[RecoveryTimeObjective|RTO]] (Recovery Time Objective)**: Le temps maximum admissible pendant lequel un [[System|système]] ou une [[SoftwareApplication|application]] peut être hors service après un incident.
    *   **[[RecoveryPointObjective|RPO]] (Recovery Point Objective)**: La quantité maximale de [[Data|données]] que l'on est prêt à perdre, mesurée en temps, entre la dernière [[Backup|sauvegarde]] et l'incident.
*   **[[BackupEncryption|Chiffrement des Sauvegardes]]**: L'utilisation de techniques de [[DataEncryption|chiffrement]] pour protéger la [[Confidentiality|confidentialité]] des [[Data|données]] stockées dans les [[Backup|sauvegardes]], les rendant illisibles pour les [[UnauthorizedAccess|accès non autorisés]].
*   **[[Immutability|Immuabilité]]**: Principe de rendre les [[Backup|sauvegardes]] non modifiables ou non supprimables après leur création (Write Once, Read Many - WORM), protégeant contre les [[Ransomware|ransomwares]] et les altérations intentionnelles.

## 💡 Importance en Cybersécurité
> La [[Backup|sauvegarde]] est un [[SecurityControl|contrôle de sécurité]] essentiel qui garantit la [[Availability|disponibilité]] et l'[[Integrity|intégrité]] des [[Data|données]]. Elle est la pierre angulaire de la [[DisasterRecovery|reprise après sinistre]] et de la [[BusinessContinuity|continuité des activités]], permettant aux organisations de se remettre de divers incidents tels que les [[Ransomware|ransomwares]], les [[DataCorruption|pertes de données]], les [[HardwareFailure|défaillances matérielles]] ou les [[HumanError|erreurs humaines]]. Sans des [[Backup|sauvegardes]] fiables, une [[System|compromission de système]] peut entraîner une [[ServiceDisruption|interruption de service]] prolongée et des pertes financières importantes. Des [[Backup|sauvegardes]] bien gérées, avec des tests réguliers de [[BackupAndRecovery|restauration]] et un [[OffsiteStorage|stockage hors site]], sont donc vitales pour la résilience de toute [[Enterprise|entreprise]] face aux [[Threat|menaces]] [[Cybersecurity|cyberséécurité]].

## 🔗 Notes Connexes
*   [[BackupAndRecovery|Sauvegarde et Récupération]]
*   [[BusinessContinuity|Continuité des Activités]]
*   [[DisasterRecovery|Reprise après sinistre]]
*   [[DataCorruption|Perte de Données]]
*   [[Ransomware|Ransomware]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[Confidentiality|Confidentialité]]
*   [[Integrity|Intégrité]]
*   [[Availability|Disponibilité]]
*   [[OffsiteStorage|Stockage Hors Site]]
*   [[DataEncryption|Chiffrement des Données]]
*   [[AccessControl|Contrôle d'Accès]]