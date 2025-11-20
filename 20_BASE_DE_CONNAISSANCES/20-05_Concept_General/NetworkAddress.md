---
tags:
aliases:
  - Adresse Réseau
  - Network Address
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse Réseau

## 📥 Définition en une phrase
> Une adresse réseau est un identifiant logique ou physique unique attribué à un dispositif au sein d'un réseau informatique, essentiel pour sa localisation, son routage et sa communication effective.

## 🧠 Concepts Clés / Piliers
*   **Identification Unique**: Chaque hôte ou interface réseau sur un réseau se voit attribuer une adresse réseau afin d'être distingué et de pouvoir échanger des données.
*   **Types et Couches**: Les deux principaux types sont :
    *   Les adresses MAC (Media Access Control), des identifiants physiques uniques (gravés sur la carte d'interface réseau) qui opèrent au niveau de la couche liaison de données (couche 2 du modèle OSI) pour la communication locale.
    *   Les adresses IP (Internet Protocol), des identifiants logiques qui opèrent au niveau de la couche réseau (couche 3 du modèle OSI) pour le routage et la communication à travers des réseaux interconnectés.
*   **Routage et Commutation**: Les routeurs exploitent les adresses IP pour déterminer les chemins d'acheminement des paquets entre différents réseaux, tandis que les commutateurs réseau utilisent les adresses MAC pour diriger les trames Ethernet vers les terminaux appropriés au sein d'un même LAN.
*   **Configuration**: Les adresses IP peuvent être attribuées de manière statique (manuellement) ou dynamique (automatiquement par un serveur DHCP).

## 💡 Importance en Cybersécurité
> Les adresses réseau sont au cœur de toute communication réseau et représentent une surface d'attaque significative. Leur intégrité et leur bonne gestion sont fondamentales pour la sécurité d'un système ou d'un réseau. Une manipulation malveillante des adresses réseau peut entraîner des accès non autorisés, des attaques de l'homme du milieu, ou des interruptions de service. Des mesures comme la segmentation réseau, le filtrage MAC ou la surveillance DHCP sont essentielles pour atténuer ces menaces et assurer la confidentialité, l'intégrité et la disponibilité des données et des ressources.

## 🔗 Notes Connexes
*   Adresse IP
*   Adresse MAC
*   Communication Réseau
*   Couche Réseau
*   Couche Liaison de Données
*   Segmentation Réseau
*   Usurpation d'adresse MAC
*   Empoisonnement ARP
*   Serveur DHCP malveillant
*   DHCP Snooping