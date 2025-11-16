---
tags:
  - reseau
  - identification
  - couche/liaison/donnees
  - securite
aliases:
  - Adresse MAC
  - MAC
  - Media Access Control Address
  - MAC address
archetype: concept-general
source:
cssclasses:
  - max
---

# Adresse MAC (Media Access Control)

## 🎯 Rôle et Couche OSI
> L'[[MediaAccessControlAddress|adresse MAC]] est un identifiant unique attribué de manière permanente à une [[NetworkInterfaceCard|interface réseau]] pour les communications au sein d'un [[NetworkSegment|segment de réseau]] local. Elle opère au niveau de la [[DataLinkLayer|couche liaison de données]] ([[OpenSystemsInterconnectionModel|couche 2 du modèle OSI]]).

## ⚙️ Caractéristiques et Fonctionnement
1.  **Identifiant Unique Permanent**: Chaque [[NetworkInterfaceCard|carte réseau]] (NIC) se voit attribuer une [[MediaAccessControlAddress|adresse MAC]] unique par le fabricant, souvent gravée dans le [[Firmware|micrologiciel]] de l'appareil.
2.  **Format**: Il s'agit d'une adresse de 48 [[Bit|bits]] (6 [[Byte|octets]]), généralement représentée sous forme [[HexadecimalValues|hexadécimale]], séparée par des deux-points ou des tirets (ex: `00:1A:2B:3C:4D:5E`).
3.  **Organisation Unique Identifier (OUI)**: Les trois premiers [[Byte|octets]] de l'[[MediaAccessControlAddress|adresse MAC]] identifient le fabricant de la [[NetworkInterfaceCard|carte réseau]] (l'OUI), tandis que les trois derniers sont un numéro de série unique attribué par ce fabricant.
4.  **Non Routable**: Contrairement aux [[InternetProtocol|adresses IP]], les [[MediaAccessControlAddress|adresses MAC]] ne sont pas utilisées pour le [[Routing|routage]] entre différents [[Network|réseaux]] [[RemoteNetwork|distants]]. Elles servent uniquement à identifier les [[Host|hôtes]] sur un même [[LocalAreaNetwork|segment de réseau local]].
5.  **Interaction avec [[AddressResolutionProtocol|ARP]]**: Le [[AddressResolutionProtocol|protocole de résolution d'adresse]] ([[AddressResolutionProtocol|ARP]]) est fondamental pour l'utilisation des [[MediaAccessControlAddress|adresses MAC]]. Il permet de résoudre une [[InternetProtocol|adresse IP]] logique en une [[MediaAccessControlAddress|adresse MAC]] physique correspondante sur un [[LocalAreaNetwork|réseau local]].

## 🛡️ Sécurité et Menaces
*   **[[MACSpoofing|Usurpation d'Adresse MAC (MAC Spoofing)]]**: Un [[ThreatActor|acteur de menace]] modifie son [[MediaAccessControlAddress|adresse MAC]] pour se faire passer pour un autre [[NetworkDevice|appareil]]. Cela peut être utilisé pour contourner les [[AccessControl|contrôles d'accès]] (ex: [[MacAddressFiltering|filtrage d'adresses MAC]]) ou masquer l'[[UserIdentity|identité]] de l'[[ThreatActor|attaquant]].
*   **[[AddressResolutionProtocolPoisoning|Empoisonnement ARP (ARP Poisoning)]]**: L'[[ThreatActor|attaquant]] envoie de fausses réponses [[AddressResolutionProtocol|ARP]] pour associer son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocol|adresse IP]] d'une [[DefaultGateway|passerelle par défaut]] ou d'un autre [[Host|hôte]]. Cette [[ManInTheMiddle|attaque de l'homme du milieu]] permet d'intercepter et potentiellement de modifier le [[NetworkCommunication|trafic réseau]].
*   **Évasion de filtres réseau**: Le [[MACSpoofing|MAC spoofing]] peut être utilisé pour contourner les [[MacAddressFiltering|filtres basés sur les adresses MAC]], permettant un [[UnauthorizedAccess|accès non autorisé]] à un [[Network|réseau]] ou à des [[Resource|ressources]].

## ✅ Mesures de Protection
*   **[[NetworkAccessControl|Contrôle d'Accès Réseau]] (NAC)**: Authentifie les [[NetworkDevice|appareils]] avant de leur permettre l'[[AccessControl|accès au réseau]]. Cela rend l'utilisation d'[[MediaAccessControlAddress|adresses MAC]] falsifiées plus difficile, car l'appareil doit également passer d'autres vérifications (ex: [[Authentication|authentification]] de l'[[User|utilisateur]] ou de l'appareil).
*   **[[PortSecurity|Sécurité des Ports]]**: Sur les [[NetworkSwitch|commutateurs réseau]], cette fonctionnalité permet de limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] qui peuvent être apprises sur un [[LANPort|port]] spécifique. Elle peut également associer statiquement une [[MediaAccessControlAddress|adresse MAC]] à un [[LANPort|port]], bloquant ainsi toute autre [[MediaAccessControlAddress|adresse MAC]].
*   **[[NetworkMonitoring|Surveillance réseau]] et [[NetworkTrafficAnalysis|Analyse du Trafic]]**: Des outils de [[NetworkMonitoring|surveillance]] peuvent détecter les [[MediaAccessControlAddress|adresses MAC]] inhabituelles ou multiples sur un même [[LANPort|port]], signalant une potentielle [[Attack|attaque]] de [[MACSpoofing|MAC spoofing]] ou d'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]].
*   **[[VirtualLocalAreaNetwork|VLANs]]**: L'utilisation de [[VirtualLocalAreaNetwork|réseaux locaux virtuels]] permet la [[NetworkSegmentation|segmentation des réseaux]], ce qui limite la portée des [[Attack|attaques]] basées sur les [[MediaAccessControlAddress|adresses MAC]] à un seul [[VirtualLocalAreaNetwork|VLAN]] plutôt qu'à l'ensemble du [[LocalAreaNetwork|réseau local]].

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[InternetProtocol|Adresse IP]]
*   [[MACSpoofing|Usurpation d'Adresse MAC (MAC Spoofing)]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP (ARP Poisoning)]]
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]]