---
tags:
  - protocole
  - reseau/couche-liaison
  - modele-osi/couche-2
  - trame
aliases:
  - Trame de Liaison
  - Cadre de la couche liaison de données
  - Data Link Layer Frame
archetype: protocole
port_defaut: N/A
couche_osi: Couche de Liaison de Données (Couche 2)
rfc:
cssclasses:
  - max
---

# Trame de Liaison

> [!info] Carte d'Identité
> * **Couche OSI** : [[NetworkAccessLayer|Couche d'Accès Réseau]] (OSI Couche 2)
> * **Port par défaut** : N/A
> * **Fonction** : Encapsulation de [[Packet|paquets IP]] pour la [[DataTransmission|transmission]] physique

Une trame de liaison, ou [[DataFrames|cadre de données]] de couche de liaison, est l'unité de [[DataTransmission|transmission de données]] utilisée par les [[NetworkProtocol|protocoles]] de la [[NetworkAccessLayer|couche de liaison de données]] (Couche 2 du modèle OSI). Elle encapsule les [[Packet|paquets]] de la [[InternetLayer|couche Internet]] pour les préparer à être envoyés sur le [[NetworkMedia|support physique du réseau]], comme un [[EthernetPatchCable|câble Ethernet]] ou une connexion [[IEEE80211|Wi-Fi]]. Son rôle principal est de gérer l'accès au support partagé, la détection d'erreurs et l'adressage local via les [[MediaAccessControlAddress|adresses MAC]].

## ⚙️ Fonctionnement (Encapsulation et Transmission)
La trame de liaison facilite la [[DataTransmission|transmission]] fiable des données entre les [[NetworkDevice|périphériques réseau]] connectés localement sur un même [[NetworkSegment|segment réseau]].

1.  **Encapsulation** : La [[NetworkAccessLayer|couche de liaison de données]] reçoit un [[Packet|paquet]] de la [[InternetLayer|couche Internet]]. Elle ajoute un [[Header|en-tête]] et une [[FrameCheckSequence|fin de trame]] (trailer) pour former la trame. L'[[Header|en-tête]] contient notamment les [[DestinationMacAddress|adresses MAC de destination et source]].
2.  **Adressage Local** : Les [[MediaAccessControlAddress|adresses MAC]] sont utilisées pour identifier les [[EndDevices|terminaux]] sur le [[LocalAreaNetwork|LAN]], permettant à la trame d'être acheminée au bon destinataire au sein du [[BroadcastDomain|domaine de diffusion]].
3.  **Contrôle d'Accès au Médium** : Les [[NetworkProtocol|protocoles]] de la [[NetworkAccessLayer|couche de liaison de données]] (comme [[EthernetProtocol|Ethernet]]) définissent comment les [[NetworkDevice|périphériques]] partagent le [[NetworkMedia|support de transmission]] pour éviter les [[Collision|collisions]] et assurer une [[DataTransmission|transmission]] ordonnée.
4.  **Détection d'Erreurs** : La [[FrameCheckSequence|séquence de vérification de trame]] (FCS) est utilisée pour détecter les erreurs de [[DataCorruption|corruption de données]] survenues pendant la [[DataTransmission|transmission physique]]. Si une erreur est détectée, la trame est généralement rejetée.

## 📦 Structure d'une Trame (Ethernet comme exemple)
La structure exacte d'une trame varie selon le [[NetworkProtocol|protocole]] de la [[NetworkAccessLayer|couche de liaison de données]] (ex: [[EthernetProtocol|Ethernet]], Wi-Fi, PPP). Voici la structure d'une [[EthernetProtocol|trame Ethernet]] standard:

| Champ | Taille | Description |
|---|---|---|
| **Préambule** | 7 octets | Synchronisation du récepteur |
| **Start Frame Delimiter (SFD)** | 1 octet | Indique le début de la trame |
| **Adresse MAC de Destination** | 6 octets | Adresse MAC du destinataire |
| **Adresse MAC Source** | 6 octets | Adresse MAC de l'expéditeur |
| **Type/Longueur** | 2 octets | Indique le type de protocole de couche supérieure (IP, IPX, etc.) ou la longueur des données |
| **Données (Payload)** | 46 à 1500 octets | Le paquet de couche réseau (ex: IPv4, IPv6) |
| **Séquence de Vérification de Trame (FCS)** | 4 octets | Champ de contrôle d'erreurs (CRC) |

## 🦈 Analyse Wireshark
Les trames de liaison sont les premières unités de données visibles lors d'une [[PacketSniffing|capture de paquets]] avec un [[Wireshark|analyseur de protocole]].

> [!tip] Filtres Utiles
> ```
> # Filtrer toutes les trames Ethernet
> eth
>
> # Filtrer par adresse MAC de destination
> eth.dst == 00:11:22:33:44:55
>
> # Filtrer les trames avec erreurs de FCS (Frame Check Sequence)
> eth.fcs.status == 1
> ```

## 🛡️ Sécurité
La [[NetworkAccessLayer|couche de liaison de données]] est vulnérable à plusieurs [[SecurityVulnerabilities|attaques]]:

*   **[[PacketSniffing|Sniffing]]** : Les données au niveau de la trame ne sont généralement pas chiffrées sur un [[LocalAreaNetwork|LAN]] (sauf si un [[SecureSocketLayer|VPN]] ou un [[HypertextTransferProtocolSecure|protocole sécurisé]] est utilisé). Un attaquant sur le même [[NetworkSegment|segment réseau]] peut intercepter et lire les trames.
*   **[[MACSpoofing|MAC Spoofing]]** : L'usurpation d'[[MediaAccessControlAddress|adresse MAC]] permet à un attaquant de se faire passer pour un autre [[NetworkDevice|périphérique]] sur le [[LocalAreaNetwork|réseau]], contournant potentiellement le [[MacAddressFiltering|filtrage d'adresses MAC]] ou les [[SecurityControl|contrôles d'accès réseau]].
*   **Attaques ARP** : Des [[AddressResolutionProtocol|requêtes ARP]] falsifiées peuvent manipuler la [[MacAddressTable|table d'adresses MAC]] des [[NetworkDevice|périphériques]] pour rediriger le trafic, comme dans une attaque [[ManInTheMiddle|de l'homme du milieu]].

## 🔗 Notes Connexes
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkAccessLayer|Couche d'Accès Réseau]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresse (ARP)]]
*   [[Packet|Paquet]]