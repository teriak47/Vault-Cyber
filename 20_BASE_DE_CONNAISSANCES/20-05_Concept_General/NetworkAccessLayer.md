---
tags:
aliases:
  - Couche d'Accès Réseau
  - Network Access Layer
  - NetworkAccessLayer
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche d'Accès Réseau (Network Access Layer)

## 📥 Définition en une phrase
> La couche d'accès réseau est le niveau le plus bas du modèle TCP/IP, combinant les fonctions des couches physique et liaison de données du modèle OSI pour gérer la transmission physique des données et l'accès au support réseau.

## 🧠 Concepts Clés / Piliers
*   **Intégration des Fonctions OSI** : Cette couche fusionne les responsabilités de la couche physique (définition des spécifications matérielles, transmission d'impulsions électriques ou d'impulsions lumineuses) et de la couche liaison de données (adressage MAC, contrôle des erreurs et accès au support réseau) des modèles OSI.
*   **Transmission et Encapsulation des Trames** : Elle est directement responsable de l'encapsulation des paquets en trames de données et de leur transmission entre périphériques réseau au sein d'un même réseau local ou sur un canal de communication direct.
*   **Adressage et Contrôle d'Accès au Support** : Elle utilise les adresses MAC pour identifier de manière unique les cartes d'interface réseau des dispositifs terminaux et pour gérer l'accès partagé au réseau physique, notamment dans un domaine de diffusion.
*   **Interface avec le Support Physique** : Elle interagit directement avec divers supports réseau, incluant les câbles de cuivre (comme les paires torsadées et les câbles coaxiaux), la fibre optique (par impulsions lumineuses) et l'air (via les ondes radio, micro-ondes ou ondes infrarouges).

## 💡 Importance en Cybersécurité
> La couche d'accès réseau est fondamentale en cybersécurité car elle constitue le point d'entrée physique et logique des données sur le réseau. Les acteurs de menace ciblent souvent cette couche pour des reconnaissances, l'interception de trafic ou des attaques par déni de service, ce qui en fait un maillon critique pour la sécurité réseau et la confidentialité des données. Une sécurité robuste à ce niveau est essentielle pour prévenir l'accès non autorisé et maintenir l'intégrité et l'disponibilité des communications réseau.

## 🔗 Notes Connexes
*   Modèle OSI
*   Modèle TCP/IP
*   Couche Physique
*   Couche Liaison de Données
*   Couche Réseau
*   Adresse MAC
*   Usurpation d'adresse MAC
*   Empoisonnement ARP
*   Attaque de l'homme du milieu
*   Sécurité des ports
*   Segmentation réseau
*   VLAN
*   DHCP Snooping (méthode de sécurité réseau liée à DHCP)
*   ARP Inspection Dynamique (méthode de sécurité réseau liée à ARP)
*   Sécurité sans fil
*   WPA2
*   WPA3
*   Surveillance réseau
*   IDS
*   SIEM