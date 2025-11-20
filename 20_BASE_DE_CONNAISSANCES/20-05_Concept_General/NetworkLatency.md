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
> La latence réseau est la mesure du délai pris par un paquet de données pour voyager d'un point à un autre sur un réseau.

## 🧠 Concepts Clés / Piliers
*   **Délai de Propagation**: Le temps nécessaire pour que le signal physique (électrique, lumineux, radio) parcoure la distance sur le support réseau. Ce délai est inévitable et est directement lié à la distance physique et à la vitesse de transmission du signal dans le médium.
*   **Délai de Traitement**: Le temps que les dispositifs réseau intermédiaires, tels que les routeurs et les commutateurs réseau, prennent pour examiner et acheminer les paquets. Cela inclut les tâches comme la vérification du checksum, la mise à jour des tables de routage, et le traitement des en-têtes.
*   **Délai de File d'Attente (Queuing Delay)**: Le temps qu'un paquet passe dans la file d'attente d'un dispositif réseau en attendant d'être transmis. Ce délai est directement affecté par la congestion du réseau et le volume de trafic réseau.
*   **Délai de Sérialisation**: Le temps nécessaire pour qu'un dispositif réseau place tous les bits d'un paquet sur le support de transmission. Il dépend de la taille du paquet et de la bande passante du lien.

## 💡 Importance en Cybersécurité
> La latence réseau est un indicateur crucial de la performance réseau et de la disponibilité des systèmes, un pilier fondamental de la triade CIA. Des augmentations inattendues de latence peuvent signaler des problèmes de congestion, des attaques par déni de service (DoS) ou DDoS, des configurations réseau incorrectes, ou même des activités malveillantes comme l'exfiltration de données sur des canaux discrets. La surveillance de la latence est donc essentielle pour la surveillance de sécurité et le dépannage des infrastructures critiques, en particulier pour les applications nécessitant une haute disponibilité et des temps de réponse rapides.

## 🔗 Notes Connexes
*   **Concept de performance**: Débit
*   **Stratégie d'optimisation**: Qualité de service (QoS)
*   **Concept général**: Performance réseau
*   **Méthode de diagnostic**: Surveillance réseau
*   **Problématique liée**: Congestion réseau