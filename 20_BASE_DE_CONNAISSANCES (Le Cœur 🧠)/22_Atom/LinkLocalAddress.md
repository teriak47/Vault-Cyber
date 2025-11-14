---
tags:
  - adresse-link-local
  - auto-configuration-ip
  - découverte-de-voisins
  - networksegmentation
  - portsecurity
  - networkmonitoring
aliases:
  - Adresse Link-Local
  - Adresse Lien Local
  - Link-Local Address
source:
  - null
cssclasses:
  - max
---

# Adresse Link-Local

## 📥 Définition en une phrase
> Une adresse Link-Local est une [[InternetProtocolAddress|adresse IP]] auto-configurée qui permet à un [[Host|hôte]] de communiquer avec d'autres [[Host|hôtes]] sur le même [[LocalAreaNetwork|segment de réseau local]] (lien), sans nécessiter de [[DynamicHostConfigurationProtocol|serveur DHCP]] ni de [[Router|routeur]].

## 🧠 Concepts Clés / Fonctionnement
*   **Auto-configuration**: Les [[OperatingSystem|systèmes d'exploitation]] attribuent automatiquement une adresse Link-Local lorsqu'aucune autre [[InternetProtocolAddress|adresse IP]] n'est disponible via [[DynamicHostConfigurationProtocol|DHCP]] ou [[StaticConfiguration|configuration statique]].
*   **Non routable**: Ces [[InternetProtocolAddress|adresses IP]] sont strictement confinées au [[LocalAreaNetwork|segment de réseau local]] et ne sont pas censées être routées au-delà par un [[Router|routeur]].
*   **[[InternetProtocolVersion4|IPv4]] (APIPA)**: En [[InternetProtocolVersion4|IPv4]], la plage d'adresses Link-Local est `169.254.0.0/16`. Le système d'exploitation attribue une adresse de cette plage et vérifie son unicité.
*   **[[InternetProtocolVersion6|IPv6]]**: En [[InternetProtocolVersion6|IPv6]], toutes les interfaces réseau se voient attribuer une [[InternetProtocolAddress|adresse Link-Local]] commençant par le préfixe `fe80::/10`. Elles sont essentielles pour la [[NeighborDiscoveryProtocol|découverte de voisins]] ([[NeighborDiscoveryProtocol|NDP]]) et d'autres protocoles [[InternetProtocolVersion6|IPv6]] sur le lien local.
*   **Utilisation**: Principalement utilisées pour la [[NeighborDiscoveryProtocol|découverte de voisins]] et l'[[AddressResolutionProtocol|ARP]] (en [[InternetProtocolVersion4|IPv4]]), ainsi que pour la communication intra-segment lorsque aucune autre configuration réseau n'est disponible.

## 🛡️ Risques / Menaces Associés
*   **[[Reconnaissance|Reconnaissance]]**: Un [[ThreatActor|attaquant]] sur le même [[LocalAreaNetwork|segment local]] peut utiliser les adresses Link-Local pour découvrir d'autres [[NetworkDevice|dispositifs]] présents, même si ces derniers ne sont pas configurés avec des [[PublicIPAddress|adresses IP routables]].
*   **[[ManInTheMiddle|Attaques de l'Homme du Milieu]]**: Si un [[ThreatActor|attaquant]] parvient à s'insérer sur le même lien local, il peut potentiellement intercepter ou altérer les communications basées sur les adresses Link-Local.
*   **[[UnauthorizedAccess|Accès non autorisé]]**: En l'absence de [[NetworkSegmentation|segmentation réseau]] adéquate, la présence d'appareils avec des adresses Link-Local peut créer une [[AttackSurface|surface d'attaque]] pour des communications inattendues ou malveillantes sur le [[LocalAreaNetwork|réseau local]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Utiliser des [[VirtualLocalAreaNetwork|VLAN]] pour isoler les différents segments de réseau et limiter la portée des communications Link-Local non désirées.
*   **[[PortSecurity|Sécurité des Ports]]**: Configurer la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs réseau]] pour contrôler quels [[MediaAccessControlAddress|adresses MAC]] sont autorisées sur chaque port.
*   **[[NetworkMonitoring|Surveillance Réseau]]**: Mettre en place une [[NetworkMonitoring|surveillance réseau]] pour détecter les activités suspectes ou les tentatives de communication entre des [[Host|hôtes]] qui ne devraient pas interagir sur le même segment.
*   **[[PhysicalSecurity|Sécurité Physique]]**: Assurer la [[PhysicalSecurity|sécurité physique]] des [[NetworkDevice|équipements réseau]] pour empêcher l'accès non autorisé au [[LocalAreaNetwork|réseau local]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[InternetProtocolVersion4|Internet Protocol Version 4]]
*   [[InternetProtocolVersion6|Internet Protocol Version 6]]
*   [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol]]
*   [[DynamicHostConfigurationProtocol|Dynamic Host Configuration Protocol]]
*   [[LocalAreaNetwork|Local Area Network]]
*   [[NetworkLayer|Couche Réseau]]