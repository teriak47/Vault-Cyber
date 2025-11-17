---
tags:
  - controle-de-flux
  - reseau
aliases:
  - Contrôle de Flux
  - Flow Control
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Contrôle de Flux (Flow Control)

## 📥 Définition en une phrase
> Le **Contrôle de Flux** est un mécanisme fondamental dans les [[NetworkCommunication|communications réseau]] qui gère le taux de [[DataTransmission|transmission de données]] entre deux nœuds, un expéditeur et un récepteur, afin d'éviter qu'un expéditeur rapide ne submerge un récepteur lent.

## 🧠 Concepts Clés / Piliers
*   **Prévention de la Submersion**: Le principal objectif est d'assurer que le récepteur peut traiter les données au fur et à mesure de leur réception, empêchant ainsi la [[DataCorruption|corruption de données]] ou la [[DataLoss|perte de données]] due à un dépassement de la capacité de son [[Buffer|tampon]].
*   **Mécanismes d'Ajustement**: Le contrôle de flux utilise diverses techniques pour informer l'expéditeur de la capacité du récepteur. Les méthodes courantes incluent le "Stop-and-Wait" (où l'expéditeur attend un accusé de réception pour chaque bloc de données) et la "Fenêtre Glissante" (Sliding Window), qui permet l'envoi de plusieurs blocs avant un accusé de réception, améliorant l'efficacité.
*   **Mise en Œuvre par les Protocoles**: Des protocoles de la [[TransportLayer|couche de transport]] comme le [[TransmissionControlProtocol|Protocole de Contrôle de Transmission]] (TCP) implémentent le contrôle de flux de manière sophistiquée. [[TransmissionControlProtocol|TCP]] utilise des fenêtres de réception dynamiques qui s'ajustent en fonction de la disponibilité du [[Buffer|tampon]] du récepteur et de la [[NetworkCongestion|congestion réseau]] pour garantir une livraison fiable et ordonnée.

## 💡 Importance en Cybersécurité
> Le contrôle de flux est un aspect crucial de la [[Reliability|fiabilité]] des [[System|systèmes]] et de la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]]. En empêchant la surcharge des récepteurs, il aide à prévenir les scénarios qui pourraient autrement être exploités pour des attaques par [[DenialOfService|déni de service]] (DoS) ou de [[DistributedDenialOfService|déni de service distribué]] (DDoS), où un attaquant tenterait de submerger un [[Server|serveur]] avec un volume de trafic supérieur à sa capacité de traitement. Il contribue également à la [[Integrity|intégrité]] des données en minimisant la perte ou la corruption due à des tampons débordés.

## 🔗 Notes Connexes
*   **Couche d'opération**: [[TransportLayer|Couche de Transport]]
*   **Problématique associée**: [[Bandwidth|Bande Passante]]
*   **Mécanisme complémentaire**: [[Retransmission]]
*   **Métriques de performance**: [[Throughput|Débit]]
*   **Gestion des ressources**: [[QualityOfService|Qualité de service (QoS)]]