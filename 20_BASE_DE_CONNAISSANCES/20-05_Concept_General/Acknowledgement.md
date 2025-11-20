---
aliases:
  - Acknowledgement
  - Accusé de réception
  - ACK
source:
  - 
cssclasses:
  - max
archetype: concept-general
---

# Accusé de Réception (Acknowledgement)

## 📥 Définition en une phrase
> Un accusé de réception est un signal ou un message envoyé par un destinataire pour confirmer la bonne réception d'une donnée ou d'un message, essentiel pour garantir la fiabilité de la communication réseau.

## 🧠 Concepts Clés / Piliers
*   **Fiabilité des Communications**: Les accusés de réception sont au cœur des protocoles réseau orientés connexion, comme le TCP, pour assurer que toutes les paquets de données envoyés ont été reçus par le destinataire. Ils garantissent l'intégrité et la livraison ordonnée des données.
*   **Mécanisme de Retransmission**: Si un expéditeur ne reçoit pas d'accusé de réception dans un certain délai après l'envoi d'un paquet, il suppose que le paquet a été perdu et le retransmet. Ce mécanisme est crucial pour la communication fiable.
*   **Contrôle de Flux**: Les accusés de réception peuvent également inclure des informations sur la quantité de données que le destinataire est prêt à recevoir (fenêtre de réception), aidant ainsi à prévenir la surcharge du récepteur et à optimiser la performance réseau.
*   **Types d'Accusés de Réception**: On distingue les ACK positifs (confirmant la réception réussie) et les NACK négatifs (signalant une erreur, une corruption ou une non-réception d'un paquet).

## 💡 Importance en Cybersécurité
> Les accusés de réception sont des mécanismes fondamentaux qui sous-tendent la fiabilité des communications réseau. En assurant la bonne transmission des données, ils contribuent directement à l'intégrité et à la disponibilité des systèmes d'information. Sans eux, la perte ou la corruption de données serait systémique, rendant de nombreux protocoles inopérants. Leur manipulation par des acteurs de menace (par exemple via des attaques d'usurpation d'ACK ou des dénis de service) peut compromettre l'intégrité des données ou causer une interruption de service, soulignant leur rôle critique dans la cybersécurité.

## 🔗 Notes Connexes
*   Protocole de Contrôle de Transmission
*   Communication Réseau
*   Retransmission
*   Intégrité
*   Disponibilité
*   Déni de Service
*   Usurpation
*   Somme de contrôle
*   Protocole Réseau
*   Paquet
*   Gestion du Trafic
*   Fiabilité
*   Communication fiable
*   Accusé de Réception Positif
*   Accusé de Réception Négatif