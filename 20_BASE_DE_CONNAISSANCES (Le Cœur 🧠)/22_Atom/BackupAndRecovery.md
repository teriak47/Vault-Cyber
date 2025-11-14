---
tags:
  - strategie/sauvegarde-3-2-1
  - sauvegarde/types-incrementiels
  - tests/restauration-donnees
  - planification/reprise-sinistre
  - planification/sauvegarde
  - gestion/continuite-activite
aliases:
  - Sauvegarde et Récupération
  - Backup and Recovery
source:
  - null
cssclasses:
  - max
---

# Sauvegarde et Récupération

## 📥 Définition en une phrase
> La sauvegarde et la récupération désignent l'ensemble des processus et des technologies visant à créer des copies de données et à les restaurer en cas de perte, de corruption ou d'indisponibilité, assurant ainsi la persistance et l'accessibilité des informations.

## 🧠 Concepts Clés / Fonctionnement
*   **Types de sauvegardes** : [[FullBackup|Sauvegardes complètes]], [[IncrementalBackup|incrémentielles]], et [[DifferentialBackup|différentielles]], chacune offrant un compromis différent entre le temps de sauvegarde et de récupération, et l'espace de stockage.
*   **Stratégie 3-2-1** : Une règle fondamentale recommandant de conserver au moins trois copies des données, sur deux types de médias différents, et au moins une copie hors site.
*   **Objectifs de Récupération (RPO/RTO)** : Le [[RecoveryPointObjective|RPO]] définit la quantité maximale de données qu'une organisation est prête à perdre, tandis que le [[RecoveryTimeObjective|RTO]] spécifie le délai maximal acceptable pour restaurer les opérations après un incident.
*   **Planification et Tests** : La création d'un [[BackupPlan|plan de sauvegarde]] détaillé et la [[BackupTesting|vérification régulière]] des processus de récupération sont cruciaux pour garantir leur efficacité en situation réelle.
*   **Stockage des sauvegardes** : Les sauvegardes peuvent être stockées sur divers supports (bandes, disques, cloud) et emplacements (sur site, hors site, dans le cloud).

## 🛡️ Risques / Menaces Associés
*   [[DataLoss|Perte de données]] due à des pannes matérielles, des erreurs humaines ou des attaques malveillantes comme les [[Ransomware|rançongiciels]].
*   [[DataCorruption|Corruption des données]] de sauvegarde rendant la restauration impossible ou inefficace.
*   [[AvailabilityRisk|Indisponibilité]] prolongée des systèmes et des données si les processus de récupération sont lents ou échouent.
*   [[InsiderThreat|Menaces internes]] pouvant compromettre l'intégrité ou la confidentialité des sauvegardes.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémenter une [[BackupStrategy|stratégie de sauvegarde]] robuste et automatisée, en respectant la règle 3-2-1.
*   Protéger les [[BackupStorage|emplacements de stockage des sauvegardes]] contre les accès non autorisés, les dommages physiques et les cyberattaques.
*   Effectuer des [[BackupTesting|tests de restauration]] réguliers et documentés pour s'assurer que les données sont récupérables et que les objectifs RPO/RTO sont respectés.
*   Utiliser le [[DataEncryption|chiffrement des données]] pour les sauvegardes, tant au repos qu'en transit, afin de protéger la confidentialité.
*   Mettre en place des mécanismes d'[[AccessControl|contrôle d'accès]] stricts pour les systèmes de sauvegarde et les données stockées.

## 🔗 Notes Connexes
*   [[BusinessContinuity|Continuité des Affaires]]
*   [[DisasterRecovery|Reprise après Désastre]]
*   [[DataRetention|Rétention des Données]]
*   [[DataIntegrity|Intégrité des Données]]