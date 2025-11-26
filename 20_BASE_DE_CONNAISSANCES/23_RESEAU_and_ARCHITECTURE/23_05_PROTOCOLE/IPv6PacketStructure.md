---
aliases:
  - Structure du Paquet IPv6
  - IPv6 Packet Structure
  - IPv6 Header
archetype: protocole
port_defaut: N/A
couche_osi:
  - "Couche 3 - Réseau"
rfc:
  - RFC 8200
  - RFC 2460
cssclasses:
  - max
tags:
  - protocole/ip/ipv6
  - modele-osi/couche-3
  - reseau/couche-3
  - protocole/ipv6/packet-structure
  - protocole/ipv6/extension-headers
  - protocole/ipv6/traffic-class
  - protocole/ipv6/flow-label
  - protocole/ipv6/payload-length
  - protocole/ipv6/next-header
  - protocole/ipv6/hop-limit
  - routage
  - qualite-de-service
---

# IPv6 Packet Structure

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 3 - Réseau
> * **Port par défaut** : `N/A`
> * **Transport** : *Indépendant du protocole de transport (TCP/UDP)*

## ⚙️ Fonctionnement

IPv6 est un protocole de la couche réseau, sans connexion. Il ne dispose pas de mécanisme de "handshake" à proprement parler pour établir des connexions, contrairement aux protocoles de la couche transport comme TCP. Son rôle principal est l'adressage et le routage des paquets de données entre les hôtes sur différents réseaux. La transmission des données s'effectue par l'envoi de paquets indépendants qui sont routés de manière autonome.

## 📦 Structure du Paquet (Header)

Un paquet IPv6 est composé d'un **en-tête de base IPv6** obligatoire, suivi de zéro ou plusieurs **en-têtes d'extension** (Extension Headers - EH), puis de la charge utile (payload).

```mermaid
graph TD
    A[Paquet IPv6] --> B[En-tête de Base IPv6 (40 octets)]
    B --> C{En-têtes d'Extension Optionnels}
    C --> D[Charge Utile (Transport Header + Data)]

    subgraph En-têtes d'Extension
        C --> C1[En-tête Hop-by-Hop Options]
        C --> C2[En-tête Destination Options]
        C --> C3[En-tête Routing]
        C --> C4[En-tête Fragment]
        C --> C5[En-tête Authentication Header (AH)]
        C --> C6[En-tête Encapsulating Security Payload (ESP)]
    end
```

### En-tête de Base IPv6

L'en-tête de base a une taille fixe de 40 octets.

| Champ             | Taille    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| :---------------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Version**       | 4 bits    | Indique la version du protocole IP. Pour IPv6, cette valeur est toujours `0110` (6 en binaire).                                                                                                                                                                                                                                                                                                                                                              |
| **Traffic Class** | 8 bits    | Similaire au champ `Type of Service` (ToS) d'IPv4. Utilisé pour la classification et la gestion du trafic (QoS). Les 6 premiers bits sont pour le *Differentiated Services Codepoint* (DSCP) et les 2 derniers pour l'*Explicit Congestion Notification* (ECN).                                                                                                                                                                                                    |
| **Flow Label**    | 20 bits   | Utilisé par une source pour étiqueter les paquets appartenant à un flux particulier pour lequel la source demande un traitement spécial par les routeurs IPv6 (par exemple, un chemin non défini par le routage standard, ou une exigence de QoS).                                                                                                                                                                                                                 |
| **Payload Length**| 16 bits   | Indique la longueur de la charge utile en octets, y compris les en-têtes d'extension et les données de la couche supérieure. La valeur maximale est 65 535 octets. Si la charge utile dépasse cette taille, le champ est mis à zéro et l'en-tête d'extension *Jumbo Payload* est utilisé.                                                                                                                                                                        |
| **Next Header**   | 8 bits    | Identifie le type d'en-tête immédiatement suivant l'en-tête de base IPv6. Cela peut être un protocole de la couche supérieure (par exemple, TCP, UDP) ou un en-tête d'extension IPv6. Les valeurs sont les mêmes que les valeurs de champ de protocole IPv4.                                                                                                                                                                                          |
| **Hop Limit**     | 8 bits    | Similaire au champ `Time-To-Live` (TTL) d'IPv4. Il est décrémenté de un par chaque nœud de routage que le paquet traverse. Si `Hop Limit` atteint zéro, le paquet est abandonné.                                                                                                                                                                                                                                                                             |
| **Source Address**| 128 bits  | L'adresse IPv6 de l'expéditeur du paquet.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Destination Address** | 128 bits | L'adresse IPv6 du destinataire du paquet.                                                                                                                                                                                                                                                                                                                                                                                                               |

### En-têtes d'Extension IPv6

Les en-têtes d'extension (EH) fournissent des fonctionnalités supplémentaires et sont chaînées les unes aux autres via le champ `Next Header`. La RFC 8200 spécifie que l'ordre des en-têtes d'extension devrait généralement être :
1.  **Hop-by-Hop Options Header** : Traité par chaque nœud sur le chemin.
2.  **Destination Options Header** : Traité par le destinataire final ou les destinataires intermédiaires spécifiques.
3.  **Routing Header** : Utilisé pour spécifier une liste de routeurs intermédiaires à visiter.
4.  **Fragment Header** : Utilisé pour fragmenter les paquets trop grands pour la *Path MTU* (Maximum Transmission Unit) du chemin.
5.  **Authentication Header (AH)** : Fournit l'authentification et l'intégrité des données sans chiffrement.
6.  **Encapsulating Security Payload (ESP) Header** : Fournit le chiffrement, l'authentification, et l'intégrité des données.
7.  **Destination Options Header** : Traité uniquement par le destinataire final.
8.  **Upper-Layer Header** : (e.g., TCP, UDP, ICMPv6).

## 🦈 Analyse Wireshark

> [!tip] Filtres Utiles
> ```
> # Filtrer tous les paquets IPv6
> ipv6
>
> # Filtrer les paquets IPv6 vers une adresse de destination spécifique
> ipv6.dst == 2001:db8::1
>
> # Filtrer les paquets IPv6 avec un Next Header spécifique (ex: TCP)
> ipv6.nxt == 6
>
> # Filtrer les paquets IPv6 utilisant un en-tête d'extension (ex: Hop-by-Hop Options)
> ipv6.nxt == 0
>
> # Filtrer les paquets IPv6 fragmentés
> ipv6.frag_offset
> ```

## 🛡️ Sécurité

> [!danger] Vulnérabilités Connues
> *   **Sniffing** : Le trafic IPv6 n'est pas chiffré par défaut. Le sniffing est possible, comme avec IPv4. Le chiffrement est implémenté au moyen de l'en-tête d'extension ESP (Encapsulating Security Payload) d'IPsec.
> *   **Spoofing** : L'authentification au niveau de la couche réseau n'est pas intrinsèque. Des adresses IPv6 source peuvent être falsifiées. Les en-têtes d'extension AH (Authentication Header) et ESP d'IPsec peuvent fournir une authentification de l'origine et une intégrité des données.
> *   **Fragment Attack** : La fragmentation IPv6 peut être exploitée pour contourner les pare-feu ou les systèmes de détection d'intrusion si elle n'est pas gérée correctement.
> *   **Neighbor Discovery Protocol (NDP) Spoofing** : Similaire à l'ARP spoofing en IPv4, le NDP peut être ciblé pour des attaques Man-in-the-Middle ou de déni de service. L'extension Secure Neighbor Discovery (SEND) vise à atténuer ces risques.