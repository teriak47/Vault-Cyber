---
cssclasses:
  - max
title: MAC et IP
module: RIB
---

# MAC et IP

Parfois, un [[Host|hôte]] doit envoyer un [[Message|message]], mais il ne connaît que l'[[InternetProtocol|adresse IP]] du [[NetworkDevice|périphérique]] de destination. L'[[Host|hôte]] doit connaître l'[[MediaAccessControlAddress|adresse MAC]] de ce [[NetworkDevice|périphérique]]. 
L'[[MediaAccessControlAddress|adresse MAC]] peut être détectée à l'aide de la [[AddressResolutionProtocol|résolution d'adresse]]. 

Chaque [[NetworkDevice|périphérique]] possède deux adresses principales sur un [[LocalAreaNetwork|LAN]] [[Ethernet|Ethernet]]:

*   **[[MediaAccessControlAddress|Adresse physique]] ([[MediaAccessControlAddress|adresse MAC]])** - Utilisée pour les [[NetworkCommunication|communications]] entre [[NetworkInterfaceCard|cartes réseau]] situées sur le même [[Ethernet|réseau Ethernet]].
*   **[[InternetProtocol|Adresse logique]] (l'[[InternetProtocol|adresse IP]])** - Utilisée pour envoyer les [[Packet|paquets]] depuis le [[NetworkDevice|périphérique]] source vers le [[NetworkDevice|périphérique]] de destination. L'[[InternetProtocol|adresse IP]] de destination peut se trouver soit sur le même [[Network|réseau]] IP que la source soit sur un [[RemoteNetwork|réseau distant]].

Lorsque l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]] ([[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]) se trouve sur un [[RemoteNetwork|réseau distant]], l'[[DestinationMacAddress|adresse MAC de destination]] sera l'adresse de la [[DefaultGateway|passerelle par défaut]] de l'[[Host|hôte]] (c'est-à-dire l'[[NetworkInterface|interface]] du [[Router|routeur]]). 
Les [[Router|routeurs]] examinent l'adresse [[InternetProtocolVersion4|IPv4]] de destination afin de déterminer le meilleur chemin pour acheminer le [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]]. 
Lorsque le [[Router|routeur]] reçoit la [[EthernetFrame|trame Ethernet]], il [[Decapsulation|décapsule]] les informations de [[DataLinkLayer|couche 2]]. 
À l'aide de l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]], il détermine le [[NetworkDevice|périphérique]] du tronçon suivant, puis [[Encapsulation|encapsule]] le [[Packet|paquet IP]] dans une nouvelle [[Frame|trame]] [[DataLinkLayer|liaison de données]] pour l'interface de sortie. Le long de chaque lien d'un chemin, un [[Packet|paquet IP]] est [[Encapsulation|encapsulé]] dans une [[Frame|trame]]. La [[Frame|trame]] est spécifique à la technologie de [[DataLinkLayer|liaison de données]] associée à cette liaison, telle qu'[[Ethernet|Ethernet]]. Si le [[NetworkDevice|périphérique]] du tronçon suivant est la destination finale, l'[[DestinationMacAddress|adresse MAC de destination]] est celle de la [[NetworkInterfaceCard|carte réseau Ethernet]] du [[NetworkDevice|périphérique]].