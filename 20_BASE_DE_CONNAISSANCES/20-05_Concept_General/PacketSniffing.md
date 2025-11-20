---
tags:
  - reseau/security
  - attaque
  - defense
  - tool
  - protocole/analyse
aliases:
  - Capture de Paquets
  - Interception de Paquets
  - Packet Sniffing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Capture de Paquets (Packet Sniffing)

## 📥 Définition en une phrase
> La capture de paquets est le processus d'interception et d'analyse du trafic réseau qui transite sur un réseau, permettant d'examiner les paquets de données à des fins de diagnostic, de surveillance ou d'attaque.

## 🧠 Concepts Clés / Piliers
*   **Mécanisme de Capture**: Le sniffing repose souvent sur le mode promiscueux d'une carte réseau, qui lui permet d'intercepter tous les paquets présents sur un segment réseau, et non uniquement ceux qui lui sont directement adressés. Des outils spécialisés appelés analyseurs de paquets (comme Wireshark ou Tcpdump) sont utilisés pour acquérir, décoder et analyser ces paquets, en inspectant leurs en-têtes et charges utiles.
*   **Dualité des Usages**: La capture de paquets est une technique à double tranchant. Elle est légitimement employée pour le monitorage réseau, le dépannage des problèmes de communication, l'analyse des performances ou la surveillance de sécurité. Cependant, elle est également un vecteur d'attaque fondamental pour des activités malveillantes comme l'écoute clandestine, le vol de données et la préparation d'attaques de l'homme du milieu.
*   **Stratégies de Protection**: Pour se prémunir contre la capture de paquets illégitime, le chiffrement du canal de communication est primordial (ex: HTTPS, SSH, TLS, VPN, WPA3). La segmentation réseau limite la portée d'une capture, et l'activation de la sécurité des ports sur les commutateurs empêche l'interception non autorisée. Les systèmes de détection d'intrusion (IDS) peuvent alerter sur les comportements suspects liés au sniffing, comme l'empoisonnement ARP.

## 💡 Importance en Cybersécurité
> La capture de paquets est fondamentale en cybersécurité car elle permet d'obtenir une visibilité directe sur le flux de données transitant sur un réseau. Pour les défenseurs (voir Blue Team), c'est un outil indispensable pour la forensique réseau, la détection d'attaques et l'optimisation des performances. Pour les attaquants (voir Red Team), elle constitue une étape initiale critique dans la reconnaissance et l'exploitation des vulnérabilités, pouvant mener à la fuite de données sensibles ou à l'accès non autorisé à des systèmes. Comprendre ses mécanismes est essentiel pour implémenter des mesures de sécurité efficaces.

## 🔗 Notes Connexes
*   Analyse du Trafic Réseau
*   Mode Promiscueux
*   Attaque de l'Homme du Milieu
*   Empoisonnement ARP
*   Wireshark
*   Chiffrement
*   Segmentation Réseau
*   Système de Détection d'Intrusion
*   Écoute Clandestine
*   Tcpdump
*   Divulgation d'informations
*   Dépannage