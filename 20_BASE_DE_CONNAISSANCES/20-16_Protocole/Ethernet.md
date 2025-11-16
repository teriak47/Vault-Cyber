---
tags:
  - protocole
  - technologie/reseau
  - standard
aliases:
  - Réseau Ethernet
  - IEEE 802.3
  - Ethernet
  - Ethernet Protocol
archetype: protocole
source:
  -
cssclasses:
  - max
---

# Ethernet (IEEE 802.3)

## 🎯 Objectif et Périmètre
> Ethernet est une famille de [[Network|technologies réseau]] standardisées, principalement utilisée pour les [[LocalAreaNetwork|réseaux locaux]] ([[LocalAreaNetwork|LAN]]), qui définit les [[NetworkProtocol|protocoles]] et les spécifications physiques pour la [[DataTransmission|transmission de données]]. Son objectif est de permettre une communication de données rapide, fiable et efficace au sein d'un environnement local.

## 🔑 Principes de Fonctionnement
*   **Standardisation [[EthernetProtocol|IEEE 802.3]]**: Largement définie par l'[[InstituteOfElectricalAndElectronicsEngineers|IEEE]] via la norme [[EthernetProtocol|802.3]], cette technologie spécifie les détails des [[PhysicalLayer|couches physique]] et [[DataLinkLayer|liaison de données]] du [[OpenSystemsInterconnectionModel|modèle OSI]], garantissant l'[[Interoperability|interopérabilité]] des [[NetworkDevice|équipements réseau]].
*   **[[EthernetFrame|Trames Ethernet]]**: Les [[Data|données]] sont encapsulées dans des [[Frame|trames Ethernet]], structurées pour inclure les [[MediaAccessControlAddress|adresses MAC]] [[SourceMacAddress|source]] et [[DestinationMacAddress|destination]], des informations de type/longueur, et le [[Payload|contenu de la charge utile]].
*   **Accès au Médium (CSMA/CD)**: Historiquement, Ethernet employait le protocole "Carrier Sense Multiple Access with Collision Detection" ([[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]]) pour gérer l'accès partagé. Avec l'adoption des [[NetworkSwitch|commutateurs réseau]] modernes, les [[Collision|collisions]] sont minimisées, chaque port de commutateur constituant un [[BroadcastDomain|domaine de collision]] dédié.
*   **[[NetworkTopology|Topologie]] dominante**: Bien que polyvalent, Ethernet est principalement mis en œuvre en [[NetworkTopology|topologie]] étoile, utilisant des [[NetworkSwitch|commutateurs]] comme point central.
*   **Variété des [[NetworkMedia|Supports]] et [[Bandwidth|Débits]]**: Supporte une large gamme de débits (Fast Ethernet, Gigabit Ethernet, 10 Gigabit Ethernet et au-delà) et s'adapte à divers [[NetworkMedia|supports physiques]], tels que les [[TwistedPair|câbles en paires torsadées]] et la [[FiberOpticCable|fibre optique]].
*   **Opération [[OpenSystemsInterconnectionModel|OSI]]**: Opère principalement aux [[PhysicalLayer|couches physique]] ([[PhysicalLayer|couche 1]]) et [[DataLinkLayer|liaison de données]] ([[DataLinkLayer|couche 2]]) du [[OpenSystemsInterconnectionModel|modèle OSI]].

## 📊 Avantages Clés
*   **[[NetworkPerformance|Performance]] et [[Redundancy|Fiabilité]]**: Offre des [[Throughput|débits]] élevés et une [[DataTransmission|transmission de données]] robuste, essentielle pour les [[LocalAreaNetwork|LAN]].
*   **Économie et Accessibilité**: Le coût du matériel et du câblage est généralement abordable, rendant Ethernet accessible pour les [[CorporateNetwork|réseaux d'entreprise]] et [[HomeNetwork|domestiques]].
*   **[[Scalability|Évolutivité]]**: Permet une expansion et une mise à niveau relativement simples pour répondre aux exigences croissantes des [[Network|réseaux]].
*   **Omniprésence et [[Interoperability|Interopérabilité]]**: Étant la [[NetworkStandard|norme]] de facto pour les [[Network|réseaux filaires]], il assure une excellente [[Interoperability|interopérabilité]] entre les différents [[EndDevices|dispositifs]] et [[NetworkDevice|équipements]].

## 🛡️ Sécurité et Risques
*   **[[Attack|Attaques]] courantes**:
    *   [[MACSpoofing|Usurpation d'adresses MAC]] ([[MACSpoofing|MAC Spoofing]]) pour contourner les [[AccessControl|contrôles d'accès]] et rediriger le [[NetworkTraffic|trafic]].
    *   [[AddressResolutionProtocolPoisoning|Usurpation d'ARP]] ([[AddressResolutionProtocolPoisoning|ARP Poisoning]]) permettant des [[ManInTheMiddle|attaques de l'homme du milieu]] en falsifiant les correspondances [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]].
    *   [[DenialOfService|Attaques par déni de service]] ([[DenialOfService|DoS]]) ciblant les [[NetworkSwitch|commutateurs]] par inondation de [[Frame|trames]] (ex: [[MacAddressTable|table MAC]] overflow).
*   **Mesures de protection**:
    *   [[NetworkSegmentation|Segmentation réseau]] à l'aide de [[VirtualLocalAreaNetwork|VLANs]] pour isoler les [[BroadcastDomain|domaines de diffusion]] et restreindre la propagation des [[Attack|attaques]].
    *   [[PortSecurity|Sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] (ex: [[MACAddressFiltering|filtrage d'adresses MAC]], [[DynamicHostConfigurationProtocol|DHCP]] Snooping, [[AccessControl|contrôle d'accès]] basé sur l'[[MediaAccessControlAddress|adresse MAC]]).
    *   Déploiement de [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] ([[IntrusionDetectionSystem|IDS]]) et de [[IntrusionPreventionSystem|systèmes de prévention d'intrusion]] ([[IntrusionPreventionSystem|IPS]]) pour la [[SecurityMonitoring|surveillance]] et l'alerte sur les [[Threat|menaces]].
    *   Renforcement de la [[PhysicalSecurity|sécurité physique]] des [[NetworkInfrastructure|infrastructures réseau]] pour prévenir l'[[UnauthorizedAccess|accès non autorisé]] ou le [[Tampering|sabotage]].
    *   Mise en œuvre de [[NetworkAccessControl|contrôles d'accès réseau]] ([[NetworkAccessControl|NAC]]) pour [[Authentication|authentifier]] et [[Authorization|autoriser]] les [[EndDevices|dispositifs]] se connectant.

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|ARP]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[PhysicalLayer|Couche Physique]]
*   [[EthernetFrame|Trame Ethernet]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkMedia|Support réseau]]
*   [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]]
*   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]]
*   [[NetworkTraffic|Trafic réseau]]