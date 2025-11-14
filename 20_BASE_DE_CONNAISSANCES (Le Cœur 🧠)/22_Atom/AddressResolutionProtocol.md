---
tags:
  - adressage/ip-mac
  - reseau/decouverte-hote
  - securite/durcissement-arp
  - protocole/arp
  - cybersecurite/empoisonnement-arp
  - securite/inspection-arp-dynamique
aliases:
  - Protocole de résolution d'adresse
  - ARP
  - Address Resolution Protocol
source:
  - null
cssclasses:
  - max
---

# Protocole de Résolution d'Adresse (ARP)

## 📥 Définition en une phrase
> L'[[AddressResolutionProtocol|ARP]] est un [[Protocols|protocole]] de communication qui permet de traduire une [[InternetProtocolAddress|adresse IP]] (couche 3) en une [[MediaAccessControlAddress|adresse MAC]] physique (couche 2) nécessaire à la communication au sein d'un [[LocalAreaNetwork|réseau local]].

## 🧠 Concepts Clés / Fonctionnement
*   **Mapping d'Adresses**: L'objectif principal est d'établir la correspondance entre les adresses logiques ([[InternetProtocolAddress|IPv4]]) et les adresses physiques ([[MediaAccessControlAddress|MAC]]).
*   **Requête ARP**: Lorsqu'un hôte doit communiquer avec un autre hôte sur le même segment de réseau et qu'il ne connaît pas son adresse MAC, il envoie une [[ARPRequest|requête ARP]] en diffusion ([[Broadcast|broadcast]]) sur le [[LocalAreaNetwork|LAN]].
*   **Réponse ARP**: L'hôte cible, reconnaissant son adresse IP dans la requête, répond avec une [[ARPReply|réponse ARP]] unicast contenant son adresse MAC.
*   **Cache ARP**: Chaque hôte maintient un [[ARPCache|cache ARP]] local pour stocker les correspondances IP-MAC récemment apprises, afin de réduire le nombre de requêtes ARP futures. Ces entrées ont une durée de vie limitée.
*   **Fonctionnement par Couche**: L'[[AddressResolutionProtocol|ARP]] opère à la [[DataLinkLayer|couche Liaison de Données]] (couche 2 du modèle [[OpenSystemsInterconnectionModel|OSI]]) tout en traitant des informations de la [[NetworkLayer|couche Réseau]] (couche 3).

## 🛡️ Risques / Menaces Associés
*   [[ARPSpoofing|Usurpation d'ARP]] (ARP Spoofing): Un attaquant peut envoyer de fausses réponses ARP pour associer son adresse MAC à l'adresse IP d'une autre machine (passerelle par défaut, ou autre hôte), lui permettant d'intercepter, modifier ou rediriger le trafic (attaque de type [[ManInTheMiddle|Homme du Milieu]]).
*   [[DenialOfService|Déni de Service]] (DoS): Des réponses ARP malveillantes peuvent inonder le cache ARP d'un hôte avec des entrées incorrectes, le rendant incapable de communiquer.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DynamicARPIngressFiltering|Inspection ARP Dynamique]] (DAI - Dynamic ARP Inspection): Les commutateurs peuvent valider les paquets ARP entrants en les comparant aux informations stockées dans les tables [[DHCP|DHCP]] snooping, rejetant les paquets ARP non valides.
*   [[StaticARPEntry|Entrées ARP statiques]]: Pour les dispositifs critiques comme les passerelles, il est possible de configurer manuellement des entrées ARP statiques pour empêcher leur modification.
*   [[PortSecurity|Sécurité des ports]]: Limiter le nombre d'adresses MAC autorisées sur un port de commutateur peut aider à prévenir les attaques d'usurpation.
*   [[NetworkAccessControl|Contrôle d'accès réseau]] (NAC): Permet de s'assurer que seuls les appareils autorisés peuvent se connecter au réseau et utiliser ARP.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Ethernet|Ethernet]]
*   [[NeighborDiscovery|Neighbor Discovery Protocol]] (Équivalent pour IPv6)
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkLayer|Couche Réseau]]