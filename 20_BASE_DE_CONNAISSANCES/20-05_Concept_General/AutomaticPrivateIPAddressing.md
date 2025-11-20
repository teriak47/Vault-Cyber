---
tags:
aliases:
  - APIPA
  - Automatic Private IP Addressing
  - Adressage IP Privé Automatique
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage IP Privé Automatique (APIPA)

## 📥 Définition en une phrase
> L'APIPA est une fonctionnalité des systèmes d'exploitation qui permet à un hôte de s'auto-attribuer une adresse IP dans une plage spécifique lorsqu'il ne peut pas contacter de serveur DHCP.

## 🧠 Concepts Clés / Piliers
*   **Plage et Masque Standard**: L'APIPA attribue aux ordinateurs une adresse IP dans la plage **169.254.0.1 à 169.254.255.254**, avec un masque de sous-réseau fixe de **255.255.0.0**.
*   **Mécanisme de Déclenchement**: Cette fonctionnalité s'active automatiquement lorsqu'un périphérique réseau, configuré pour obtenir son adresse IP via DHCP, ne parvient pas à recevoir de réponse d'un serveur DHCP après plusieurs tentatives.
*   **Vérification des Conflits**: Avant d'utiliser une adresse IP générée, l'hôte effectue une vérification de sa disponibilité sur le réseau local à l'aide du Protocole de Résolution d'Adresse (ARP).
*   **Portée de la Communication**: Les hôtes utilisant des adresses APIPA peuvent communiquer entre eux sur le même segment de réseau. Cependant, ils ne peuvent pas accéder à d'autres réseaux ou à l'Internet sans la présence d'un routeur ou d'une passerelle configurée avec une adresse IP routable.

## 💡 Importance en Cybersécurité
> Bien que l'APIPA soit conçue pour assurer une connectivité de base en l'absence de DHCP, elle présente des implications significatives en cybersécurité. Elle peut masquer une interruption de service du serveur DHCP, rendant l'identification des problèmes de configuration réseau plus difficile. Les hôtes avec des adresses APIPA ont une connectivité limitée, ce qui peut entraîner des problèmes de communication réseau et une exposition involontaire si des données sont censées être transmises à des réseaux externes. De plus, un acteur de menace pourrait potentiellement exploiter cette dépendance en déployant un serveur DHCP malveillant pour attribuer des adresses IP contrôlées, augmentant ainsi la surface d'attaque. Pour atténuer ces risques, une surveillance réseau rigoureuse du DHCP, une segmentation réseau (par exemple, via des VLAN) et des audits de sécurité réguliers sont essentiels, complétés par une sensibilisation des utilisateurs et des administrateurs.

## 🔗 Notes Connexes
*   Protocole de Configuration d'Hôte Dynamique (DHCP)
*   Adresse IP
*   Réseau Local (LAN)
*   Configuration Réseau
*   Masque de Sous-réseau
*   Protocole de Résolution d'Adresse (ARP)
*   Serveur DHCP
*   Serveur DHCP malveillant
*   Sécurité Réseau
*   Segmentation Réseau
---