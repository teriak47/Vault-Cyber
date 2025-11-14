---
tags:
  - point-defaillance-unique
  - stockage/raid
  - basculement
  - infrastructure/redondance
  - architecture/haute-disponibilite
  - infrastructure/tolerance-pannes
aliases:
  - Redondance
  - Redundancy
source:
  - null
cssclasses:
  - max
---

# Redondance

## 📥 Définition en une phrase
> La redondance est la duplication de composants ou de chemins critiques au sein d'un système pour garantir sa [[HighAvailability|Haute Disponibilité]] et sa [[Resilience|Résilience]] face à une défaillance.

## 🧠 Concepts Clés / Fonctionnement
*   **Duplication de Composants** : Consiste à avoir des copies multiples de matériels (serveurs, disques, alimentations), logiciels ou chemins réseau.
*   **Tolérance aux Pannes** : Permet au système de continuer à fonctionner même si un ou plusieurs composants échouent, grâce à la commutation automatique vers les éléments redondants.
*   **Objectifs Principaux** : Améliorer la [[HighAvailability|Disponibilité]] (minimiser les temps d'arrêt), la [[Reliability|Fiabilité]] (assurer le bon fonctionnement continu) et la [[DataIntegrity|Intégrité des Données]].
*   **Exemples d'Application** :
    *   [[RAID]] pour le stockage des données.
    *   Clusters de serveurs (failover, load balancing).
    *   Alimentations électriques redondantes (UPS, générateurs).
    *   Chemins réseau multiples (MPLS, BGP).

## 🛡️ Risques / Menaces Associés
*   **[[SinglePointOfFailure|Point de Défaillance Unique]]** : Une mauvaise conception peut laisser des points faibles qui, s'ils tombent en panne, annulent les bénéfices de la redondance.
*   **Complexité de Gestion** : Les systèmes redondants sont plus complexes à configurer, à surveiller et à maintenir, augmentant le risque d'[[ConfigurationError|erreurs de configuration]].
*   **Coût Accru** : La duplication de ressources entraîne inévitablement des coûts supplémentaires en matériel, énergie et maintenance.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre des [[DisasterRecoveryPlan|Plans de Reprise d'Activité]] et des [[BusinessContinuity|Plans de Continuité d'Activité]].
*   Utiliser des solutions de [[Backup|Sauvegarde]] et de réplication des données.
*   Tester régulièrement les mécanismes de failover et la capacité des systèmes redondants à prendre le relais.
*   Concevoir des [[HighAvailabilityArchitecture|Architectures à Haute Disponibilité]] dès la phase de conception.

## 🔗 Notes Connexes
*   [[HighAvailability|Haute Disponibilité]]
*   [[FaultTolerance|Tolérance aux Pannes]]
*   [[Resilience|Résilience]]
*   [[BusinessContinuity|Continuité d'Activité]]
*   [[DisasterRecovery|Reprise d'Activité]]
