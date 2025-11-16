---
tags:
  - protocole
aliases:
  - Protocole Internet version 6
  - IPv6
  - Internet Protocol Version 6
  - IP version 6
archetype: protocole
rfc: RFC 8200
cssclasses:
  - max
---

# Protocole Internet version 6 (IPv6)

## 🎯 Rôle et Couche OSI
> [[InternetProtocolVersion6|IPv6]] est la version la plus récente du [[NetworkProtocol|protocole de couche réseau]] fondamental pour l'[[InterconnectedNetworks|interconnexion des réseaux]]. Il opère à la [[NetworkLayer|couche réseau]] (Couche 3) du [[OSIModel|modèle OSI]] et du [[InternetProtocolSuite|modèle TCP/IP]]. Son rôle principal est d'identifier de manière unique les [[EndDevices|dispositifs]] sur un [[Network|réseau]] et de [[Routing|router]] les [[Packet|paquets]] de données entre les réseaux, succédant à [[InternetProtocolVersion4|IPv4]] pour pallier la pénurie d'[[InternetProtocolAddressBlocks|adresses IP]] et offrir des améliorations de performances et de [[Security|sécurité]].

## ⚙️ Fonctionnement
1.  **Gestion des [[IPAddressing|adresses IP]]**: [[InternetProtocolVersion6|IPv6]] utilise des adresses de 128 bits, offrant un espace d'adressage considérablement élargi ($2^{128}$ adresses uniques) par rapport aux 32 bits d'[[InternetProtocolVersion4|IPv4]]. Ces adresses sont représentées par huit groupes de quatre [[HexadecimalValues|valeurs hexadécimales]] séparées par des deux-points (par exemple, `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
2.  **[[Packet|Encapsulation]] et [[Routing|Routage]]**: Il [[Encapsulation|encapsule]] les données en [[Packet|paquets]] et les [[Routing|route]] d'une [[Host|source]] à une [[Host|destination]] à travers [[InterconnectedNetworks|des réseaux interconnectés]]. L'[[Header|en-tête]] [[InternetProtocolVersion6|IPv6]] est simplifié pour un traitement plus efficace par les [[Router|routeurs]], avec des champs comme la classe de trafic ([[TrafficClass|Traffic Class]]) et l'étiquette de flux ([[FlowLabel|Flow Label]]) pour le [[QualityOfService|QoS]].
3.  **[[StatelessAddressAutoConfiguration|Auto-configuration sans état (SLAAC)]]**: Permet aux [[Host|hôtes]] de générer automatiquement leurs propres [[LinkLocalAddress|adresses IPv6 link-local]] et [[PublicIPAddress|globales]] sans nécessiter de [[DHCPServer|serveur DHCP]]. Ils peuvent former une [[LinkLocalAddress|adresse link-local]] en combinant un préfixe réseau avec leur [[NetworkInterfaceCard|adresse MAC]] ou un identifiant aléatoire, et peuvent ensuite obtenir une [[PublicIPAddress|adresse globale]] via des messages de [[RouterAdvertisement|publicité de routeur (RA)]].
4.  **Absence de [[NetworkAddressTranslation|NAT]] pour la pénurie d'adresses**: Grâce à l'énorme espace d'adressage, le [[NetworkAddressTranslation|NAT]] (Traduction d'Adresses Réseau), souvent utilisé en [[InternetProtocolVersion4|IPv4]] pour pallier la pénurie d'adresses, n'est plus nécessaire à cette fin, simplifiant la connectivité de bout en bout et les applications client-serveur.
5.  **Prise en charge de [[Multicast|Multicast]] et [[Anycast|Anycast]]**: [[InternetProtocolVersion6|IPv6]] remplace les [[Broadcast|diffusions]] d'[[InternetProtocolVersion4|IPv4]] par le [[Multicast|multicast]] (envoi à un groupe spécifique) et l'[[Anycast|anycast]] (envoi à l'hôte le plus proche d'un groupe), permettant une livraison plus efficace des [[Packet|paquets]].
* **Ports par défaut**: Le [[InternetProtocolVersion6|Protocole Internet version 6]] opère à la [[NetworkLayer|couche réseau]] (couche 3) et n'utilise pas de ports au sens des [[TransportLayer|protocoles de transport]] comme [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]].

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * **[[ShadowIT|Visibilité réduite]] / [[ConfigurationDrift|Dérive de configuration]]**: La complexité de la transition ou la méconnaissance d'[[InternetProtocolVersion6|IPv6]] peut entraîner des services [[InternetProtocolVersion6|IPv6]] actifs mais non sécurisés ou [[NetworkMonitoring|monitorés]], créant des failles de [[Security|sécurité]].
  * **[[Bypass|Contournement des contrôles]]**: Des [[Firewall|pare-feux]] ou [[IntrusionPreventionSystem|IPS]] mal configurés pour [[InternetProtocolVersion6|IPv6]] peuvent être contournés, permettant à des [[Malware|logiciels malveillants]] ou des [[AdvancedPersistentThreat|APT]] de s'infiltrer.
  * **[[NeighborDiscoveryProtocol|Attaques NDP]]**: Des vulnérabilités similaires au [[AddressResolutionProtocolPoisoning|spoofing ARP]] d'[[InternetProtocolVersion4|IPv4]] existent pour le [[NeighborDiscoveryProtocol|NDP]] (par exemple, [[CachePoisoning|empoisonnement du cache NDP]]), permettant des [[ManInTheMiddle|attaques de l'homme du milieu]].
  * **[[RouterAdvertisement|Falsification de RA]]**: Un [[ThreatActor|acteur de menace]] peut annoncer de fausses informations de [[Routing|routage]] pour rediriger le [[NetworkTrafficAnalysis|trafic]].
  * **[[DenialOfService|Attaques DoS]]**: L'exploitation de fragments [[InternetProtocolVersion6|IPv6]] ou de [[Packet|paquets malformés]] peut être utilisée pour des [[DenialOfService|attaques par déni de service]].
* **Sécurité intégrée**:
  * [[IPsec|IPsec]] est une exigence fondamentale dans [[InternetProtocolVersion6|IPv6]], facilitant le [[Encryption|chiffrement]] de bout en bout et l'[[Authentication|authentification]] des [[Packet|paquets IP]], offrant une base [[Security|sécurisée]] pour les communications.
  * **[[VulnerabilityManagement|Gestion des vulnérabilités]]**: Audits réguliers des configurations [[InternetProtocolVersion6|IPv6]] pour identifier et corriger les faiblesses.
  * **[[AccessControl|Contrôle d'accès]]**: Mettre en œuvre des politiques [[NetworkAccessControl|NAC]] pour contrôler les [[NetworkDevice|périphériques]] connectés via [[InternetProtocolVersion6|IPv6]].
  * **[[Firewall|Configuration des pare-feux]]**: Assurer que les règles de [[Firewall|pare-feu]] sont correctement appliquées au [[NetworkTrafficAnalysis|trafic IPv6]], idéalement en mode "deny by default".
  * **[[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]]**: Déployer des systèmes capables de surveiller et de bloquer les [[Attack|attaques]] spécifiques à [[InternetProtocolVersion6|IPv6]].
  * **[[NetworkSegmentation|Segmentation réseau]]**: Isoler les [[System|systèmes]] critiques et limiter la propagation des [[Threat|menaces]].
  * **[[SecurityAwareness|Sensibilisation]]**: Former les [[Team|équipes techniques]] aux spécificités et aux [[SecurityVulnerabilities|risques de sécurité]] d'[[InternetProtocolVersion6|IPv6]].

## 🔗 Notes Connexes
*   [[InternetProtocolVersion4|IPv4]]
*   [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol (NDP)]]
*   [[IPsec|IPsec]]
*   [[NetworkAddressTranslation|NAT]]
*   [[DualStack|Dual-Stack]]
*   [[DynamicHostConfigurationProtocol|DHCPv6]]
*   [[NetworkLayer|Couche réseau]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[OSIModel|Modèle OSI]]
*   [[Packet|Paquet]]
*   [[Routing|Routage]]
*   [[InternetEngineeringTaskForce|IETF]]
*   [[InternetAssignedNumbersAuthority|IANA]]
*   [[UnicastAddress|Adresses Unicast]]
*   [[Multicast|Multicast]]
*   [[Anycast|Anycast]]
*   [[TransitionMechanism|Mécanismes de transition IPv4 vers IPv6]]
*   [[Wireshark]]