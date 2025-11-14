---
tags:
  - reseau/controle-acces/media
  - couche-liaison/protocole/ppp
  - transmission/format-trame/encadrement
  - couche/liaison-donnees
  - reseau/adressage-mac
  - securite/inspection-arp-dynamique
aliases:
  - Couche Liaison de Données
  - Data Link Layer
source:
  - null
cssclasses:
  - max
---

# Couche Liaison de Données

## 📥 Définition en une phrase
> La couche liaison de données est la deuxième couche du [[OpenSystemsInterconnectionModel|Modèle OSI]], chargée d'assurer le transfert fiable des données entre deux nœuds adjacents sur un même segment de réseau local (LAN).

## 🧠 Concepts Clés / Fonctionnement
*   **Encadrement (Framing)** : Organise les bits provenant de la [[NetworkLayer|couche réseau]] en unités logiques appelées "trames" pour la transmission.
*   **Adressage Physique (MAC Addressing)** : Utilise les [[MediaAccessControlAddress|adresses MAC]] (Media Access Control) pour identifier de manière unique les dispositifs sur un segment de réseau local.
*   **Contrôle d'Accès au Média (MAC - Media Access Control)** : Gère la manière dont les périphériques partagent le support de transmission physique (par exemple, [[Ethernet|Ethernet]] utilise CSMA/CD, [[WirelessLocalAreaNetwork|Wi-Fi]] utilise CSMA/CA).
*   **Détection et Correction d'Erreurs** : Ajoute des mécanismes (comme le CRC - Cyclic Redundancy Check) pour détecter les erreurs de transmission et, dans certains cas, les corriger.
*   **Contrôle de Flux** : Aide à prévenir la surcharge d'un récepteur plus lent par un émetteur plus rapide en régulant le débit de données.
*   **Protocoles Courants** : Incluent [[Ethernet|Ethernet]] (IEEE 802.3), [[WirelessLocalAreaNetwork|Wi-Fi]] (IEEE 802.11) et Point-to-Point Protocol (PPP).

## 🛡️ Risques / Menaces Associés
*   [[MACAddressSpoofing|Usurpation d'adresse MAC]] : Un attaquant se fait passer pour un autre appareil en utilisant son adresse MAC.
*   [[ARPPoisoning|Empoisonnement ARP]] : Manipulation de la table [[AddressResolutionProtocol|ARP]] pour intercepter ou rediriger le trafic.
*   [[VLANHopping|Saut de VLAN]] : Techniques permettant à un attaquant d'accéder à des VLANs auxquels il ne devrait pas avoir accès.
*   [[DenialOfService|Attaques par déni de service]] : Par exemple, inondation de la table MAC d'un commutateur (`MAC Flooding`).

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation réseau]] : Utilisation de [[VirtualLocalAreaNetwork|VLANs]] pour isoler les différents segments de réseau.
*   [[PortSecurity|Sécurité des ports]] : Limiter le nombre d'adresses MAC autorisées par port de commutateur pour prévenir le MAC spoofing et le MAC flooding.
*   [[DynamicARPInspection|Inspection ARP Dynamique (DAI)]] : Valide les paquets ARP pour prévenir l'empoisonnement ARP.
*   [[DHCPSnooping|DHCP Snooping]] : Empêche les serveurs DHCP non autorisés et protège contre certaines attaques.
*   [[AccessControlList|Listes de contrôle d'accès (ACLs)]] : Configuration sur les commutateurs pour filtrer le trafic au niveau de la couche 2.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Ethernet|Ethernet]]
*   [[WirelessLocalAreaNetwork|Wi-Fi]]
*   [[AddressResolutionProtocol|ARP]]