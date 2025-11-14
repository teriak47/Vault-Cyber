---
tags:
  - transmission/mode-duplex/integral
  - transmission/mode-duplex/semi-integral
  - algorithme/retrait-aleatoire
  - reseau/collision
  - acces-media/csma-cd
  - reseau/domaine-collision
aliases:
  - Collision (réseau)
  - Collision de paquets
  - Packet Collision
cssclasses:
  - max
---

# Collision (Réseau)

## 📥 Définition en une phrase
> Une collision se produit dans un réseau partagé lorsqu'au moins deux appareils tentent de transmettre des données simultanément sur le même support de communication, entraînant la corruption des données et nécessitant une retransmission.

## 🧠 Concepts Clés / Fonctionnement
*   **Contexte Historique** : Principalement associée aux anciens réseaux [[Ethernet]] utilisant des [[Hub]] et fonctionnant en [[HalfDuplex|mode half-duplex]], où la bande passante est partagée.
*   **Mécanisme** : Le protocole [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]] est mis en œuvre sur ces réseaux. Un appareil écoute le support avant de transmettre (Carrier Sense), et si le support est libre, il transmet. Si une collision est détectée pendant la transmission, tous les appareils impliqués arrêtent leur transmission, attendent un laps de temps aléatoire (backoff algorithm), puis tentent de retransmettre.
*   **Zone de Collision** : Désigne un segment de réseau où les collisions peuvent se produire. Dans un réseau utilisant un hub, tous les ports font partie de la même zone de collision.
*   **Impact** : Les collisions réduisent l'efficacité du réseau, augmentent la latence et entraînent une [[PacketLoss|perte de paquets]] car les données corrompues doivent être retransmises.

## 🛡️ Risques / Menaces Associés
*   [[NetworkCongestion|Congestion Réseau]]
*   [[PacketLoss|Perte de Paquets]]
*   [[PerformanceDegradation|Dégradation des performances]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utilisation de Commutateurs** : Remplacer les [[Hub]] par des [[NetworkSwitch|commutateurs réseau]] (switches). Un commutateur crée une zone de collision distincte pour chaque port, éliminant ainsi la plupart des collisions.
*   **Mode Full-Duplex** : Configurer les interfaces réseau en [[FullDuplex|mode full-duplex]], ce qui permet la transmission et la réception simultanées sans risque de collision sur la même liaison.
*   **[[NetworkSegmentation|Segmentation du réseau]]** : Diviser un grand réseau en segments plus petits (par exemple, avec des routeurs ou des VLAN) pour réduire la taille des zones de collision.

## 🔗 Notes Connexes
*   [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]]
*   [[Ethernet]]
*   [[Hub|Hub ]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[HalfDuplex|Half Duplex]]
*   [[FullDuplex|Full Duplex]]