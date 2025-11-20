---
tags:
  - reseau
  - donnee
aliases:
  - Paquet
  - Datagram
  - Packet
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Paquet (Packet)

## 🎯 Rôle et Couche OSI
> Un paquet est une unité fondamentale de données encapsulée et transmise sur un réseau, conçue pour un acheminement efficace et structuré. Il opère principalement au niveau de la couche réseau (couche 3) du modèle OSI et du modèle TCP/IP, où le Protocole Internet (IP) en est le principal régisseur. Les datagrammes UDP et les segments TCP sont les équivalents du couche de transport (couche 4).

## ⚙️ Fonctionnement
1.  **Encapsulation**: Le paquet est le résultat de l'encapsulation des données du couche application par les protocoles des couches inférieures. Il est composé d'un en-tête qui contient les informations d'adressage (par exemple, adresses IP source et destination, numéros de port), des informations de contrôle et du corps du message qui est la donnée utile.
2.  **Structure**: Un paquet comprend typiquement un en-tête, la charge utile et, pour certains protocoles, un pied de page (trailer) qui contient des informations pour le contrôle d'erreur.
3.  **Routage**: Les routeurs et autres dispositifs intermédiaires analysent les informations présentes dans l'en-tête du paquet pour déterminer le chemin optimal pour son acheminement vers sa destination.
4.  **Protocoles**: La structure et le comportement d'un paquet sont rigoureusement définis par les protocoles réseau sous-jacents, tels que TCP, UDP et IP au sein de la suite de protocoles TCP/IP.
5.  **Fragmentation**: En cas de besoin, les paquets peuvent être fragmentés en unités plus petites pour traverser des réseaux ayant des Unités de Transmission Maximale (MTU) différentes, avant d'être réassemblés à leur destination.

## 🛡️ Sécurité des Paquets
*   **Vulnérabilités connues**:
    *   Analyse de paquets (interception et lecture des données sensibles)
    *   Attaque de l'homme du milieu (interception et modification des paquets)
    *   Attaques par déni de service (DDoS) (inondation ou malformation de paquets pour épuiser les ressources)
    *   Usurpation d'IP (falsification de l'adresse IP source dans l'en-tête du paquet)
    *   Dépassement de tampon (en envoyant des paquets malformés ou trop grands)
*   **Mesures de protection**:
    *   Chiffrement (pour protéger la charge utile des paquets, ex: TLS, VPN)
    *   Pare-feu (pour filtrer les paquets en fonction de leurs en-têtes et règles de sécurité)
    *   Systèmes de détection d'intrusion (IntrusionDetectionSystem) et Systèmes de prévention d'intrusion (IntrusionPreventionSystem) (pour analyser les paquets à la recherche de signatures d'attaques)
    *   Utilisation de protocoles sécurisés (ex: HTTPS au lieu de HTTP)
    *   Segmentation réseau (pour limiter la portée des paquets malveillants et contenir les attaques)

## 🔗 Notes Connexes
*   Trame
*   Datagramme
*   Analyse du trafic réseau
*   Pile de protocoles
*   TCP
*   UDP
*   IP
*   Couche Réseau
*   Couche de Transport
*   Wireshark
*   En-tête
*   Charge utile
*   Unité de Transmission Maximale