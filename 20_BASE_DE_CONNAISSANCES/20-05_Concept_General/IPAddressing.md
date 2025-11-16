---
tags:
aliases:
  - Adressage IP
  - IP Addressing
  - Gestion des Adresses IP
  - IPAM
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage IP

## 📥 Définition en une phrase
> L'[[IPAddressing|Adressage IP]] est le processus fondamental d'attribution et de gestion des [[InternetProtocol|adresses IP]] aux [[EndDevices|appareils]] connectés à un [[Network|réseau]], leur permettant une [[NetworkCommunication|communication]] unique et [[Routing|routable]].

## 🧠 Concepts Clés / Piliers
*   **Identifiants Logiques**: Les [[InternetProtocol|adresses IP]] sont des identifiants numériques logiques qui désignent de manière unique un [[Host|hôte]] ou une [[NetworkInterface|interface réseau]] au sein d'un [[Network|réseau]] [[InternetProtocol|IP]].
*   **Versions**: Il existe deux versions principales : [[InternetProtocolVersion4|IPv4]] (32 bits, ex: 192.168.1.1) et [[InternetProtocolVersion6|IPv6]] (128 bits, ex: 2001:0db8::1), chacune avec ses propres formats et capacités.
*   **Segmentation et Sous-réseautage**: Chaque [[InternetProtocol|adresse IP]] est associée à un [[SubnetMask|masque de sous-réseau]] qui délimite la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]] de l'adresse, une notion essentielle pour le [[Subnetting|sous-réseautage]] et la [[NetworkSegmentation|segmentation réseau]].
*   **Méthodes d'Attribution**: Les [[InternetProtocol|adresses IP]] peuvent être attribuées de manière [[StaticIPAddressing|statique]] (manuellement) pour une configuration fixe ou [[DynamicHostConfigurationProtocol|dynamiquement]] via un [[DynamicHostConfigurationProtocol|serveur DHCP]] pour une gestion automatisée.
*   **Routage**: L'[[IPAddressing|adressage IP]] est le pilier du [[Routing|routage]] des [[Packet|paquets de données]] entre différents [[InterconnectedNetworks|réseaux interconnectés]] grâce à des [[Router|routeurs]] et des [[Gateway|passerelles]].

## 💡 Importance en Cybersécurité
> L'[[IPAddressing|adressage IP]] est un élément fondamental de la [[NetworkSecurity|sécurité réseau]] car il est la base de toute [[NetworkCommunication|communication]]. Sa gestion appropriée est cruciale pour prévenir et détecter les [[DigitalAttack|attaques numériques]]. Une mauvaise configuration ou une exploitation des vulnérabilités liées à l'adressage IP peut mener à des [[UnauthorizedAccess|accès non autorisés]], à des [[DenialOfService|dénis de service]] et à la [[DataTheft|fuite de données]]. La [[NetworkSegmentation|segmentation réseau]] basée sur l'adressage IP permet d'isoler les [[System|systèmes]] critiques et de contenir les [[Attack|attaques]], tandis que la [[SecurityMonitoring|surveillance]] active des [[Log|journaux]] d'adresses IP est indispensable pour la [[IncidentResponse|réponse aux incidents]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Protocole Internet]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[Subnetting|Sous-réseautage]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[DomainNameSystem|Système de Noms de Domaine]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[NetworkLayer|Couche Réseau]]
*   [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]
*   [[Router|Routeur]]
*   [[Firewall|Pare-feu]]
*   [[Spoofing|Usurpation d'adresse IP]]
*   [[DenialOfService|Attaque par déni de service]]
*   [[NetworkMonitoring|Scans de réseau]]
*   [[AccessControl|Contrôle d'accès]]
*   [[DHCPSnooping|DHCP Snooping]]