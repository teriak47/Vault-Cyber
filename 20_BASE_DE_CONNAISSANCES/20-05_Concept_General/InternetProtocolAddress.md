---
tags:
  - adresse-ip
  - reseau/adressage
  - ipv4
  - ipv6
aliases:
  - Adresse IP
  - IP Address
  - Adresse Internet Protocol
  - IP
archetype: concept-general
couche_osi: Internet Layer | Couche Internet (3)
rfc:
  - RFC 791 (IPv4)
  - RFC 8200 (IPv6)
  - RFC 1918 (Adresses Privées IPv4)
cssclasses:
  - max
---

# Adresse IP (Internet Protocol Address)

> [!info] Carte d'Identité
> * **Rôle Principal** : Identification et localisation unique d'un dispositif sur un [[Network|réseau]] [[InternetProtocol|IP]].
> * **Couche OSI** : [[InternetLayer|Couche Internet (3)]]
> * **Versions** : [[InternetProtocolVersion4|IPv4]], [[InternetProtocolVersion6|IPv6]]

Une [[InternetProtocolAddress|adresse IP]] est un identifiant numérique attribué à chaque dispositif connecté à un [[Network|réseau]] informatique qui utilise le [[InternetProtocol|Protocole Internet]] pour la [[NetworkCommunication|communication]]. Elle permet aux appareils de se trouver et de communiquer entre eux sur un [[Network|réseau]] local ou sur l'[[Internet|Internet]].

## 🌐 Versions Principales

### [[InternetProtocolVersion4|IPv4]]
La version 4 du [[InternetProtocol|Protocole Internet]] utilise des adresses de 32 bits, généralement représentées sous forme de quatre nombres décimaux (octets) séparés par des points (ex: 192.168.1.1). Le nombre limité d'adresses [[InternetProtocolVersion4|IPv4]] (environ 4,3 milliards) a mené à son épuisement progressif.

#### Structure [[InternetProtocolVersion4|IPv4]]
Une adresse [[InternetProtocolVersion4|IPv4]] se compose de deux parties : la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]]. Le masque de sous-réseau ou le [[ClasslessInterDomainRouting|CIDR]] (`/préfixe`) détermine quelle portion de l'adresse appartient au [[NetworkAddress|réseau]] et quelle portion est dédiée à l'[[HostAddress|hôte]].

### [[InternetProtocolVersion6|IPv6]]
La version 6 du [[InternetProtocol|Protocole Internet]] a été développée pour résoudre le problème d'épuisement des adresses [[InternetProtocolVersion4|IPv4]]. Elle utilise des adresses de 128 bits, offrant un nombre quasi illimité d'adresses uniques. Les adresses [[InternetProtocolVersion6|IPv6]] sont représentées sous forme de huit groupes de quatre [[HexadecimalValues|valeurs hexadécimales]] (appelés [[Hextet|hextets]]) séparés par des deux-points, avec la possibilité d'utiliser le [[DoubleColon|double-colon]] pour compresser les séquences de zéros.

## 🏷️ Types d'Adresses IP

*   **[[PublicIPAddress|Adresses Publiques]]** : Attribuées par les [[InternetServiceProvider|FAI]] (Fournisseurs d'Accès Internet), elles sont [[RoutableInternetAddress|routables]] sur l'[[Internet|Internet]] et uniques à l'échelle mondiale.
*   **[[PrivateIPAddress|Adresses Privées]]** : Réservées à une utilisation dans les [[InternalNetwork|réseaux internes]] (LAN), elles ne sont pas routables sur l'[[Internet|Internet]]. Des plages spécifiques sont définies par la [[InternetAssignedNumbersAuthority|IANA]] (ex: 192.168.0.0/16, 10.0.0.0/8).
*   **[[StaticIPAddressing|Adresses Statiques]]** : Attribuées manuellement à un dispositif et ne changent pas, idéales pour les [[Server|serveurs]] ou les [[NetworkPrinter|imprimantes réseau]].
*   **[[DynamicHostConfigurationProtocol|Adresses Dynamiques]]** : Attribuées automatiquement par un [[DHCPServer|serveur DHCP]] pour une durée limitée, courantes pour les [[Client|clients]] (ordinateurs, smartphones).
*   **[[LoopbackAddress|Adresses de Bouclage]]** : Utilisées pour tester le [[Network|réseau]] local de l'appareil (ex: 127.0.0.1 pour [[InternetProtocolVersion4|IPv4]], ::1 pour [[InternetProtocolVersion6|IPv6]]).
*   **[[LinkLocalAddress|Adresses Link-Local]]** : Adresses auto-configurées pour la communication sur un seul segment de [[LocalAreaNetwork|LAN]], sans l'aide d'un [[DHCPServer|serveur DHCP]] ou d'un [[Router|routeur]] (ex: [[AutomaticPrivateIPAddressing|APIPA]] pour [[InternetProtocolVersion4|IPv4]], fe80::/10 pour [[InternetProtocolVersion6|IPv6]]).
*   **[[BroadcastAddress|Adresses de Diffusion]]** ([[InternetProtocolVersion4|IPv4]] uniquement) : Utilisées pour envoyer des messages à tous les hôtes d'un [[BroadcastDomain|segment réseau]].
*   **[[Multicast|Adresses de Multidiffusion]]** : Utilisées pour envoyer des données à un groupe spécifique d'hôtes simultanément.

## 🛡️ Sécurité et Adresses IP

> [!danger] Risques et Mesures
> *   **[[IPSpoofing|Usurpation d'IP]]** : Un attaquant forge l'[[InternetProtocolAddress|adresse IP]] source d'un paquet pour se faire passer pour un autre dispositif. Peut être utilisé dans les [[DenialOfService|attaques par déni de service]].
> *   **Suivi et Confidentialité** : L'[[InternetProtocolAddress|adresse IP publique]] peut être utilisée pour identifier la localisation géographique d'un [[User|utilisateur]] ou suivre son activité en ligne, soulevant des préoccupations de [[PrivacyInvasion|confidentialité]].
> *   **[[NetworkAddressTranslation|NAT]]** : Bien que principalement conçue pour économiser des adresses [[InternetProtocolVersion4|IPv4]], la [[NetworkAddressTranslation|NAT]] agit comme une forme rudimentaire de [[Firewall|pare-feu]], masquant les [[PrivateIPAddress|adresses IP privées]] du [[InternalNetwork|réseau interne]] aux entités externes.

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|Protocole de résolution d'adresse (ARP)]]
*   [[DomainNameSystem|Système de Noms de Domaine (DNS)]]
*   [[InternetProtocolAddressBlocks|Blocs d'adresses IP]]
*   [[NetworkAddress|Adresse Réseau]]
*   [[HostAddress|Adresse d'Hôte]]
*   [[DefaultGateway|Passerelle par défaut]]