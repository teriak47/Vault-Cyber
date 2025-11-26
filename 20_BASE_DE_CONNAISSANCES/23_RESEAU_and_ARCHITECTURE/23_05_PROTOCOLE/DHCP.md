---
aliases:
  - DHCP
  - Dynamic Host Configuration Protocol
  - Protocole de configuration dynamique d'hôtes
archetype: protocole
port_defaut: 67, 68
couche_osi:
  - "Couche 7 - Application"
rfc:
  - "RFC 2131"
  - "RFC 2132"
cssclasses:
  - max
tags:
  - protocole/dhcp
  - modele-osi/couche-7
  - protocole/udp
  - reseau/adressage/ip
  - communication/handshake
  - outil/wireshark
  - protocole/dns
  - reseau/routage
---

# DHCP

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 7 - Application
> * **Port par défaut** : `UDP 67/68`
> * **Transport** : UDP

## ⚙️ Fonctionnement (Handshake)
Le protocole DHCP (Dynamic Host Configuration Protocol) permet l'attribution dynamique d'adresses IP et d'autres paramètres de configuration réseau aux hôtes. Son fonctionnement principal repose sur un échange de messages en quatre étapes, souvent appelé processus **DORA** (Discover, Offer, Request, Acknowledge).

1.  **DHCP Discover** : Un client, ne possédant pas encore d'adresse IP, envoie un message **DHCP Discover** en *broadcast* sur le réseau. Ce message a pour but de localiser les serveurs DHCP disponibles. Le client utilise l'adresse IP de destination 255.255.255.255 (broadcast) et l'adresse MAC du client comme identifiant.
2.  **DHCP Offer** : Un serveur DHCP qui reçoit le message Discover répond avec un message **DHCP Offer** en *broadcast* ou *unicast* (selon le client). Ce message propose une adresse IP disponible au client, ainsi que d'autres informations de configuration (masque de sous-réseau, passerelle par défaut, serveurs DNS, etc.).
3.  **DHCP Request** : Le client reçoit une ou plusieurs offres et sélectionne la première qu'il reçoit ou celle d'un serveur spécifique. Il envoie alors un message **DHCP Request** en *broadcast* pour indiquer au serveur sélectionné qu'il accepte son offre, et aux autres serveurs qu'il décline les leurs.
4.  **DHCP Acknowledge (ACK)** : Le serveur DHCP sélectionné reçoit le message Request et confirme l'attribution de l'adresse IP et des paramètres de configuration en envoyant un message **DHCP ACK**. Le client peut alors utiliser son adresse IP et participer au réseau.

Les options DHCP, spécifiées dans la RFC 2132, permettent de configurer divers paramètres en plus de l'adresse IP, tels que :
*   **Option 1** : Subnet Mask (masque de sous-réseau)
*   **Option 3** : Router (passerelle par défaut)
*   **Option 6** : Domain Name Server (serveurs DNS)
*   **Option 15** : Domain Name (nom de domaine)
*   **Option 51** : IP Address Lease Time (durée du bail de l'adresse IP)
*   **Option 53** : DHCP Message Type (type de message DHCP : Discover, Offer, Request, ACK, NAK, Release, Decline, Inform)
*   **Option 54** : DHCP Server Identifier (identifiant du serveur DHCP)

```mermaid
sequenceDiagram
    participant Client
    participant Server: DHCP Server

    Client->>Server: DHCP Discover (Broadcast)
    Server->>Client: DHCP Offer (Broadcast/Unicast)
    Client->>Server: DHCP Request (Broadcast)
    Server->>Client: DHCP ACK (Broadcast/Unicast)
```

## 📦 Structure du Paquet (Header)

Le protocole DHCP est basé sur BOOTP (Bootstrap Protocol) et utilise le format de message BOOTP avec des extensions pour les options DHCP. Le message DHCP est encapsulé dans des paquets UDP.

| Champ               | Taille (Octets) | Description                                                              |
|:--------------------|:----------------|:-------------------------------------------------------------------------|
| **Op Code (op)**    | 1               | Type de message (1 pour Request, 2 pour Reply)                  |
| **Hardware Type (htype)** | 1               | Type d'adresse matérielle (ex: 1 pour Ethernet)               |
| **Hardware Length (hlen)** | 1               | Longueur de l'adresse matérielle (ex: 6 pour Ethernet)        |
| **Hops (hops)**     | 1               | Nombre de "sauts" si un agent de relais est utilisé (normalement 0) |
| **Transaction ID (xid)** | 4               | Identifiant de la transaction, utilisé par le client et le serveur pour faire correspondre les requêtes et les réponses |
| **Seconds (secs)**  | 2               | Temps écoulé depuis le début du processus d'acquisition d'une adresse IP |
| **Flags**           | 2               | Indicateurs (bit de broadcast, etc.)                             |
| **Client IP Address (ciaddr)** | 4               | Adresse IP du client (si connue)                               |
| **Your IP Address (yiaddr)** | 4               | Adresse IP proposée ou assignée au client (par le serveur)    |
| **Server IP Address (siaddr)** | 4               | Adresse IP du prochain serveur à utiliser pour le processus de démarrage |
| **Gateway IP Address (giaddr)** | 4               | Adresse IP de l'agent de relais (Relay Agent) si un relais est utilisé |
| **Client Hardware Address (chaddr)** | 16              | Adresse matérielle (MAC) du client                             |
| **Server Host Name (sname)** | 64              | Nom d'hôte du serveur DHCP                                     |
| **Boot File Name (file)** | 128             | Nom du fichier de démarrage (pour les clients sans disque)      |
| **Options**         | Variable        | Champs d'options DHCP (Type de message, masque de sous-réseau, DNS, etc.) |

## 🦈 Analyse Wireshark
Wireshark est un outil essentiel pour analyser le trafic DHCP. Les messages DHCP sont généralement courts et facilement identifiables.

> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole DHCP
> dhcp
>
> # Filtrer spécifiquement les messages Discover
> dhcp.option.dhcp_message_type == 1
>
> # Filtrer spécifiquement les messages Offer
> dhcp.option.dhcp_message_type == 2
>
> # Filtrer les messages Request
> dhcp.option.dhcp_message_type == 3
>
> # Filtrer les messages ACK
> dhcp.option.dhcp_message_type == 5
>
> # Filtrer par adresse MAC du client
> eth.addr == [adresse_mac_client]
> ```

## 🛡️ Sécurité
Le protocole DHCP n'inclut pas de mécanismes d'authentification ou de chiffrement intrinsèques, ce qui le rend vulnérable à plusieurs types d'attaques.

> [!danger] Vulnérabilités Connues
> *   **Sniffing** : Est-ce chiffré ? [Non]. Les messages DHCP sont transmis en clair, ce qui permet à un attaquant d'intercepter les requêtes et réponses et de collecter des informations sur le réseau (adresses IP attribuées, serveurs DNS, etc.).
> *   **Spoofing (DHCP Starvation / Rogue DHCP Server)** : Authentification faible ? [Oui, très faible].
    *   **DHCP Starvation** : Un attaquant peut inonder le serveur DHCP de requêtes Discover avec de fausses adresses MAC, épuisant ainsi le pool d'adresses IP disponibles. Cela entraîne un déni de service pour les clients légitimes qui ne peuvent plus obtenir d'adresse IP.
    *   **Rogue DHCP Server** : Un attaquant peut configurer un serveur DHCP malveillant sur le réseau. Ce "serveur voyou" peut proposer des adresses IP incorrectes, des passerelles par défaut ou des serveurs DNS malveillants, redirigeant le trafic des clients vers des machines contrôlées par l'attaquant (attaques *Man-in-the-Middle*).
*   **DHCP Snooping** : Pour atténuer ces risques, des mécanismes comme le *DHCP Snooping* sur les commutateurs réseau peuvent être mis en œuvre. Le DHCP Snooping permet aux administrateurs de spécifier des ports de confiance et de non-confiance pour le trafic DHCP, empêchant ainsi les serveurs DHCP non autorisés et les attaques de *starvation*.