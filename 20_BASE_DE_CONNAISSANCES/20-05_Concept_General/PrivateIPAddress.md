---
tags:
  - reseau
  - ip/addressing
aliases:
  - Adresse IP Privée
  - Private IP Address
  - Adresse IP Interne
  - Internal IP Address
archetype: concept-general
rfc:
  - RFC 1918
  - RFC 4193
cssclasses:
  - max
---

# Adresse IP Privée

## 🎯 Rôle et Place dans l'Architecture Réseau
> Une adresse [[InternetProtocol|IP]] privée est un type d'[[IPAddressing|adressage IP]] conçu pour être utilisé exclusivement au sein d'un [[LocalAreaNetwork|réseau local]] (LAN) ou d'un [[InternalNetwork|réseau interne]]. Ces adresses ne sont pas routables sur l'[[Internet|Internet]] public, offrant une isolation native et opérant principalement au niveau de la [[NetworkLayer|couche réseau]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement et Caractéristiques Clés
1.  **Non-Routabilité Publique**: Les paquets de données dont l'adresse [[DestinationInternetProtocolVersion4Address|IP de destination]] est une adresse privée sont bloqués et ne sont pas acheminés par les [[Router|routeurs]] de l'[[Internet|Internet]] public. Cette caractéristique fondamentale assure une première couche de [[Security|sécurité]] et d'[[Isolation|isolation]] pour les [[InternalNetwork|réseaux internes]].
2.  **Réutilisation Globale**: Les mêmes plages d'adresses [[PrivateIPAddress|IP privées]] peuvent être utilisées de manière indépendante et simultanée dans un nombre illimité de [[LocalAreaNetwork|réseaux locaux]] différents sans causer de conflits d'[[IPAddressing|adressage IP]] globaux.
3.  **Plages Réservées pour [[InternetProtocolVersion4|IPv4]] (RFC 1918)**:
    *   Classe A: `10.0.0.0` à `10.255.255.255` (bloc `/8`) - Masque de sous-réseau par défaut: `255.0.0.0`
    *   Classe B: `172.16.0.0` à `172.31.255.255` (bloc `/12`) - Masque de sous-réseau par défaut: `255.255.0.0`
    *   Classe C: `192.168.0.0` à `192.168.255.255` (bloc `/16`) - Masque de sous-réseau par défaut: `255.255.255.0`
4.  **Plages Réservées pour [[InternetProtocolVersion6|IPv6]]**:
    *   [[UniqueLocalAddress|Adresses Uniques Locales (ULA)]]: `fc00::/7` (RFC 4193). Similaires aux [[PrivateIPAddress|adresses IP privées]] [[InternetProtocolVersion4|IPv4]], elles sont utilisées pour la communication locale et ne sont pas routées sur l'[[Internet|Internet]] global.
    *   [[LinkLocalAddress|Adresses Link-Local]]: `fe80::/10`. Utilisées pour la communication au sein d'un même [[NetworkSegment|segment de réseau]], elles sont automatiquement configurées et ne sont pas routables au-delà du lien local.
5.  **Communication Externe**: Pour qu'un [[EndDevices|appareil]] configuré avec une [[PrivateIPAddress|adresse IP privée]] puisse accéder aux [[OnlineServices|services en ligne]] sur l'[[Internet|Internet]], son trafic doit passer par un processus de [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]. Ce [[Process|processus]] est généralement effectué par un [[Router|routeur]] ou un [[Firewall|pare-feu]] situé à la [[Gateway|passerelle]] du [[InternalNetwork|réseau interne]], traduisant l'[[PrivateIPAddress|adresse IP privée]] en une [[PublicIPAddress|adresse IP publique]] routable.

## 🛡️ Sécurité et Bonnes Pratiques
*   **Vulnérabilités associées**:
    *   **[[InsiderThreat|Menaces internes]]**: Bien que les [[PrivateIPAddress|adresses IP privées]] ne soient pas directement accessibles depuis l'extérieur, elles sont la cible principale des [[Threat|menaces]] provenant de l'[[InternalNetwork|intérieur du réseau]] ou d'[[Attack|attaques]] ayant déjà compromis le [[Security|périmètre]].
    *   **[[ConfigurationDrift|Dérive de configuration]] et [[InadvertentExposure|exposition involontaire]]**: Une [[NetworkConfiguration|mauvaise configuration]] du [[NetworkAddressTranslation|NAT]] ou des [[Firewall|règles de pare-feu]] peut entraîner l'[[InadvertentExposure|exposition accidentelle]] de [[Server|serveurs]] ou [[Resource|ressources]] internes à l'[[Internet|Internet]] public, créant ainsi des [[SecurityVulnerabilities|vulnérabilités de sécurité]].
*   **Mesures de Protection / Bonnes Pratiques**:
    *   **[[NetworkSegmentation|Segmentation Réseau]]**: L'utilisation de [[VirtualLocalAreaNetwork|VLANs]] et le [[Subnetting|sous-réseautage]] permettent d'[[Isolation|isoler]] différents groupes d'[[EndDevices|appareils]] et de [[User|utilisateurs]] au sein du [[InternalNetwork|réseau privé]], limitant ainsi la propagation d'[[Malware|logiciels malveillants]] ou d'[[Attack|attaques]].
    *   **[[Firewall|Règles de Pare-feu]]**: Implémenter des [[SecurityControl|contrôles de sécurité]] stricts via des [[Firewall|pare-feu]] pour réguler et filtrer le [[NetworkCommunication|trafic réseau]] entre les différents [[NetworkSegment|segments privés]] et entre le [[InternalNetwork|réseau interne]] et l'[[Internet|Internet]] externe.
    *   **[[SecurityAudit|Audit de Configuration Réseau]]**: Des [[SecurityAudit|audits]] réguliers de la [[NetworkConfiguration|configuration réseau]] sont essentiels pour identifier et corriger toute [[SecurityVulnerabilities|vulnérabilité]] ou [[InadvertentExposure|exposition involontaire]] due à une [[NetworkConfiguration|configuration]] erronée ou obsolète.

## 🔗 Notes Connexes
*   [[PublicIPAddress|Adresse IP Publique]]
*   [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[InternetProtocol|Protocole Internet (IP)]]
*   [[InternetProtocolVersion4|Protocole Internet version 4 (IPv4)]]
*   [[InternetProtocolVersion6|Protocole Internet version 6 (IPv6)]]
*   [[Subnetting|Subdivision de réseau]]
*   [[IPAddressing|Adressage IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[HierarchicalAddressing|Adressage Hiérarchique]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[RoutableInternetAddress|Adresse Internet Routable]]
---