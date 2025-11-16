---
tags:
aliases:
  - Couche Réseau
  - Network Layer
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche Réseau

## 📥 Définition en une phrase
> La [[NetworkLayer|couche réseau]] est la troisième couche du [[OpenSystemsInterconnectionModel|Modèle OSI]], chargée de l'adressage logique et de l'acheminement des [[Packet|paquets]] de [[Data|données]] entre des [[InterconnectedNetworks|réseaux interconnectés]].

## 🧠 Concepts Clés / Piliers
*   **Adressage Logique**: Utilise des [[InternetProtocol|protocoles d'adressage logique]] comme [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]] pour identifier de manière unique les [[Host|hôtes]] et les [[NetworkDevice|dispositifs réseau]] au sein d'un [[Network|réseau]] et entre eux.
*   **[[Routing|Routage]]**: Détermine le chemin optimal pour les [[Packet|paquets]] à travers l'[[Internet|internet]] ou un [[Network|réseau]] étendu, s'appuyant sur les [[Router|routeurs]] et leurs [[RoutingTable|tables de routage]] pour atteindre leur [[DestinationInternetProtocolVersion4Address|destination]].
*   **[[Encapsulation|Encapsulation]] et [[Decapsulation|Décapsulation]]**: Processus par lequel les [[Data|données]] de la [[TransportLayer|couche transport]] sont encapsulées dans des [[Packet|paquets]] au départ et désencapsulées à l'arrivée pour reconstituer le [[Message|message]] original.
*   **[[IPFragmentation|Fragmentation IP]]**: La capacité de diviser un [[Packet|paquet]] en unités plus petites si sa taille dépasse la [[MaximumTransmissionUnit|MTU]] (Maximum Transmission Unit) d'un [[NetworkMedia|support réseau]], assurant la flexibilité de la [[DataTransmission|transmission]].
*   **Dispositifs Clés**: Les [[Router|routeurs]] sont les principaux [[IntermediateDevice|dispositifs intermédiaires]] de cette couche, essentiels pour connecter différents [[Network|réseaux]] et prendre les décisions de [[Routing|routage]].

## 💡 Importance en Cybersécurité
> La [[NetworkLayer|couche réseau]] est fondamentale pour l'[[NetworkCommunication|interconnexion]] et la [[NetworkCommunication|communication]] entre les [[System|systèmes]]. Elle constitue une [[AttackSurface|surface d'attaque]] critique en [[Cybersecurity|cybersécurité]], car une compromission à ce niveau peut entraîner des [[DenialOfService|dénis de service]], des [[DataTheft|vols de données]] ou un [[UnauthorizedAccess|accès non autorisé]] via la manipulation du [[NetworkTrafficAnalysis|trafic]] ou de l'[[IPAddressing|adressage]]. La sécurisation de cette couche est donc essentielle pour la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[Data|informations]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocol|Protocole Internet (IP)]]
*   [[InternetProtocolVersion4|Internet Protocol version 4 (IPv4)]]
*   [[InternetProtocolVersion6|Internet Protocol version 6 (IPv6)]]
*   [[Routing|Routage]]
*   [[Router|Routeur]]
*   [[RoutingTable|Table de routage]]
*   [[Packet|Paquet]]
*   [[Encapsulation|Encapsulation]]
*   [[Decapsulation|Décapsulation]]
*   [[TransportLayer|Couche Transport]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[DistributedDenialOfService|Attaque par Déni de Service Distribué (DDoS)]]
*   [[IPSpoofing|Usurpation d'adresse IP (IP Spoofing)]]
*   [[RoutingTablePoisoning|Empoisonnement des tables de routage]]
*   [[PacketSniffing|Reniflage de paquets]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]]
*   [[Firewall|Pare-feu]]
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel (VLAN)]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[VirtualPrivateNetwork|Réseau Privé Virtuel (VPN)]]
*   [[SecureRoutingProtocols|Protocoles de routage sécurisés]]
*   [[Authentication|Authentification]]
*   [[IPFragmentation|Fragmentation IP]]
*   [[MaximumTransmissionUnit|Maximum Transmission Unit (MTU)]]
*   [[BorderGatewayProtocolSecurity|BGPsec]]