---
tags:
  - protocole
aliases:
  - Trame Ethernet
  - Ethernet Frame
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Trame Ethernet

## 🎯 Rôle et Couche OSI
> Une [[EthernetFrame|trame Ethernet]] est l'unité de données fondamentale encapsulée et transmise sur un réseau [[Ethernet|Ethernet]]. Elle opère au niveau de la [[DataLinkLayer|couche liaison de données]] (couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]) et permet l'échange d'informations entre les [[NetworkDevice|dispositifs réseau]] sur un même [[BroadcastDomain|domaine de diffusion]].

## ⚙️ Fonctionnement : Structure et Champs
La [[EthernetFrame|trame Ethernet]] est structurée pour assurer la livraison et l'intégrité des [[Data|données]] sur un réseau local. Voici ses principaux composants :

1.  **[[Preamble|Préambule]] (7 octets) et [[StartFrameDelimiter|SFD]] (1 octet)**
    *   Utilisés pour la [[SignalTransmission|synchronisation]] des horloges entre les [[NetworkDevice|équipements]] émetteurs et récepteurs. Le [[StartFrameDelimiter|SFD]] marque le début réel de la trame.
2.  **[[DestinationMacAddress|Adresse MAC de destination]] (6 octets)**
    *   Identifie l'[[NetworkInterfaceCard|interface réseau]] spécifique à laquelle la trame est destinée. Peut être une [[Unicast|adresse unicast]], [[Multicast|multicast]] ou [[BroadcastAddress|broadcast]].
3.  **[[SourceMacAddress|Adresse MAC source]] (6 octets)**
    *   Identifie l'[[NetworkInterfaceCard|interface réseau]] qui a émis la trame.
4.  **Champ Type/Longueur (EtherType) (2 octets)**
    *   Indique soit la longueur du champ de [[Payload|données]], soit le [[NetworkProtocol|protocole]] de [[ApplicationLayer|couche supérieure]] encapsulé dans la [[EthernetFrame|trame]] (ex: [[InternetProtocol|IP]], [[AddressResolutionProtocol|ARP]]).
5.  **Champ de [[Payload|Données]] (46 à 1500 octets)**
    *   Contient les [[Data|données]] réelles des [[NetworkProtocol|protocoles]] de [[ApplicationLayer|couche supérieure]], comme un [[Packet|paquet]] [[InternetProtocol|IP]] ou un [[TransmissionControlProtocol|segment TCP]].
6.  **[[FrameCheckSequence|Séquence de Vérification de Trame (FCS)]] (4 octets)**
    *   Contient une valeur de [[CyclicRedundancyCheck|CRC]] (Cyclic Redundancy Check) de 32 bits, utilisée par le récepteur pour détecter les erreurs de transmission dans la trame, assurant ainsi l'[[Integrity|intégrité des données]].

*   **Taille de la Trame**: La taille totale d'une [[EthernetFrame|trame Ethernet]] (des [[DestinationMacAddress|adresses MAC]] au [[FrameCheckSequence|FCS]]) varie entre 64 octets (minimum) et 1518 octets (maximum) pour Ethernet II.
*   **Pas de ports par défaut** : La [[EthernetFrame|trame Ethernet]] opère à la [[DataLinkLayer|couche Liaison de Données]] et n'utilise pas de [[PortNumber|numéros de port]] comme les [[NetworkProtocol|protocoles]] des couches supérieures ([[TransportLayer|couche transport]]).

## 🛡️ Sécurité de la Trame Ethernet
La [[EthernetFrame|trame Ethernet]] en elle-même n'intègre pas de [[SecurityControl|mécanismes de sécurité]] intrinsèques, ce qui la rend vulnérable à plusieurs [[Attack|attaques]].

*   **Vulnérabilités et Attaques connues**:
    *   [[PacketSniffing|Reniflage de paquets]] : Les [[EthernetFrame|trames]] peuvent être interceptées et analysées sur le [[NetworkSegment|segment réseau]], exposant des [[Cleartext|données en texte clair]].
    *   [[MACSpoofing|Usurpation d'adresse MAC]] : Un [[ThreatActor|attaquant]] peut modifier l'[[MediaAccessControlAddress|adresse MAC]] de sa [[NetworkInterfaceCard|carte réseau]] pour se faire passer pour un autre [[Host|hôte]], potentiellement pour contourner les [[AccessControl|contrôles d'accès]].
    *   [[ManInTheMiddle|Attaques de l'Homme du Milieu (MITM)]] : Des techniques comme l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]] manipulent les [[MediaAccessControlAddress|adresses MAC]] pour rediriger le [[NetworkTrafficAnalysis|trafic]] via la machine de l'[[ThreatActor|attaquant]], permettant l'écoute et la modification des [[Data|données]].
    *   [[NetworkCongestion|Congestion Réseau]] / [[DenialOfService|Déni de Service]] : Un [[ThreatActor|attaquant]] peut inonder un [[Network|réseau]] de [[EthernetFrame|trames]] excessives, comme lors d'une [[SmurfAttack|attaque Smurf]] (qui exploite le [[Broadcast|broadcast]]), pour provoquer une [[ServiceDisruption|interruption de service]].

*   **Mesures de Protection Spécifiques**:
    *   [[NetworkSegmentation|Segmentation réseau]] (ex: [[VirtualLocalAreaNetwork|VLAN]]) : Limite la portée de la [[Broadcast|diffusion]] des [[EthernetFrame|trames]] et des [[Attack|attaques]] potentielles, isolant les [[NetworkSegment|segments réseau]].
    *   [[PortSecurity|Sécurité des ports]] : Configure les [[NetworkSwitch|commutateurs réseau]] pour restreindre les [[MediaAccessControlAddress|adresses MAC]] autorisées sur chaque [[NetworkSwitch|port]], empêchant ainsi l'[[MACSpoofing|usurpation d'adresse MAC]].
    *   [[DataEncryption|Chiffrement des données]] : Utilisation de [[NetworkProtocol|protocoles de chiffrement]] aux [[ApplicationLayer|couches supérieures]] (ex: [[HypertextTransferProtocolSecure|HTTPS]], [[VirtualPrivateNetwork|VPN]]) pour protéger le [[Payload|contenu de la charge utile]] de la [[EthernetFrame|trame]], même si la trame elle-même est interceptée.
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] : Surveillent le [[NetworkTrafficAnalysis|trafic de trames]] pour détecter les [[AnomalyDetection|anomalies]] ou les [[Malware|activités malveillantes]], et peuvent prendre des mesures préventives.
    *   [[MACAddressFiltering|Filtrage d'adresses MAC]] : Contrôle les [[MediaAccessControlAddress|adresses MAC]] autorisées à communiquer sur un [[NetworkSegment|segment réseau]], mais est facilement contournable.

## 🔗 Notes Connexes
*   [[Ethernet|Ethernet]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[AddressResolutionProtocol|ARP]]
*   [[InternetProtocol|IP]]
*   [[TransmissionControlProtocol|TCP]]
*   [[Wireshark|Wireshark]] (Outil d'analyse de trames)
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[CyclicRedundancyCheck|CRC]]