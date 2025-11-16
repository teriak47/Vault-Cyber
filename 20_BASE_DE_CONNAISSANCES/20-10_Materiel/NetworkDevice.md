---
tags:
  - materiel
aliases:
  - Périphérique Réseau
  - Dispositif Réseau
  - Équipement Réseau
  - Network Device
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Périphérique Réseau

## 🎯 Rôle et Fonction
> Un [[NetworkDevice|périphérique réseau]] est un [[Hardware|composant physique]] essentiel qui permet la [[NetworkCommunication|communication]] et le partage de [[Data|données]] entre des [[Computer|ordinateurs]] et d'autres [[EndDevices|équipements terminaux]] au sein d'un [[Network|réseau]]. Il constitue le fondement d'une [[NetworkInfrastructure|infrastructure réseau]], facilitant le flux d'informations et l'accès aux [[Resource|ressources]].

## 🛠️ Caractéristiques Techniques
*   **Fonctionnalités Principales**:
    *   **[[Routing|Routage]]**: Déterminer le meilleur chemin pour les [[Packet|paquets]] de [[Data|données]] entre différents [[Network|réseaux]] (ex: [[Router|routeurs]]).
    *   **[[PacketSwitching|Commutation de paquets]]**: Connecter les [[EndDevices|dispositifs terminaux]] au sein d'un même [[LocalAreaNetwork|LAN]] et diriger le [[NetworkTrafficAnalysis|trafic]] vers la [[DestinationMacAddress|destination]] appropriée (ex: [[NetworkSwitch|commutateurs réseau]]).
    *   **[[WirelessTransmission|Transmission sans fil]]**: Permettre la connectivité des [[WirelessDevices|appareils sans fil]] à un [[WirelessNetwork|réseau sans fil]] (ex: [[AccessPoint|points d'accès]]).
    *   **Filtrage et [[Security|Sécurité]]**: Surveiller et contrôler le [[NetworkTrafficAnalysis|trafic]] [[NetworkCommunication|entrant et sortant]] basé sur des règles prédéfinies (ex: [[Firewall|pare-feu]]).
*   **Types Courants**:
    *   [[Router|Routeurs]]
    *   [[NetworkSwitch|Commutateurs réseau]]
    *   [[AccessPoint|Points d'accès]] ([[AccessPoint|AP]])
    *   [[Firewall|Pare-feu]]
    *   [[Hub|Concentrateurs]] (moins courants, créent un seul [[CollisionDomain|domaine de collision]])
*   **Connectivité**: Utilise divers [[NetworkMedia|supports réseau]] comme les [[EthernetPatchCable|câbles Ethernet]] avec [[RJ45Connector|connecteurs RJ45]], la [[WirelessFidelity|technologie Wi-Fi]] ou le [[Bluetooth|Bluetooth]].
*   **[[Protocol|Protocoles]] supportés**: Opère avec des [[NetworkProtocol|protocoles réseau]] tels que la [[InternetProtocolSuite|suite TCP/IP]] ([[TransmissionControlProtocol|TCP/IP]]), [[EthernetProtocol|Ethernet]], [[AddressResolutionProtocol|ARP]] et [[DynamicHostConfigurationProtocol|DHCP]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Facilitent la [[NetworkCommunication|communication]] et le partage de [[Resource|ressources]] sur de multiples [[Network|réseaux]].
    *   Offrent des fonctionnalités de [[NetworkSegmentation|segmentation]] et de [[NetworkSecurity|sécurité]] essentielles pour protéger les [[Data|données]].
    *   Contribuent à l'[[Scalability|évolutivité]] et la [[Redundancy|redondance]] des [[NetworkInfrastructure|infrastructures réseau]].
    *   Optimisent la [[NetworkPerformance|performance réseau]] par la [[TrafficManagement|gestion du trafic]] et la [[QualityOfService|qualité de service]].
*   **Inconvénients**:
    *   Peuvent être la cible de [[DigitalAttack|cyberattaques]] telles que les [[DenialOfService|attaques par déni de service (DoS)]] ou [[DistributedDenialOfService|DDoS]].
    *   Soumis à des [[SoftwareVulnerability|vulnérabilités logicielles]] et à la [[ConfigurationDrift|dérive de configuration]] s'ils ne sont pas gérés correctement.
    *   Nécessitent une [[SecurityPolicy|politique de sécurité]], une [[NetworkConfiguration|configuration]] rigoureuse et une [[SecurityMonitoring|surveillance continue]].
    *   Une [[HardwareFailure|défaillance matérielle]] peut entraîner une [[ServiceDisruption|interruption de service]] si aucune [[Redundancy|redondance]] n'est mise en place.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] aux locaux abritant les [[NetworkDevice|périphériques réseau]].
*   [[EnvironmentalControls|Contrôles environnementaux]] (température, humidité) pour assurer le bon fonctionnement du [[Hardware|matériel]] et éviter les [[HardwareFailure|défaillances]].
*   Verrouillage des [[NetworkRack|armoires réseau]] et des baies de serveurs pour prévenir le [[Tampering|sabotage]] et le [[DataTheft|vol]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocolSuite|Suite de Protocoles Internet (TCP/IP)]]
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[NetworkCommunication|Communication réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[EndDevices|Terminaux]]
*   [[IntermediateDevice|Dispositifs Intermédiaires]]
*   [[NetworkMedia|Supports Réseau]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[AccessPoint|Point d'Accès]]
*   [[Firewall|Pare-feu]]
*   [[WirelessNetwork|Réseau sans fil]]
*   [[PowerLineCommunications|Communications par Courants Porteurs en Ligne (CPL)]]