---
tags:
aliases:
  - Disaster Recovery
  - Plan de Reprise d'Activité
  - PRA
  - Disaster Recovery Planning
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Reprise Après Sinistre (PRA)

## 📥 Définition en une phrase
> Stratégie et processus mis en œuvre pour restaurer les opérations [[Computer|informatiques]] et l'accès aux [[Data|données]] après un événement perturbateur majeur comme une [[NaturalDisaster|catastrophe naturelle]], une [[Attack|cyberattaque]] ou une [[HardwareFailure|défaillance système]] grave.

## 🧠 Concepts Clés / Piliers
*   **Objectifs de Récupération (RPO & RTO)**: Le [[RecoveryPointObjective|RPO]] (Objectif de Point de Récupération) définit la quantité maximale de [[Data|données]] qu'une [[Enterprise|organisation]] est prête à perdre, mesurée en temps depuis le dernier point de [[Backup|sauvegarde]]. Le [[RecoveryTimeObjective|RTO]] (Objectif de Temps de Récupération) spécifie la durée maximale admissible pendant laquelle un [[System|système]] ou une [[SoftwareApplication|application]] peut être hors service avant que l'impact ne devienne inacceptable. Ces métriques sont fondamentales pour dimensionner la stratégie de [[DisasterRecovery|reprise après sinistre]].
*   **Plan de Reprise d'Activité (DRP)**: Le [[DisasterRecoveryPlanning|DRP]] est un document structuré et détaillé qui formalise les [[Process|procédures]], les rôles et les responsabilités pour restaurer les [[System|systèmes]] et services [[Enterprise|critiques]] post-sinistre. Il est le cœur de toute initiative de [[DisasterRecovery|reprise d'activité]] et doit être intégré dans le [[BusinessContinuityPlanning|planification globale de la continuité des activités]].
*   **Stratégies de Réplication et de [[BackupAndRecovery|Sauvegarde]]**: La [[Redundancy|redondance]] des [[Data|données]] et des [[System|systèmes]] est atteinte via la mise en place de sites de secours (chauds, tièdes, froids), la [[DataEncryption|réplication des données]] en temps réel ou quasi-réel, et des [[BackupAndRecovery|sauvegardes]] régulières et robustes (souvent selon la règle 3-2-1). L'utilisation de la [[Virtualization|virtualisation]] et du [[Cloud|cloud computing]] peut grandement faciliter ces processus en offrant flexibilité et évolutivité.
*   **Tests et Mises à Jour Réguliers**: Un [[DisasterRecoveryPlanning|plan de reprise d'activité]] n'est efficace que s'il est testé régulièrement et mis à jour pour s'adapter à l'évolution de l'[[NetworkInfrastructure|infrastructure]], des [[Software|logiciels]] et des [[Threat|menaces]]. Ces tests (par exemple, des simulations de sinistre) permettent d'identifier les lacunes, de valider les [[Process|procédures]] et de s'assurer de l'atteinte des objectifs RPO/RTO.

## 💡 Importance en Cybersécurité
> Le [[DisasterRecovery|Plan de Reprise d'Activité]] est une composante essentielle de la [[Cybersecurity|cybersécurité]] et de la [[BusinessContinuity|continuité des activités]]. Il assure la [[Availability|disponibilité]] et l'[[Integrity|intégrité]] des [[System|systèmes]] et des [[Data|données]] face à des [[Threat|menaces]] majeures, qu'elles soient d'origine [[NaturalDisaster|naturelle]], accidentelle (comme une [[HumanError|erreur humaine]]) ou malveillante (comme une [[Attack|cyberattaque]] telle que le [[Ransomware|rançongiciel]] ou le [[DistributedDenialOfService|déni de service distribué]]). En minimisant les [[ServiceDisruption|interruptions de service]] et la [[DataCorruption|perte de données]], le PRA protège l'[[Enterprise|organisation]] contre des [[FinancialLoss|pertes financières]] importantes et des [[ReputationalDamage|dommages réputationnels]], tout en garantissant la [[LegalCompliance|conformité légale]] et réglementaire.

## 🔗 Notes Connexes
*   [[BusinessContinuity|Continuité d'Activité]]
*   [[BusinessContinuityPlanning|Planification de la Continuité des Activités]]
*   [[IncidentResponse|Réponse aux Incidents]]
*   [[BackupAndRecovery|Sauvegarde et Récupération]]
*   [[RecoveryPointObjective|Objectif de Point de Récupération (RPO)]]
*   [[RecoveryTimeObjective|Objectif de Temps de Récupération (RTO)]]
*   [[DisasterRecoveryPlanning|Planification de la Reprise après Sinistre]]
*   [[RiskManagement|Gestion des Risques]]
*   [[Availability|Disponibilité]]
*   [[Integrity|Intégrité]]
*   [[Cloud|Cloud Computing]]
*   [[Virtualization|Virtualisation]]
*   [[NaturalDisaster|Catastrophe naturelle]]