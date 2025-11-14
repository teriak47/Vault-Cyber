---
tags:
  - communication/accuse-reception/ack-positif
  - communication/accuse-reception/nack-negatif
  - attaque/usurpation-accuse-reception
  - communication/accuse-reception
  - reseau/retransmission
  - reseau/controle-flux
aliases:
  - Acknowledgement
  - Accusé de réception
source:
  - null
cssclasses:
  - max
---

# Accusé de Réception (Acknowledgement)

## 📥 Définition en une phrase
> Un accusé de réception est un signal ou un message envoyé par un destinataire pour confirmer la bonne réception d'une donnée ou d'un message, essentiel pour garantir la fiabilité de la [[NetworkCommunication|communication réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   **Fiabilité des données** : Les accusés de réception sont au cœur des [[NetworkProtocol|protocoles réseau]] orientés connexion, comme le [[TransmissionControlProtocol|TCP]], pour assurer que toutes les [[Packet|paquets]] de données envoyés ont été reçus par le destinataire.
*   **Mécanisme de retransmission** : Si un expéditeur ne reçoit pas d'accusé de réception dans un certain délai après l'envoi d'un [[Packet|paquet]], il suppose que le [[Packet|paquet]] a été perdu et le retransmet.
*   **Contrôle de flux** : Les accusés de réception peuvent également inclure des informations sur la quantité de données que le destinataire est prêt à recevoir, aidant ainsi à prévenir la surcharge du récepteur.
*   **Types d'accusés de réception** : Il peut s'agir d'un ACK positif (confirmant la réception) ou d'un NACK négatif (indiquant que le paquet a été reçu mais est corrompu ou qu'un problème est survenu).

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service]] (DoS/DDoS) : L'interception ou la falsification des accusés de réception peut perturber le flux de données, conduisant à des retransmissions inutiles et potentiellement à une [[ServiceDisruption|interruption de service]].
*   [[SpoofingAttack|Usurpation]] : Des attaquants peuvent envoyer de faux accusés de réception pour manipuler l'état de la connexion, par exemple pour faire croire à un expéditeur qu'un paquet a été reçu alors qu'il ne l'est pas, ou vice versa.
*   [[PacketLoss|Perte de paquets]] : L'absence d'accusés de réception peut signaler une [[PacketLoss|perte de paquets]] sur le réseau, souvent due à une congestion ou à des interférences, nécessitant une [[Retransmission|retransmission]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utilisation de [[NetworkProtocol|protocoles réseau]] fiables** : S'appuyer sur des protocoles comme [[TransmissionControlProtocol|TCP]] qui intègrent nativement des mécanismes d'accusé de réception et de [[Retransmission|retransmission]].
*   **Validation des [[Checksum|sommes de contrôle]]** : Utiliser des [[Checksum|sommes de contrôle]] au niveau de chaque [[Packet|paquet]] pour s'assurer de l'intégrité des données avant d'envoyer un accusé de réception.
*   **Sécurisation du réseau** : Implémenter des [[NetworkSecurity|mesures de sécurité réseau]] pour prévenir les [[SpoofingAttack|usurpations]] et les manipulations de [[Packet|paquets]], telles que des pare-feu et des systèmes de détection d'intrusion.

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|Protocole de contrôle de transmission]]
*   [[NetworkCommunication|Communication réseau]]
*   [[Protocol|Protocole]]
*   [[Packet|Paquet]]
*   [[Retransmission|Retransmission]]
*   [[Checksum|Somme de contrôle]]
---