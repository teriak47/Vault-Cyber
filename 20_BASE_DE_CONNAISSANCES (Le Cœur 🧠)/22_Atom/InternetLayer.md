---
tags:
  - ip-encapsulation
  - ipv6-neighbor-discovery
  - reseau/couche-reseau
  - reseau/adressage
  - securite/pare-feu
aliases:
  - Couche Internet
  - Internet Layer
source:
  - ComparaisonModeleOsiEtModeleTcpip_Cour
  - ProtocolStacksAndReferenceModels_Cour
cssclasses:
  - max
---

# Couche Internet

## 📥 Définition en une phrase
> La couche Internet est une abstraction dans la [[InternetProtocolSuite|suite de protocoles TCP/IP]] qui est responsable de l'adressage logique et du routage des [[Packet|paquets]] de données à travers différentes [[InterconnectedNetworks|réseaux interconnectés]].

## 🧠 Concepts Clés / Fonctionnement
*   **Adresage Logique**: Utilise les [[InternetProtocolAddress|adresses IP]] ([[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]) pour identifier de manière unique les hôtes sur un [[Network|réseau]] et permettre le routage. Contrairement aux [[MediaAccessControlAddress|adresses MAC]] qui sont physiques, les adresses IP sont logiques et peuvent changer en fonction du réseau.
*   **Routage des [[Packet|Paquets]]**: Les [[Router|routeurs]] opèrent à cette couche pour transférer les [[Packet|paquets]] de la [[SourceMacAddress|source]] à la [[DestinationMacAddress|destination]] en se basant sur les [[RoutingTable|tables de routage]].
*   **Protocole IP**: Le [[InternetProtocol|Protocole Internet]] est le protocole principal de cette couche, gérant l'[[Encapsulation|encapsulation]] des données des couches supérieures dans des [[Packet|paquets]] IP, leur adressage et leur fragmention/réassemblage si nécessaire.
*   **[[InternetControlMessageProtocol|ICMP]]**: Un protocole auxiliaire utilisé pour envoyer des messages d'erreur et des informations opérationnelles, par exemple, lorsqu'un [[Packet|paquet]] ne peut pas atteindre sa destination. Pour [[InternetProtocolVersion6|IPv6]], [[ICMPv6|ICMPv6]] inclut des fonctionnalités comme le [[NeighborDiscoveryProtocol|NDP]].

## 🛡️ Risques / Menaces Associés
*   [[SpoofingAttack|Usurpation d'adresse IP]] (IP spoofing), où un attaquant falsifie l'[[InternetProtocolAddress|adresse IP]] source d'un [[Packet|paquet]] pour masquer son identité ou contourner les contrôles de [[Security|sécurité]].
*   [[DenialOfService|Attaques par déni de service (DoS)]] et [[DistributedDenialOfService|DDoS]] qui ciblent la disponibilité du réseau en saturant les [[Router|routeurs]] ou les liens réseau avec un trafic malveillant.
*   [[PacketSniffing|Capture de paquets]] pour intercepter des informations sensibles transitant par le réseau, si les [[Packet|paquets]] ne sont pas [[Encryption|chiffrés]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Déploiement de [[Firewall|pare-feu]] pour contrôler le trafic entrant et sortant et filtrer les [[Packet|paquets]] en fonction des [[InternetProtocolAddress|adresses IP]] et des [[PortNumber|numéros de port]].
*   Mise en œuvre de la [[NetworkSegmentation|segmentation réseau]] pour isoler les différentes parties du réseau et limiter la propagation des attaques.
*   Utilisation de systèmes [[IntrusionDetectionSystem|IDS]] et [[IntrusionPreventionSystem|IPS]] pour détecter et prévenir les activités malveillantes ciblant cette couche.
*   Configuration de [[SecureRoutingProtocols|protocoles de routage sécurisés]] pour empêcher la falsification des [[RoutingTable|tables de routage]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocolSuite|Suite de Protocoles Internet]]
*   [[InternetProtocol|Protocole Internet]]
*   [[Router|Routeur]]