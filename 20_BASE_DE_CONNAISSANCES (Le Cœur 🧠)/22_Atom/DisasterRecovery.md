---
tags:
  - infrastructure/sites-secours
  - planification/tests-validation
  - gestion/continuite-activite
  - planification/reprise-sinistre
  - planification/objectif/point-recuperation
  - planification/objectif/temps-recuperation
aliases:
  - Disaster Recovery
  - Plan de Reprise d'Activité
  - PRA
source:
  - null
cssclasses:
  - max
---

# Reprise Après Sinistre (PRA)

## 📥 Définition en une phrase
> Stratégie et processus mis en œuvre pour restaurer les opérations informatiques et l'accès aux données après un événement perturbateur majeur comme une catastrophe naturelle, une cyberattaque ou une défaillance système grave.

## 🧠 Concepts Clés / Fonctionnement
*   [[RecoveryPointObjective|Objectif de Point de Récupération (RPO)]] : La quantité maximale de données qu'une organisation est prête à perdre, mesurée en temps depuis le dernier point de sauvegarde.
*   [[RecoveryTimeObjective|Objectif de Temps de Récupération (RTO)]] : La durée maximale admissible pendant laquelle un système ou une application peut être hors service après une défaillance avant que l'impact ne devienne inacceptable.
*   [[DisasterRecoveryPlan|Plan de Reprise d'Activité (PRA)]] : Un document détaillé décrivant les procédures et responsabilités pour restaurer les opérations critiques et les services informatiques après un sinistre.
*   Implique souvent la mise en place de sites de secours (chauds, tièdes ou froids), la réplication des données et des systèmes, et la restauration à partir de [[BackupAndRecovery|sauvegardes]].
*   Les tests réguliers du PRA sont cruciaux pour valider son efficacité et identifier les lacunes.

## 🛡️ Risques / Menaces Associés
*   [[NaturalDisaster|Catastrophes naturelles]] (inondations, incendies, tremblements de terre)
*   [[CyberAttack|Cyberattaques]] majeures (ex: [[RansomwareAttack|attaques par rançongiciel]], [[DistributedDenialOfService|attaques par déni de service distribué]])
*   [[HardwareFailure|Pannes matérielles]] ou logicielles massives à l'échelle d'un datacenter.
*   [[HumanError|Erreurs humaines]] critiques entraînant des pertes de données ou des pannes généralisées.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Élaboration, documentation et mise à jour régulière d'un [[DisasterRecoveryPlan|Plan de Reprise d'Activité]] exhaustif.
*   Mise en œuvre d'une stratégie de [[BackupAndRecovery|sauvegarde et de restauration]] robuste (par exemple, la règle 3-2-1: 3 copies de données, sur 2 types de supports différents, avec 1 copie hors site).
*   Utilisation de la [[Virtualization|virtualisation]] et du [[CloudComputing|cloud computing]] pour faciliter la réplication des environnements et la restauration rapide.
*   Tests réguliers et réalistes du PRA pour s'assurer de sa faisabilité et de son adéquation avec les objectifs RPO/RTO.
*   Intégration du PRA dans la stratégie globale de [[BusinessContinuityManagement|gestion de la continuité d'activité (PCA)]].

## 🔗 Notes Connexes
*   [[BusinessContinuity|Continuité d'Activité]]
*   [[IncidentResponse|Réponse aux Incidents]]
*   [[BackupAndRecovery|Sauvegarde et Restauration]]
*   [[RiskManagement|Gestion des Risques]]