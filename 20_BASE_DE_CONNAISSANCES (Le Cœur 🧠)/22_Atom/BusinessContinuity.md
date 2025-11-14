---
tags:
  - plan-continuité
  - ingenierie/resilience
  - risques/catastrophe-naturelle
  - planification/continuite-activite
  - gestion-risques/analyse-impact-affaires
  - planification/objectif/temps-recuperation
aliases:
  - Continuité des Activités
  - Continuité des Affaires
  - BCA
  - Business Continuity
source:
  - null
cssclasses:
  - max
---

# Continuité des Activités (BCA)

## 📥 Définition en une phrase
> La capacité d'une organisation à maintenir ses fonctions critiques pendant et après une perturbation majeure, afin de minimiser les interruptions de service et les impacts opérationnels.

## 🧠 Concepts Clés / Fonctionnement
*   **Analyse d'Impact sur les Affaires (BIA)**: Processus d'identification des fonctions et processus critiques d'une organisation et d'évaluation des impacts financiers et opérationnels d'une interruption.
*   **Objectif de Temps de Reprise (RTO)**: Le temps maximal acceptable pendant lequel une application ou un système peut être indisponible après un incident.
*   **Objectif de Point de Reprise (RPO)**: La quantité maximale de données qui peut être perdue à la suite d'un incident, généralement mesurée en temps (ex: 4 heures de données).
*   **Stratégies de Continuité**: Développement et mise en œuvre de mesures pour assurer la reprise des opérations critiques (ex: redondance, sauvegardes, sites de repli).
*   **Plan de Continuité des Activités (PCA / BCP)**: Un plan documenté détaillant les étapes et les procédures à suivre pour réagir à une interruption et rétablir les fonctions essentielles.

## 🛡️ Risques / Menaces Associés
*   [[CyberAttack|Cyberattaques]] (ex: [[Ransomware|Ransomware]], [[DDoSAttack|attaques DDoS]])
*   [[NaturalDisaster|Catastrophes naturelles]] (ex: inondations, tremblements de terre, incendies)
*   [[HumanError|Erreurs humaines]] (ex: suppression accidentelle de données, configuration incorrecte)
*   [[HardwareFailure|Pannes matérielles]] et [[SoftwareFailure|logiciels]] (ex: défaillance de serveurs, bugs critiques)
*   [[SupplyChainAttack|Défaillances de la chaîne d'approvisionnement]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[BusinessImpactAnalysis|Analyse d'Impact sur les Affaires (BIA)]]
*   [[DisasterRecoveryPlan|Plan de Reprise d'Activité (PRA)]]
*   [[BackupAndRecovery|Stratégies de sauvegarde et de récupération]] robustes
*   [[Redundancy|Mise en place de la redondance]] pour les systèmes critiques (ex: serveurs, réseaux, alimentation électrique)
*   [[IncidentResponsePlan|Plan de Réponse aux Incidents]] pour une gestion rapide et efficace des perturbations.
*   [[EmployeeTraining|Formation des employés]] sur les procédures de continuité.

## 🔗 Notes Connexes
*   [[DisasterRecovery|Reprise d'Activité (DR)]]
*   [[RiskManagement|Gestion des Risques]]
*   [[ResilienceEngineering|Ingénierie de la Résilience]]
*   [[InformationSecurityManagementSystem|Système de Gestion de la Sécurité de l'Information (SGSI)]]