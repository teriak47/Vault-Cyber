---
tags:
  - reseau
aliases:
  - Latence
  - Network Latency
  - Latency
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Latence (Latency)

## 📥 Définition en une phrase
> La latence est le délai temporel mesurable entre l'envoi d'un [[SignalTransmission|signal]] et sa réception, ou entre une instruction et le début de son exécution dans un [[Network|réseau]] ou un [[System|système]] [[Computer|informatique]].

## 🧠 Concepts Clés / Piliers
*   **Mesure** : Généralement exprimée en [[BitsPerSecond|millisecondes]] (ms), elle quantifie le temps nécessaire à un [[Packet|paquet]] de [[Data|données]] pour traverser un [[CommunicationChannel|canal de communication]]. Le [[RoundTripTime|temps d'aller-retour (RTT)]] est une mesure courante.
*   **Causes** : Elle peut être due à la [[Distance|distance géographique]], la [[NetworkCongestion|congestion du réseau]], le nombre de sauts (hops) à travers des [[Router|routeurs]], les performances des [[NetworkDevice|équipements réseau]], et les traitements intermédiaires (ex: [[Firewall|pare-feu]], [[Proxy|proxies]]).
*   **Impact** : Une [[Latency|latence]] élevée dégrade l'[[UserExperience|expérience utilisateur]] pour les [[SoftwareApplication|applications]] interactives telles que les [[OnlineGaming|jeux en ligne]], la [[VoIP|Voix sur IP]] et la [[VideoConferencing|visioconférence]], ainsi que pour les [[Transaction|transactions]] sensibles au temps.
*   **Variabilité** : La [[Jitter|gigue]] est la variation de la latence au fil du temps, affectant la qualité des [[RealTimeCommunication|communications en temps réel]].

## 💡 Importance en Cybersécurité
> La [[Latency|latence]] est un indicateur crucial de la [[NetworkPerformance|performance réseau]] et de la [[Availability|disponibilité]] des [[System|systèmes]], un pilier fondamental de la [[CIATriad|triade CIA]]. Une augmentation soudaine ou persistante de la [[Latency|latence]] peut signaler des [[Attack|attaques]] comme le [[DenialOfService|déni de service]] ou le [[DistributedDenialOfService|déni de service distribué]], des [[NetworkCongestion|congestions réseau]] dues à des [[Malware|logiciels malveillants]] ([[Botnet|botnets]]) ou des [[ConfigurationDrift|dérives de configuration]]. Sa surveillance est essentielle pour détecter les anomalies et maintenir la [[Security|sécurité]] opérationnelle.

## 🔗 Notes Connexes
*   [[Bandwidth|Bande passante]]
*   [[Throughput|Débit]]
*   [[Jitter|Gigue]]
*   [[NetworkPerformance|Performance Réseau]]
*   [[RoundTripTime|Temps d'Aller-Retour (RTT)]]
*   [[NetworkMonitoring|Surveillance réseau]]
*   [[QualityOfService|Qualité de Service (QoS)]]
*   [[ContentDeliveryNetwork|Content Delivery Network (CDN)]]
*   [[BandwidthManagement|Gestion de la bande passante]]
*   [[DenialOfService|Déni de Service]]
*   [[DistributedDenialOfService|Déni de Service Distribué]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[EdgeComputing|Edge Computing]]