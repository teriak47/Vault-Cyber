---
tags:
  - concept
aliases:
  - Default Gateway
  - passerelle par défaut
  - default gateway
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Passerelle par Défaut

## 📥 Définition en une phrase
> La passerelle par défaut est le routeur sur un réseau local qui sert de point de sortie pour le trafic destiné à des réseaux distants, tels que l'Internet.

## 🧠 Concepts Clés / Piliers
*   **Point de Sortie**: Chaque hôte sur un LAN doit connaître l'adresse IP de sa passerelle par défaut pour envoyer des paquets en dehors de son segment réseau local.
*   **Routage**: Lorsqu'un ordinateur doit communiquer avec un appareil qui n'est pas sur son réseau local, il envoie les paquets à la passerelle par défaut, qui est chargée de les acheminer vers le réseau de destination.
*   **Configuration**: L'adresse IP de la passerelle par défaut est souvent attribuée dynamiquement aux appareils terminaux par un serveur DHCP, mais elle peut aussi être configurée statiquement.
*   **Couche Réseau**: La passerelle par défaut opère principalement à la couche réseau du modèle OSI (ou couche Internet du modèle TCP/IP), prenant des décisions de routage basées sur les adresses IP.

## 💡 Importance en Cybersécurité
> La passerelle par défaut est un composant critique de la sécurité réseau, car elle représente un point de contrôle et de vulnérabilité majeur. Une attaque réussie contre la passerelle par défaut peut entraîner une interruption de service généralisée, compromettre la confidentialité et l'intégrité des données via des attaques de l'Homme du Milieu, ou permettre l'accès non autorisé à un réseau interne. Sa sécurité est donc essentielle pour maintenir la disponibilité et la protection des données des systèmes et des utilisateurs. La mise en œuvre de contrôles de sécurité robustes sur la passerelle est une composante fondamentale de la gestion des risques en cybersécurité.

## 🔗 Notes Connexes
*   Routeur
*   Serveur DHCP
*   Couche Réseau
*   Adresse IP
*   Routage
*   LAN
*   WAN
*   NIC
*   Réseau Logique
*   Serveur DHCP malveillant
*   Vulnérabilités de sécurité
*   Attaque de l'Homme du Milieu
*   Surveillance réseau
*   Segmentation réseau