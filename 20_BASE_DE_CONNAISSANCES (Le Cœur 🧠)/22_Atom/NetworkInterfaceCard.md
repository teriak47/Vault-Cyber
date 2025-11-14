---
tags:
  - nic
  - mac-address
  - wireless-fidelity
  - MACSpoofing
  - PortSecurity
  - NetworkSegmentation
aliases:
  - Carte d'Interface Réseau
  - NIC
  - Network Interface Card
cssclasses:
  - max
---

# Carte d'Interface Réseau (NIC)

## 📥 Définition en une phrase
> Une [[NetworkInterfaceCard|Carte d'Interface Réseau]] (NIC) est un composant matériel qui permet à un [[Computer|ordinateur]] ou un autre [[NetworkDevice|périphérique réseau]] de se connecter à un [[Network|réseau]] et de communiquer avec d'autres appareils.

## 🧠 Concepts Clés / Fonctionnement
*   **Connexion physique**: La [[NetworkInterfaceCard|NIC]] fournit la connexion physique entre le [[Computer|système]] et le [[NetworkMedia|support réseau]] (comme un [[TwistedPairCable|câble à paire torsadée]] ou [[WirelessMedia|sans fil]]).
*   **Adresse MAC**: Chaque [[NetworkInterfaceCard|NIC]] possède une [[MediaAccessControlAddress|adresse MAC]] (Media Access Control Address) unique, gravée par le fabricant, utilisée pour l'identification au sein du [[DataLinkLayer|couche liaison de données]].
*   **Encapsulation et Décapsulation**: Elle est responsable de l'[[Encapsulation|encapsulation]] et de la [[Decapsulation|décapsulation]] des [[Data|données]] en [[Frame|trames]] pour la transmission et la réception sur le [[Network|réseau]].
*   **Modèle OSI**: Opère principalement à la [[PhysicalLayer|Couche Physique]] et à la [[DataLinkLayer|Couche Liaison de Données]] du [[OpenSystemsInterconnectionModel|modèle OSI]].
*   **Types**: Les [[NetworkInterfaceCard|NICs]] peuvent être intégrées à la carte mère ou être des cartes d'extension, supportant diverses technologies comme [[Ethernet|Ethernet]] (filaire) ou [[WirelessFidelity|Wi-Fi]] (sans fil).

## 🛡️ Risques / Menaces Associés
*   [[MACSpoofing|Usurpation d'adresse MAC]]: Un attaquant peut modifier l'[[MediaAccessControlAddress|adresse MAC]] de sa [[NetworkInterfaceCard|NIC]] pour se faire passer pour un autre appareil sur le [[LocalAreaNetwork|LAN]].
*   [[PacketSniffing|Capture de Paquets]]: Une [[NetworkInterfaceCard|NIC]] en mode promiscuité peut être utilisée pour intercepter tout le trafic passant sur un [[NetworkSegment|segment réseau]], même s'il n'est pas directement destiné à l'appareil.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des Ports]]: Configurer les [[NetworkSwitch|commutateurs réseau]] pour limiter les [[MediaAccessControlAddress|adresses MAC]] autorisées sur un [[PortNumber|port]] spécifique.
*   [[NetworkSegmentation|Segmentation Réseau]]: Utiliser des [[VirtualLocalAreaNetwork|VLAN]] ou d'autres techniques de [[NetworkSegmentation|segmentation réseau]] pour isoler les systèmes et limiter la portée des attaques.
*   [[AccessControl|Contrôle d'accès]]: Mettre en œuvre des politiques de [[AccessControl|contrôle d'accès]] strictes pour empêcher les appareils non autorisés de se connecter au [[Network|réseau]].

## 🔗 Notes Connexes
*   [[Network|Réseau]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Ethernet|Ethernet]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkDevice|Périphérique Réseau]]