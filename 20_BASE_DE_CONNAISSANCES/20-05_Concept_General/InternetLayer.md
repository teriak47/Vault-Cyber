---
tags:
aliases:
  - Couche Internet
  - Internet Layer
  - Couche Réseau
archetype: concept-general
rfc:
cssclasses:
  - max
source:
  - ComparaisonModeleOsiEtModeleTcpip_Cour
  - ProtocolStacksAndReferenceModels_Cour
---

# Couche Internet

## 🎯 Rôle et Couche OSI
> La [[InternetLayer|couche Internet]] est une abstraction fondamentale de la [[InternetProtocolSuite|suite de protocoles TCP/IP]], responsable de l'adressage logique et du [[Routing|routage]] des [[Packet|paquets]] de données entre différents [[InterconnectedNetworks|réseaux interconnectés]]. Elle est l'équivalent fonctionnel de la [[NetworkLayer|couche réseau]] du [[OpenSystemsInterconnectionModel|modèle OSI]].

## ⚙️ Fonctionnement
1.  **Adressage Logique**: Utilise les [[InternetProtocol|adresses IP]] ([[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]) pour identifier de manière unique les [[Host|hôtes]] sur un [[Network|réseau]] et permettre leur [[Routing|routage]]. Contrairement aux [[MediaAccessControlAddress|adresses MAC]] qui sont physiques et utilisées à la [[DataLinkLayer|couche liaison de données]], les [[InternetProtocol|adresses IP]] sont logiques et peuvent changer en fonction du réseau.
2.  **Routage des [[Packet|Paquets]]**: Les [[Router|routeurs]] opèrent à cette couche pour transférer les [[Packet|paquets]] de la source à la destination en se basant sur les [[RoutingTable|tables de routage]].
3.  **[[InternetProtocol|Protocole IP]]**: C'est le protocole principal de cette couche. Il gère l'[[Encapsulation|encapsulation]] des données des couches supérieures dans des [[Packet|paquets]] IP, leur adressage, et leur fragmentation/réassemblage si nécessaire pour traverser différents médias.
4.  **Protocoles auxiliaires**:
    *   **[[InternetControlMessageProtocol|ICMP]]**: Un protocole auxiliaire utilisé pour envoyer des messages d'erreur et des informations opérationnelles (ex: diagnostic de connectivité).
    *   **[[ICMPv6|ICMPv6]]**: Pour [[InternetProtocolVersion6|IPv6]], il inclut des fonctionnalités supplémentaires comme le [[NeighborDiscoveryProtocol|NDP]] pour la résolution d'adresses et la découverte de routeurs.
*   **Ports par défaut**: La [[InternetLayer|couche Internet]] elle-même ne travaille pas avec des [[PortNumber|numéros de port]], qui sont gérés par la [[TransportLayer|couche de transport]].

## 🛡️ Sécurité de la Couche Internet
*   **Vulnérabilités connues**:
    *   [[Spoofing|Usurpation d'adresse IP]] (IP spoofing), où un [[ThreatActor|attaquant]] falsifie l'[[InternetProtocol|adresse IP]] source d'un [[Packet|paquet]] pour masquer son identité ou contourner les contrôles de [[Security|sécurité]].
    *   [[DenialOfService|Attaques par déni de service (DoS)]] et [[DistributedDenialOfService|DDoS]] qui ciblent la [[Availability|disponibilité]] du réseau en saturant les [[Router|routeurs]] ou les liens réseau avec un [[NetworkTrafficAnalysis|trafic]] malveillant.
    *   [[PacketSniffing|Capture de paquets]] pour intercepter des informations sensibles transitant par le réseau, si les [[Packet|paquets]] ne sont pas [[Encryption|chiffrés]] par les couches supérieures.
    *   [[RoutingAttack|Attaques de routage]] visant à manipuler les [[RoutingTable|tables de routage]] pour rediriger le trafic ou causer des [[ServiceDisruption|interruptions de service]].
*   **Mesures de protection**:
    *   Déploiement de [[Firewall|pare-feu]] pour contrôler le trafic entrant et sortant et filtrer les [[Packet|paquets]] en fonction des [[InternetProtocol|adresses IP]] et d'autres critères.
    *   Mise en œuvre de la [[NetworkSegmentation|segmentation réseau]] (par exemple, via [[VirtualLocalAreaNetwork|VLAN]]) pour isoler les différentes parties du réseau et limiter la propagation des attaques.
    *   Utilisation de systèmes [[IntrusionDetectionSystem|IDS]] et [[IntrusionPreventionSystem|IPS]] pour détecter et prévenir les activités malveillantes ciblant cette couche.
    *   Configuration de [[SecureRoutingProtocols|protocoles de routage sécurisés]] pour empêcher la falsification des [[RoutingTable|tables de routage]].
    *   [[Encryption|Chiffrement]] du trafic au niveau des couches supérieures (ex: [[TransportLayerSecurity|TLS]], [[VirtualPrivateNetwork|VPN]]) pour protéger la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des données.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocolSuite|Suite de Protocoles Internet]]
*   [[InternetProtocol|Protocole Internet]]
*   [[Router|Routeur]]
*   [[InternetControlMessageProtocol|ICMP]]
*   [[ICMPv6|ICMPv6]]
*   [[NeighborDiscoveryProtocol|NDP]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[VirtualPrivateNetwork|VPN]]
---