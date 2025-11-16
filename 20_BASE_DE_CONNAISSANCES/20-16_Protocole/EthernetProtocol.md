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
> L'[[EthernetProtocol|Ethernet]] est une famille de [[NetworkTechnology|technologies de mise en réseau]] standardisée (référencée par l'[[InstituteOfElectricalAndElectronicsEngineers|IEEE]] sous la norme 802.3) qui définit les règles de transmission et de réception des [[Data|données]] sur un [[LocalAreaNetwork|réseau local]] (LAN) filaire. Il opère principalement au niveau de la [[DataLinkLayer|couche liaison de données]] (couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]) pour l'[[MediaAccessControlAddress|adressage MAC]] et au niveau de la [[PhysicalLayer|couche physique]] (couche 1 du [[OpenSystemsInterconnectionModel|modèle OSI]]) pour la transmission des [[ElectricalSignals|signaux électriques]] ou [[OpticalSignals|optiques]].

## ⚙️ Fonctionnement
1.  **Standardisation** : L'[[EthernetProtocol|Ethernet]] est le [[NetworkStandard|standard de fait]] le plus répandu pour les [[LocalAreaNetwork|réseaux locaux]], également utilisé dans les [[MetropolitanAreaNetwork|réseaux métropolitains]] (MAN) et [[WideAreaNetwork|réseaux étendus]] (WAN).
2.  **[[EthernetFrame|Trames Ethernet]]** : Les [[Data|données]] sont encapsulées dans des structures appelées [[EthernetFrame|trames Ethernet]]. Une [[EthernetFrame|trame]] contient des champs essentiels tels que l'[[SourceMacAddress|adresse MAC source]], l'[[DestinationMacAddress|adresse MAC de destination]], le type de [[Protocol|protocole]] (ex: [[InternetProtocolVersion4|IPv4]], [[InternetProtocolVersion6|IPv6]]), et la [[Payload|charge utile]] (les [[Data|données]] réelles).
3.  **[[MediaAccessControlAddress|Adresses MAC]]** : Chaque [[NetworkInterfaceCard|interface réseau]] compatible [[EthernetProtocol|Ethernet]] est identifiée par une [[MediaAccessControlAddress|adresse MAC]] unique de 48 bits, utilisée pour le [[AddressingInformation|adressage]] au sein d'un [[NetworkSegment|segment de réseau]] local.
4.  **Gestion de l'Accès au Médium** :
    *   Historiquement, les réseaux [[EthernetProtocol|Ethernet]] partageaient un médium et utilisaient le [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]] pour gérer les accès et détecter/résoudre les [[Collision|collisions]].
    *   Les [[EthernetProtocol|réseaux Ethernet]] modernes reposent sur des [[NetworkSwitch|commutateurs réseau]] et fonctionnent en [[FullDuplex|full-duplex]], ce qui permet une communication simultanée dans les deux directions et élimine les [[Collision|collisions]].
*   **Ports par défaut**: N/A (opère aux [[PhysicalLayer|couches physique]] et [[DataLinkLayer|liaison de données]], sans notion de ports de [[TransportLayer|couche transport]]).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[Eavesdropping|Écoute clandestine]] : Facile sur des [[FlatNetwork|réseaux plats]] ou via des techniques d'[[Spoofing|usurpation]].
    *   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]] : Permet d'intercepter le [[NetworkTrafficAnalysis|trafic réseau]] en manipulant les tables [[AddressResolutionProtocol|ARP]] des [[Host|hôtes]].
    *   [[MacFlooding|MAC Flooding]] : Attaque saturant la [[MacAddressTable|table d'adresses MAC]] d'un [[NetworkSwitch|commutateur]], le forçant à opérer comme un [[Hub|concentrateur]] (hub).
*   **Mesures de Sécurité**:
    *   **Utilisation de [[NetworkSwitch|commutateurs réseau]]** : Préférer les [[NetworkSwitch|commutateurs]] aux [[Hub|concentrateurs]] pour la [[NetworkSegmentation|segmentation du trafic]] et la réduction du [[BroadcastDomain|domaine de diffusion]].
    *   **[[VirtualLocalAreaNetwork|VLANs]]** : Implémentation de [[VirtualLocalAreaNetwork|réseaux locaux virtuels]] pour isoler logiquement le [[NetworkTrafficAnalysis|trafic]] et appliquer des [[AccessControl|contrôles d'accès]] granulaires.
    *   **[[PortSecurity|Sécurité des Ports]]** : Configurer la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] pour limiter les [[MediaAccessControlAddress|adresses MAC]] autorisées à se connecter à un port spécifique.
    *   [[IEEE8021X|Authentification 802.1X]] : Protocole de [[Authentication|contrôle d'accès au réseau]] basé sur les ports, permettant d'[[Authentication|authentifier]] les [[User|utilisateurs]] et les [[NetworkDevice|appareils]] avant qu'ils n'accèdent au [[Network|réseau]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[EthernetFrame|Trame Ethernet]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]]
*   [[AddressResolutionProtocol|ARP]]
*   [[Wireshark]]