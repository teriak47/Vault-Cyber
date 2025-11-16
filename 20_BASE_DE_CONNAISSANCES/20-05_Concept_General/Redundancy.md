---
tags:
aliases:
  - Redondance
  - Redundancy
  - Duplication de Ressources
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Redondance

## 📥 Définition en une phrase
> La redondance est une stratégie qui consiste à dupliquer des composants ou des chemins critiques au sein d'un [[System|système]] pour assurer sa [[HighAvailability|haute disponibilité]] et sa [[Resilience|résilience]] face aux [[HardwareFailure|défaillances]] ou [[ServiceDisruption|interruptions de service]].

## 🧠 Concepts Clés / Piliers
*   **Duplication Stratégique**: Implique la création de copies multiples de [[Hardware|matériels]] (par exemple, [[Server|serveurs]], disques, alimentations), de [[Software|logiciels]] ou de [[Network|chemins réseau]] pour éliminer les [[SinglePointOfFailure|points de défaillance uniques]].
*   **[[FaultTolerance|Tolérance aux Pannes]]**: Permet à un [[System|système]] de continuer à fonctionner sans interruption significative même si un ou plusieurs de ses composants primaires échouent, grâce à des mécanismes de [[Failover|basculement]] automatique vers les éléments dupliqués.
*   **Objectifs de Résilience**: Les buts principaux de la redondance sont d'améliorer la [[HighAvailability|disponibilité]] (minimiser les temps d'arrêt), la [[Reliability|fiabilité]] (garantir un fonctionnement continu et correct) et l'[[Integrity|intégrité des données]] face aux imprévus.

## 💡 Importance en Cybersécurité
> La redondance est un pilier fondamental de la [[Cybersecurity|cybersécurité]] et de la [[BusinessContinuity|continuité des activités]]. Elle assure la [[Availability|disponibilité]] des [[Resource|ressources]] et des [[Data|données]], même en cas d'[[Attack|attaque]], de [[HardwareFailure|panne matérielle]], d'[[SoftwareVulnerability|erreur logicielle]] ou d'[[HumanError|erreur humaine]]. En minimisant les [[ServiceDisruption|interruptions de service]] et la [[DataLoss|perte de données]], la redondance protège la [[Reputation|réputation]] d'une [[Enterprise|entreprise]] et réduit le [[FinancialLoss|risque de pertes financières]] importantes, contribuant ainsi à la [[Resilience|résilience]] globale de l'[[InformationSecurity|infrastructure d'information]].

## 🔗 Notes Connexes
*   [[HighAvailability|Haute Disponibilité]]
*   [[FaultTolerance|Tolérance aux Pannes]]
*   [[Resilience|Résilience]]
*   [[BusinessContinuityPlanning|Planification de la Continuité des Activités]]
*   [[DisasterRecoveryPlanning|Planification de la Reprise d'Activité]]
*   [[Backup|Sauvegarde]]
*   [[LoadBalancing|Équilibrage de charge]]
*   [[Integrity|Intégrité]]