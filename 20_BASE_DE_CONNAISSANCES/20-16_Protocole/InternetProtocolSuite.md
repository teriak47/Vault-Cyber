---
tags:
  - protocole
aliases:
  - Suite de Protocoles Internet
  - TCP/IP Stack
  - Protocoles TCP/IP
  - TCP/IP
  - Transmission Control Protocol/Internet Protocol
  - Pile de protocoles TCP/IP
archetype: protocole
rfc:
source:
cssclasses:
  - max
---

# Transmission Control Protocol/Internet Protocol (TCP/IP)

## 🎯 Rôle et Couche OSI
> La [[TransmissionControlProtocol|Suite de Protocoles Internet]] (communément appelée [[TransmissionControlProtocol|TCP/IP]]) est un ensemble fondamental de [[NetworkProtocol|protocoles réseau]] qui constitue l'épine dorsale technique de l'[[Internet]] et de la plupart des [[Network|réseaux informatiques]]. Elle permet la [[NetworkCommunication|communication réseau]] entre des appareils diversifiés en définissant comment les données doivent être formatées, adressées, transmises, acheminées et reçues. Le [[TransmissionControlProtocol|modèle TCP/IP]] est son propre [[ReferenceModel|modèle de référence]] qui opère sur l'ensemble des couches, de la [[NetworkAccessLayer|couche d'accès réseau]] à la [[ApplicationLayer|couche application]].

## ⚙️ Fonctionnement
Le [[TransmissionControlProtocol|modèle TCP/IP]] est organisé en un [[ProtocolStack|pile de protocoles]] à quatre couches, chacune ayant des responsabilités spécifiques :

1.  **Couche d'Accès Réseau ([[NetworkAccessLayer|Network Access Layer]])**:
    *   Combine les fonctions des couches physique et liaison de données du [[OpenSystemsInterconnectionModel|modèle OSI]].
    *   Gère les détails physiques de la [[DataTransmission|transmission de données]] via le [[NetworkMedia|support réseau]] (ex: [[Ethernet]], [[WirelessFidelity|Wi-Fi]]).
    *   Inclut des protocoles comme [[EthernetProtocol|Ethernet]] et [[IEEE80211|802.11]].
2.  **Couche Internet ([[InternetLayer|Internet Layer]])**:
    *   Équivaut à la [[NetworkLayer|couche réseau]] du [[OpenSystemsInterconnectionModel|modèle OSI]].
    *   Responsable de l'[[IPAddressing|adressage]] logique et du [[Routing|routage]] des [[Packet|paquets]] de données à travers les [[InterconnectedNetworks|réseaux interconnectés]].
    *   Le protocole clé est l'[[InternetProtocol|IP]] ([[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]]).
3.  **Couche de Transport ([[TransportLayer|Transport Layer]])**:
    *   Équivaut à la [[TransportLayer|couche transport]] du [[OpenSystemsInterconnectionModel|modèle OSI]].
    *   Assure la [[DataTransmission|transmission de données]] de bout en bout et la gestion des connexions entre les applications sur les [[Host|hôtes]].
    *   Deux protocoles principaux :
        *   **[[TransmissionControlProtocol|TCP]]**: Offre une [[TransmissionControlProtocol|transmission fiable]], ordonnée et avec contrôle d'erreur (connexion orientée). Gère le contrôle de flux et la [[Retransmission|retransmission]].
        *   **[[UserDatagramProtocol|UDP]]**: Fournit un service de [[UserDatagramProtocol|transmission]] sans connexion et non fiable, mais rapide (idéal pour la vidéo, la voix, le [[DomainNameSystem|DNS]]).
4.  **Couche Application ([[ApplicationLayer|Application Layer]])**:
    *   Combine les fonctions des couches session, présentation et application du [[OpenSystemsInterconnectionModel|modèle OSI]].
    *   Fournit des services réseau aux [[SoftwareApplication|applications]] et gère le formatage des données.
    *   Exemples de protocoles : [[HypertextTransferProtocol|HTTP]], [[DomainNameSystem|DNS]], [[FileTransferProtocol|FTP]], [[SecureShell|SSH]], [[Email|SMTP]].

*   **[[Encapsulation|Encapsulation]]/[[Decapsulation|Décapsulation]]**: Lors de l'envoi, chaque couche ajoute ses propres informations d'[[Header|en-tête]] aux données (encapsulation). À la réception, les en-têtes sont progressivement supprimés (décapsulation) par les couches correspondantes.
*   **[[Interoperability|Interopérabilité]]**: L'adhésion aux [[NetworkStandard|normes TCP/IP]] permet à des [[OperatingSystem|systèmes d'exploitation]] et [[Hardware|matériels]] disparates de communiquer efficacement.
*   **Ports par défaut**: Les protocoles de la [[TransmissionControlProtocol|suite TCP/IP]] utilisent divers [[PortNumber|ports par défaut]] selon leur fonction (ex: [[HypertextTransferProtocol|HTTP]] sur TCP/80, [[FileTransferProtocol|FTP]] sur TCP/20 et TCP/21, [[DomainNameSystem|DNS]] sur UDP/53).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[DenialOfService|Attaques par Déni de Service (DoS/DDoS)]]: Peuvent cibler la [[TransportLayer|couche transport]] (ex: TCP SYN Flood) ou la [[NetworkLayer|couche internet]] (ex: [[InternetControlMessageProtocol|ICMP]] Flood) pour saturer les [[Resource|ressources]] et rendre les services inaccessibles.
    *   [[Spoofing|Usurpation d'identité]]: Les [[InternetProtocol|adresses IP]] ou les [[MediaAccessControlAddress|adresses MAC]] peuvent être falsifiées pour masquer l'identité d'un [[ThreatActor|attaquant]] ou rediriger le [[NetworkTrafficAnalysis|trafic]].
    *   [[ManInTheMiddle|Attaques de l'Homme du Milieu (MITM)]]: Exploitation de faiblesses de protocoles comme l'[[AddressResolutionProtocol|ARP]] ou le [[DomainNameSystem|DNS]] pour intercepter et potentiellement modifier les communications.
    *   [[SoftwareVulnerability|Vulnérabilités logicielles]] dans les implémentations: Des défauts dans les [[Software|logiciels]] implémentant les [[TransmissionControlProtocol|protocoles TCP/IP]] peuvent être [[Exploitation|exploités]] pour diverses [[Attack|attaques]], y compris l'[[RemoteCodeExecution|exécution de code à distance]].
*   **Mesures de Protection / Bonnes Pratiques**:
    *   [[Firewall|Utilisation de Pare-feu]]: Filtrent le [[NetworkTrafficAnalysis|trafic réseau]] en fonction des [[PortNumber|numéros de port]], des [[InternetProtocol|adresses IP]] et des [[Protocol|protocoles]], bloquant les communications non autorisées.
    *   [[NetworkSegmentation|Segmentation Réseau]]: Diviser un grand [[Network|réseau]] en [[Subnet|segments]] plus petits pour limiter la portée des [[Attack|attaques]] et contrôler le flux de [[NetworkTrafficAnalysis|trafic]].
    *   [[DataEncryption|Chiffrement des Données]]: Utilisation de protocoles sécurisés comme [[SecureSocketLayer|SSL]] ou [[TransportLayerSecurity|TLS]] pour chiffrer les données aux couches supérieures, protégeant ainsi la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des communications.
    *   [[PatchManagement|Gestion des Patchs]]: Appliquer régulièrement les mises à jour de [[Security|sécurité]] pour corriger les [[SoftwareVulnerability|vulnérabilités logicielles]] connues dans les implémentations des protocoles [[TransmissionControlProtocol|TCP/IP]].
    *   [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]]: Surveillent le [[NetworkTrafficAnalysis|trafic réseau]] pour détecter et/ou bloquer les activités malveillantes ou les tentatives d'[[Exploitation|exploitation]] de faiblesses protocolaires.
*   **Versions et alternatives sécurisées (exemples)**:
    *   [[HypertextTransferProtocolSecure|HTTPS]] (pour [[HypertextTransferProtocol|HTTP]])
    *   [[DomainNameSystemSecurityExtensions|DNSSEC]] (pour [[DomainNameSystem|DNS]])
    *   [[SecureShell|SSH]] (alternative sécurisée à Telnet, [[FileTransferProtocolSecure|FTPS]], [[SSHFileTransferProtocol|SFTP]])
    *   Mise en œuvre du [[ZeroTrust|modèle Zero Trust]] pour une approche de [[Security|sécurité]] continue.

## 🔗 Notes Connexes
*   [[Internet]]
*   [[NetworkProtocol]]
*   [[TransmissionControlProtocol|TCP]]
*   [[InternetProtocol|IP]]
*   [[UserDatagramProtocol|UDP]]
*   [[[[InternetProtocolSuite|Modèle TCP/IP]]   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[ProtocolStack|Pile de Protocoles]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Wireshark|Wireshark]]