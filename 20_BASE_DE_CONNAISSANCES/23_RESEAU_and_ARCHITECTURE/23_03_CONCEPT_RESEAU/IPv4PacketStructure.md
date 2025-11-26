---
aliases:
  - Structure d'un paquet IPv4
  - IPv4 Packet Structure
  - IPv4 Header
  - Internet Protocol Version 4 Packet
archetype: concept-reseau
couche_osi:
  - "Couche 3 - Réseau"
technologie:
  - IPv4
  - IP
cssclasses:
  - max
tags:
  - protocole/ip/ipv4
  - protocole/ip/header
  - paquet
  - encapsulation
  - reseau/routage
  - checksum
  - ttl
  - protocole/tcp
  - protocole/udp
  - protocole/icmp
  - ethernet
  - modele-tcp-ip/couche-internet
  - definition
---

# IPv4 Packet Structure

> [!abstract] Définition
> Un paquet *IPv4* est l'unité de données fondamentale du protocole *Internet Protocol version 4* (IPv4), utilisé pour acheminer des données sur les réseaux interconnectés. Il encapsule des informations de la couche transport (ou supérieure) et ajoute un en-tête contenant les métadonnées nécessaires au routage et à la livraison de bout en bout.

## ⚙️ Mécanisme & Fonctionnement
La structure d'un paquet *IPv4* est composée d'un en-tête de longueur variable (20 à 60 octets) suivi de la charge utile (données). L'en-tête *IPv4* contient plusieurs champs qui définissent les caractéristiques du paquet et guident son acheminement.

### Encapsulation / Traitement
*   **Entrée** : Segment *TCP*, datagramme *UDP*, ou toute autre PDU (Protocol Data Unit) de la couche transport ou supérieure.
*   **Action** : Le protocole *IPv4* ajoute son en-tête à la PDU entrante. Ce processus inclut la détermination des adresses *IP* source et destination, la définition du *Time to Live* (TTL), le calcul du *checksum* de l'en-tête et la gestion de la fragmentation si nécessaire.
*   **Sortie** : Un datagramme *IPv4* complet, prêt à être transmis à la couche de liaison de données pour être encapsulé dans une trame (par exemple, *Ethernet*).

### Champs de l'En-tête IPv4

| Champ                 | Taille (bits) | Rôle                                                                                                |
| :-------------------- | :------------ | :-------------------------------------------------------------------------------------------------- |
| **Version**           | 4             | Indique la version du protocole IP, pour IPv4, c'est `0100` (4).                                             |
| **IHL** (Internet Header Length) | 4             | Longueur de l'en-tête IP en mots de 32 bits (4 octets). La valeur minimale est 5 (20 octets) et maximale 15 (60 octets). |
| **Type of Service (ToS) / Differentiated Services Code Point (DSCP) / Explicit Congestion Notification (ECN)** | 8             | Priorise ou différencie le traitement des paquets. Inclut *DSCP* (6 bits) et *ECN* (2 bits). |
| **Total Length**      | 16            | Longueur totale du datagramme *IP* (en-tête + données) en octets. La valeur maximale est 65 535 octets. |
| **Identification**    | 16            | Utilisé pour identifier de manière unique les fragments d'un même datagramme original.               |
| **Flags**             | 3             | Contrôle la fragmentation. Contient des bits "Don't Fragment" (DF) et "More Fragments" (MF). |
| **Fragment Offset**   | 13            | Indique la position du fragment actuel par rapport au début du datagramme original.               |
| **Time to Live (TTL)** | 8             | Nombre maximal de sauts (routeurs) qu'un paquet peut traverser avant d'être supprimé, empêchant les boucles infinies. |
| **Protocol**          | 8             | Indique le protocole de la couche supérieure encapsulé dans la charge utile (ex: 6 pour *TCP*, 17 pour *UDP*, 1 pour *ICMP*). |
| **Header Checksum**   | 16            | Utilisé pour la détection d'erreurs dans l'en-tête *IPv4*. Recalculé à chaque saut.               |
| **Source IP Address** | 32            | Adresse *IPv4* de l'expéditeur du paquet.                                                     |
| **Destination IP Address** | 32            | Adresse *IPv4* du destinataire final du paquet.                                                  |
| **Options**           | Variable (0-320) | Champs optionnels pour des fonctionnalités étendues (ex: sécurité, routage source). Non toujours présents. |
| **Padding**           | Variable      | Remplit l'en-tête pour s'assurer qu'il est un multiple de 32 bits lorsque des options sont utilisées. |

```mermaid
graph TD
    subgraph IPv4 Header (20-60 Octets)
        Version(Version: 4 bits) --- IHL(IHL: 4 bits)
        IHL --- ToS(Type of Service: 8 bits)
        ToS --- TotalLength(Total Length: 16 bits)
        TotalLength --- Identification(Identification: 16 bits)
        Identification --- Flags(Flags: 3 bits)
        Flags --- FragOffset(Fragment Offset: 13 bits)
        FragOffset --- TTL(Time to Live: 8 bits)
        TTL --- Protocol(Protocol: 8 bits)
        Protocol --- HeaderChecksum(Header Checksum: 16 bits)
        HeaderChecksum --- SrcIP(Source IP Address: 32 bits)
        SrcIP --- DstIP(Destination IP Address: 32 bits)
        DstIP --- Options(Options: 0-320 bits)
        Options --- Padding(Padding: Variable)
    end
    Padding --- Payload(Payload (Data))
```

## 💡 Cas d'Usage Typique
1.  **Communication de Bout en Bout** : L'*IPv4* est la base de la communication sur Internet et les réseaux *IP* privés, permettant l'échange de données entre n'importe quelles machines équipées d'adresses *IP* uniques.
2.  **Routage Inter-réseaux** : Les routeurs utilisent les adresses *IP* source et destination contenues dans l'en-tête pour déterminer le chemin optimal pour faire transiter les paquets à travers des réseaux hétérogènes.
3.  **Fragmentation** : L'*IPv4* permet de fragmenter les paquets trop volumineux pour tenir dans la *MTU* (Maximum Transmission Unit) d'un lien réseau, assurant que les données peuvent être transmises même sur des chemins avec des contraintes différentes.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Épuisement des adresses** : Le nombre limité d'adresses *IPv4* (environ 4,3 milliards) a conduit à des problèmes d'épuisement, nécessitant des solutions comme le *NAT* (Network Address Translation) et la transition vers l'*IPv6*.
> *   **Sécurité** : L'en-tête *IPv4* ne comprend pas de mécanismes de sécurité intégrés (comme l'authentification ou le chiffrement), ce qui rend les communications *IP* vulnérables sans l'ajout de protocoles comme *IPsec*.
> *   **Surcharge du routeur avec la fragmentation** : La fragmentation *IPv4* peut imposer une charge de traitement significative aux routeurs, car ils doivent gérer et réassembler les fragments, ce qui peut affecter les performances du réseau.