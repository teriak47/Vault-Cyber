---
cssclasses:
  - max
title: Configuration DHCPv4
tags:
  - configuration-dhcpv4
  - processus-dora
  - reseau-domestique
  - DHCPServer
  - InternetProtocolAddress
  - DynamicHostConfigurationProtocol
module: RIB
---

# Configuration DHCPv4

## Processus d'Attribution d'Adresse DHCP (DORA)

Le [[DHCPServer|serveur DHCP]] possède une plage, ou pool, d'[[InternetProtocolAddress|adresses]] [[InternetProtocolVersion4|IPv4]] qui peuvent être attribuées aux [[Client|clients]] [[DynamicHostConfigurationProtocol|DHCP]]. 

Le processus d'attribution se déroule en quatre étapes :

1.  **Détection (Discover)**: Un [[Client|client]] nécessitant une [[InternetProtocolAddress|adresse IPv4]] envoie un message de détection [[DynamicHostConfigurationProtocol|DHCP]]. Il s'agit d'une [[Broadcast|diffusion]] avec :
    *   Une [[DestinationInternetProtocolVersion4Address|adresse IPv4 de destination]] de `255.255.255.255` (32 bits à 1).
    *   Une [[DestinationMacAddress|adresse MAC de destination]] de `FF-FF-FF-FF-FF-FF` (48 bits à 1).
    *   Tous les [[Host|hôtes]] sur le [[Network|réseau]] reçoivent cette [[Frame|trame]] de [[Broadcast|diffusion]], mais seul un [[DHCPServer|serveur DHCP]] y répond.
2.  **Offre (Offer)**: Le [[DHCPServer|serveur]] répond avec une offre [[DynamicHostConfigurationProtocol|DHCP]], suggérant une [[InternetProtocolAddress|adresse IPv4]] au [[Client|client]].
3.  **Requête (Request)**: L'[[Host|hôte]] envoie alors une requête [[DynamicHostConfigurationProtocol|DHCP]] au [[DHCPServer|serveur]], demandant à utiliser l'[[InternetProtocolAddress|adresse IPv4]] suggérée.
4.  **Accusé de réception (Acknowledge)**: Le [[DHCPServer|serveur]] répond avec un [[Acknowledgement|accusé de réception]] [[DynamicHostConfigurationProtocol|DHCP]], finalisant l'attribution.

## Configuration sur un Réseau Domestique

Sur la plupart des [[HomeNetwork|réseaux domestiques]] et de PME, un [[WirelessRouter|routeur sans fil]] fournit les services [[DynamicHostConfigurationProtocol|DHCP]] aux [[Client|clients]] du [[LocalAreaNetwork|réseau local]].

Pour [[WirelessRouterConfiguration|configurer un routeur sans fil domestique]], il faut accéder à son interface web graphique via un [[WebBrowsers|navigateur]] en saisissant l'[[InternetProtocolAddress|adresse IPv4]] par défaut du [[Router|routeur]].

*   **Valeurs par défaut courantes** :
    *   **Adresse IPv4** : `192.168.0.1`
    *   **Masque de sous-réseau** : `255.255.255.0`

Cette [[InternetProtocolAddress|adresse]] représente la [[Gateway|passerelle par défaut]] pour tous les [[Host|hôtes]] du [[LocalAreaNetwork|réseau local]] et sert également d'[[InternetProtocolAddress|adresse IPv4]] pour le [[DHCPServer|serveur DHCP]] interne. 
La plupart des [[WirelessRouter|routeurs sans fil]] domestiques ont un [[DHCPServer|serveur DHCP]] activé par défaut.