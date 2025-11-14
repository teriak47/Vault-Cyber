---
cssclasses:
  - max
title: Confinement des diffusions
tags:
  - segmentation-lan
  - optimisation-performance-reseau
  - domaine-de-diffusion
  - broadcast
  - media-access-control-address
  - address-resolution-protocol
module: RIB
---

# Confinement des diffusions

Un [[Message|message]] peut contenir une seule [[DestinationMacAddress|adresse MAC de destination]]. 
La résolution d'adresses permet à un [[Host|hôte]] d'envoyer un message de [[Broadcast|diffusion]] à une [[MediaAccessControlAddress|adresse MAC]] unique qui est reconnue par tous les hôtes.

## L'Adresse MAC de Diffusion

L'[[MediaAccessControlAddress|adresse MAC]] de [[Broadcast|diffusion]] est une adresse de 48 [[BinaryDigit|bits]] composée uniquement de uns. 
Les [[MediaAccessControlAddress|adresses MAC]] sont généralement représentées en [[HexadecimalValues|notation hexadécimale]]. 
L'adresse MAC de diffusion en hexadécimal est `FFFF.FFFF.FFFF`. Chaque 'F' représente quatre uns dans l'adresse binaire.

## Le Domaine de Diffusion

Lorsqu'un [[Host|hôte]] envoie un [[Message|message]] de [[Broadcast|diffusion]], les [[NetworkSwitch|commutateurs]] acheminent le message jusqu'à chaque [[Host|hôte]] connecté sur le même [[LocalAreaNetwork|réseau local]] ([[LocalAreaNetwork|LAN]]). 
C'est pourquoi un [[LocalAreaNetwork|LAN]] qui contient un ou plusieurs [[NetworkSwitch|commutateurs]] Ethernet est également appelé un [[BroadcastDomain|domaine de diffusion]].

Si les hôtes connectés au même [[BroadcastDomain|domaine de diffusion]] sont trop nombreux, le trafic de [[Broadcast|diffusion]] peut devenir disproportionné. 
Pour améliorer les [[NetworkPerformance|performances]], il est parfois nécessaire de scinder un [[LocalAreaNetwork|LAN]] en plusieurs réseaux, ou [[BroadcastDomain|domaines de diffusion]]. 
Les [[Router|routeurs]] sont utilisés pour diviser le [[Network|réseau]] en plusieurs [[BroadcastDomain|domaines de diffusion]].

## Résolution d'Adresse

Sur un [[LocalAreaNetwork|LAN]] [[Ethernet|Ethernet]], une [[NetworkInterfaceCard|carte réseau]] (NIC) n'accepte une [[Frame|trame]] que si l'adresse de destination est l'[[MediaAccessControlAddress|adresse MAC]] de [[Broadcast|diffusion]], ou si elle correspond à sa propre [[MediaAccessControlAddress|adresse MAC]]. 
La plupart des applications réseau se basent sur l'[[InternetProtocolAddress|adresse IP]] logique de destination pour identifier l'emplacement des [[Server|serveurs]] et des [[Client|clients]].

L'hôte émetteur utilise le [[AddressResolutionProtocol|protocole de résolution d'adresse]] ([[AddressResolutionProtocol|ARP]]) pour découvrir l'[[MediaAccessControlAddress|adresse MAC]] de tous les hôtes se trouvant sur le même [[LocalAreaNetwork|réseau local]].

### Processus ARP

Le protocole [[AddressResolutionProtocol|ARP]] utilise un processus en trois étapes pour détecter et enregistrer l'[[MediaAccessControlAddress|adresse MAC]] d'un [[Host|hôte]] sur le [[LocalAreaNetwork|LAN]], lorsque seule l'adresse [[InternetProtocolVersion4|IPv4]] de l'hôte est connue.

1.  L'hôte émetteur crée et envoie une [[Frame|trame]] adressée à une [[MediaAccessControlAddress|adresse MAC]] de [[Broadcast|diffusion]]. La [[Frame|trame]] contient un [[Message|message]] avec l'adresse [[InternetProtocolVersion4|IPv4]] de l'hôte de destination.
2.  Chaque [[Host|hôte]] du [[Network|réseau]] reçoit la [[Frame|trame]] de [[Broadcast|diffusion]] et compare l'adresse [[InternetProtocolVersion4|IPv4]] du [[Message|message]] à son adresse [[InternetProtocolVersion4|IPv4]] configurée. L'hôte dont l'adresse [[InternetProtocolVersion4|IPv4]] correspond renvoie son [[MediaAccessControlAddress|adresse MAC]] à l'hôte émetteur.
3.  L'hôte émetteur reçoit le [[Message|message]] et enregistre l'[[MediaAccessControlAddress|adresse MAC]] et l'adresse [[InternetProtocolVersion4|IPv4]] dans une table appelée [[MacAddressTable|table ARP]].

### Alternative pour IPv6

Le protocole [[InternetProtocolVersion6|IPv6]] utilise une méthode similaire, appelée [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol]] (protocole de découverte des voisins).