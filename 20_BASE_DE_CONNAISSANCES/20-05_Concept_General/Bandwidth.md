---
tags:
aliases:
  - Bande Passante
  - Débit
  - Network Bandwidth
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Bande Passante (Bandwidth)

## 📥 Définition en une phrase
> La [[Bandwidth|bande passante]] désigne la capacité maximale théorique de transfert de [[Data|données]] d'une connexion [[Network|réseau]] ou d'un [[CommunicationChannel|canal de communication]], mesurée en [[BitsPerSecond|bits par seconde]] (bps).

## 🧠 Concepts Clés / Piliers
*   **Capacité Théorique**: Elle représente la "largeur du tuyau" par lequel les [[Data|données]] peuvent circuler, indiquant le volume maximal qui *pourrait* être transféré. Il est crucial de la distinguer du [[Throughput|débit réel]] (throughput), qui est la quantité effective de données transférées et souvent inférieure en raison de facteurs comme la [[Latency|latence]], les pertes de [[Packet|paquets]] ou la [[NetworkCongestion|congestion réseau]].
*   **Unités de Mesure**: La [[Bandwidth|bande passante]] est généralement exprimée en [[KilobitsPerSecond|kilobits par seconde]] (Kbps), [[MegabitsPerSecond|mégabits par seconde]] (Mbps), ou [[GigabitsPerSecond|gigabits par seconde]] (Gbps), reflétant la vitesse potentielle de [[DataTransmission|transmission de données]].
*   **Facteurs d'Influence**: La [[Bandwidth|bande passante]] disponible est déterminée par la [[WirelessTechnology|technologie de connexion]] utilisée (ex: [[FiberOpticCable|fibre optique]], [[CableInternet|Internet par câble]], [[WirelessFidelity|Wi-Fi]]), la performance du [[Hardware|matériel réseau]] (comme les [[Router|routeurs]] et les [[NetworkSwitch|commutateurs réseau]]), la qualité de la [[CommunicationChannel|ligne]] et le nombre d'[[User|utilisateurs]] et d'[[SoftwareApplication|applications]] actives.
*   **Goulots d'Étranglement**: Une [[Bandwidth|bande passante]] insuffisante à un point critique du [[Network|réseau]] peut créer un [[Bottleneck|goulot d'étranglement]] majeur, entraînant une dégradation des [[NetworkPerformance|performances réseau]] et potentiellement une [[ServiceDisruption|interruption de service]] pour les [[SoftwareApplication|applications]] critiques.

## 💡 Importance en Cybersécurité
> La [[Bandwidth|bande passante]] est une [[Resource|ressource]] fondamentale pour la [[NetworkCommunication|communication réseau]] et l'[[Availability|disponibilité]] des [[OnlineServices|services en ligne]]. Sa gestion et sa [[SecurityMonitoring|surveillance]] sont essentielles pour maintenir une [[Security|sécurité]] robuste et une [[Availability|disponibilité]] optimale. [[DenialOfService|Les attaques par Déni de Service]] (DoS/DDoS) ciblent spécifiquement la [[Bandwidth|bande passante]] pour saturer les [[CommunicationChannel|canaux de communication]] et provoquer des [[ServiceDisruption|interruptions de service]]. Une utilisation anormale de la [[Bandwidth|bande passante]] peut également être un indicateur d'[[DataExfiltration|exfiltration de données]] ou d'activités malveillantes, rendant sa [[NetworkMonitoring|surveillance du réseau]] cruciale pour la [[ThreatDetection|détection des menaces]]. La mise en œuvre de [[QualityOfService|mécanismes de Qualité de Service]] (QoS) permet de prioriser le trafic vital, assurant ainsi la [[Availability|disponibilité]] des [[Resource|ressources]] même sous contrainte.

## 🔗 Notes Connexes
*   [[Throughput|Débit]]
*   [[Latency|Latence]]
*   [[DenialOfService|Attaque par Déni de Service]]
*   [[DistributedDenialOfService|Attaque par Déni de Service Distribué]]
*   [[NetworkPerformance|Performance Réseau]]
*   [[NetworkMonitoring|Surveillance du réseau]]
*   [[QualityOfService|Qualité de Service]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[DataExfiltration|Exfiltration de données]]
*   [[ServiceDisruption|Interruption de Service]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[IntrusionDetectionSystem|Système de détection d'intrusion]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion]]