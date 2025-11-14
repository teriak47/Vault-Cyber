---
cssclasses:
  - max
title: Limites du Réseau
tags:
  - routeur-isp
  - connexion-internet
  - DefaultGateway
  - DHCPServer
  - StaticConfiguration
module: RIB
---

# Limites du Réseau

## Rôle de la Passerelle par Défaut

Chaque [[Host|hôte]] sur un [[Network|réseau]] doit utiliser le [[Router|routeur]] comme [[Gateway|passerelle]] vers d'autres réseaux. Par conséquent, chaque [[Host|hôte]] doit connaître l'adresse [[InternetProtocolVersion4|IPv4]] de l'[[NetworkInterface|interface]] du [[Router|routeur]] qui est connectée au [[Network|réseau]] sur lequel se trouve l'[[Host|hôte]].

*   Cette adresse est l'**adresse de la [[DefaultGateway|passerelle par défaut]]**.
*   Elle peut être configurée sur l'[[Host|hôte]] de manière **[[StaticConfiguration|statique]]** ou reçue de manière dynamique via [[DynamicHostConfigurationProtocol|DHCP]].

## Le Routeur comme Frontière

Le [[WirelessRouter|routeur sans fil]] joue le rôle de [[DHCPServer|serveur DHCP]] pour tous les [[Host|hôtes]] locaux qui y sont rattachés au moyen d'un [[EthernetPatchCable|câble Ethernet]] ou via une [[WirelessTransmissions|connexion sans fil]].

*   Ces [[Host|hôtes]] locaux sont situés sur un **[[InternalNetwork|réseau interne]]**, ou intérieur.
*   Lorsqu'un [[WirelessRouter|routeur sans fil]] est connecté au [[InternetServiceProvider|FAI]], il agit comme un **[[DynamicHostConfigurationProtocolClient|client DHCP]]** pour recevoir la bonne [[InternetProtocolVersion4|adresse IPv4]] du [[RemoteNetwork|réseau externe]] pour l'[[NetworkInterface|interface Internet]].
*   Les [[InternetServiceProvider|FAI]] indiquent généralement une **[[RoutableInternetAddress|adresse routable sur Internet]]** qui permet aux [[Host|hôtes]] connectés au [[WirelessRouter|routeur sans fil]] d'accéder à [[Internet|Internet]].
*   Le [[WirelessRouter|routeur sans fil]] sert de frontière entre le [[LocalAreaNetwork|réseau interne local]] et l'[[Internet|Internet]], à l'extérieur.