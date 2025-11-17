---
tags:
  - concept-general
  - reseau
  - performance
  - optimisation/performance
  - qualite-de-service
  - trafic-reseau
  - delai
  - diagnostic
  - fiabilite
  - communication
aliases:
  - Latence Réseau
  - Latence
  - Network Latency
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Network Latency (Latence Réseau)

## 📥 Définition en une phrase
> La latence réseau est la mesure du délai pris par un paquet de [[Data|données]] pour voyager d'un point à un autre sur un [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Délai de Propagation**: Le temps nécessaire pour que le signal physique (électrique, lumineux, radio) parcoure la distance sur le [[NetworkMedia|support réseau]]. Ce délai est inévitable et est directement lié à la distance physique et à la vitesse de [[SignalTransmission|transmission du signal]] dans le médium.
*   **Délai de Traitement**: Le temps que les [[NetworkDevice|dispositifs réseau]] intermédiaires, tels que les [[Router|routeurs]] et les [[NetworkSwitch|commutateurs réseau]], prennent pour examiner et acheminer les [[Packet|paquets]]. Cela inclut les tâches comme la vérification du checksum, la mise à jour des tables de routage, et le traitement des en-têtes.
*   **Délai de File d'Attente (Queuing Delay)**: Le temps qu'un paquet passe dans la file d'attente d'un [[NetworkDevice|dispositif réseau]] en attendant d'être transmis. Ce délai est directement affecté par la [[NetworkCongestion|congestion du réseau]] et le volume de [[NetworkTraffic|trafic réseau]].
*   **Délai de Sérialisation**: Le temps nécessaire pour qu'un [[NetworkDevice|dispositif réseau]] place tous les bits d'un paquet sur le [[NetworkMedia|support de transmission]]. Il dépend de la taille du paquet et de la [[Bandwidth|bande passante]] du lien.

## 💡 Importance en Cybersécurité
> La [[NetworkLatency|latence réseau]] est un indicateur crucial de la [[NetworkPerformance|performance réseau]] et de la [[Availability|disponibilité]] des [[System|systèmes]], un pilier fondamental de la [[CIATriad|triade CIA]]. Des augmentations inattendues de latence peuvent signaler des problèmes de [[NetworkCongestion|congestion]], des attaques par [[DenialOfService|déni de service]] (DoS) ou [[DistributedDenialOfService|DDoS]], des configurations réseau incorrectes, ou même des activités malveillantes comme l'[[DataExfiltration|exfiltration de données]] sur des canaux discrets. La surveillance de la latence est donc essentielle pour la [[SecurityMonitoring|surveillance de sécurité]] et le [[Troubleshooting|dépannage]] des infrastructures critiques, en particulier pour les applications nécessitant une [[HighAvailability|haute disponibilité]] et des temps de réponse rapides.

## 🔗 Notes Connexes
*   **Concept de performance**: [[Throughput|Débit]]
*   **Stratégie d'optimisation**: [[QualityOfService|Qualité de service (QoS)]]
*   **Concept général**: [[NetworkPerformance|Performance réseau]]
*   **Méthode de diagnostic**: [[NetworkMonitoring|Surveillance réseau]]
*   **Problématique liée**: [[NetworkCongestion|Congestion réseau]]