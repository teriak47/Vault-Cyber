---
tags:
  - protocole
aliases:
  - Protocole Ethernet
  - IEEE 802.3
  - Ethernet Protocol
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocole Ethernet (IEEE 802.3)

## 🎯 Rôle et Couche OSI
> L'Ethernet est une famille de technologies de mise en réseau standardisée (référencée par l'IEEE sous la norme 802.3) qui définit les règles de transmission et de réception des données sur un réseau local (LAN) filaire. Il opère principalement au niveau de la couche liaison de données (couche 2 du modèle OSI) pour l'adressage MAC et au niveau de la couche physique (couche 1 du modèle OSI) pour la transmission des signaux électriques ou optiques.

## ⚙️ Fonctionnement
1.  **Standardisation** : L'Ethernet est le standard de fait le plus répandu pour les réseaux locaux, également utilisé dans les réseaux métropolitains (MAN) et réseaux étendus (WAN).
2.  **Trames Ethernet** : Les données sont encapsulées dans des structures appelées trames Ethernet. Une trame contient des champs essentiels tels que l'adresse MAC source, l'adresse MAC de destination, le type de protocole (ex: IPv4, IPv6), et la charge utile (les données réelles).
3.  **Adresses MAC** : Chaque interface réseau compatible Ethernet est identifiée par une adresse MAC unique de 48 bits, utilisée pour le adressage au sein d'un segment de réseau local.
4.  **Gestion de l'Accès au Médium** :
    *   Historiquement, les réseaux Ethernet partageaient un médium et utilisaient le CSMA/CD pour gérer les accès et détecter/résoudre les collisions.
    *   Les réseaux Ethernet modernes reposent sur des commutateurs réseau et fonctionnent en full-duplex, ce qui permet une communication simultanée dans les deux directions et élimine les collisions.
*   **Ports par défaut**: N/A (opère aux couches physique et liaison de données, sans notion de ports de couche transport).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Écoute clandestine : Facile sur des réseaux plats ou via des techniques d'usurpation.
    *   Empoisonnement ARP : Permet d'intercepter le trafic réseau en manipulant les tables ARP des hôtes.
    *   MAC Flooding : Attaque saturant la table d'adresses MAC d'un commutateur, le forçant à opérer comme un concentrateur (hub).
*   **Mesures de Sécurité**:
    *   **Utilisation de commutateurs réseau** : Préférer les commutateurs aux concentrateurs pour la segmentation du trafic et la réduction du domaine de diffusion.
    *   **VLANs** : Implémentation de réseaux locaux virtuels pour isoler logiquement le trafic et appliquer des contrôles d'accès granulaires.
    *   **Sécurité des Ports** : Configurer la sécurité des ports sur les commutateurs pour limiter les adresses MAC autorisées à se connecter à un port spécifique.
    *   Authentification 802.1X : Protocole de contrôle d'accès au réseau basé sur les ports, permettant d'authentifier les utilisateurs et les appareils avant qu'ils n'accèdent au réseau.

## 🔗 Notes Connexes
*   Modèle OSI
*   Modèle TCP/IP
*   Adresse MAC
*   Carte d'Interface Réseau (NIC)
*   Trame Ethernet
*   Commutateur Réseau
*   VLAN
*   CSMA/CD
*   ARP
*   Wireshark