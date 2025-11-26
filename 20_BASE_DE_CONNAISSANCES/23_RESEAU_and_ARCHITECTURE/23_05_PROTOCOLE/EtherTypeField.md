---
cssclasses:
  - max
aliases:
  - "Champ EtherType"
  - "EtherType"
  - "Ether Type Field"
archetype: protocole
port_defaut:
couche_osi:
  - "Couche 2 - Liaison"
rfc:
  - "IEEE 802.3"
tags:
  - ethertype
  - protocole/ethernet
  - reseau/trame
  - modele-osi/couche-2
  - protocole/ip/ipv4
  - protocole/arp
  - protocole/ieee-802-1q
  - reseau/vlan
  - protocole/ip/ipv6
  - protocole/mpls
  - protocole/lldp
  - norme/ieee-802-3
  - outil/wireshark
---

# EtherType Field

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 2 - Liaison
> * **Port par défaut** : `N/A`
> * **Transport** : `N/A`

L'**EtherType** est un champ de deux octets situé dans l'en-tête d'une trame Ethernet. Il sert à identifier le protocole encapsulé dans la charge utile de la trame, permettant ainsi aux dispositifs récepteurs de déterminer comment traiter le contenu subséquent. Dérivé de la spécification Ethernet Version 2, il a été formalisé dans la norme IEEE 802.3 en tant que champ Longueur/Type.

Historiquement, le champ EtherType et le champ de longueur de la charge utile pouvaient coexister, entraînant une ambiguïté potentielle. Pour résoudre cela, la norme IEEE 802.3x-1997 a introduit une règle unificatrice : les valeurs EtherType doivent être supérieures ou égales à 1536 (0x0600 en hexadécimal). Les valeurs inférieures ou égales à 1500 indiquent la longueur de la charge utile.

Les valeurs EtherType sont attribuées et gérées par l'IEEE Registration Authority, assurant des identifiants uniques et reconnus mondialement pour les protocoles.

## 📦 Structure du Paquet (Header)

Le champ EtherType suit les adresses MAC source et destination dans l'en-tête de la trame Ethernet.

| Champ | Taille | Description |
|---|---|---|
| **EtherType** | 16 bits | Indique le protocole de couche supérieure encapsulé dans la charge utile de la trame Ethernet. |

## Valeurs EtherType Typiques

Voici quelques-unes des valeurs EtherType les plus couramment utilisées et leur signification :

| Valeur (Hex) | Protocole | Description |
|---|---|---|
| `0x0800` | **IPv4** | Internet Protocol version 4. Prend en charge la majorité du trafic internet. |
| `0x0806` | **ARP** | Address Resolution Protocol. Essentiel pour la correspondance des adresses IP aux adresses MAC sur les réseaux locaux. |
| `0x8100` | **IEEE 802.1Q** | VLAN Tagging. Permet la segmentation des réseaux locaux virtuels (VLAN). |
| `0x86DD` | **IPv6** | Internet Protocol version 6. Facilite la transition vers des espaces d'adressage plus grands. |
| `0x8847` | **MPLS Unicast** | Multiprotocol Label Switching (unicast). Utilisé pour l'ingénierie du trafic dans les environnements des fournisseurs de services. |
| `0x8848` | **MPLS Multicast** | Multiprotocol Label Switching (multicast). |
| `0x88CC` | **LLDP** | Link Layer Discovery Protocol. Utilisé pour les annonces de capacités et l'auto-découverte sur les réseaux locaux. |

## 🦈 Analyse Wireshark
> [!tip] Filtres Utiles
> ```
> # Filtrer par EtherType
> eth.type == 0x0800 # Affiche uniquement le trafic IPv4
> eth.type == 0x0806 # Affiche uniquement le trafic ARP
> eth.type == 0x86DD # Affiche uniquement le trafic IPv6
> eth.type == 0x8100 # Affiche uniquement le trafic 802.1Q VLAN
>
> # Filtrer par nom de protocole (Wireshark décode souvent automatiquement)
> ip
> arp
> ipv6
> vlan
> ```