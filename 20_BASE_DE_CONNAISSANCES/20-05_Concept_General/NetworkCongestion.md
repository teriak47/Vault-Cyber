---
tags:
aliases:
  - Congestion Réseau
  - Network Congestion
  - Traffic Congestion
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Congestion Réseau

## 📥 Définition en une phrase
> La congestion réseau est un état où le volume de [[Data|données]] transitant par un [[Network|réseau]] excède sa [[Bandwidth|capacité]] de traitement, provoquant une dégradation significative des performances.

## 🧠 Concepts Clés / Piliers
*   **Symptômes de la Congestion**: Manifestation visible de la surcharge, incluant l'augmentation de la [[Latency|latence]], la [[DataCorruption|perte de paquets]] (due à l'abandon), et la réduction du [[Throughput|débit]].
*   **Causes Sous-Jacentes**: Facteurs menant à la congestion, tels que des pics de [[TrafficManagement|trafic]] (y compris les [[DistributedDenialOfService|attaques DDoS]]), une [[NetworkInfrastructure|infrastructure réseau]] sous-dimensionnée, ou des [[NetworkConfiguration|configurations]] suboptimales.
*   **Impact sur les Services**: Conséquences directes sur la [[Availability|disponibilité]] des [[OnlineServices|services]] et la performance des applications, affectant l'[[UserExperience|expérience utilisateur]] et les opérations [[Enterprise|commerciales]].
*   **Mécanismes de Gestion**: Stratégies intégrées aux [[NetworkProtocol|protocoles réseau]] (ex: [[TransmissionControlProtocol|TCP]] avec ses fenêtres glissantes) pour tenter d'atténuer la congestion, bien que souvent insuffisantes face à une surcharge sévère.

## 💡 Importance en Cybersécurité
> La congestion réseau est un enjeu majeur en [[Cybersecurity|cybersécurité]] car elle constitue une cible fréquente d'[[Attack|attaques]] de [[DenialOfService|déni de service]] (DoS/[[DistributedDenialOfService|DDoS]]). Sa manipulation peut compromettre la [[Availability|disponibilité]] des [[System|systèmes]] et des [[Resource|ressources]], un pilier essentiel de la [[CIATriad|Triade CIA]], entraînant des [[ServiceDisruption|interruptions de service]] et des [[FinancialLoss|pertes financières]].

## 🔗 Notes Connexes
*   [[Bandwidth|Bande Passante]]
*   [[Latency|Latence]]
*   [[Throughput|Débit]]
*   [[Packet|Paquet]]
*   [[QualityOfService|Qualité de service]]
*   [[DenialOfService|Déni de Service]]
*   [[Network|Réseau]]
*   [[TrafficManagement|Gestion du Trafic]]
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[LoadBalancing|Équilibrage de charge]]
*   [[RateLimiting|Limitation de débit]]
*   [[NetworkMonitoring|Surveillance réseau]]