---
tags:
  - congestion-reseau
  - dégradation-performances
  - gestion-du-trafic
  - networksegmentation
  - qualityofservice
  - bandwidth
aliases:
  - Congestion Réseau
  - Network Congestion
source:
  - null
cssclasses:
  - max
---

# Congestion Réseau

## 📥 Définition en une phrase
> La [[NetworkCongestion|congestion réseau]] se produit lorsque le volume de [[Data|données]] circulant sur un [[Network|réseau]] dépasse la [[Bandwidth|capacité]] du [[CommunicationChannel|canal de communication]], entraînant une dégradation des performances.

## 🧠 Concepts Clés / Fonctionnement
*   **Symptômes**: Se manifeste par une augmentation de la [[Latency|latence]], des pertes de [[Packet|paquets]], des délais de [[Retransmission|retransmission]] et une diminution du [[Throughput|débit]].
*   **Causes**: Peut être due à un trafic excessif (ex: pics d'utilisation, [[DistributedDenialOfService|attaques DDoS]]), une infrastructure [[Network|réseau]] sous-dimensionnée, des [[SoftwareBugs|bogues logiciels]] dans les équipements réseau ou des configurations inadéquates.
*   **Impact**: Affecte la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]] et la réactivité des applications, nuisant à l'expérience utilisateur et aux opérations [[Enterprise|commerciales]].
*   **Mécanismes de Résolution**: Les [[NetworkProtocol|protocoles réseau]] intègrent des mécanismes (comme les fenêtres glissantes dans [[TransmissionControlProtocol|TCP]]) pour tenter de gérer la [[NetworkCongestion|congestion]], mais ils ne peuvent pas toujours empêcher la dégradation lorsque la surcharge est sévère.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service]] (DoS) : Une [[Attack|attaque]] intentionnelle visant à provoquer une [[NetworkCongestion|congestion]].
*   [[ServiceDisruption|Interruption de Service]] : Une conséquence directe de la [[NetworkCongestion|congestion réseau]].
*   [[Availability|Perte de Disponibilité]] : Le système devient inaccessible ou inopérant.
*   [[DataLoss|Perte de Données]] : Des [[Packet|paquets]] peuvent être abandonnés en cas de [[NetworkCongestion|congestion extrême]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[QualityOfService|Qualité de service]] (QoS)** : Prioriser certains types de [[TrafficManagement|trafic réseau]] pour garantir des performances minimales.
*   **Augmentation de la [[Bandwidth|bande passante]]** : Mettre à niveau l'infrastructure pour supporter des volumes de [[Data|données]] plus importants.
*   **[[NetworkSegmentation|Segmentation réseau]]** : Diviser un grand [[Network|réseau]] en segments plus petits pour isoler le [[TrafficManagement|trafic]] et contenir la [[NetworkCongestion|congestion]].
*   **[[LoadBalancing|Équilibrage de charge]]** : Répartir le [[TrafficManagement|trafic]] sur plusieurs [[Server|serveurs]] ou chemins réseau pour éviter la surcharge d'un point unique.
*   **[[RateLimiting|Limitation de débit]]** : Restreindre la quantité de [[TrafficManagement|trafic]] qu'une [[Host|hôte]] ou un [[NetworkInterface|port]] peut envoyer ou recevoir.
*   **[[NetworkMonitoring|Surveillance réseau]]** : Utiliser des outils pour surveiller le [[TrafficManagement|trafic]], la [[Bandwidth|bande passante]], la [[Latency|latence]] et les erreurs afin de détecter et de résoudre la [[NetworkCongestion|congestion]] de manière proactive.

## 🔗 Notes Connexes
*   [[Bandwidth|Bande Passante]]
*   [[Latency|Latence]]
*   [[Throughput|Débit]]
*   [[Packet|Paquet]]
*   [[QualityOfService|Qualité de service]]
*   [[DenialOfService|Déni de Service]]
*   [[Network|Réseau]]
*   [[TrafficManagement|Gestion du Trafic]]