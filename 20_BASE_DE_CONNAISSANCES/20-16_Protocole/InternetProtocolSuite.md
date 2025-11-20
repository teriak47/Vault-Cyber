---
tags:
  - protocole
  - protocole/tcp-ip
aliases:
  - Suite de Protocoles Internet
  - TCP/IP Stack
  - Protocoles TCP/IP
  - TCP/IP
  - Transmission Control Protocol/Internet Protocol
  - Pile de protocoles TCP/IP
  - Internet Protocol Suite
archetype: protocole
cssclasses:
  - max
---

# Suite de Protocoles Internet (TCP/IP)

> [!info] Carte d'Identité
> * **Couche OSI** : Modèle à 4 couches (correspondant aux couches 1 à 7 du [[OpenSystemsInterconnectionModel|Modèle OSI]])
> * **Port par défaut** : `N/A`
> * **Transport** : [[TransmissionControlProtocol|TCP]] / [[UserDatagramProtocol|UDP]]

## 🎯 Principe Fondamental
La Suite de Protocoles Internet, communément appelée TCP/IP, est un ensemble de [[NetworkProtocol|protocoles]] de [[NetworkCommunication|communication réseau]] qui constitue la base technique de l'[[Internet|Internet]] et de la plupart des réseaux informatiques modernes. Son objectif principal est de permettre la [[Communication|communication]] et l'échange de [[Data|données]] entre des hôtes hétérogènes, quel que soit leur [[Hardware|matériel]] ou leur [[OperatingSystem|système d'exploitation]] sous-jacent.

## 🧩 Composants / Éléments Clés
Le modèle TCP/IP est traditionnellement structuré en quatre [[Layer|couches]], chacune ayant des responsabilités spécifiques :

*   **[[ApplicationLayer|Couche Application]]**: Elle fournit des [[NetworkService|services de réseau]] aux [[SoftwareApplication|applications]] et gère les [[ApplicationData|données]] de l'utilisateur. Des [[Protocol|protocoles]] comme le [[HypertextTransferProtocol|HTTP]] (pour le World Wide Web), le [[FileTransferProtocol|FTP]] (pour le transfert de fichiers) et le [[DomainNameSystem|DNS]] (pour la résolution de noms) résident à ce niveau.
*   **[[TransportLayer|Couche Transport]]**: Responsable de la communication de bout en bout entre les applications. Les principaux protocoles sont le [[TransmissionControlProtocol|TCP]] (fiable, orienté connexion) et l'[[UserDatagramProtocol|UDP]] (sans connexion, rapide).
*   **[[InternetLayer|Couche Internet]]**: Gère l'[[IPAddressing|adressage logique]] et le [[Routing|routage]] des [[Packet|paquets]] de [[Data|données]] à travers les [[InterconnectedNetworks|réseaux interconnectés]]. Le [[InternetProtocol|Protocole Internet (IP)]] est le [[Protocol|protocole]] central de cette [[Layer|couche]], avec ses versions [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]].
*   **[[NetworkAccessLayer|Couche d'Accès Réseau]]**: Combine les fonctionnalités des couches physique et liaison de données du [[OpenSystemsInterconnectionModel|Modèle OSI]]. Elle gère les détails spécifiques de l'[[NetworkMedia|accès au support réseau]], tels que l'[[EthernetProtocol|Ethernet]] pour les LAN filaires ou le [[WirelessFidelity|Wi-Fi]] pour les [[WirelessNetwork|réseaux sans fil]], et l'[[MediaAccessControlAddress|adressage MAC]].

## ⚙️ Fonctionnement (Encapsulation et Décapsulation)
La Suite de Protocoles Internet fonctionne sur le principe de l'[[Encapsulation|encapsulation]] et de la [[Decapsulation|décapsulation]]. Lorsqu'une [[Data|donnée]] est envoyée, elle descend les [[Layer|couches]], et chaque couche ajoute son propre [[Header|en-tête]] d'informations de protocole avant d'être transmise. À la réception, le processus inverse se produit (décapsulation).

*   **Flux des Données**: Lors de l'envoi, une [[SoftwareApplication|application]] génère des [[Data|données]] qui traversent séquentiellement les couches de la [[ProtocolStack|pile TCP/IP]] vers le bas. Chaque couche effectue ses opérations spécifiques (ex: segmentation par [[TransmissionControlProtocol|TCP]], ajout d'[[InternetProtocolAddress|adresses IP]]) et ajoute un [[Header|en-tête]] (et parfois un "trailer") à l'unité de [[DataTransmission|donnée]] reçue de la couche supérieure. Ce [[Process|processus]] est appelé [[Encapsulation|encapsulation]]. L'unité encapsulée est ensuite transmise à la couche inférieure.
*   **Transmission Physique**: À la [[NetworkAccessLayer|couche d'Accès Réseau]], les [[Data|données]] sont converties en [[PhysicalStates|signaux physiques]] ([[ElectricalSignals|électriques]], [[OpticalSignals|optiques]], [[WirelessSignals|sans fil]]) et transmises sur le [[NetworkMedia|support réseau]].
*   **Réception et Décapsulation**: Du côté du destinataire, le [[Process|processus]] est inversé. Les [[PhysicalStates|signaux physiques]] sont reçus par la [[NetworkAccessLayer|couche d'Accès Réseau]] et décapsulés couche par couche vers le haut. Chaque couche retire son [[Header|en-tête]] et traite les informations qu'il contient avant de passer le reste du [[Packet|paquet]] à la couche supérieure, jusqu'à ce que les [[Data|données]] originales atteignent l'[[SoftwareApplication|application]] cible.

## 📦 Structure du Paquet (Header)
Chaque [[Layer|couche]] de la Suite de Protocoles Internet ajoute un [[Header|en-tête]] spécifique à la [[Data|donnée]] qu'elle reçoit de la couche supérieure lors du [[Encapsulation|processus d'encapsulation]]. Ces en-têtes contiennent les informations nécessaires au bon fonctionnement du protocole à cette couche (par exemple, [[SourceInternetProtocolVersion4Address|adresses IP]] à la [[InternetLayer|couche Internet]], [[InternetPort|numéros de port]] à la [[TransportLayer|couche Transport]]).

## 🦈 Analyse Wireshark
> [!tip] Filtres Utiles
> Pour analyser le [[NetworkTrafficTypes|trafic réseau]] de la Suite de Protocoles Internet avec [[Wireshark|Wireshark]], vous devez généralement filtrer par des [[NetworkProtocol|protocoles]] spécifiques au sein des couches :
> ```
> # Filtrer par protocole au niveau application (ex: HTTP, DNS)
> http
> dns
>
> # Filtrer par protocole au niveau transport (ex: TCP, UDP)
> tcp
> udp
>
> # Filtrer par protocole au niveau internet (ex: IP, ICMP)
> ip
> icmp
>
> # Filtrer le trafic TCP/IP d'une adresse IP spécifique
> ip.addr == 192.168.1.1
>
> # Filtrer une erreur spécifique (exemple pour TCP)
> tcp.flags.reset == 1
> ```

## 🛡️ Sécurité
> [!danger] Vulnérabilités Connues
> *   **Sniffing** : Par défaut, les [[Data|données]] ne sont pas chiffrées au sein de la Suite de Protocoles Internet. Le chiffrement dépend de [[Protocol|protocoles]] spécifiques de la [[ApplicationLayer|couche Application]] ou de la [[TransportLayer|couche Transport]] (ex: [[HypertextTransferProtocolSecure|HTTPS]], [[TransportLayerSecurity|TLS]]). Les [[Packet|paquets]] peuvent être interceptés en [[Cleartext|clair]] si aucune mesure de [[DataEncryption|chiffrement]] n'est appliquée.
> *   **Spoofing** : Certains [[NetworkProtocol|protocoles]] plus anciens, comme [[InternetProtocolVersion4|IPv4]], ne disposent pas de mécanismes d'[[Authentication|authentification]] robustes pour vérifier l'[[SourceInternetProtocolVersion4Address|adresse source]], les rendant vulnérables au spoofing IP. Le [[TransmissionControlProtocol|TCP]] est également sujet au spoofing TCP et à la prédiction des numéros de séquence, pouvant conduire à des [[ManInTheMiddle|attaques de l'homme du milieu]].

## 🔗 Notes Connexes
*   **Modèle de référence**: [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   **Protocole clé (Transport)**: [[TransmissionControlProtocol|TCP]]
*   **Protocole clé (Internet)**: [[InternetProtocol|IP]]
*   **Mécanisme fondamental**: [[Encapsulation|Encapsulation]]
*   **Protocole d'adressage**: [[DynamicHostConfigurationProtocol|DHCP]]
*   **Version Sécurisée (Transport)** : [[TransportLayerSecurity|TLS]]