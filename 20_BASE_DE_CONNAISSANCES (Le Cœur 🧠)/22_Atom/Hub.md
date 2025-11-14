---
tags:
  - reseau/domaine-collision
  - reseau/domaine-broadcast
  - technologie/obsolete
  - concentrateur-reseau
  - couche/physique
  - cybersecurite/ecoute-clandestine
aliases:
  - Concentrateur
  - Ethernet Hub
source:
  - null
cssclasses:
  - max
---

# Hub (Concentrateur)

## 📥 Définition en une phrase
> Un hub, ou concentrateur, est un dispositif réseau de couche physique (couche 1 du [[OpenSystemsInterconnectionModel|modèle OSI]]) qui connecte plusieurs appareils Ethernet ensemble et qui répète les signaux entrants à tous les autres ports sans filtrage.

## 🧠 Concepts Clés / Fonctionnement
*   Fonctionne au niveau de la [[PhysicalLayer|couche physique]] (couche 1 du [[OpenSystemsInterconnectionModel|modèle OSI]]).
*   Répète chaque paquet de données reçu sur un port à tous les autres ports du hub, sans distinguer la destination.
*   Tous les appareils connectés à un hub partagent le même [[CollisionDomain|domaine de collision]] et le même [[BroadcastDomain|domaine de broadcast]].
*   Les collisions sont fréquentes, ce qui réduit l'efficacité et la bande passante disponible sur le réseau, car seul un appareil peut transmettre à la fois.
*   Considéré comme une technologie réseau obsolète, largement remplacée par les [[NetworkSwitch|switchs réseau]] pour leurs performances et leur sécurité supérieures.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : Tout le trafic est diffusé à tous les ports, facilitant l'interception et l'analyse du trafic par n'importe quel appareil connecté.
*   [[DenialOfService|Déni de service]] (DoS) : La nature du domaine de collision unique rend le réseau vulnérable à des ralentissements ou des pannes en cas de trafic excessif ou malveillant.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Remplacer les hubs par des [[NetworkSwitch|switchs réseau]] (commutateurs) modernes qui segmentent les domaines de collision et améliorent les performances et la sécurité.
*   Utiliser la [[NetworkSegmentation|segmentation réseau]] pour isoler les différents segments du réseau et réduire la portée des domaines de collision et de broadcast.

## 🔗 Notes Connexes
*   [[NetworkSwitch|Switch réseau]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[CollisionDomain|Domaine de collision]]
*   [[BroadcastDomain|Domaine de broadcast]]
*   [[Ethernet|Ethernet]]