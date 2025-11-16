---
tags:
aliases:
  - Couche Liaison de Données
  - Data Link Layer
  - Couche 2
  - DLL
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche Liaison de Données

## 📥 Définition en une phrase
> La [[DataLinkLayer|Couche Liaison de Données]] est la deuxième couche du [[OpenSystemsInterconnectionModel|Modèle OSI]], chargée d'assurer le transfert fiable des [[Data|données]] entre deux [[EndDevices|nœuds]] adjacents sur un même [[NetworkSegment|segment de réseau local]].

## 🧠 Concepts Clés / Piliers
*   **Encadrement (Framing)**: Organise les [[Bit|bits]] provenant de la [[NetworkLayer|Couche Réseau]] en unités logiques appelées "[[Frame|trames]]" pour la [[DataTransmission|transmission]].
*   **Adressage Physique (MAC Addressing)**: Utilise les [[MediaAccessControlAddress|adresses MAC]] pour identifier de manière unique les [[NetworkDevice|dispositifs]] sur un [[LocalAreaNetwork|réseau local]].
*   **Contrôle d'Accès au Média (MAC - Media Access Control)**: Gère la manière dont les [[NetworkDevice|périphériques]] partagent le [[NetworkMedia|support de transmission physique]] (par exemple, [[Ethernet|Ethernet]] utilise CSMA/CD, [[WirelessFidelity|Wi-Fi]] utilise CSMA/CA).
*   **Détection et Correction d'Erreurs**: Ajoute des mécanismes comme le [[CyclicRedundancyCheck|CRC]] (Cyclic Redundancy Check) pour détecter les [[DataCorruption|erreurs de transmission]] et, dans certains cas, les corriger.
*   **Contrôle de Flux**: Aide à prévenir la surcharge d'un récepteur plus lent par un émetteur plus rapide en régulant le [[Bandwidth|débit de données]].
*   **Protocoles Courants**: Inclut [[Ethernet|Ethernet]] (IEEE 802.3), [[WirelessFidelity|Wi-Fi]] (IEEE 802.11) et le [[PointToPointProtocol|Point-to-Point Protocol (PPP)]].

## 💡 Importance en Cybersécurité
> La [[DataLinkLayer|Couche Liaison de Données]] est fondamentale pour la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[Data|données]] au sein des [[LocalAreaNetwork|réseaux locaux]]. Des [[SecurityVulnerabilities|vulnérabilités]] à ce niveau peuvent mener à des [[Attack|attaques]] telles que l'[[MACSpoofing|usurpation d'adresse MAC]], l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]], le [[VLANHopping|saut de VLAN]] ou des [[DenialOfService|dénis de service]] (comme le MAC flooding). Une configuration et une [[SecurityMonitoring|surveillance]] appropriées, incluant la [[NetworkSegmentation|segmentation réseau]] via les [[VirtualLocalAreaNetwork|VLANs]], la [[PortSecurity|sécurité des ports]], l'[[DynamicARPInspection|Inspection ARP Dynamique (DAI)]] et le [[DHCPSnooping|DHCP Snooping]], sont essentielles pour renforcer la [[NetworkSecurity|sécurité réseau]] et protéger l'[[AttackSurface|surface d'attaque]] des [[System|systèmes]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Ethernet|Ethernet]]
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]
*   [[AddressResolutionProtocol|Protocole de résolution d'adresse (ARP)]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[PortSecurity|Sécurité des ports]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[DynamicARPInspection|Inspection ARP Dynamique (DAI)]]
*   [[DHCPSnooping|DHCP Snooping]]
*   [[AccessControlList|Listes de contrôle d'accès (ACLs)]]