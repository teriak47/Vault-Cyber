---
aliases:
  - Types d'adresses IPv6
  - IPv6 Address Types
  - IPv6 Unicast
  - IPv6 Multicast
  - IPv6 Anycast
  - Global Unicast Address
  - Link-Local Address
  - Unique Local Address
archetype: protocole
port_defaut: N/A
couche_osi:
  - "Couche 3 - Réseau"
rfc:
  - RFC 4291
  - RFC 4193
  - RFC 4291
  - RFC 2526
cssclasses:
  - max
tags:
  - protocole/ip/ipv6
  - protocole/ipv6/adressage
  - protocole/ipv6/adressage/unicast
  - protocole/ipv6/adressage/global-unicast
  - protocole/ipv6/adressage/link-local
  - protocole/ipv6/adressage/unique-local
  - protocole/ipv6/adressage/multicast
  - protocole/ipv6/adressage/anycast
  - modele-osi/couche-3
  - protocole/ndp
  - protocole/ipv6/slaac
  - protocole/ipv6/eui-64
---

# IPv6 Address Types

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 3 - Réseau
> * **Port par défaut** : `N/A`
> * **Transport** : IPv6

## ⚙️ Fonctionnement (Usage et Allocation)

Les adresses IPv6 sont des identifiants de 128 bits utilisés pour identifier les interfaces réseau et router le trafic. Il existe trois types fondamentaux d'adresses IPv6, chacun avec un but et une portée spécifiques.

### Unicast

Une adresse *unicast* identifie une interface unique. Un paquet envoyé à une adresse unicast est délivré à l'interface identifiée par cette adresse.

*   **Global Unicast Address (GUA)** :
    *   Ces adresses sont globalement uniques et routables sur Internet.
    *   Elles sont l'équivalent des adresses IPv4 publiques.
    *   Le format typique est `2000::/3`, bien que les implémentations actuelles utilisent `2001::/16`, `2002::/16`, `2003::/16` et `2004::/16`. Les adresses `2000::/3` sont définies pour le routage global..
    *   Exemple : `2001:0db8:85a3:0000:0000:8a2e:0370:7334`.

*   **Link-Local Address (LLA)** :
    *   Ces adresses sont utilisées uniquement sur un *lien* (segment de réseau local) et ne sont pas routables au-delà de celui-ci.
    *   Elles sont principalement utilisées pour la découverte de voisins (NDP), la configuration automatique sans état (SLAAC) et les communications intra-lien.
    *   Toutes les interfaces IPv6 doivent avoir au moins une adresse Link-Local.
    *   Elles commencent toujours par le préfixe `fe80::/10`. En pratique, le préfixe `fe80::/64` est utilisé.
    *   Exemple : `fe80::a00:27ff:fe75:9d4d`.

*   **Unique Local Address (ULA)** :
    *   Ces adresses sont destinées aux communications locales au sein d'un site ou entre un nombre limité de sites, ne nécessitant pas de connectivité globale.
    *   Elles sont routables au sein de réseaux privés mais ne sont pas routées sur Internet.
    *   Elles commencent par le préfixe `fc00::/7`. En pratique, `fd00::/8` est utilisé après le processus de génération pseudo-aléatoire.
    *   Exemple : `fdc8:31f5:128b:2d36:c001:ff:fe00:1`.

### Multicast

Une adresse *multicast* identifie un groupe d'interfaces. Un paquet envoyé à une adresse multicast est délivré à toutes les interfaces membres de ce groupe.

*   Elles sont utilisées pour la diffusion de données à plusieurs destinataires simultanément.
*   Toutes les adresses multicast commencent par le préfixe `ff00::/8`.
*   Des exemples incluent `ff02::1` (tous les nœuds sur le lien local) et `ff02::2` (tous les routeurs sur le lien local).
*   Exemple : `ff02::1`.

### Anycast

Une adresse *anycast* identifie un groupe d'interfaces, mais un paquet envoyé à une adresse anycast est délivré *à la plus proche* de ces interfaces (selon la métrique du protocole de routage).

*   Les adresses anycast sont assignées à plusieurs interfaces.
*   Elles sont généralement utilisées pour la résilience et la répartition de charge, par exemple pour les serveurs DNS.
*   Les adresses anycast sont configurées comme des adresses unicast ordinaires sur plusieurs interfaces. Il n'y a pas de plage d'adresses spécifique pour l'anycast ; une adresse unicast peut être configurée comme anycast.
*   Exemple : Une adresse GUA `2001:db8::1` utilisée comme anycast sur plusieurs serveurs.

## 📦 Structure de l'Adresse IPv6

Une adresse IPv6 est un nombre de 128 bits, généralement représenté sous forme de huit groupes de quatre chiffres hexadécimaux, séparés par des deux-points (par exemple, `ABCD:EF01:2345:6789:ABCD:EF01:2345:6789`).

| Champ             | Taille (bits) | Description                                                               |
|-------------------|---------------|---------------------------------------------------------------------------|
| **Préfixe de routage** | Variable      | Partie réseau de l'adresse, utilisée pour le routage.                      |
| **ID de sous-réseau** | Variable      | Identifie le sous-réseau au sein de l'organisation.                         |
| **ID d'interface**  | 64            | Identifie de manière unique une interface au sein du sous-réseau.          |

La structure spécifique et l'interprétation des bits varient selon le type d'adresse :

*   **Global Unicast Address (GUA)** :
    *   Généralement, les 48 premiers bits représentent le préfixe de routage global (`/48`), les 16 bits suivants l'ID de sous-réseau (`/64`), et les 64 derniers bits l'ID d'interface.
    *   Format : `Préfixe Global (n bits) : ID Sous-réseau (m bits) : ID Interface (128-n-m bits)`. Souvent `n+m=64`.
    *   L'ID d'interface peut être généré via EUI-64 ou aléatoirement.

*   **Link-Local Address (LLA)** :
    *   Format : `fe80::/64` (les 10 premiers bits sont `1111 1110 10`, suivis de 54 zéros).
    *   Les 64 derniers bits constituent l'ID d'interface, souvent dérivé de l'adresse MAC de l'interface (via EUI-64) ou généré de manière aléatoire.

*   **Unique Local Address (ULA)** :
    *   Format : `fc00::/7` (`1111 110x` où `x` est 0 ou 1). `fd00::/8` est le préfixe recommandé pour les ULA générées aléatoirement..
    *   Les 40 bits suivants constituent un ID global pseudo-aléatoire.
    *   Les 16 bits suivants représentent le Subnet ID.
    *   Les 64 derniers bits constituent l'ID d'interface.

*   **Multicast Address** :
    *   Format : `ff` (8 bits) `flags` (4 bits) `scope` (4 bits) `group ID` (112 bits).
    *   Les `flags` indiquent des propriétés spécifiques de l'adresse multicast.
    *   Le `scope` définit la portée de l'adresse (par exemple, `1` pour interface-local, `2` pour link-local, `5` pour site-local, `e` pour global)..
    *   Le `group ID` identifie le groupe multicast spécifique.

## 🦈 Analyse Wireshark

> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole IPv6
> ipv6
>
> # Filtrer le trafic unicast global
> ipv6.addr.global_unicast
>
> # Filtrer le trafic link-local
> ipv6.addr.linklocal
>
> # Filtrer le trafic unique local (si préfixe connu)
> ipv6.addr == fd00::/8
>
> # Filtrer le trafic multicast
> ipv6.mcast_group
>
> # Filtrer le trafic vers une adresse IPv6 spécifique
> ipv6.addr == 2001:db8::1
>
> # Filtrer par adresse source ou destination
> ipv6.src == fe80::/64
> ipv6.dst == ff02::1
> ```

## 🛡️ Sécurité

> [!danger] Vulnérabilités Connues
> *   **Sniffing** :
> 	*  Les communications IPv6 ne sont pas chiffrées par défaut. Le *sniffing* de trafic est possible si un attaquant a un accès au support de transmission. Le chiffrement doit être mis en œuvre aux couches supérieures (TLS, SSH) ou via IPsec.
> 	*  *Est-ce chiffré ?* Non, pas nativement.
> * **Spoofing** :
> 	*    Le *spoofing* d'adresses IPv6 (source ou destination) est possible.
> 	*    Les adresses Link-Local sont particulièrement vulnérables au *spoofing*, ce qui peut perturber la découverte de voisins (NDP) et entraîner des attaques de type "man-in-the-middle".
> 	*    Les adresses Anycast peuvent être détournées si un attaquant peut annoncer une route plus courte, mais cela relève davantage de la sécurité du routage BGP.
> 	*    *Authentification faible ?* Oui, l'authentification des adresses elle-même est inexistante sans mécanismes additionnels comme SEND (Secure Neighbor Discovery) pour les Link-Local.
> * **Vie privée (Privacy Issues)** :
> 	*    Les ID d'interface basés sur EUI-64 peuvent révéler l'adresse MAC physique de l'appareil, ce qui peut être utilisé pour le suivi des utilisateurs.
> 	*    Les adresses de confidentialité (Privacy Extensions) `RFC 4941` ont été introduites pour atténuer ce risque en utilisant des ID d'interface aléatoires et temporaires.


