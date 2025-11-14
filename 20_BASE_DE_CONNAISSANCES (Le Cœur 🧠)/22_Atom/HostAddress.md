---
tags:
  - adresse-ip
  - adresse-mac
  - gestion-adressage-ip
  - MACSpoofing
  - RogueDHCPServer
  - NetworkSegmentation
aliases:
  - Adresse d'Hôte
  - Host Address
source:
  - null
cssclasses:
  - max
---

# Adresse d'Hôte

## 📥 Définition en une phrase
> Une adresse d'hôte est un identifiant unique attribué à un [[Host|hôte]] (un périphérique, comme un [[Computer|ordinateur]] ou un [[Server|serveur]]) sur un [[Network|réseau]] informatique, permettant sa localisation et sa communication.

## 🧠 Concepts Clés / Fonctionnement
*   L'adresse d'hôte est fondamentale pour l'[[NetworkCommunication|identification]] et la [[NetworkCommunication|communication]] entre les [[EndDevices|dispositifs terminaux]] au sein d'un [[Network|réseau]].
*   Dans le contexte des [[InternetProtocolSuite|protocoles TCP/IP]], elle fait principalement référence à l'[[InternetProtocolAddress|adresse IP]] (une adresse logique gérée par la [[NetworkLayer|couche réseau]]) et à l'[[MediaAccessControlAddress|adresse MAC]] (une adresse physique gérée par la [[DataLinkLayer|couche liaison de données]]).
*   Une [[InternetProtocolAddress|adresse IP]] est divisée en deux parties : une [[NetworkPortion|partie réseau]] qui identifie le [[NetworkSegment|segment réseau]] et une [[HostPortion|partie hôte]] qui identifie l'[[Host|hôte]] spécifique au sein de ce segment.
*   L'[[MediaAccessControlAddress|adresse MAC]] est un identifiant physique unique gravé dans la [[NetworkInterfaceCard|carte d'interface réseau]] de chaque périphérique.
*   L'[[IPAddressing|adressage IP]] et la gestion des [[MediaAccessControlAddress|adresses MAC]] sont des mécanismes clés pour assurer que les paquets de [[Data|données]] atteignent leur [[DestinationInternetProtocolVersion4Address|destination]] correcte.

## 🛡️ Risques / Menaces Associés
*   [[MACSpoofing|Usurpation d'adresse MAC]] : Un [[ThreatActor|attaquant]] peut se faire passer pour un [[Host|hôte]] légitime en utilisant son [[MediaAccessControlAddress|adresse MAC]].
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]] : Manipulation des tables [[AddressResolutionProtocol|ARP]] pour associer une [[InternetProtocolAddress|adresse IP]] à une [[MediaAccessControlAddress|adresse MAC]] frauduleuse, souvent utilisée dans les attaques de type [[ManInTheMiddle|homme du milieu]].
*   [[RogueDHCPServer|Serveurs DHCP malveillants]] : Peuvent distribuer des informations d'[[IPAddressing|adressage]] incorrectes, redirigeant le [[NetworkTrafficAnalysis|trafic]] ou causant des [[ServiceDisruption|interruptions de service]].
*   [[InadvertentExposure|Exposition involontaire]] d'informations d'adressage peut faciliter la [[Reconnaissance|reconnaissance]] par des [[ThreatActor|attaquants]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] : Limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] autorisées par port de [[NetworkSwitch|commutateur]] et les lier statiquement.
*   [[MacAddressFiltering|Filtrage d'adresses MAC]] : Restreindre l'accès au [[Network|réseau]] aux [[MediaAccessControlAddress|adresses MAC]] connues et approuvées (bien que facilement contournable, offre une couche de base).
*   [[NetworkSegmentation|Segmentation réseau]] : Utiliser des [[VirtualLocalAreaNetwork|VLAN]] pour isoler les [[Host|hôtes]] et limiter la portée des attaques.
*   [[DynamicHostConfigurationProtocol|DHCP Snooping]] : Pour prévenir les [[RogueDHCPServer|serveurs DHCP malveillants]] en validant les messages [[DynamicHostConfigurationProtocol|DHCP]].
*   [[SecureRoutingProtocols|Protocoles de routage sécurisés]] : Assurer l'intégrité des informations d'[[IPAddressing|adressage]] échangées entre les [[Router|routeurs]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[IPAddressing|Adressage IP]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkAddress|Adresse Réseau]]