---
tags:
  - reseau/retransmission
  - protocole/delai-attente
  - reseau/retransmission-rapide
  - protocole/fiabilite
  - communication/accuse-reception
  - couche/transport
aliases:
  - Retransmission
  - Réémission
source:
  - null
cssclasses:
  - max
---

# Retransmission (Réémission)

## 📥 Définition en une phrase
> La retransmission est un mécanisme par lequel un émetteur renvoie des données précédemment envoyées parce qu'elles n'ont pas été reçues correctement ou du tout par le destinataire, afin d'assurer la fiabilité de la communication.

## 🧠 Concepts Clés / Fonctionnement
*   **Fiabilité de la Transmission :** Principalement utilisée par des protocoles orientés connexion comme le [[TransmissionControlProtocol|TCP]] pour garantir que tous les paquets de données atteignent leur destination.
*   **Mécanisme d'Accusé de Réception :** L'émetteur attend un accusé de réception (ACK) du destinataire pour chaque paquet envoyé.
*   **Déclencheurs :** Une retransmission est déclenchée si l'émetteur ne reçoit pas d'ACK dans un délai prédéfini (timeout) ou s'il reçoit des accusés de réception dupliqués ("Fast Retransmit").
*   **Causes Communes :** La perte de paquets peut être due à la [[NetworkCongestion|congestion du réseau]], des erreurs de transmission, des défaillances matérielles ou des attaques.

## 🛡️ Risques / Menaces Associés
*   [[NetworkCongestion|Congestion du Réseau]]: Un nombre excessif de retransmissions peut saturer davantage un réseau déjà encombré, créant un cercle vicieux et ralentissant le trafic général.
*   [[DenialOfService|Attaque par Déni de Service (DoS)]]: Des acteurs malveillants peuvent tenter de provoquer un grand nombre de pertes de paquets ou de retransmissions pour épuiser les ressources du réseau ou de l'hôte.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[QualityOfService|Qualité de Service (QoS)]]: Implémenter la QoS pour prioriser le trafic critique et réduire la probabilité de perte de paquets.
*   **Surveillance Réseau :** Utiliser des outils de surveillance pour détecter les augmentations anormales du taux de retransmission, qui peuvent indiquer une congestion ou des problèmes de liaison.
*   **Optimisation du Buffer :** Configurer correctement les tampons (buffers) des équipements réseau pour gérer les pics de trafic sans perte excessive de paquets.
*   **Amélioration de l'Infrastructure :** Mettre à niveau les équipements réseau et l'infrastructure pour réduire les erreurs de transmission et augmenter la capacité.

## 🔗 Notes Connexes
*   [[PacketLoss|Perte de Paquets]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[TransmissionControlProtocol|TCP]]
*   [[Acknowledgement|Accusé de Réception (ACK)]]