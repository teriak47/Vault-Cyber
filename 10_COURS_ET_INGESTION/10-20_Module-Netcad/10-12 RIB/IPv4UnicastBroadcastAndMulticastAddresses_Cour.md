---
cssclasses:
  - max
title: Adresses IPv4 de monodiffusion, de diffusion et de multidiffusion
module: RIB
---

# Adresses IPv4 de monodiffusion, de diffusion et de multidiffusion

## Transmission Monodiffusion (Unicast)

La transmission [[Unicast|monodiffusion]] fait référence à un périphérique qui envoie un [[Message|message]] à un autre périphérique dans les [[OneToOneCommunications|communications un-à-un]]. 

*   Un [[Packet|paquet]] [[Unicast|monodiffusion]] a une [[DestinationInternetProtocolVersion4Address|adresse IP de destination]] qui est une adresse [[Unicast|monodiffusion]] destinée à un seul destinataire.
*   Une [[SourceInternetProtocolVersion4Address|adresse IP source]] ne peut être qu'une adresse [[Unicast|unicast]] car le [[Packet|paquet]] ne peut provenir que d'une seule source. Ceci est vrai que l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]] soit une [[Unicast|monodiffusion]], une [[Broadcast|diffusion]] ou une [[Multicast|multidiffusion]].
*   Les adresses d'hôtes [[Unicast|unicast]] [[InternetProtocolVersion4|IPv4]] se situent dans la plage d'adresses de *1.1.1.1 à 223.255.255.255*.

## Transmission par Diffusion (Broadcast)

La transmission par [[Broadcast|diffusion]] fait référence à un appareil qui envoie un [[Message|message]] à tous les appareils d'un [[Network|réseau]] dans le cadre d'une communication un à tous.

*   Un [[Packet|paquet]] de [[Broadcast|diffusion]] a une [[DestinationInternetProtocolVersion4Address|adresse IP de destination]] avec tous les bits à 1 dans la [[HostPortion|partie hôte]], ou 32 bits à 1.
*   Un [[Packet|paquet]] de [[Broadcast|diffusion]] doit être traité par tous les périphériques du même [[BroadcastDomain|domaine de diffusion]].
*   La [[Broadcast|diffusion]] peut être *dirigée* ou *limitée*.
    *   Une **[[DirectedBroadcast|diffusion dirigée]]** est envoyée à tous les [[Host|hôtes]] d'un [[Network|réseau]] particulier.
    *   Une **[[LimitedBroadcast|diffusion limitée]]** est envoyée à *255.255.255.255*.
*   Par défaut, les [[Router|routeurs]] ne transfèrent pas les diffusions.

## Transmission Multidiffusion (Multicast)

La transmission [[Multicast|multidiffusion]] réduit le volume du trafic en permettant à un [[Host|hôte]] d'envoyer un seul [[Packet|paquet]] à un groupe d'[[Host|hôtes]] désigné inscrits à un groupe de [[Multicast|multidiffusion]].

*   Un [[Packet|paquet]] de [[Multicast|multidiffusion]] est un [[Packet|paquet]] avec une [[DestinationInternetProtocolVersion4Address|adresse IP de destination]] qui est une adresse de [[Multicast|multidiffusion]].
*   [[InternetProtocolVersion4|IPv4]] a réservé les adresses *224.0.0.0 à 239.255.255.255* comme plage de [[Multicast|multidiffusion]].
*   Chaque groupe de [[Multicast|multidiffusion]] est représenté par une seule [[DestinationInternetProtocolVersion4Address|adresse de destination multidiffusion]] [[InternetProtocolVersion4|IPv4]].
*   Lorsqu'un [[Host|hôte]] [[InternetProtocolVersion4|IPv4]] s'abonne à un groupe de [[Multicast|multidiffusion]], il traite les paquets envoyés à cette adresse de [[Multicast|multidiffusion]], ainsi que ceux destinés à son [[UnicastAddress|adresse de monodiffusion]], qui lui a été attribuée individuellement.