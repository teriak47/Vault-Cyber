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
> Une collision se produit dans un réseau partagé lorsqu'au moins deux appareils tentent de transmettre des données simultanément sur le même support de communication, entraînant la corruption des données et nécessitant une retransmission.

## 🧠 Concepts Clés / Piliers
*   **Contexte Historique**: Principalement associée aux anciens réseaux Ethernet utilisant des hubs et fonctionnant en mode half-duplex, où la bande passante est partagée et un seul appareil peut transmettre à la fois.
*   **Mécanisme**: Le protocole CSMA/CD est historiquement mis en œuvre sur ces réseaux. Un appareil écoute le support avant de transmettre (Carrier Sense). Si le support est libre, il transmet. Si une collision est détectée pendant la transmission, tous les appareils impliqués arrêtent leur transmission, attendent un laps de temps aléatoire défini par un algorithme de backoff, puis tentent de retransmettre.
*   **Domaine de Collision**: Désigne un segment de réseau où les collisions peuvent se produire. Dans un réseau utilisant un hub, tous les ports font partie du même domaine de collision. Les commutateurs réseau modernes créent un domaine de collision distinct par port, ce qui élimine les collisions dans un environnement full-duplex.
*   **Impact**: Les collisions réduisent l'efficacité du réseau, augmentent la latence et entraînent une perte de paquets car les données corrompues doivent être retransmises.

## 💡 Importance en Cybersécurité
> Bien que moins fréquentes dans les réseaux modernes basés sur les commutateurs, la compréhension des collisions est cruciale pour identifier les problèmes de performance réseau et les vulnérabilités de sécurité potentielles dans les environnements hérités ou mal configurés. Des collisions excessives peuvent indiquer une congestion réseau, des problèmes de configuration ou des tentatives de déni de service dans des contextes spécifiques, pouvant entraîner une corruption de données et une interruption de service.

## 🔗 Notes Connexes
*   CSMA/CD
*   Ethernet
*   Hub
*   Commutateur Réseau
*   Half Duplex
*   Full Duplex
*   Segmentation du réseau
*   Domaine de Collision
*   Algorithme de Backoff
*   Performance Réseau
*   Vulnérabilités de Sécurité
*   Congestion Réseau
*   Corruption de Données
*   Interruption de Service