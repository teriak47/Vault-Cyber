---
tags:
  - materiel
aliases:
  - Carte d'Interface Réseau
  - NIC
  - Network Interface Card
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Carte d'Interface Réseau (NIC)

## 🎯 Rôle et Fonction
> La [[NetworkInterfaceCard|Carte d'Interface Réseau]] est un composant [[Hardware|matériel]] essentiel qui permet à un [[Computer|ordinateur]] ou à tout autre [[NetworkDevice|périphérique réseau]] de se connecter à un [[Network|réseau]] et d'établir des [[NetworkCommunication|communications]] avec d'autres appareils. Elle sert de pont entre le [[Computer|système]] interne et le [[NetworkMedia|support réseau]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   Intégrées à la [[Motherboard|carte mère]] (onboard) ou cartes d'extension.
    *   Filaire (par exemple, pour [[Ethernet|Ethernet]]) ou [[WirelessTechnology|sans fil]] (pour [[WirelessFidelity|Wi-Fi]], [[Bluetooth|Bluetooth]]).
*   **Connectique**:
    *   [[RJ45Connector|Connecteur RJ45]] pour les connexions [[EthernetPatchCable|Ethernet filaires]].
    *   [[WirelessAntenna|Antennes]] intégrées ou externes pour les connexions [[WirelessNetwork|sans fil]].
*   **Performances**: Les capacités varient en fonction du modèle, supportant des débits de [[MegabitsPerSecond|Mbps]] à plusieurs [[GigabitsPerSecond|Gbps]].
*   **Normes associées**:
    *   [[EthernetProtocol|IEEE 802.3]] pour les [[Ethernet|réseaux Ethernet]] filaires.
    *   [[IEEE80211|IEEE 802.11]] pour les [[WirelessFidelity|réseaux Wi-Fi]] sans fil.

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Permet la [[NetworkCommunication|communication réseau]] fondamentale pour les [[Computer|ordinateurs]] et [[NetworkDevice|périphériques]].
    *   Offre une flexibilité pour se connecter à différents [[NetworkMedia|supports réseau]] (filaire ou sans fil).
    *   Supporte des vitesses de [[DataTransmission|transmission de données]] élevées.
*   **Inconvénients**:
    *   Peut représenter une [[AttackSurface|surface d'attaque]] pour certaines menaces spécifiques au [[NetworkLayer|réseau]].
    *   La [[ConfigurationDrift|configuration]] incorrecte peut introduire des [[SecurityVulnerabilities|vulnérabilités de sécurité]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: En tant que [[Hardware|composant matériel]], elle est sujette aux risques physiques classiques, nécessitant des mesures de [[PhysicalSecurity|sécurité physique]] pour protéger l'[[Computer|ordinateur]] hôte.
*   [[EnvironmentalControls|Contrôles environnementaux (température, humidité)]]: Les mêmes considérations que pour tout autre [[Hardware|matériel informatique]] s'appliquent pour assurer la longévité et le bon fonctionnement.

## 🛡️ Considérations de Cybersécurité
*   **Vulnérabilités et Risques**:
    *   [[MACSpoofing|Usurpation d'adresse MAC]]: Les attaquants peuvent modifier l'[[MediaAccessControlAddress|adresse MAC]] de leur [[NetworkInterfaceCard|NIC]] pour contourner les contrôles d'[[AccessControl|accès]] ou se faire passer pour un autre appareil sur le [[LocalAreaNetwork|LAN]].
    *   [[PacketSniffing|Capture de Paquets]]: Une [[NetworkInterfaceCard|NIC]] peut être configurée en mode promiscuité pour intercepter et analyser tout le [[NetworkTrafficAnalysis|trafic réseau]] passant sur un [[NetworkSegment|segment réseau]], y compris les [[Data|données]] non destinées à l'appareil.
*   **Mesures de Protection**:
    *   [[PortSecurity|Sécurité des Ports]]: Configurer les [[NetworkSwitch|commutateurs réseau]] pour limiter les [[MediaAccessControlAddress|adresses MAC]] autorisées sur un [[PortNumber|port]] spécifique afin d'empêcher les appareils non autorisés.
    *   [[NetworkSegmentation|Segmentation Réseau]]: Utiliser des [[VirtualLocalAreaNetwork|VLAN]] ou d'autres techniques de [[NetworkSegmentation|segmentation réseau]] pour isoler les [[System|systèmes]] et limiter la portée des [[Attack|attaques]].
    *   [[AccessControl|Contrôle d'accès]]: Implémenter des politiques de [[AccessControl|contrôle d'accès]] strictes au niveau du [[NetworkDevice|périphérique réseau]] pour s'assurer que seuls les appareils légitimes peuvent se connecter.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Ethernet|Ethernet]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[NetworkDevice|Périphérique Réseau]]
*   [[Computer|Ordinateur]]
*   [[Network|Réseau]]
*   [[NetworkInterface|Interface Réseau]]
---