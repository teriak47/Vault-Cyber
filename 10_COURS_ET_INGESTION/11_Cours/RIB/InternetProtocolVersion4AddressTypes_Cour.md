---
cssclasses:
  - max
title: Les types d'adresses IPv4
tags:
  - adresse-ipv4-classe
  - nat
  - gestion-adresse-ip
  - PublicIPAddress
  - PrivateIPAddress
  - NetworkAddressTranslation
module: RIB
---

# Les types d'adresses IPv4

## Adresses Publiques vs. Privées

Les [[PublicIPAddress|adresses IPv4 publiques]] sont acheminées de manière globale entre les [[Router|routeurs]] [[InternetServiceProvider|FAI]]. 
Cependant, toutes les [[InternetProtocolVersion4|adresses IPv4]] disponibles ne peuvent pas être utilisées sur l'[[Internet|Internet]]. 
Certains blocs d'adresses, appelés [[PrivateIPAddress|adresses privées]], sont utilisés par la plupart des entreprises pour attribuer des [[InternetProtocolVersion4|adresses IPv4]] aux [[Host|hôtes]] internes. 

La plupart des réseaux internes, des grandes [[Enterprise|entreprises]] aux [[HomeNetwork|réseaux domestiques]], utilisent des [[PrivateIPAddress|adresses IPv4 privées]] pour adresser tous les périphériques internes (intranet), y compris les [[Host|hôtes]] et les [[Router|routeurs]]. 
Cependant, les [[PrivateIPAddress|adresses privées]] ne sont pas routables globalement. Avant que le [[InternetServiceProvider|FAI]] ne puisse transmettre un [[Packet|paquet]], il doit traduire l'[[SourceInternetProtocolVersion4Address|adresse IPv4 source]], qui est une adresse privée, en une [[PublicIPAddress|adresse IPv4 publique]] à l'aide de la [[NetworkAddressTranslation|NAT]].

## Adresses à Usage Spécial

### Adresses de Bouclage
Les [[LoopbackAddress|adresses de bouclage]] (127.0.0.0 /8 ou 127.0.0.1 à 127.255.255.254), plus communément identifiées comme 127.0.0.1 (Localhost), sont des adresses spéciales utilisées par un [[Host|hôte]] pour diriger le trafic vers lui-même.

### Adresses Link-Local (APIPA)
Les [[LinkLocalAddress|Adresses link-local]] ou [[AutomaticPrivateIPAddressing|adresses APIPA (Adressage IP privé automatique)]] (169.254.0.0 /16 ou 169.254.0.1 à 169.254.255.254) sont utilisées par un client [[DynamicHostConfigurationProtocol|DHCP]] [[Windows|Windows]] pour s'auto-configurer dans le cas où aucun [[DHCPServer|serveur DHCP]] n'est disponible.

## Adressage par Classe

En 1981, les [[InternetProtocolVersion4|adresses IPv4]] ont été attribuées en utilisant l'[[ClassfulAddressing|adressage par classe]] tel que défini dans la [[RequestForComments|RFC 790]], *Numéros attribués*. 
On attribuait aux clients une [[NetworkAddress|adresse réseau]] selon l'une des trois classes (A, B ou C). La [[RequestForComments|RFC]] répartissait les plages d'adresses à [[Unicast|monodiffusion]] en plusieurs classes:

*   **Classe A (0.0.0.0/8 à 127.0.0.0/8)** : Conçue pour prendre en charge des réseaux de très grande envergure avec plus de 16 millions d'[[HostAddress|adresses d'hôte]].
*   **Classe B (128.0.0.0 /16 à 191.255.0.0 /16)** : Conçue pour répondre aux besoins des réseaux de moyenne à grande envergure avec jusqu'à 65 000 [[HostAddress|adresses d'hôte]] environ.
*   **Classe C (192.0.0.0 /24 - 223.255.255.0 /24)** : Conçue pour prendre en charge les petits réseaux comptant un maximum de 254 [[Host|hôtes]].

Il existe également un bloc de [[Multicast|multidiffusion]] de **classe D** (224.0.0.0 à 239.0.0.0) et un bloc d'[[ExperimentalAddresses|adresses expérimentales]] de **classe E** (240.0.0.0 à 255.0.0.0).

## Gestion des Adresses IP Publiques

Les [[PublicIPAddress|adresses IPv4 publiques]] sont des adresses qui sont globalement acheminées sur l'[[Internet|internet]]. 
Elles doivent être uniques. Les [[InternetProtocolVersion4|adresses IPv4]] et [[InternetProtocolVersion6|IPv6]] sont toutes deux gérées par l'[[InternetAssignedNumbersAuthority|IANA (L'autorité d'assignation des numéros internet)]]. 

L'IANA gère les [[InternetProtocolAddressBlocks|blocs d'adresses IP]] et les attribue aux [[RegionalInternetRegistry|organismes d'enregistrement Internet locaux (RIR)]]. 
Les RIR sont chargés d'attribuer des [[InternetProtocolAddress|adresses IP]] à des [[InternetServiceProvider|ISP]] qui, à leur tour, fournissent des blocs d'[[InternetProtocolVersion4|adresses IPv4]] aux [[Enterprise|entreprises]] et aux [[InternetServiceProvider|ISP]] de plus petite envergure. Les organisations peuvent également obtenir leurs adresses directement auprès d'un RIR (sous réserve des politiques de ce RIR).