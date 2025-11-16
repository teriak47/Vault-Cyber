---
tags:
  - adressage
  - reseau
  - ipv4
aliases:
  - Adresse IP de Destination IPv4
  - Destination IPv4 Address
  - Destination IP Address
  - Destination Internet Protocol Version 4 Address
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Adresse IP de Destination IPv4

## 🎯 Rôle et Couche OSI
> L'[[InternetProtocol|adresse IP]] de destination [[InternetProtocolVersion4|IPv4]] est l'identifiant numérique unique du [[Host|système final]] destiné à recevoir un [[Packet|paquet]] de [[Data|données]] au sein d'un [[InternetProtocolVersion4|réseau IPv4]]. Elle opère principalement à la [[NetworkLayer|couche Réseau]] du [[InternetProtocolSuite|modèle TCP/IP]], responsable de l'[[IPAddressing|adressage logique]] et du [[Routing|routage]] inter-réseaux.

## ⚙️ Fonctionnement
1.  **Identification du destinataire**: Chaque [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] contient une [[SourceInternetProtocolVersion4Address|adresse IP source]] et une adresse IP de destination. Cela permet aux [[NetworkDevice|périphériques réseau]] et aux [[Router|routeurs]] d'acheminer le [[Packet|paquet]] vers son récepteur final.
2.  **Rôle des [[Router|routeurs]]**: Les [[Router|routeurs]] examinent l'adresse IP de destination dans l'[[Header|en-tête]] du [[Packet|paquet]] pour déterminer le chemin optimal à travers l'[[Internet|Internet]] ou un [[CorporateNetwork|réseau d'entreprise]], en utilisant leur [[RoutingTable|table de routage]].
3.  **Types d'[[IPAddressing|adressage]]**: L'adresse de destination peut prendre différentes formes pour cibler :
    *   **[[Unicast|Unidiffusion]]**: Un seul destinataire spécifique.
    *   **[[Multicast|Multidiffusion]]**: Un groupe de destinataires spécifiques.
    *   **[[Broadcast|Diffusion]]**: Tous les destinataires sur un [[NetworkSegment|segment de réseau]] donné.
4.  **[[Encapsulation|Encapsulation]] et [[Decapsulation|décapsulation]]**: Lors de la [[DataTransmission|transmission]] des [[Data|données]], le [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] avec son adresse de destination est [[Encapsulation|encapsulé]] dans une [[EthernetFrame|trame Ethernet]] (ou équivalent) à la [[DataLinkLayer|couche Liaison de Données]]. L'adresse de destination est lue et traitée lors de la [[Decapsulation|décapsulation]] à chaque saut de [[Router|routeur]] pour un routage correct.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[Spoofing|Usurpation]] d'adresse IP (IP Spoofing) : Un [[ThreatActor|attaquant]] peut falsifier l'[[SourceInternetProtocolVersion4Address|adresse IP source]] pour masquer son [[UserIdentity|identité]] ou diriger des réponses vers une autre [[Host|cible]].
    *   [[DenialOfService|Attaques par déni de service]] (DoS) et [[DistributedDenialOfService|attaques par déni de service distribué]] ([[DistributedDenialOfService|DDoS]]) : L'envoi de vastes volumes de [[Packet|paquets]] avec des adresses de destination légitimes peut submerger un [[Server|serveur]] ou un [[Network|réseau]], provoquant une [[ServiceDisruption|interruption de service]].
    *   [[Eavesdropping|Écoute clandestine]] : Si le [[Routing|routage]] est compromis, des [[Packet|paquets]] destinés à une [[Host|cible]] légitime peuvent être redirigés ou interceptés par un [[ThreatActor|attaquant]].
*   **Mesures de protection**:
    *   **[[Firewall|Pare-feux]]**: Configurer des [[Firewall|pare-feux]] pour filtrer le [[NetworkTrafficAnalysis|trafic]] entrant et sortant en fonction des adresses IP de destination autorisées.
    *   **[[NetworkSegmentation|Segmentation réseau]]**: Utiliser des [[VirtualLocalAreaNetwork|VLAN]] et d'autres méthodes de [[NetworkSegmentation|segmentation réseau]] pour isoler les [[OnlineServices|services]] et réduire la [[AttackSurface|surface d'attaque]].
    *   **[[IntrusionPreventionSystem|Systèmes de prévention d'intrusion]] ([[IntrusionPreventionSystem|IPS]])**: Déployer des [[IntrusionPreventionSystem|IPS]] pour détecter et bloquer le [[Malware|trafic malveillant]] basé sur l'analyse des adresses de destination et du comportement.
    *   **[[SecureRoutingProtocols|Protocoles de routage sécurisés]]**: Implémenter des [[SecureRoutingProtocols|protocoles de routage sécurisés]] pour prévenir les modifications non autorisées des [[RoutingTable|tables de routage]] et les redirections de [[NetworkTrafficAnalysis|trafic]] malveillantes.
    *   **[[AccessLayer|Contrôles au niveau de la couche d'accès réseau]]**: Mettre en œuvre le [[PortSecurity|filtrage de ports]] et d'autres [[SecurityControl|contrôles]] sur les [[NetworkSwitch|commutateurs réseau]] pour empêcher les [[MACSpoofing|usurpations d'adresses MAC]] et IP.

## 🔗 Notes Connexes
*   [[SourceInternetProtocolVersion4Address|Adresse IP Source IPv4]]
*   [[InternetProtocol|Adresse IP]]
*   [[InternetProtocolVersion4|Internet Protocol version 4]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Router|Routeur]]
*   [[Packet|Paquet]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[Wireshark|Wireshark]]