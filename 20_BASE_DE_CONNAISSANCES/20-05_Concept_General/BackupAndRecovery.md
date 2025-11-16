---
tags:
aliases:
  - Sauvegarde et Récupération
  - Backup and Recovery
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sauvegarde et Récupération

## 📥 Définition en une phrase
> La sauvegarde et la récupération désignent l'ensemble des processus et des technologies visant à créer des copies de [[Data|données]] et à les restaurer en cas de [[DataCorruption|perte]], de [[DataCorruption|corruption]] ou d'[[Availability|indisponibilité]], assurant ainsi la persistance et l'accessibilité des [[Information|informations]].

## 🧠 Concepts Clés / Piliers
*   **Stratégies de Sauvegarde**: Impliquent la sélection des [[Data|données]] à protéger, la fréquence des sauvegardes et le type de sauvegarde. Les types courants incluent les [[FullBackup|sauvegardes complètes]] (toutes les [[Data|données]]), les [[IncrementalBackup|sauvegardes incrémentielles]] (uniquement les changements depuis la dernière sauvegarde) et les [[DifferentialBackup|sauvegardes différentielles]] (changements depuis la dernière sauvegarde complète). La [[BackupStrategy|stratégie 3-2-1]] est une règle fondamentale, recommandant au moins trois copies des [[Data|données]], sur deux types de [[NetworkMedia|médias]] différents, et une copie [[OffsiteBackup|hors site]].
*   **Objectifs de Récupération (RPO/RTO)**: Le [[RecoveryPointObjective|RPO]] (Recovery Point Objective) définit la quantité maximale de [[Data|données]] qu'une organisation est prête à perdre. Le [[RecoveryTimeObjective|RTO]] (Recovery Time Objective) spécifie le délai maximal acceptable pour restaurer les opérations après un incident. Ces objectifs sont cruciaux pour définir les exigences du [[BackupPlan|plan de sauvegarde]].
*   **Planification et Tests**: Un [[BackupPlan|plan de sauvegarde]] détaillé doit être élaboré, documentant les procédures, les responsabilités et les outils. La [[BackupTesting|vérification régulière]] des processus de récupération est essentielle pour garantir leur efficacité et leur fiabilité en situation réelle, en s'assurant que les [[Data|données]] sont effectivement récupérables.
*   **Sécurité des Sauvegardes**: Les [[BackupStorage|sauvegardes]] elles-mêmes doivent être protégées contre les accès non autorisés, les [[DataCorruption|altérations]] et les [[Attack|attaques]] (ex: [[Ransomware|rançongiciels]]). Cela inclut le [[DataEncryption|chiffrement des données]] au repos et en transit, des [[AccessControl|contrôles d'accès]] stricts, et un [[SecureStorage|stockage sécurisé]], potentiellement [[OffsiteBackup|hors site]] ou dans le [[Cloud|cloud]].

## 💡 Importance en Cybersécurité
> La [[BackupAndRecovery|sauvegarde et la récupération]] sont des composantes fondamentales de la [[Cybersecurity|cybersécurité]] et de la [[BusinessContinuity|continuité des activités]], car elles garantissent la [[Availability|disponibilité]] et l'[[Integrity|intégrité des données]] critiques. Elles permettent aux organisations de se remettre d'incidents majeurs tels que les [[HardwareFailure|pannes matérielles]], les [[SoftwareBugs|erreurs logicielles]], les [[HumanError|erreurs humaines]], les [[Ransomware|attaques de rançongiciels]] ou les [[DataCorruption|violations de données]], minimisant ainsi l'[[ServiceDisruption|interruption de service]] et la [[DataCorruption|perte de données]]. Sans processus de sauvegarde et de récupération fiables, toute [[SystemCompromise|compromission de système]] ou incident peut entraîner des pertes financières catastrophiques, une atteinte à la réputation et une non-conformité réglementaire.

## 🔗 Notes Connexes
*   [[BusinessContinuity|Continuité des Activités]]
*   [[DisasterRecovery|Reprise après Désastre]]
*   [[Availability|Disponibilité]]
*   [[Integrity|Intégrité]]
*   [[DataCorruption|Perte de données]]
*   [[Ransomware|Ransomware]]
*   [[DataEncryption|Chiffrement des Données]]
*   [[AccessControl|Contrôle d'accès]]
*   [[SecureStorage|Stockage Sécurisé]]
*   [[Cybersecurity|Cybersécurité]]