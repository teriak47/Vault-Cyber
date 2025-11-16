---
aliases:
  - Protocole de résolution d'adresse
  - ARP
  - Address Resolution Protocol
  - ARP Protocol
source:
  - 
rfc:
  - RFC 826
cssclasses:
  - max
archetype: protocole
---

# Protocole de Résolution d'Adresse (ARP)

## 🎯 Rôle et Couche OSI
> L'[[AddressResolutionProtocol|ARP]] est un [[Protocol|protocole]] de communication essentiel qui établit la correspondance entre une [[InternetProtocol|adresse IP]] logique ([[InternetProtocolVersion4|IPv4]]) et l'[[MediaAccessControlAddress|adresse MAC]] physique correspondante d'un [[Host|hôte]]. Cette traduction est nécessaire pour la [[NetworkCommunication|communication réseau]] au sein d'un [[LocalAreaNetwork|réseau local]].
> Il opère principalement à la [[DataLinkLayer|couche Liaison de Données]] (couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]) pour la résolution de l'[[MediaAccessControlAddress|adresse MAC]], tout en manipulant des informations de la [[NetworkLayer|couche Réseau]] (couche 3) pour l'[[InternetProtocol|adresse IP]]. Pour le [[InternetProtocolSuite|modèle TCP/IP]], il est souvent considéré comme faisant partie de la [[NetworkAccessLayer|couche d'accès réseau]].

## ⚙️ Fonctionnement
1.  **Recherche dans le [[ARPCache|cache ARP]]**: Avant d'envoyer une [[AddressResolutionProtocolRequest|requête ARP]], un [[Host|hôte]] vérifie son [[ARPCache|cache ARP]] local pour voir s'il possède déjà la correspondance [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]] de la [[DestinationInternetProtocolVersion4Address|destination]].
2.  **[[AddressResolutionProtocolRequest|Requête ARP]] (Broadcast)**: Si la correspondance n'est pas trouvée, l'[[Host|hôte]] émet une [[AddressResolutionProtocolRequest|requête ARP]] en [[Broadcast|diffusion]] ([[BroadcastDomain|domaine de diffusion]]) sur le [[LocalAreaNetwork|LAN]]. Cette requête contient l'[[InternetProtocol|adresse IP]] de la [[DestinationInternetProtocolVersion4Address|machine cible]] et demande son [[MediaAccessControlAddress|adresse MAC]].
3.  **[[AddressResolutionProtocolReply|Réponse ARP]] (Unicast)**: Le [[Host|hôte]] dont l'[[InternetProtocol|adresse IP]] correspond à celle de la requête répond avec une [[AddressResolutionProtocolReply|réponse ARP]]. Cette réponse contient sa propre [[MediaAccessControlAddress|adresse MAC]] et est envoyée directement en [[Unicast|unicast]] à l'[[SourceInternetProtocolVersion4Address|expéditeur]] de la requête.
4.  **Mise à jour du [[ARPCache|cache ARP]]**: L'[[SourceInternetProtocolVersion4Address|hôte demandeur]] reçoit la [[AddressResolutionProtocolReply|réponse ARP]] et stocke la nouvelle correspondance [[InternetProtocol|IP]]-[[MediaAccessControlAddress|MAC]] dans son [[ARPCache|cache ARP]] pour une durée limitée.

*   **Ports par défaut**: L'[[AddressResolutionProtocol|ARP]] n'utilise pas de [[PortNumber|numéros de port]] [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] car il opère directement à un niveau inférieur (couche 2/3) de la [[ProtocolStack|pile de protocoles]].

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[AddressResolutionProtocolPoisoning|Usurpation d'ARP]] (ARP Spoofing): Un [[ThreatActor|attaquant]] peut envoyer de fausses [[AddressResolutionProtocolReply|réponses ARP]] pour associer son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocol|adresse IP]] d'un autre [[NetworkDevice|dispositif]] légitime (comme une [[Gateway|passerelle par défaut]] ou un [[Server|serveur]]). Cela permet au [[ThreatActor|malveillant]] d'intercepter, modifier ou rediriger le [[NetworkTrafficAnalysis|trafic]] (une forme d'[[ManInTheMiddle|attaque de l'homme du milieu]]).
    *   [[DenialOfService|Déni de Service]] (DoS): Des [[AddressResolutionProtocolReply|réponses ARP]] malveillantes massives peuvent inonder le [[ARPCache|cache ARP]] d'un [[Host|hôte]] avec des entrées incorrectes, le rendant incapable de communiquer avec d'autres [[EndDevices|dispositifs]] sur le [[NetworkSegment|segment réseau]].
*   **Mesures de protection**:
    *   [[DynamicARPIngressFiltering|Inspection ARP Dynamique]] (DAI - Dynamic ARP Inspection): Les [[NetworkSwitch|commutateurs réseau]] peuvent valider les [[Packet|paquets ARP]] entrants en les comparant aux informations stockées dans les tables [[DynamicHostConfigurationProtocol|DHCP]] snooping, rejetant les [[Packet|paquets ARP]] non valides ou usurpés.
    *   [[StaticARPEntry|Entrées ARP statiques]]: Pour les [[IntermediateDevice|dispositifs]] critiques comme les [[Router|routeurs]] ou les [[FileServer|serveurs de fichiers]], il est possible de configurer manuellement des [[StaticARPEntry|entrées ARP statiques]] dans leur [[ARPCache|cache ARP]] afin d'empêcher toute modification dynamique malveillante.
    *   [[PortSecurity|Sécurité des ports]]: Configurer la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] permet de limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] autorisées sur un port, aidant à prévenir les attaques d'[[MACSpoofing|usurpation d'adresse MAC]] et par extension les attaques [[AddressResolutionProtocolPoisoning|ARP spoofing]].
    *   [[NetworkAccessControl|Contrôle d'accès réseau]] (NAC): Les solutions de [[NetworkAccessControl|NAC]] peuvent aider à garantir que seuls les [[EndDevices|appareils]] [[Authorization|autorisés]] sont capables de se connecter au [[Network|réseau]] et d'utiliser l'[[AddressResolutionProtocol|ARP]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Ethernet|Ethernet]]
*   [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol]] (l'équivalent de l'[[AddressResolutionProtocol|ARP]] pour [[InternetProtocolVersion6|IPv6]])
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkLayer|Couche Réseau]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement du protocole de résolution d'adresses]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[Wireshark|Wireshark]] (Outil pour analyser le [[NetworkTrafficAnalysis|trafic réseau]] incluant les [[Packet|paquets ARP]])