---
tags:
  - donnees/replication
  - planification/tests-basculement
  - systeme/surveillance-disponibilite
  - architecture/haute-disponibilite
  - infrastructure/redondance
  - infrastructure/tolerance-pannes
aliases:
  - Haute Disponibilité
  - High Availability
source:
  - null
cssclasses:
  - max
---

# Haute Disponibilité

## 📥 Définition en une phrase
> La Haute Disponibilité (HA) est la capacité d'un système ou d'un service à rester opérationnel et accessible pendant une période de temps prolongée, minimisant les interruptions et garantissant un niveau de performance convenu.

## 🧠 Concepts Clés / Fonctionnement
*   **[[Redundancy|Redondance]]**: Duplication de composants critiques (matériel, logiciel, réseau) pour éliminer les points de défaillance uniques et assurer la continuité en cas de panne.
*   **[[FaultTolerance|Tolérance aux Pannes]]**: La capacité d'un système à continuer de fonctionner, même de manière dégradée, malgré la défaillance d'un ou plusieurs de ses composants.
*   **Basculement (Failover)**: Processus automatique ou manuel de transfert d'un service d'un composant ou système défaillant vers un composant ou système de secours en fonctionnement.
*   **[[LoadBalancing|Équilibrage de Charge]]**: Distribution du trafic réseau ou des requêtes sur plusieurs ressources (serveurs, liens réseau) pour optimiser l'utilisation des ressources, améliorer les performances et augmenter la résilience.
*   **Surveillance et Alertes**: Mise en place d'outils de surveillance pour détecter rapidement les défaillances ou les dégradations de performance et déclencher des alertes.
*   **Réplication des Données**: Maintenir des copies synchronisées des données sur plusieurs emplacements ou périphériques pour prévenir la perte de données en cas de défaillance.

## 🛡️ Risques / Menaces Associés
*   **Coût et Complexité**: La mise en œuvre et la maintenance de solutions de HA peuvent être coûteuses et complexes à concevoir, déployer et gérer.
*   **Points de Défaillance cachés**: Malgré la redondance, des configurations incorrectes ou des dépendances inattendues peuvent créer de nouveaux points de défaillance.
*   **Défaillance de Composants Critiques non redondants**: Oubli de certains composants dans la stratégie de redondance (ex: un switch non redondant au sein d'une architecture).
*   **Attaques par [[DistributedDenialOfService|Déni de Service Distribué (DDoS)]]**: Visent spécifiquement à surcharger un système pour le rendre indisponible, contournant parfois les mécanismes de HA standards.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Architecture [[Redundancy|Redondante]]**: Concevoir les systèmes avec une redondance à tous les niveaux critiques (serveurs, réseau, stockage, alimentation).
*   **Mise en place de la [[FaultTolerance|Tolérance aux Pannes]]**: Utilisation de clusters, de serveurs de basculement et de la réplication de données.
*   **Tests Réguliers**: Effectuer des tests de basculement et de reprise après sinistre pour valider l'efficacité des mécanismes de HA.
*   **Planification de la [[BusinessContinuity|Continuité des Activités]] et de la [[DisasterRecovery|Reprise après Sinistre]]**: Intégrer la HA comme composante essentielle de ces plans.
*   **Gestion des Changements Rigoureuse**: Tout changement doit être testé pour s'assurer qu'il n'introduit pas de vulnérabilités ou de points de défaillance.
*   **[[ServiceLevelAgreement|SLA]] (Accords de Niveau de Service)**: Définir clairement les objectifs de disponibilité et les métriques associées.

## 🔗 Notes Connexes
*   [[BusinessContinuity|Continuité des Activités]]
*   [[DisasterRecovery|Reprise après Sinistre]]
*   [[Redundancy|Redondance]]
*   [[FaultTolerance|Tolérance aux Pannes]]
*   [[LoadBalancing|Équilibrage de Charge]]
*   [[ServiceLevelAgreement|SLA (Accord de Niveau de Service)]]