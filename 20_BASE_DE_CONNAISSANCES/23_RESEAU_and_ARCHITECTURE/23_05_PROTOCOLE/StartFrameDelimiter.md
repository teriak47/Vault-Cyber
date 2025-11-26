---
aliases:
  - Délimiteur de Début de Trame
  - SFD
  - Start Frame Delimiter
archetype: protocole
port_defaut: N/A
couche_osi:
  - "Couche 1 - Physique"
  - "Couche 2 - Liaison"
rfc:
  - "RFC 894"
  - "RFC 1042"
  - "IEEE 802.3"
cssclasses:
  - max
tags:
  - protocole/ethernet
  - reseau/trame
  - modele-osi/couche-1
  - modele-osi/couche-2
  - transmission-donnees
  - synchronisation
  - protocole/ethernet/sfd
  - protocole/ethernet/preamble
  - definition
---

# Start Frame Delimiter (SFD)

> [!info] Carte d'Identité
> * **Couche OSI** : Couche1, Couche2
> * **Port par défaut** : `N/A`
> * **Transport** : *Ethernet*

## ⚙️ Fonctionnement (Synchronisation de la Trame)
Le *Start Frame Delimiter (SFD)* est un champ essentiel dans les trames Ethernet, positionné immédiatement après le *Preamble* et juste avant la *Destination MAC Address*. Son rôle principal est de marquer la fin du préambule et le début de la trame Ethernet réelle, en fournissant une indication claire aux stations réceptrices pour la synchronisation au niveau du bit et de la trame.

Le préambule et le SFD sont des séquences de bits binaires qui permettent à la carte réseau réceptrice de s'aligner sur la cadence de transmission de l'expéditeur et de déterminer le début exact des données de la trame. Le préambule fournit un modèle pour la synchronisation de l'horloge, tandis que le SFD signale que les octets suivants sont le début de la trame.

```mermaid
graph LR
    A[Preamble] --> B[SFD];
    B --> C[Destination MAC Address];
    C --> D[Source MAC Address];
    D --> E[Type/Length];
    E --> F[Payload (Données)];
    F --> G[FCS];
```

## 📦 Structure du Paquet (Preamble et SFD Ethernet)

Dans le contexte d'Ethernet (IEEE 802.3), le préambule est une séquence de 7 octets (56 bits) de alternant 1s et 0s (10101010...). Le SFD suit immédiatement le préambule et est un octet (8 bits) avec une séquence de 10101011.

| Champ                  | Taille (bits) | Valeur (binaire) | Description                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :--------------------- | :------------ | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Preamble**           | 56            | 10101010... (x7) | Sert à la synchronisation d'horloge entre l'émetteur et le récepteur. Il est composé de sept octets alternant des 1 et des 0, permettant à l'horloge du récepteur de se synchroniser avec le signal entrant.                                                                                                                                                                                                                |
| **Start Frame Delimiter (SFD)** | 8             | 10101011         | Indique la fin du préambule et signale que les bits suivants constituent le début de la trame Ethernet. La séquence unique "10101011" permet au récepteur de distinguer le début effectif de la trame des octets de synchronisation du préambule. Le dernier bit "1" du SFD est crucial car il rompt le motif du préambule et alerte le récepteur que le champ suivant est l'adresse MAC de destination. |
| **Destination MAC Address** | 48            |                  | Adresse MAC du destinataire de la trame.                                                                                                                                                                                                                                                                                                                                                                                     |

## 🦈 Analyse Wireshark
Dans Wireshark, le préambule et le SFD ne sont généralement pas affichés directement car ils sont des artefacts du processus de transmission physique et sont généralement traités par la carte d'interface réseau (NIC) avant que les données ne soient passées au système d'exploitation. Cependant, leur présence est implicite pour la détection et le traitement correct de la trame Ethernet.

Si une trame est mal formée ou si la synchronisation échoue, Wireshark peut signaler une erreur au niveau de la couche liaison de données, bien que ce ne soit pas une erreur directe du SFD en soi.

> [!tip] Filtres Utiles
> ```
> # Filtrer le trafic Ethernet (général)
> eth
>
> # Filtrer les trames mal formées ou avec des erreurs CRC
> eth.fcs.status == 1
> ```

## 🛡️ Sécurité
Le SFD lui-même n'est pas une source directe de vulnérabilités, car il s'agit d'un mécanisme de bas niveau pour la synchronisation du support physique. Cependant, une mauvaise implémentation ou des interférences physiques affectant la détection du SFD peuvent entraîner des problèmes de détection de trame, des pertes de paquets ou des erreurs de transmission.

> [!danger] Vulnérabilités Connues (indirectes)
> * **Interférences Physiques** : Des interférences électromagnétiques ou des problèmes de câblage peuvent corrompre le préambule et le SFD, empêchant le récepteur de détecter correctement le début de la trame.
> * **Erreurs de Synchronisation** : Si le SFD n'est pas correctement interprété, la trame peut être rejetée par le récepteur, entraînant une perte de données.
> * **Sniffing** : Le SFD fait partie du processus de transmission non chiffré. Bien qu'il ne révèle pas de données sensibles, il est un élément fondamental de la structure de la trame qui peut être interceptée lors de l'écoute passive du réseau.