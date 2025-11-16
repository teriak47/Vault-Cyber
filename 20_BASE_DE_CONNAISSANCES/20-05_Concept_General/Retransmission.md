---
tags:
aliases:
  - Réémission
  - Retransmission
  - Packet Retransmission
  - Réémission de Paquets
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Retransmission (Réémission)

## 📥 Définition en une phrase
> La [[Retransmission|retransmission]] est un [[Protocol|mécanisme]] par lequel un émetteur renvoie des [[Data|données]] précédemment envoyées parce qu'elles n'ont pas été reçues correctement ou du tout par le destinataire, afin d'assurer la [[Reliability|fiabilité]] de la [[NetworkCommunication|communication réseau]].

## 🧠 Concepts Clés / Piliers
*   **Fiabilité de la Transmission**: Principalement utilisée par des [[NetworkProtocol|protocoles]] orientés [[TransmissionControlProtocol|connexion]] comme le [[TransmissionControlProtocol|TCP]] pour garantir que tous les [[Packet|paquets]] de [[Data|données]] atteignent leur [[Destination|destination]].
*   **Mécanisme d'Accusé de Réception**: L'émetteur attend un [[Acknowledgement|accusé de réception]] (ACK) du destinataire pour chaque [[Packet|paquet]] envoyé, confirmant sa bonne [[Delivery|livraison]].
*   **Déclencheurs**: Une [[Retransmission|retransmission]] est déclenchée si l'émetteur ne reçoit pas d'[[Acknowledgement|ACK]] dans un délai prédéfini (timeout) ou s'il reçoit des [[Acknowledgement|accusés de réception]] dupliqués ("Fast Retransmit"), signalant une potentielle [[Packet|perte de paquets]].
*   **Causes Communes**: La [[Packet|perte de paquets]] peut être due à la [[NetworkCongestion|congestion du réseau]], des erreurs de [[DataTransmission|transmission]], des [[HardwareFailure|défaillances matérielles]] ou des [[Attack|attaques]].

## 💡 Importance en Cybersécurité
> Comprendre la [[Retransmission|retransmission]] est crucial en [[Cybersecurity|cybersécurité]] car des taux élevés peuvent indiquer des [[SecurityVulnerabilities|vulnérabilités de sécurité]] ou être un symptôme d'une [[DigitalAttack|attaque]]. Par exemple, une [[DistributedDenialOfService|attaque par Déni de Service Distribué (DDoS)]] peut viser à provoquer des [[Retransmission|retransmissions]] excessives pour saturer le [[Network|réseau]] et les [[Resource|ressources]] de l'[[Host|hôte]], entraînant une [[ServiceDisruption|interruption de service]]. La [[SecurityMonitoring|surveillance]] des [[Retransmission|retransmissions]] aide à la [[AnomalyDetection|détection d'anomalies]] et à la [[IncidentResponse|réponse aux incidents]].

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|Transmission Control Protocol (TCP)]]
*   [[Acknowledgement|Accusé de Réception]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[Packet|Paquet]]
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[NetworkPerformance|Performance Réseau]]
*   [[DataTransmission|Transmission de Données]]