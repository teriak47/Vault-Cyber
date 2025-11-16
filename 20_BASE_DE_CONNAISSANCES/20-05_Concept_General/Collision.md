---
tags:
aliases:
  - Collision (réseau)
  - Collision de paquets
  - Packet Collision
  - Collision
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Collision (Réseau)

## 📥 Définition en une phrase
> Une collision se produit dans un [[Network|réseau]] partagé lorsqu'au moins deux [[NetworkDevice|appareils]] tentent de transmettre des [[Data|données]] simultanément sur le même [[NetworkMedia|support de communication]], entraînant la [[DataCorruption|corruption des données]] et nécessitant une [[Retransmission|retransmission]].

## 🧠 Concepts Clés / Piliers
*   **Contexte Historique**: Principalement associée aux anciens [[Ethernet|réseaux Ethernet]] utilisant des [[Hub|hubs]] et fonctionnant en [[HalfDuplex|mode half-duplex]], où la [[Bandwidth|bande passante]] est partagée et un seul appareil peut transmettre à la fois.
*   **Mécanisme**: Le protocole [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]] est historiquement mis en œuvre sur ces réseaux. Un appareil écoute le support avant de transmettre (Carrier Sense). Si le support est libre, il transmet. Si une [[Collision|collision]] est détectée pendant la [[SignalTransmission|transmission]], tous les appareils impliqués arrêtent leur transmission, attendent un laps de temps aléatoire défini par un [[BackoffAlgorithm|algorithme de backoff]], puis tentent de retransmettre.
*   **[[CollisionDomain|Domaine de Collision]]**: Désigne un [[NetworkSegment|segment de réseau]] où les collisions peuvent se produire. Dans un réseau utilisant un [[Hub|hub]], tous les ports font partie du même [[CollisionDomain|domaine de collision]]. Les [[NetworkSwitch|commutateurs réseau]] modernes créent un [[CollisionDomain|domaine de collision]] distinct par port, ce qui élimine les collisions dans un environnement [[FullDuplex|full-duplex]].
*   **Impact**: Les collisions réduisent l'efficacité du [[Network|réseau]], augmentent la [[Latency|latence]] et entraînent une [[PacketLoss|perte de paquets]] car les [[DataCorruption|données corrompues]] doivent être [[Retransmission|retransmises]].

## 💡 Importance en Cybersécurité
> Bien que moins fréquentes dans les [[Network|réseaux]] modernes basés sur les [[NetworkSwitch|commutateurs]], la compréhension des collisions est cruciale pour identifier les problèmes de [[NetworkPerformance|performance réseau]] et les [[SecurityVulnerabilities|vulnérabilités de sécurité]] potentielles dans les environnements hérités ou mal configurés. Des collisions excessives peuvent indiquer une [[NetworkCongestion|congestion réseau]], des problèmes de [[NetworkConfiguration|configuration]] ou des tentatives de [[DenialOfService|déni de service]] dans des contextes spécifiques, pouvant entraîner une [[DataCorruption|corruption de données]] et une [[ServiceDisruption|interruption de service]].

## 🔗 Notes Connexes
*   [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]]
*   [[Ethernet]]
*   [[Hub]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[HalfDuplex|Half Duplex]]
*   [[FullDuplex|Full Duplex]]
*   [[NetworkSegmentation|Segmentation du réseau]]
*   [[CollisionDomain|Domaine de Collision]]
*   [[BackoffAlgorithm|Algorithme de Backoff]]
*   [[NetworkPerformance|Performance Réseau]]
*   [[SecurityVulnerabilities|Vulnérabilités de Sécurité]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[DataCorruption|Corruption de Données]]
*   [[ServiceDisruption|Interruption de Service]]