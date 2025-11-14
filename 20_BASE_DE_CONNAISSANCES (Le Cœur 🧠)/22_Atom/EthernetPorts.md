---
tags:
  - port-ethernet
  - securite-fisique-reseau
  - controle-acces-port
  - reseau/segment-local
  - reseau/segmentation-vlan
  - reseau/port/bien-connu
aliases:
  - Ports Ethernet
  - Ethernet Ports
source:
  - null
cssclasses:
  - max
---

# Ports Ethernet

## 📥 Définition en une phrase
> Un port Ethernet est une interface physique présente sur un appareil réseau ou un ordinateur, conçue pour permettre une connexion filaire à un [[LocalAreaNetwork|réseau local]] (LAN) via un [[EthernetCable|câble Ethernet]].

## 🧠 Concepts Clés / Fonctionnement
*   **Interface Physique** : Généralement un connecteur [[RJ45|RJ-45]], il sert de point de connexion pour les [[EthernetCable|câbles Ethernet]] (Cat5e, Cat6, etc.).
*   **Transmission de Données** : Les ports Ethernet supportent des vitesses de transmission de données variées (10/100 Mbps, 1 Gbps, 10 Gbps et plus) et opèrent généralement en mode [[FullDuplex|full-duplex]], permettant l'envoi et la réception simultanés.
*   **Standards** : Le fonctionnement des ports Ethernet est régi par les normes de la famille [[IEEE802_3|IEEE 802.3]], qui définissent les spécifications physiques et de la couche de liaison de données.
*   **Connectivité** : Ils sont utilisés pour connecter des appareils tels que des ordinateurs, des imprimantes, des [[NetworkSwitch|commutateurs réseau]], des [[Router|routeurs]] et des serveurs à un réseau filaire.

## 🛡️ Risques / Menaces Associés
*   [[PhysicalAccess|Accès physique]] non autorisé : Permet à un attaquant de se connecter directement au réseau.
*   [[RogueDevice|Appareil malveillant]] : Connexion d'un appareil non autorisé (ex: [[PacketSniffer|renifleur de paquets]], mini-routeur) pour intercepter le trafic.
*   [[DenialOfService|Attaques par déni de service]] : Surcharge de ports par des requêtes malveillantes.
*   [[PortScanning|Scan de ports]] : Utilisation pour découvrir des services ouverts et des vulnérabilités sur les appareils connectés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PhysicalSecurity|Sécurité physique]] : Verrouillage des salles serveurs et des armoires réseau, ou utilisation de verrous de ports physiques.
*   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]] : Authentification des appareils tentant de se connecter via un port Ethernet.
*   [[PortSecurity|Sécurité des ports]] : Configuration des commutateurs pour limiter les adresses MAC autorisées sur chaque port ou pour désactiver les ports inutilisés.
*   [[VirtualLocalAreaNetwork|Segmentation VLAN]] : Isoler les différents types de trafic ou de départements sur des [[VirtualLocalAreaNetwork|VLANs]] séparés pour limiter la portée d'une compromission.
*   Désactivation des ports inutilisés : Éteindre les ports des commutateurs qui ne sont pas utilisés.

## 🔗 Notes Connexes
*   [[Ethernet|Ethernet]]
*   [[LocalAreaNetwork|Réseau local (LAN)]]
*   [[NetworkInterfaceCard|Carte d'interface réseau (NIC)]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[Router|Routeur]]