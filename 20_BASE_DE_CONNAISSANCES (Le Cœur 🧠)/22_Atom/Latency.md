---
tags:
  - performance/temps-aller-retour
  - reseau/gigue
  - infrastructure/calcul-peripherique
  - reseau/latence
  - reseau/congestion
  - gestion-trafic/qualite-service
aliases:
  - Latence
  - Network Latency
source:
  - null
cssclasses:
  - max
---

# Latence

## 📥 Définition en une phrase
> La latence est le délai temporel entre le moment où une instruction est donnée ou un signal est envoyé, et le début de son exécution ou la réception du signal.

## 🧠 Concepts Clés / Fonctionnement
*   **Mesure** : Généralement exprimée en millisecondes (ms), elle représente le temps qu'il faut à un paquet de données pour voyager d'un point à un autre sur un réseau.
*   **Types** : On distingue la latence aller simple (one-way latency) et le temps d'aller-retour (Round Trip Time - RTT), ce dernier étant le plus couramment mesuré.
*   **Causes** : Peut être influencée par la distance géographique, la congestion du réseau, le nombre de sauts (hops) entre les routeurs, la performance des équipements réseau, et les traitements intermédiaires (ex: pare-feu, proxies).
*   **Impact** : Une latence élevée peut dégrader l'expérience utilisateur pour les applications interactives (jeux en ligne, VoIP, visioconférence) et les transactions sensibles au temps.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS)]] et [[DistributedDenialOfService|DDoS]] qui saturent le réseau et augmentent drastiquement la latence.
*   [[PerformanceDegradation|Dégradation des performances]] des systèmes et applications critiques.
*   [[NetworkCongestion|Congestion réseau]] résultant d'un trafic excessif ou de goulots d'étranglement.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkMonitoring|Surveillance réseau]] proactive pour identifier les sources de latence.
*   [[QualityOfService|Mise en œuvre de la Qualité de Service (QoS)]] pour prioriser le trafic sensible à la latence.
*   Utilisation de [[ContentDeliveryNetwork|Content Delivery Networks (CDNs)]] pour rapprocher le contenu des utilisateurs.
*   Optimisation du routage réseau et [[BandwidthManagement|gestion de la bande passante]].
*   Déploiement d'infrastructures physiques plus proches des utilisateurs finaux (edge computing).

## 🔗 Notes Connexes
*   [[Bandwidth|Bande passante]]
*   [[Throughput|Débit]]
*   [[Jitter|Gigue]]
*   [[NetworkPerformance|Performance Réseau]]
*   [[RoundTripTime|Temps d'Aller-Retour (RTT)]]