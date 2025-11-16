---
tags:
aliases:
  - Performance réseau
  - Network Performance
  - Performances réseau
  - Performance Réseau
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Performance Réseau

## 📥 Définition en une phrase
> La [[NetworkPerformance|performance réseau]] mesure l'efficacité et la rapidité avec lesquelles un [[Network|réseau]] transmet les [[Data|données]], en évaluant des facteurs clés tels que la [[Bandwidth|bande passante]], le [[Throughput|débit]], la [[Latency|latence]] et le taux d'[[Errors|erreurs]].

## 🧠 Concepts Clés / Piliers
*   **[[Bandwidth|Bande Passante]]**: Représente la capacité maximale théorique d'un [[CommunicationChannel|canal de communication]] à transporter des [[Data|données]] par unité de temps (mesurée en [[BitsPerSecond|bps]], [[KilobitsPerSecond|Kbps]], [[MegabitsPerSecond|Mbps]], [[GigabitsPerSecond|Gbps]]).
*   **[[Throughput|Débit]]**: La quantité réelle de [[Data|données]] transférées avec succès sur le [[Network|réseau]] pendant une période donnée, souvent inférieure à la [[Bandwidth|bande passante]] en raison de facteurs comme la [[NetworkCongestion|congestion]] et la surcharge protocolaire.
*   **[[Latency|Latence]]**: Le temps de retard entre l'envoi d'un paquet de [[Data|données]] par un [[Host|hôte]] et sa réception par un autre, un facteur critique pour la réactivité des applications.
*   **[[Jitter|Jitter]]**: La variation de la [[Latency|latence]] entre les paquets de [[Data|données]], particulièrement importante pour la qualité des applications en temps réel (voix, vidéo).
*   **[[Errors|Erreurs]]**: Le nombre de paquets de [[Data|données]] corrompus ou perdus pendant la [[DataTransmission|transmission]], nécessitant des [[Retransmission|retransmissions]] et impactant directement l'efficacité.

## 💡 Importance en Cybersécurité
> Une [[NetworkPerformance|bonne performance réseau]] est fondamentale pour maintenir la [[CIATriad|disponibilité]] (A de la [[CIATriad|triade CIA]]) des systèmes et des [[OnlineServices|services en ligne]]. Une [[NetworkPerformance|performance]] dégradée ou une [[NetworkCongestion|congestion réseau]] peut être le symptôme ou la conséquence d'une [[Attack|attaque]] (comme un [[DenialOfService|déni de service]]), compromettant l'accès légitime aux [[Resource|ressources]]. De plus, une [[NetworkPerformance|performance]] optimale est essentielle pour le bon fonctionnement des [[SecurityControl|contrôles de sécurité]] (ex: [[Firewall|pare-feu]], [[IntrusionPreventionSystem|IPS]]) et des outils de [[SecurityMonitoring|surveillance]] (comme le [[NetworkMonitoring|monitorage réseau]] et l'[[NetworkTrafficAnalysis|analyse du trafic]]) qui détectent les [[Threat|menaces]] et les [[AnomalyDetection|anomalies]]. Des [[QualityOfService|politiques de QoS]] bien configurées peuvent également être utilisées comme mesure de [[Security|sécurité]] pour prioriser le [[NetworkCommunication|trafic]] critique pendant une [[IncidentResponse|réponse aux incidents]].

## 🔗 Notes Connexes
*   [[Bandwidth|Bande Passante]]
*   [[Throughput|Débit]]
*   [[Latency|Latence]]
*   [[Jitter|Jitter]]
*   [[Errors|Erreurs]]
*   [[NetworkMonitoring|Surveillance Réseau]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[QualityOfService|Qualité de Service]]
*   [[Network|Réseau]]
*   [[DataTransmission|Transmission de Données]]
*   [[Availability|Disponibilité]]
*   [[Integrity|Intégrité]]