---
tags:
  - protocole
  - reseau
  - adressage
aliases:
  - Protocole Internet
  - IP
  - Internet Protocol
  - Protocole IP
archetype: protocole
rfc:
cssclasses:
  - max
---

# Protocole Internet (IP)

## 🎯 Rôle et Couche OSI
> Le [[InternetProtocol|Protocole Internet]] ([[InternetProtocol|IP]]) est le principal [[Protocol|protocole]] de la [[NetworkLayer|couche réseau]] ([[OpenSystemsInterconnectionModel|couche 3 du modèle OSI]] et [[InternetProtocolSuite|couche Internet du modèle TCP/IP]]) au sein de la [[InternetProtocolSuite|suite de protocoles Internet]]. Il est responsable de l'[[IPAddressing|adressage]] logique et du [[Routing|routage]] des [[Packet|paquets de données]] entre les [[Host|hôtes]] et les [[Network|réseaux]] interconnectés.

## ⚙️ Fonctionnement
1.  **[[IPAddressing|Adressage IP]]**: Chaque [[EndDevices|appareil]] connecté à un [[Network|réseau IP]] se voit attribuer une [[[InternetProtocol|adresse IP]]unique ([[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]). Cette [[[InternetProtocol|adresse IP]]sert d'identifiant logique pour la [[NetworkCommunication|communication]] au sein du [[Network|réseau]] et au-delà.
2.  **[[Routing|Routage]]**: Les [[Packet|paquets de données]] sont acheminés à travers le [[Network|réseau]] grâce à des [[Router|routeurs]]. Les [[Router|routeurs]] examinent l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]] contenue dans l'[[Header|en-tête IP]] du [[Packet|paquet]] et utilisent leurs [[RoutingTable|tables de routage]] pour déterminer le chemin le plus efficace vers la destination.
3.  **[[Encapsulation|Encapsulation]]**: Les [[Data|données]] des couches supérieures sont [[Encapsulation|encapsulées]] dans des [[Packet|paquets IP]]. Chaque [[Packet|paquet IP]] comprend un [[Header|en-tête]] qui contient des informations essentielles telles que les [[SourceInternetProtocolVersion4Address|adresses IP source et destination]], la [[Protocol|version du protocole]] ([[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]), le temps de vie (TTL) et le type de service.
4.  **Sans connexion (Stateless)**: [[InternetProtocol|IP]] est un [[Protocol|protocole]] "sans connexion" ([[StatelessProtocol|stateless]]). Cela signifie qu'il ne maintient pas d'état ni de connexion continue entre l'émetteur et le récepteur. Chaque [[Packet|paquet]] est traité indépendamment, ce qui rend le [[Network|réseau]] flexible mais nécessite des [[Protocol|protocoles]] de couches supérieures (comme [[TransmissionControlProtocol|TCP]]) pour la fiabilité.
5.  **[[Packet|Fragmentation]]**: Si un [[Packet|paquet IP]] est trop grand pour être transmis sur un [[NetworkSegment|segment de réseau]] spécifique (dépassant le MTU - Maximum Transmission Unit), il peut être fragmenté en unités plus petites. Ces fragments sont ensuite réassemblés à la destination.
* **Ports par défaut**: Le [[InternetProtocol|Protocole Internet]] ([[InternetProtocol|IP]]) n'utilise pas de [[PortNumber|ports]] dans le sens des [[TransportLayer|protocoles de transport]] comme [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]]. Son rôle est de fournir l'[[IPAddressing|adressage]] logique et le [[Routing|routage]] entre les [[Host|hôtes]].

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * [[IPSpoofing|Usurpation d'IP]]: Un [[ThreatActor|attaquant]] falsifie l'[[SourceInternetProtocolVersion4Address|adresse IP source]] d'un [[Packet|paquet]] pour masquer son [[UserIdentity|identité]] ou se faire passer pour un autre [[Host|hôte]].
  * [[DenialOfService|Attaques par déni de service (DoS)]] / [[DistributedDenialOfService|DDoS]]: Utilisation abusive de [[Packet|paquets IP]] pour submerger une [[Resource|cible]], rendant ses [[OnlineServices|services]] inaccessibles.
  * [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]]: Bien que non directement une vulnérabilité [[InternetProtocol|IP]], de nombreuses [[ManInTheMiddle|attaques MitM]] manipulent le [[Routing|routage]] ou l'[[IPAddressing|adressage IP]] (ex: [[AddressResolutionProtocolPoisoning|ARP Poisoning]]) pour intercepter et potentiellement modifier les [[Packet|paquets IP]] en transit.
  * [[InadvertentExposure|Fuite d'informations]]: Les [[Header|en-têtes IP]] peuvent révéler des informations sur la [[NetworkTopology|topologie du réseau]] ou les [[OperatingSystem|systèmes d'exploitation]] utilisés.
* **Mesures de protection**:
  * [[Firewall|Filtrage par pare-feu]]: Configuration de [[Firewall|pare-feu]] pour contrôler le [[NetworkTrafficAnalysis|trafic IP]] en fonction des [[[InternetProtocol|adresses IP]]source/destination, des [[PortNumber|ports]] et des [[Protocol|protocoles]] de couche supérieure.
  * [[NetworkSegmentation|Segmentation réseau]]: Isolation des différentes parties d'un [[Network|réseau]] pour limiter la propagation d'[[Attack|attaques]] et réduire la [[AttackSurface|surface d'attaque]].
  * [[InternetProtocolSecurity|IPsec]]: Une [[InternetProtocolSecurity|suite de protocoles]] qui offre l'[[Authentication|authentification]] et le [[Encryption|chiffrement]] des [[Packet|paquets IP]], protégeant l'[[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] des [[NetworkCommunication|communications]].
  * [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|Prévention d'intrusion (IPS)]]: [[SecurityMonitoring|Surveillance]] continue du [[NetworkTrafficAnalysis|trafic IP]] pour détecter et potentiellement bloquer les activités [[Malware|malveillantes]] ou suspectes.
  * **Validation des [[Packet|paquets]]**: Implémentation de mécanismes pour vérifier la validité des [[SourceInternetProtocolVersion4Address|adresses IP source]] des [[Packet|paquets]] entrants, afin de contrer l'[[IPSpoofing|usurpation d'IP]].

## 🔗 Notes Connexes
* [[TransmissionControlProtocol|TCP]]
* [[UserDatagramProtocol|UDP]]
* [[InternetProtocolVersion4|IPv4]]
* [[InternetProtocolVersion6|IPv6]]
* [[NetworkLayer|Couche Réseau]]
* [[Wireshark|Outil d'analyse de protocoles comme Wireshark]]