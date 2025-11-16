---
tags:
  - reseau
  - ip
aliases:
  - Adresse Link-Local
  - Adresse Lien Local
  - Link-Local Address
  - LinkLocalAddress
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse Link-Local

## 📥 Définition en une phrase
> Une [[LinkLocalAddress|adresse Link-Local]] est une [[InternetProtocol|adresse IP]] auto-configurée qui permet aux [[Host|hôtes]] d'un même [[NetworkSegment|segment de réseau local]] de communiquer directement, sans dépendre d'un [[DHCPServer|serveur DHCP]] ni d'un [[Router|routeur]].

## 🧠 Concepts Clés / Piliers
*   **Auto-configuration**: Les [[OperatingSystem|systèmes d'exploitation]] attribuent automatiquement une [[LinkLocalAddress|adresse Link-Local]] lorsqu'aucune autre [[InternetProtocol|adresse IP]] n'est disponible via [[DynamicHostConfigurationProtocol|DHCP]] ou [[StaticConfiguration|configuration statique]]. Ce processus garantit une connectivité de base sur le lien.
*   **Non routable**: Ces [[InternetProtocol|adresses IP]] sont intrinsèquement conçues pour la communication intra-[[LocalAreaNetwork|LAN]] et ne doivent pas être acheminées au-delà du [[NetworkSegment|segment local]] par un [[Router|routeur]].
*   **Spécificités [[InternetProtocolVersion4|IPv4]] (APIPA)**: Pour [[InternetProtocolVersion4|IPv4]], la plage dédiée est `169.254.0.0/16` (connu sous le nom d'APIPA - [[AutomaticPrivateIPAddressing|Automatic Private IP Addressing]]). Le [[System|système]] attribue une adresse et vérifie son unicité sur le lien.
*   **Spécificités [[InternetProtocolVersion6|IPv6]]**: En [[InternetProtocolVersion6|IPv6]], chaque [[NetworkInterface|interface réseau]] se voit attribuer une [[LinkLocalAddress|adresse Link-Local]] avec le préfixe `fe80::/10`. Elles sont fondamentales pour des protocoles essentiels comme le [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol]] ([[NeighborDiscoveryProtocol|NDP]]) sur le lien local.
*   **Rôles principaux**: Elles sont utilisées pour la [[NeighborDiscoveryProtocol|découverte de voisins]], la résolution d'[[MediaAccessControlAddress|adresses MAC]] (similaire à l'[[AddressResolutionProtocol|ARP]] en [[InternetProtocolVersion4|IPv4]]) et pour établir une communication de base en l'absence de toute autre [[NetworkConfiguration|configuration réseau]].

## 💡 Importance en Cybersécurité
> Les [[LinkLocalAddress|adresses Link-Local]] sont cruciales pour la connectivité réseau de base, permettant aux [[NetworkDevice|dispositifs]] de communiquer sur un même [[NetworkSegment|segment]] même sans [[DHCPServer|serveur DHCP]] ou [[StaticIPAddressing|configuration statique]]. Cependant, leur nature auto-configurée et non routable présente des [[SecurityVulnerabilities|vulnérabilités de sécurité]] significatives. Un [[ThreatActor|acteur de menace]] présent sur le même [[LocalAreaNetwork|réseau local]] peut exploiter ces adresses pour la [[Reconnaissance|reconnaissance]] des [[Host|hôtes]] et des [[NetworkDevice|dispositifs]], potentiellement menant à des [[ManInTheMiddle|attaques de l'homme du milieu]] ou à des tentatives d'[[UnauthorizedAccess|accès non autorisé]] si la [[NetworkSegmentation|segmentation réseau]] est faible. Une gestion et une [[NetworkMonitoring|surveillance réseau]] rigoureuses sont donc essentielles pour prévenir l'[[InadvertentExposure|exposition involontaire]] et limiter la [[AttackSurface|surface d'attaque]] potentielle, même si les [[Host|hôtes]] ne sont pas configurés avec des [[RoutableInternetAddress|adresses IP routables]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[NetworkSegment|Segment de Réseau]]
*   [[DHCPServer|Serveur DHCP]]
*   [[Router|Routeur]]
*   [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol]]
*   [[AddressResolutionProtocol|ARP]]
*   [[AutomaticPrivateIPAddressing|APIPA]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[NetworkMonitoring|Surveillance Réseau]]
*   [[AttackSurface|Surface d'attaque]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[Reconnaissance|Reconnaissance]]