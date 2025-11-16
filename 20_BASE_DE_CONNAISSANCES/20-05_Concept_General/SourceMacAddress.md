---
tags:
  - concept
  - concept/general
  - protocole/mac
  - protocole/arp
  - couche/liaison/donnees
  - reseau/local
aliases:
  - Adresse MAC Source
  - Source MAC Address
  - Source Media Access Control Address
  - Adresse MAC émettrice
archetype: concept-general
source:
  -
cssclasses:
  - max
---

# Adresse MAC Source

## 📥 Définition en une phrase
> L'[[SourceMacAddress|adresse MAC source]] est l'[[MediaAccessControlAddress|identifiant physique unique]] d'une [[NetworkInterfaceCard|carte réseau]] qui initie une [[NetworkCommunication|communication réseau]] sur un [[LocalAreaNetwork|réseau local]].

## 🧠 Concepts Clés / Piliers
*   **Identifiant Matériel Unique**: Chaque [[NetworkInterfaceCard|carte réseau]] possède une [[MediaAccessControlAddress|adresse MAC]] (Media Access Control) unique, gravée par le fabricant. Elle est généralement représentée par une suite de douze [[HexadecimalValues|valeurs hexadécimales]] (par exemple, `00:1A:2B:3C:4D:5E`).
*   **Opération à la [[DataLinkLayer|Couche Liaison de Données]]**: L'[[SourceMacAddress|adresse MAC source]] est utilisée à la [[DataLinkLayer|couche de liaison de données]] ([[OpenSystemsInterconnectionModel|Couche 2 du modèle OSI]]) pour identifier l'[[EndDevices|appareil émetteur]] au sein d'un même [[NetworkSegment|segment de réseau]] ou [[BroadcastDomain|domaine de diffusion]].
*   **Identification de l'Expéditeur**: Elle est intégrée dans l'[[EthernetFrame|en-tête de trame Ethernet]] et permet aux [[NetworkSwitch|commutateurs réseau]] d'identifier la source d'une [[Frame|trame]] de données, ce qui est crucial pour le processus d'[[Encapsulation|encapsulation]] et de transmission.
*   **Non-Routable sur [[Internet|Internet]]**: Contrairement aux [[InternetProtocolAddressBlocks|adresses IP]], les [[MediaAccessControlAddress|adresses MAC]] ne sont pas utilisées pour le [[Routing|routage]] sur des [[InterconnectedNetworks|réseaux étendus]] ou [[Internet|Internet]]. Elles sont locales au [[Subnet|sous-réseau]] et sont remplacées à chaque saut par les [[MediaAccessControlAddress|adresses MAC]] des [[Router|routeurs]] ou [[NetworkSwitch|commutateurs]] intermédiaires.
*   **Rôle dans le [[AddressResolutionProtocol|Protocole ARP]]**: L'[[SourceMacAddress|adresse MAC source]] est un élément fondamental du [[AddressResolutionProtocol|Protocole de Résolution d'Adresses]] ([[AddressResolutionProtocol|ARP]]), qui permet de mapper les [[InternetProtocol|adresses IP]] logiques aux [[MediaAccessControlAddress|adresses MAC]] physiques sur un [[LocalAreaNetwork|réseau local]].

## 💡 Importance en Cybersécurité
> L'[[SourceMacAddress|adresse MAC source]] est fondamentale pour le bon fonctionnement des [[Network|réseaux locaux]], mais elle est également une cible potentielle pour certaines [[Attack|attaques]] en [[Cybersecurity|cybersécurité]]. Comprendre son rôle est essentiel pour la [[NetworkSecurity|sécurité réseau]]. Par exemple, des [[ThreatActor|acteurs de menace]] peuvent utiliser le [[MACSpoofing|MAC Spoofing]] pour masquer leur identité ou contourner des [[AccessControl|contrôles d'accès]] basés sur l'[[MediaAccessControlAddress|adresse MAC]], ou exploiter l'[[AddressResolutionProtocolPoisoning|ARP Poisoning]] pour intercepter le [[NetworkTrafficAnalysis|trafic réseau]]. Le [[SecurityMonitoring|monitorage]] et l'[[AnomalyDetection|analyse d'anomalies]] des [[SourceMacAddress|adresses MAC sources]] peuvent aider à détecter de telles [[Attack|attaques]].

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[DestinationMacAddress|Adresse MAC de Destination]]
*   [[MacAddressTable|Table d'adresses MAC]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]]
*   [[MACSpoofing|Usurpation d'adresse MAC]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkSwitch|Commutateur réseau]]