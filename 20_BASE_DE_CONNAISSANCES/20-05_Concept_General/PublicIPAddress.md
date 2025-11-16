---
tags:
  - reseau
  - ip/addressing
aliases:
  - Adresse IP Publique
  - Public IP Address
  - Adresse Internet Routable
  - Routable IP Address
archetype: concept-general
rfc:
source:
cssclasses:
  - max
---

# Adresse IP Publique

## 🎯 Définition et Caractéristiques
> Une [[PublicIPAddress|adresse IP publique]] est une [[InternetProtocol|adresse IP]] globalement unique et [[Routing|routable]] sur l'[[Internet|Internet]]. Elle est utilisée pour identifier un [[NetworkDevice|appareil]] ou un [[Network|réseau]] sur le [[WorldWideWeb|réseau mondial]], permettant ainsi la [[NetworkCommunication|communication directe]] avec des [[OnlineServices|services en ligne]] externes.

## ⚙️ Fonctionnement et Attributions
Les [[PublicIPAddress|adresses IP publiques]] sont essentielles pour la connectivité [[Internet|Internet]] et le [[Routing|routage]] des [[Packet|paquets]] de [[Data|données]].

1.  **Globalement Unique**: Chaque [[PublicIPAddress|adresse IP publique]] est unique à l'échelle de l'[[Internet|Internet]] à un moment donné, évitant les conflits d'[[IPAddressing|adressage]].
2.  **Attribution**: Elles sont généralement attribuées par les [[InternetServiceProvider|Fournisseurs d'Accès Internet]] ([[InternetServiceProvider|FAI]]) à un [[Router|routeur]] ou un [[Server|serveur]] en amont du [[HomeNetwork|réseau domestique]] ou du [[CorporateNetwork|réseau d'entreprise]].
3.  **Accessibilité**: Elles permettent à un [[Host|hôte]] ou à un [[Network|réseau]] d'être directement accessible depuis n'importe quel point de l'[[Internet|Internet]], ce qui est crucial pour héberger des [[WebServer|serveurs web]], des [[FileServer|serveurs de fichiers]] ou d'autres [[OnlineServices|services en ligne]].
4.  **Types**: Une [[PublicIPAddress|adresse IP publique]] peut être:
    *   **[[StaticIPAddressing|Statique]]**: Une adresse fixe qui ne change pas, souvent utilisée pour les [[Server|serveurs]] ou les [[NetworkDevice|périphériques réseau]] nécessitant une identification constante.
    *   **[[DynamicHostConfigurationProtocol|Dynamique]]**: Une adresse allouée temporairement par un [[DHCPServer|serveur DHCP]] et qui peut changer périodiquement.
5.  **Distinction avec les adresses privées**: Contrairement aux [[PrivateIPAddress|adresses IP privées]], qui sont utilisées au sein d'un [[LocalAreaNetwork|LAN]] et ne sont pas [[Routing|routables]] sur l'[[Internet|Internet]], les [[PublicIPAddress|adresses IP publiques]] sont directement exposées au [[WorldWideWeb|réseau mondial]].

## 🛡️ Implications de Sécurité
L'exposition d'une [[PublicIPAddress|adresse IP publique]] rend les [[System|systèmes]] et [[Network|réseaux]] potentiellement visibles et accessibles à tous les [[ThreatActor|acteurs de menace]] sur l'[[Internet|Internet]].

*   **Risques et Menaces Associés**:
    *   [[DistributedDenialOfService|Attaques par déni de service distribué]] ([[DistributedDenialOfService|DDoS]]) visant à saturer la [[Bandwidth|bande passante]] ou les [[Resource|ressources]] du [[Server|serveur]] ou du [[Network|réseau]] ciblé.
    *   [[PortScanning|Scans de ports]] et [[Reconnaissance|tentatives de reconnaissance]] pour découvrir les services actifs et les [[SoftwareVulnerability|vulnérabilités logicielles]] potentielles.
    *   [[InformationLeakage|Fuite d'informations]] via des services mal configurés ou des [[SoftwareBugs|bugs logiciels]] sur les [[Server|serveurs]] exposés.
    *   [[Exploitation|Exploitation]] de [[SoftwareVulnerability|vulnérabilités logicielles]] sur les [[Server|serveurs]] ou [[NetworkDevice|périphériques réseau]] accessibles publiquement.
    *   [[BruteForceAttack|Attaques par force brute]] sur les [[Login|mécanismes d'authentification]] des services exposés.

*   **Mesures de Protection et Bonnes Pratiques**:
    *   Implémenter un [[Firewall|pare-feu]] robuste pour contrôler et filtrer le [[NetworkCommunication|trafic réseau]] entrant et sortant, en n'autorisant que les connexions légitimes et nécessaires.
    *   Utiliser la [[NetworkAddressTranslation|Traduction d'Adresses Réseau]] ([[NetworkAddressTranslation|NAT]]) pour masquer les [[PrivateIPAddress|adresses IP privées]] du [[InternalNetwork|réseau interne]] et n'exposer que les [[Server|serveurs]] ou [[SoftwareApplication|applications]] spécifiques via le [[Firewall|pare-feu]].
    *   Déployer un [[VirtualPrivateNetwork|VPN]] pour [[Encryption|chiffrer]] le [[DataTransmission|transfert de données]] et sécuriser l'[[RemoteNetwork|accès distant]] aux [[Resource|ressources]] internes.
    *   Assurer la [[PatchManagement|gestion des patchs]] et les mises à jour régulières de tous les [[OperatingSystem|systèmes d'exploitation]], [[Software|logiciels]] et [[Firmware|micrologiciels]] des [[NetworkDevice|périphériques réseau]] exposés publiquement.
    *   Désactiver les [[NetworkProtocol|protocoles]] et [[OnlineServices|services en ligne]] inutiles ou non essentiels sur les [[Host|hôtes]] avec des [[PublicIPAddress|adresses IP publiques]] afin de réduire la [[AttackSurface|surface d'attaque]].
    *   Appliquer le [[PrincipleOfLeastPrivilege|principe du moindre privilège]] pour tous les [[User|utilisateurs]] et [[Process|processus]] accédant ou étant exposés publiquement.

## 🔗 Notes Connexes
*   [[PrivateIPAddress|Adresse IP Privée]]
*   [[NetworkAddressTranslation|NAT]]
*   [[InternetProtocol|Protocole Internet]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[IPAddressing|Adressage IP]]
*   [[RoutableInternetAddress|Adresse Internet Routable]]