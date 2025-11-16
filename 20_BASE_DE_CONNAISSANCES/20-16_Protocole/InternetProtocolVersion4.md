---
tags:
  - protocole
aliases:
  - IPv4
  - Internet Protocol version 4
  - Protocole Internet version 4
  - InternetProtocolVersion4
archetype: protocole
rfc: RFC 791
cssclasses:
  - max
---

# Protocole Internet version 4 (IPv4)

## 🎯 Rôle et Couche OSI
> L'[[InternetProtocolVersion4|IPv4]] est la quatrième version du [[InternetProtocol|Protocole Internet]], chargée de l'adressage logique et du [[Routing|routage]] des [[Packet|paquets]] de [[Data|données]] entre les [[Host|hôtes]] sur les [[InterconnectedNetworks|réseaux interconnectés]]. Il opère à la [[NetworkLayer|couche réseau]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et à la [[InternetLayer|couche Internet]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
1.  **Adresses 32-bit**: Chaque [[Computer|appareil]] participant à un [[Network|réseau]] [[InternetProtocolVersion4|IPv4]] se voit attribuer une [[InternetProtocolAddressBlocks|adresse IP]] unique de 32 [[Bit|bits]], généralement représentée en notation décimale pointée (ex: 192.168.1.1).
2.  **[[SubnetMask|Masque de sous-réseau]]**: Un [[SubnetMask|masque de sous-réseau]] est utilisé pour délimiter la [[NetworkPortion|partie réseau]] de l'[[HostPortion|partie hôte]] d'une [[InternetProtocolAddressBlocks|adresse IP]], facilitant la [[NetworkSegmentation|segmentation des réseaux]] en [[Subnet|sous-réseaux]].
3.  **[[Routing|Routage]]**: Les [[Router|routeurs]] utilisent l'[[NetworkAddress|adresse réseau]] pour déterminer le chemin optimal par lequel les [[Packet|paquets]] doivent être acheminés vers leur [[DestinationInternetProtocolVersion4Address|destination]].
4.  **Fragmentation**: [[InternetProtocolVersion4|IPv4]] prend en charge la fragmentation des [[Packet|paquets]] si leur taille dépasse la [[MessageSize|taille maximale]] du [[NetworkSegment|segment réseau]] sur lequel ils sont transmis, puis leur réassemblage à l'arrivée.
5.  **[[ClasslessInterDomainRouting|CIDR]]**: Le [[ClasslessInterDomainRouting|Classless Inter-Domain Routing]] (CIDR) a été mis en œuvre pour améliorer l'efficacité de l'[[IPAddressing|allocation des adresses IP]] et remplacer l'[[ClassfulAddressing|adressage classique]] par l'utilisation de [[NetworkPrefix|préfixes]] de longueur variable.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[DenialOfService|Attaques par déni de service]] ([[DenialOfService|DoS]]): Des attaques comme les SYN floods peuvent exploiter les mécanismes de gestion de connexion d'[[InternetProtocolVersion4|IPv4]] pour submerger un [[System|système]] ou un [[Network|réseau]].
    *   [[IPSpoofing|Usurpation d'adresse IP]]: Les [[ThreatActor|attaquants]] peuvent [[Spoofing|falsifier]] l'[[SourceInternetProtocolVersion4Address|adresse IP source]] dans les [[Packet|paquets]] [[InternetProtocolVersion4|IPv4]] pour masquer leur identité ou contourner les [[AccessControl|contrôles d'accès]] basés sur l'[[InternetProtocolAddressBlocks|IP]].
    *   [[ManInTheMiddle|Attaques de l'homme du milieu]] ([[ManInTheMiddle|MitM]]): Des vulnérabilités au niveau de l'[[AddressResolutionProtocol|ARP]], comme l'[[AddressResolutionProtocolPoisoning|ARP poisoning]], peuvent être exploitées dans les [[LocalAreaNetwork|LAN]] [[InternetProtocolVersion4|IPv4]] pour intercepter le [[NetworkCommunication|trafic réseau]].
    *   [[Vulnerability|Pénurie d'adresses]]: La conception 32-bit d'[[InternetProtocolVersion4|IPv4]] a conduit à une [[Vulnerability|pénurie]] d'[[InternetProtocolAddressBlocks|adresses IP]] disponibles, ce qui constitue un défi majeur pour l'[[Internet|Internet]] moderne et a poussé à l'adoption d'[[InternetProtocolVersion6|IPv6]].
*   **Versions sécurisées**:
    *   [[InternetProtocolSecurity|IPsec]]: Le protocole [[InternetProtocolSecurity|IPsec]] peut être utilisé pour ajouter des capacités de [[DataEncryption|chiffrement des données]] et d'[[Authentication|authentification]] aux communications [[InternetProtocolVersion4|IPv4]], sécurisant ainsi les transmissions.

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|IPv6]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetControlMessageProtocol|ICMP]]
*   [[Subnetting|Sous-réseautage]]
*   [[Firewall|Pare-feu]]
*   [[NetworkAddressTranslation|NAT]]
*   [[AccessControlList|Listes de contrôle d'accès]]
*   [[AddressResolutionProtocol|ARP]]
*   [[Wireshark|Wireshark]]