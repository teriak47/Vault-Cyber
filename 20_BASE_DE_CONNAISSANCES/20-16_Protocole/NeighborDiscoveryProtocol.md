---
tags:
  - protocole
aliases:
  - Neighbor Discovery Protocol
  - NDP
  - Protocole de Découverte de Voisins
archetype: protocole
rfc: RFC 4861
cssclasses:
  - max
---

# Protocole de Découverte de Voisins (NDP)

## 🎯 Rôle et Couche OSI
Le [[NeighborDiscoveryProtocol|Protocole de Découverte de Voisins]] ([[NeighborDiscoveryProtocol|NDP]]) est un [[NetworkProtocol|protocole]] essentiel pour [[InternetProtocolVersion6|IPv6]], qui remplace et combine les fonctionnalités d'[[AddressResolutionProtocol|ARP]] et d'[[InternetControlMessageProtocol|ICMP]] Router Discovery pour la découverte de voisins, la [[IPAddressing|résolution d'adresses]], et la gestion des [[Router|routeurs]] sur un [[NetworkSegment|segment de réseau]] local. Il opère principalement à la [[NetworkLayer|couche Réseau]] du [[InternetProtocolSuite|modèle TCP/IP]] et à la [[InternetLayer|couche Internet]] pour la gestion des interactions entre hôtes sur le même lien. Il utilise les messages [[InternetControlMessageProtocolVersion6|ICMPv6]].

## ⚙️ Fonctionnement
1.  **Résolution d'Adresse**: Un [[Host|nœud]] détermine l'[[MediaAccessControlAddress|adresse MAC]] (couche liaison de données) d'un autre [[Host|nœud]] [[InternetProtocolVersion6|IPv6]] sur le même lien, en utilisant les messages [[InternetControlMessageProtocolVersion6|ICMPv6]] `Neighbor Solicitation` et `Neighbor Advertisement`.
2.  **Découverte de Routeur**: Les [[Host|hôtes]] identifient les [[Router|routeurs]] disponibles sur le lien local et découvrent leurs [[NetworkPrefix|préfixes réseau]] via les messages [[InternetControlMessageProtocolVersion6|ICMPv6]] `Router Solicitation` et `Router Advertisement`. Cela facilite l'[[StatelessAddressAutoConfiguration|auto-configuration sans état (SLAAC)]] des [[InternetProtocolVersion6|adresses IPv6]].
3.  **Détection d'Adresses Dupliquées (DAD)**: Un [[Host|nœud]] utilise le [[NeighborDiscoveryProtocol|NDP]] pour s'assurer qu'une [[InternetProtocolVersion6|adresse IPv6]] qu'il souhaite utiliser n'est pas déjà assignée à un autre [[Host|nœud]] sur le même lien.
4.  **Découverte de Préfixe**: Les [[Router|routeurs]] annoncent les [[NetworkPrefix|préfixes IPv6]] disponibles, permettant aux [[Host|hôtes]] de configurer automatiquement leurs [[InternetProtocolVersion6|adresses IPv6]] et d'identifier les [[DefaultGateway|passerelles par défaut]].
5.  **Redirection**: Un [[Router|routeur]] peut informer un [[Host|hôte]] qu'un meilleur [[Routing|chemin]] existe pour atteindre une [[DestinationInternetProtocolVersion4Address|destination]] spécifique via un autre [[Router|routeur]] sur le même lien.
*   **Ports par défaut**: N/A (opère au niveau de la [[NetworkLayer|couche Réseau]] via [[InternetControlMessageProtocolVersion6|ICMPv6]], non basé sur des ports TCP/UDP).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]]: L'[[ThreatActor|attaquant]] peut intercepter et modifier le [[NetworkTrafficAnalysis|trafic]] en usurpant des [[UserIdentity|identités]] via de fausses annonces [[NeighborDiscoveryProtocol|NDP]].
    *   [[DenialOfService|Déni de Service (DoS)]]: L'[[ThreatActor|attaquant]] sature le [[Network|réseau]] avec des messages [[NeighborDiscoveryProtocol|NDP]] falsifiés, surchargeant les [[Host|hôtes]] et les [[Router|routeurs]], perturbant ainsi la [[NetworkCommunication|communication IPv6]].
    *   [[AddressSpoofing|Usurpation d'adresses]]: Falsification des messages [[NeighborDiscoveryProtocol|NDP]] pour associer une [[InternetProtocolVersion6|adresse IPv6]] légitime à l'[[MediaAccessControlAddress|adresse MAC]] de l'[[ThreatActor|attaquant]].
    *   [[RouterAdvertisementSpoofing|Usurpation d'Annonce de Routeur]]: L'[[ThreatActor|attaquant]] se fait passer pour un [[Router|routeur]] légitime, distribue de fausses [[Routing|informations de routage]] ou de [[NetworkPrefix|préfixes]], et détourne le [[NetworkTrafficAnalysis|trafic]].
*   **Mesures de protection**:
    *   [[FirstHopSecurity|Sécurité du Premier Saut (FHS)]]: Inclut `RA-Guard` (protection contre les fausses annonces de [[Router|routeur]]) et `NDP Snooping` sur les [[NetworkSwitch|commutateurs réseau]] pour valider et bloquer les messages [[NeighborDiscoveryProtocol|NDP]] non autorisés.
    *   [[SecureNeighborDiscovery|SEND (Secure Neighbor Discovery)]]: Une extension de [[NeighborDiscoveryProtocol|NDP]] utilisant la [[Cryptography|cryptographie]] ([[DigitalCertificate|certificats X.509]] et [[DigitalSignature|signatures numériques]]) pour authentifier les messages. Son [[Interoperability|adoption]] reste limitée.
    *   [[NetworkSegmentation|Segmentation Réseau]]: Isoler les [[System|systèmes]] critiques sur des [[NetworkSegment|segments de réseau]] distincts pour limiter l'[[AttackSurface|surface d'attaque]].
    *   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]]: Restreindre l'[[AccessControl|accès au réseau]] aux [[WirelessDevices|appareils]] autorisés et surveiller leur [[Process|comportement]].
    *   [[SecurityMonitoring|Surveillance de sécurité]] et [[IntrusionDetectionSystem|détection d'intrusion]]: Mettre en place des [[System|systèmes]] pour identifier les [[AnomalyDetection|anomalies]] dans le [[NetworkTrafficAnalysis|trafic NDP]].

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|IPv6]]
*   [[AddressResolutionProtocol|ARP]]
*   [[InternetControlMessageProtocolVersion6|ICMPv6]]
*   [[RouterAdvertisementSpoofing|Usurpation d'Annonce de Routeur]]
*   [[FirstHopSecurity|Sécurité du Premier Saut]]
*   [[Wireshark|Wireshark]] (Outil d'analyse)
*   [[StatelessAddressAutoConfiguration|Auto-configuration sans état (SLAAC)]]