---
tags:
  - controle-de-flux
  - reseau
aliases:
  - Contrôle de Flux
  - Flow Control
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Contrôle de Flux (Flow Control)

## 📥 Définition en une phrase
> Le **Contrôle de Flux** est un mécanisme fondamental dans les communications réseau qui gère le taux de transmission de données entre deux nœuds, un expéditeur et un récepteur, afin d'éviter qu'un expéditeur rapide ne submerge un récepteur lent.

## 🧠 Concepts Clés / Piliers
*   **Prévention de la Submersion**: Le principal objectif est d'assurer que le récepteur peut traiter les données au fur et à mesure de leur réception, empêchant ainsi la corruption de données ou la perte de données due à un dépassement de la capacité de son tampon.
*   **Mécanismes d'Ajustement**: Le contrôle de flux utilise diverses techniques pour informer l'expéditeur de la capacité du récepteur. Les méthodes courantes incluent le "Stop-and-Wait" (où l'expéditeur attend un accusé de réception pour chaque bloc de données) et la "Fenêtre Glissante" (Sliding Window), qui permet l'envoi de plusieurs blocs avant un accusé de réception, améliorant l'efficacité.
*   **Mise en Œuvre par les Protocoles**: Des protocoles de la couche de transport comme le Protocole de Contrôle de Transmission (TCP) implémentent le contrôle de flux de manière sophistiquée. TCP utilise des fenêtres de réception dynamiques qui s'ajustent en fonction de la disponibilité du tampon du récepteur et de la congestion réseau pour garantir une livraison fiable et ordonnée.

## 💡 Importance en Cybersécurité
> Le contrôle de flux est un aspect crucial de la fiabilité des systèmes et de la disponibilité des services en ligne. En empêchant la surcharge des récepteurs, il aide à prévenir les scénarios qui pourraient autrement être exploités pour des attaques par déni de service (DoS) ou de déni de service distribué (DDoS), où un attaquant tenterait de submerger un serveur avec un volume de trafic supérieur à sa capacité de traitement. Il contribue également à la intégrité des données en minimisant la perte ou la corruption due à des tampons débordés.

## 🔗 Notes Connexes
*   **Couche d'opération**: Couche de Transport
*   **Problématique associée**: Bande Passante
*   **Mécanisme complémentaire**: Retransmission
*   **Métriques de performance**: Débit
*   **Gestion des ressources**: Qualité de service (QoS)