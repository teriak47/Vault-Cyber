---
tags:
aliases:
  - Adresse Réseau
  - Network Address
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse Réseau

## 📥 Définition en une phrase
> Une adresse réseau est un identifiant logique ou physique unique attribué à un [[NetworkDevice|dispositif]] au sein d'un [[Network|réseau informatique]], essentiel pour sa localisation, son [[Routing|routage]] et sa [[NetworkCommunication|communication]] effective.

## 🧠 Concepts Clés / Piliers
*   **Identification Unique**: Chaque [[Host|hôte]] ou [[NetworkInterface|interface réseau]] sur un [[Network|réseau]] se voit attribuer une [[NetworkAddress|adresse réseau]] afin d'être distingué et de pouvoir échanger des [[Data|données]].
*   **Types et Couches**: Les deux principaux types sont :
    *   Les [[MediaAccessControlAddress|adresses MAC]] (Media Access Control), des identifiants physiques uniques (gravés sur la [[NetworkInterfaceCard|carte d'interface réseau]]) qui opèrent au niveau de la [[DataLinkLayer|couche liaison de données]] ([[OpenSystemsInterconnectionModel|couche 2 du modèle OSI]]) pour la [[NetworkCommunication|communication]] locale.
    *   Les [[InternetProtocol|adresses IP]] (Internet Protocol), des identifiants logiques qui opèrent au niveau de la [[NetworkLayer|couche réseau]] ([[OpenSystemsInterconnectionModel|couche 3 du modèle OSI]]) pour le [[Routing|routage]] et la [[NetworkCommunication|communication]] à travers des [[InterconnectedNetworks|réseaux interconnectés]].
*   **Routage et Commutation**: Les [[Router|routeurs]] exploitent les [[InternetProtocol|adresses IP]] pour déterminer les chemins d'acheminement des [[Packet|paquets]] entre différents [[Network|réseaux]], tandis que les [[NetworkSwitch|commutateurs réseau]] utilisent les [[MediaAccessControlAddress|adresses MAC]] pour diriger les [[EthernetFrame|trames Ethernet]] vers les [[EndDevices|terminaux]] appropriés au sein d'un même [[LocalAreaNetwork|LAN]].
*   **Configuration**: Les [[InternetProtocol|adresses IP]] peuvent être attribuées de manière [[StaticConfiguration|statique]] (manuellement) ou [[DynamicHostConfigurationProtocol|dynamique]] (automatiquement par un [[DynamicHostConfigurationProtocol|serveur DHCP]]).

## 💡 Importance en Cybersécurité
> Les [[NetworkAddress|adresses réseau]] sont au cœur de toute [[NetworkCommunication|communication réseau]] et représentent une [[AttackSurface|surface d'attaque]] significative. Leur intégrité et leur bonne gestion sont fondamentales pour la [[Security|sécurité]] d'un [[System|système]] ou d'un [[Network|réseau]]. Une manipulation malveillante des [[NetworkAddress|adresses réseau]] peut entraîner des [[UnauthorizedAccess|accès non autorisés]], des [[ManInTheMiddle|attaques de l'homme du milieu]], ou des [[ServiceDisruption|interruptions de service]]. Des mesures comme la [[NetworkSegmentation|segmentation réseau]], le [[PortSecurity|filtrage MAC]] ou la [[DHCPSnooping|surveillance DHCP]] sont essentielles pour atténuer ces [[Threat|menaces]] et assurer la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[Data|données]] et des [[Resource|ressources]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[MACSpoofing|Usurpation d'adresse MAC]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]]
*   [[RogueDHCPServer|Serveur DHCP malveillant]]
*   [[DHCPSnooping|DHCP Snooping]]