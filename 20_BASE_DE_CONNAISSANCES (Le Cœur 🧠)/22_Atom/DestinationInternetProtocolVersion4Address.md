---
tags:
  - adresse-ip-de-destination
  - optimisation-routing
  - paquet-ipv4
  - adressage-ipv4
  - segmentation-reseau
  - firewall
aliases:
  - Adresse IP de Destination IPv4
  - Destination IPv4 Address
  - Destination IP Address
cssclasses:
  - max
---

# Adresse IP de Destination IPv4

## 📥 Définition en une phrase
> L'[[InternetProtocolAddress|adresse IP]] de destination [[InternetProtocolVersion4|IPv4]] est l'identifiant numérique unique du système final (hôte) destiné à recevoir un [[Packet|paquet]] de données au sein d'un [[InternetProtocolVersion4|réseau IPv4]].

## 🧠 Concepts Clés / Fonctionnement
*   **Identification du destinataire :** Chaque [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] contient une [[SourceInternetProtocolVersion4Address|adresse IP source]] et une adresse IP de destination, permettant aux [[NetworkDevice|périphériques réseau]] d'acheminer le paquet vers son récepteur final.
*   **Rôle des [[Router|routeurs]] :** Les [[Router|routeurs]] examinent l'adresse IP de destination dans l'[[Header|en-tête]] du [[Packet|paquet]] pour déterminer le chemin optimal à travers l'[[Internet|Internet]] ou un [[EnterpriseNetwork|réseau d'entreprise]], en utilisant leur [[RoutingTable|table de routage]].
*   **Couche [[NetworkLayer|Réseau]] :** Cette adresse est fondamentale pour le fonctionnement de la [[NetworkLayer|couche Réseau]] du [[TcpIpModel|modèle TCP/IP]], responsable de l'adressage logique et du routage inter-réseaux.
*   **Types d'[[IPAddressing|adressage]] :** L'adresse de destination peut être une [[Unicast|unidiffusion]] (un seul destinataire), une [[Multicast|multidiffusion]] (un groupe de destinataires) ou une [[Broadcast|diffusion]] (tous les destinataires sur un segment de [[Network|réseau]]).
*   **[[Encapsulation|Encapsulation]] et [[Decapsulation|décapsulation]] :** Lors de la [[DataTransmission|transmission]], le [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] avec son adresse de destination est [[Encapsulation|encapsulé]] dans une [[EthernetFrame|trame Ethernet]] (ou équivalent) à la [[DataLinkLayer|couche Liaison de Données]]. L'adresse de destination est lue lors de la [[Decapsulation|décapsulation]] à chaque saut de [[Router|routeur]].

## 🛡️ Risques / Menaces Associés
*   [[SpoofingAttack|Usurpation]] d'adresse IP (IP Spoofing) : Un [[ThreatActor|attaquant]] peut falsifier l'adresse IP source pour masquer son identité ou diriger des réponses vers une autre [[Host|cible]].
*   [[DenialOfService|Attaques par déni de service]] (DoS/[[DistributedDenialOfService|DDoS]]) : L'envoi de vastes volumes de [[Packet|paquets]] avec des adresses de destination légitimes peut submerger un [[Server|serveur]] ou un [[Network|réseau]].
*   [[Eavesdropping|Écoute clandestine]] : Si le routage est compromis, des [[Packet|paquets]] destinés à une [[Host|cible]] légitime peuvent être redirigés ou interceptés par un [[ThreatActor|attaquant]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Firewall|Pare-feux]] :** Configurer des [[Firewall|pare-feux]] pour filtrer le trafic entrant et sortant en fonction des adresses IP de destination autorisées.
*   **[[NetworkSegmentation|Segmentation réseau]] :** Utiliser des [[VirtualLocalAreaNetwork|VLAN]] et d'autres méthodes de [[NetworkSegmentation|segmentation réseau]] pour isoler les services et réduire la [[AttackSurface|surface d'attaque]].
*   **[[IntrusionPreventionSystem|Systèmes de prévention d'intrusion]] (IPS) :** Déployer des [[IntrusionPreventionSystem|IPS]] pour détecter et bloquer le trafic malveillant basé sur l'analyse des adresses de destination et du comportement.
*   **[[SecureRoutingProtocols|Protocoles de routage sécurisés]] :** Implémenter des [[SecureRoutingProtocols|protocoles de routage sécurisés]] pour prévenir les modifications non autorisées des [[RoutingTable|tables de routage]] et les redirections de trafic malveillantes.
*   **[[NetworkAccessLayer|Contrôles au niveau de la couche d'accès réseau]] :** Mettre en œuvre le [[PortSecurity|filtrage de ports]] et d'autres [[SecurityControl|contrôles]] sur les [[NetworkSwitch|commutateurs réseau]] pour empêcher les [[SpoofingAttack|usurpations d'adresses MAC]] et IP.

## 🔗 Notes Connexes
*   [[SourceInternetProtocolVersion4Address|Adresse IP Source IPv4]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[InternetProtocolVersion4|Internet Protocol version 4]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Router|Routeur]]
*   [[Packet|Paquet]]
*   [[TcpIpModel|Modèle TCP/IP]]