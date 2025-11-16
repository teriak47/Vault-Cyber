---
tags:
  - protocole
aliases:
  - Internet Control Message Protocol version 6
  - Protocol de Message de Contrôle Internet version 6
  - ICMPv6
archetype: protocole
rfc: RFC 4443
cssclasses:
  - max
---

# Protocole de Message de Contrôle Internet version 6 (ICMPv6)

## 🎯 Rôle et Couche OSI
> L'[[ICMPv6|ICMPv6]] est un [[Protocol|protocole]] fondamental pour [[InternetProtocolVersion6|IPv6]], opérant à la [[InternetLayer|couche Internet]] ([[NetworkLayer|Couche Réseau]]) du [[InternetProtocolSuite|modèle TCP/IP]]. Son rôle principal est de signaler les erreurs de traitement des [[Packet|paquets]], de fournir des fonctions de [[Testing|diagnostic]] et d'offrir des fonctionnalités essentielles à la gestion du réseau [[InternetProtocolVersion6|IPv6]], telles que la [[NeighborDiscoveryProtocol|découverte de voisins]] et de [[Router|routeurs]].

## ⚙️ Fonctionnement
1.  **Signalement d'erreurs**: [[ICMPv6|ICMPv6]] informe les [[Host|hôtes]] et les [[Router|routeurs]] des problèmes rencontrés lors de la [[DataTransmission|transmission de données]]. Les types de messages d'erreur incluent "Destination Unreachable" (destination inaccessible), "Packet Too Big" (paquet trop grand, lié à la [[PathMTUDiscovery|découverte du MTU de chemin]]), "Time Exceeded" (temps dépassé, pour les boucles ou les paquets expirés) et "Parameter Problem" (problème de paramètre dans l'en-tête [[InternetProtocolVersion6|IPv6]]).
2.  **Fonctions de diagnostic**: Il permet de vérifier la [[NetworkCommunication|connectivité réseau]] entre les [[Host|hôtes]] via les messages "Echo Request" et "Echo Reply", similaires à la commande `ping` d'[[InternetControlMessageProtocol|ICMP pour IPv4]].
3.  **[[NeighborDiscoveryProtocol|Découverte de Voisins (NDP)]]**: Un ensemble crucial de messages [[ICMPv6|ICMPv6]] utilisé pour diverses fonctions locales au [[NetworkSegment|segment réseau]], notamment la [[AddressResolutionProtocol|résolution d'adresses MAC]], la [[DuplicateAddressDetection|détection d'adresses en double]] et la [[RouterDiscovery|découverte de routeurs]]. Les messages [[NeighborDiscoveryProtocol|NDP]] comprennent:
    *   **[[RouterSolicitation|Router Solicitation (RS)]]**: Envoyé par un [[Host|hôte]] pour demander aux [[Router|routeurs]] d'envoyer un [[RouterAdvertisement|Router Advertisement]] immédiatement.
    *   **[[RouterAdvertisement|Router Advertisement (RA)]]**: Envoyé par un [[Router|routeur]] en réponse à un [[RouterSolicitation|RS]] ou périodiquement pour annoncer sa présence, les [[NetworkPrefix|préfixes réseau]] disponibles et d'autres informations de [[NetworkConfiguration|configuration]].
    *   **[[NeighborSolicitation|Neighbor Solicitation (NS)]]**: Utilisé par un [[Host|hôte]] pour déterminer l'[[MediaAccessControlAddress|adresse MAC]] d'un [[Neighbor|voisin]] ou pour détecter une [[DuplicateAddressDetection|adresse en double]].
    *   **[[NeighborAdvertisement|Neighbor Advertisement (NA)]]**: Réponse à un [[NeighborSolicitation|NS]], annonçant l'[[MediaAccessControlAddress|adresse MAC]] de l'[[Host|hôte]] ou du [[Router|routeur]] ciblé.
    *   **[[ICMPv6RedirectMessage|Redirection]]**: Envoyé par un [[Router|routeur]] pour informer un [[Host|hôte]] d'une meilleure route vers une destination spécifique sur le même [[NetworkSegment|segment réseau]].
4.  **[[MulticastListenerDiscovery|Multicast Listener Discovery (MLD)]]**: Gère l'adhésion et le départ des [[Host|hôtes]] aux groupes de [[Multicast|diffusion multilatérale]] sur un [[LocalAreaNetwork|LAN]].
* **Ports par défaut**: [[ICMPv6|ICMPv6]] n'utilise pas de [[PortNumber|numéros de port]] au sens [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]], car il opère à la [[InternetLayer|couche Internet]].

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * [[DenialOfService|Attaques par déni de service (DoS)]]: Une inondation de requêtes [[ICMPv6|ICMPv6]] (ex: Echo Request) peut saturer les ressources d'un [[Host|hôte]] ou d'un [[Network|réseau]].
  * [[Reconnaissance|Reconnaissance]]: Les messages Echo peuvent être utilisés par les [[ThreatActor|acteurs de menace]] pour scanner un [[Network|réseau]] et identifier les [[Host|hôtes]] actifs.
  * [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]]: Le [[NeighborDiscoveryProtocol|NDP]] est vulnérable au [[Spoofing|spoofing]], où un attaquant peut envoyer de fausses [[RouterAdvertisement|RA]] ou [[NeighborAdvertisement|NA]] pour rediriger le [[NetworkTraffic|trafic]].
  * [[AddressSpoofing|Usurpation d'adresse]]: Des messages [[ICMPv6|ICMPv6]] malveillants peuvent tenter de faire passer une [[InternetProtocol|adresse IPv6]] pour une autre.
* **Versions sécurisées**:
  * [[SecureNeighborDiscovery|Secure Neighbor Discovery (SEND)]]: Une extension de sécurité qui utilise la [[Cryptography|cryptographie]] pour protéger le [[NeighborDiscoveryProtocol|NDP]] contre le [[Spoofing|spoofing]] et les [[ManInTheMiddle|attaques MitM]], en assurant l'[[Authentication|authentification]] des messages.

## 🔗 Notes Connexes
* [[InternetProtocolVersion6|Protocole Internet version 6 (IPv6)]]
* [[InternetControlMessageProtocol|Protocole de Message de Contrôle Internet (ICMP) pour IPv4]]
* [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol (NDP)]]
* [[MulticastListenerDiscovery|Multicast Listener Discovery (MLD)]]
* [[RouterSolicitation|Router Solicitation (RS)]]
* [[RouterAdvertisement|Router Advertisement (RA)]]
* [[NeighborSolicitation|Neighbor Solicitation (NS)]]
* [[NeighborAdvertisement|Neighbor Advertisement (NA)]]
* [[ICMPv6RedirectMessage|Redirection (ICMPv6)]]
* [[SecureNeighborDiscovery|Secure Neighbor Discovery (SEND)]]
* [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]]
* [[Wireshark|Wireshark]] (pour l'analyse du trafic [[ICMPv6|ICMPv6]])