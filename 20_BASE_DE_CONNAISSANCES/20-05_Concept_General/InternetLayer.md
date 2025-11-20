---
tags:
aliases:
  - Couche Internet
  - Internet Layer
  - Couche Réseau
archetype: concept-general
rfc:
cssclasses:
  - max
source:
  - ComparaisonModeleOsiEtModeleTcpip_Cour
  - ProtocolStacksAndReferenceModels_Cour
---

# Couche Internet

## 🎯 Rôle et Couche OSI
> La couche Internet est une abstraction fondamentale de la suite de protocoles TCP/IP, responsable de l'adressage logique et du routage des paquets de données entre différents réseaux interconnectés. Elle est l'équivalent fonctionnel de la couche réseau du modèle OSI.

## ⚙️ Fonctionnement
1.  **Adressage Logique**: Utilise les adresses IP (IPv4 ou IPv6) pour identifier de manière unique les hôtes sur un réseau et permettre leur routage. Contrairement aux adresses MAC qui sont physiques et utilisées à la couche liaison de données, les adresses IP sont logiques et peuvent changer en fonction du réseau.
2.  **Routage des Paquets**: Les routeurs opèrent à cette couche pour transférer les paquets de la source à la destination en se basant sur les tables de routage.
3.  **Protocole IP**: C'est le protocole principal de cette couche. Il gère l'encapsulation des données des couches supérieures dans des paquets IP, leur adressage, et leur fragmentation/réassemblage si nécessaire pour traverser différents médias.
4.  **Protocoles auxiliaires**:
    *   **ICMP**: Un protocole auxiliaire utilisé pour envoyer des messages d'erreur et des informations opérationnelles (ex: diagnostic de connectivité).
    *   **ICMPv6**: Pour IPv6, il inclut des fonctionnalités supplémentaires comme le NDP pour la résolution d'adresses et la découverte de routeurs.
*   **Ports par défaut**: La couche Internet elle-même ne travaille pas avec des numéros de port, qui sont gérés par la couche de transport.

## 🛡️ Sécurité de la Couche Internet
*   **Vulnérabilités connues**:
    *   Usurpation d'adresse IP (IP spoofing), où un attaquant falsifie l'adresse IP source d'un paquet pour masquer son identité ou contourner les contrôles de sécurité.
    *   Attaques par déni de service (DoS) et DDoS qui ciblent la disponibilité du réseau en saturant les routeurs ou les liens réseau avec un trafic malveillant.
    *   Capture de paquets pour intercepter des informations sensibles transitant par le réseau, si les paquets ne sont pas chiffrés par les couches supérieures.
    *   Attaques de routage visant à manipuler les tables de routage pour rediriger le trafic ou causer des interruptions de service.
*   **Mesures de protection**:
    *   Déploiement de pare-feu pour contrôler le trafic entrant et sortant et filtrer les paquets en fonction des adresses IP et d'autres critères.
    *   Mise en œuvre de la segmentation réseau (par exemple, via VLAN) pour isoler les différentes parties du réseau et limiter la propagation des attaques.
    *   Utilisation de systèmes IDS et IPS pour détecter et prévenir les activités malveillantes ciblant cette couche.
    *   Configuration de protocoles de routage sécurisés pour empêcher la falsification des tables de routage.
    *   Chiffrement du trafic au niveau des couches supérieures (ex: TLS, VPN) pour protéger la confidentialité et l'intégrité des données.

## 🔗 Notes Connexes
*   Modèle OSI
*   Couche Réseau
*   Suite de Protocoles Internet
*   Protocole Internet
*   Routeur
*   ICMP
*   ICMPv6
*   NDP
*   DHCP
*   VPN
---