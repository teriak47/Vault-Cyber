---
tags:
  - a-revoir
aliases:
  - Domaine de Collision
  - Collision Domain
archetype: definition
source:
  - 
cssclasses:
  - max
---

# Domaine de Collision

## 📥 En Bref
> Un domaine de collision est un segment d'un réseau local (LAN) où les transmissions de données peuvent entrer en collision si plusieurs appareils tentent de communiquer simultanément, nécessitant alors une retransmission.

## 💡 Analogie ou Exemple Simple
> Imaginez une salle de conversation unique où tout le monde écoute avant de parler. Si deux personnes commencent à parler en même temps, leurs voix se chevauchent, créant une "collision" où personne ne peut comprendre l'autre. Dans un domaine de collision, tous les appareils partagent le même "espace de parole" et doivent gérer ces chevauchements.

## 📜 Origine / Étymologie
> Le concept de domaine de collision est intrinsèquement lié aux premières implémentations du protocole Ethernet et à l'utilisation de concentrateurs qui partageaient le même support de transmission, rendant les collisions inévitables et nécessitant des mécanismes de détection et de résolution comme le CSMA/CD.

## Détails
Un domaine de collision est une zone logique d'un réseau local où tous les appareils partagent le même support de transmission. Dans ce type de configuration, si deux ou plusieurs appareils transmettent des signaux simultanément, leurs signaux entrent en collision, rendant les données corrompues et nécessitant une retransmission.

Ces collisions sont gérées par la Couche Liaison de Données (plus spécifiquement la sous-couche MAC) à l'aide de protocoles tels que CSMA/CD (Carrier Sense Multiple Access with Collision Detection) dans les réseaux Ethernet. Chaque collision réduit l'efficacité de la bande passante disponible et dégrade la performance du réseau.

Caractéristiques principales :
*   **Support partagé** : Tous les appareils au sein du domaine partagent la même bande passante et le même support physique (par exemple, un câble coaxial ou un câble à paire torsadée connecté à un concentrateur).
*   **Limitation de performance** : Plus le nombre d'appareils dans un domaine de collision est élevé, plus la probabilité de collisions augmente, ce qui réduit le débit effectif du réseau.
*   **Segmentation** : Les commutateurs réseau et les routeurs sont des dispositifs réseau qui segmentent les domaines de collision. Chaque port d'un commutateur constitue généralement un domaine de collision distinct, permettant aux appareils connectés d'envoyer et de recevoir des données en unidiffusion dédiée sans collision.

## Impact sur la cybersécurité :
Bien que la gestion des domaines de collision soit principalement une question de conception réseau, un réseau plat (avec de grands domaines de collision) peut présenter des vulnérabilités de sécurité. Dans un tel environnement, il est plus facile pour un acteur de menace d'effectuer du sniffing de paquets pour intercepter le trafic réseau et de lancer des attaques par déni de service en saturant la chaîne de communication avec un trafic élevé, provoquant de nombreuses collisions et rendant le réseau inutilisable. Une segmentation réseau adéquate est donc une mesure de sécurité essentielle.

## 🔗 Notes Connexes
*   **Concept complémentaire**: Domaine de diffusion
*   **Dispositif obsolète**: Concentrateur
*   **Dispositif moderne**: Commutateur réseau
*   **Protocole sous-jacent**: Ethernet
*   **Couche OSI associée**: Couche Physique