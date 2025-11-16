---
module: RIB
cssclasses:
  - max
---
# Transmission IP Unicast et Types d'Adressage IPv4

Découvrez les mécanismes fondamentaux de la Transmission IP Unicast et explorez les différentes méthodes de communication réseau. Ce guide complet vous permettra de maîtriser les concepts essentiels de l'Adressage IPv4, depuis la transmission un-à-un jusqu'aux communications de groupe, ainsi que les particularités des adresses publiques et privées.

# Qu'est-ce que la Transmission IP Unicast ?

La transmission Unicast représente le mode de communication le plus fondamental dans les Réseau IP. Elle fait référence à un périphérique qui envoie un message à un autre périphérique dans une communication strictement **un-à-un**.

Un Paquet Unicast possède une Adresse IP de Destination qui est une adresse unicast, destinée à **un seul destinataire**. Par exemple, lorsque l'Hôte 172.16.4.1 envoie un paquet à l'imprimante 172.16.4.253, seule cette imprimante recevra et traitera le paquet.

**Point clé** : Une Adresse IP Source ne peut être qu'une adresse unicast, car le paquet ne peut provenir que d'une seule source. Cela reste vrai indépendamment du type d'adresse de destination (unicast, broadcast ou multicast).

# Exemple Pratique de Transmission Unicast

## 01 Origine du Paquet
L'hôte avec l'Adresse IP Source **172.16.4.1** crée un paquet destiné à un périphérique spécifique

## 02 Adressage de Destination
L'Adresse IP de Destination est configurée sur **172.16.4.253**, qui correspond à l'imprimante réseau

## 03 Acheminement Ciblé
Le paquet voyage uniquement vers l'appareil désigné, sans être dupliqué vers d'autres hôtes du réseau

## 04 Réception Exclusive
Seule l'imprimante 172.16.4.253 reçoit et traite ce paquet, optimisant ainsi l'utilisation de la Bande passante

# Diffusion IPv4 (Broadcast)

La transmission par Broadcast permet à un appareil d'envoyer un message simultanément à tous les appareils d'un Réseau dans le cadre d'une communication **un-à-tous**.

### Adresse Spéciale
Un Paquet de Diffusion utilise l'adresse **255.255.255.255**, composée de 32 bits à 1, signalant une distribution universelle sur le Réseau Local

### Inondation du Réseau
Le Commutateur Ethernet reçoit le paquet et l'inonde sur tous les Port (réseau), sauf le port entrant, assurant une couverture totale

### Limitation des Routeurs
Les Routeur ne transmettent pas les paquets de diffusion vers d'autres réseaux, confinant ainsi le trafic au Domaine de Diffusion local

**Important** : IPv4 utilise des paquets de diffusion, mais il n'existe pas de paquets de diffusion avec IPv6.

# Types de Diffusion et Domaines

## Diffusion Dirigée
Envoyée à tous les hôtes d'un réseau particulier. Par exemple, un hôte sur le Sous-réseau **172.16.4.0/24** envoie un paquet à **172.16.4.255**, atteignant uniquement les appareils de ce sous-réseau spécifique.

## Diffusion Limitée
Envoyée à l'adresse **255.255.255.255**, cette diffusion reste confinée au réseau local immédiat et ne traverse jamais les routeurs.

> Performance Réseau : Les paquets de diffusion consomment des ressources et obligent chaque hôte à traiter le paquet. Le trafic de diffusion doit être limité pour ne pas dégrader les performances. Les routeurs séparent les Domaine de Diffusion, et la création de Sous-réseau peut améliorer significativement les performances en éliminant le trafic de diffusion excessif.

# Multidiffusion IPv4 (Multicast)

La Multidiffusion représente une approche optimisée qui réduit le volume du trafic en permettant à un hôte d'envoyer un seul paquet à un groupe d'hôtes désignés inscrits à un Groupe de Multidiffusion.

### Plage Réservée
IPv4 réserve les adresses **224.0.0.0** à **239.255.255.255** exclusivement pour la multidiffusion

### Adresse Unique
Chaque groupe est représenté par une seule Adresse de Destination Multidiffusion IPv4

### Inscription au Groupe
Les hôtes deviennent Client Multidiffusion en s'abonnant à un groupe spécifique via un programme client

### Traitement Sélectif
Seuls les membres du groupe traitent les paquets, les autres périphériques les ignorent

# Applications de la Multidiffusion

## Protocoles de Routage OSPF
Les [[Protocol|Protocole]] de Routage comme OSPF utilisent intensivement les transmissions multidiffusion pour optimiser les communications entre routeurs.

Par exemple, les routeurs activés avec OSPF communiquent entre eux à l'aide de l'adresse de multidiffusion réservée **224.0.0.5**. Cette approche garantit que seuls les périphériques activés avec OSPF traiteront ces paquets.

**Avantage clé** : Tous les autres périphériques du réseau ignoreront automatiquement ces paquets, préservant ainsi les ressources système et réduisant la charge de traitement inutile.

# Comparaison des Types de Transmission

### Unicast
*   **Communication** : Un-à-un
*   **Destination** : Adresse unique
*   **Efficacité** : Optimale pour communications ciblées
*   **Exemple** : 172.16.4.253

### Broadcast
*   **Communication** : Un-à-tous
*   **Destination** : Tous les appareils du réseau
*   **Efficacité** : Consomme beaucoup de ressources
*   **Exemple** : 255.255.255.255

### Multicast
*   **Communication** : Un-à-groupe
*   **Destination** : Groupe d'abonnés
*   **Efficacité** : Optimale pour distribution groupée
*   **Exemple** : 224.0.0.5

# Adresses IPv4 Publiques et Privées

Tout comme il existe différentes façons de transmettre un paquet IPv4, il existe également différents types d'adresse IPv4 avec des utilisations spécifiques.

### Adresses Publiques
Les Adresse IP Publique sont acheminées de manière globale entre les routeurs des ISP. Elles sont uniques sur Internet et permettent la communication mondiale.

### Adresses Privées
Les Adresse Privée, définies dans la RFC 1918, sont utilisées par les entreprises pour les Réseau Interne. Elles ne sont pas routables sur Internet et peuvent être réutilisées par différentes organisations.

### Contexte Historique
Introduites au milieu des années 1990 avec l'explosion du World Wide Web, les adresses privées ont été créées pour pallier l'Épuisement IPv4.

# Plages d'Adresses Privées RFC 1918

*   Classe A : **10.0.0.0/8**
    *   Plage : **10.0.0.0 à 10.255.255.255** – Idéale pour les très grandes entreprises avec plus de 16 millions d'adresses disponibles
*   Classe B : **172.16.0.0/12**
    *   Plage : **172.16.0.0 à 172.31.255.255** – Convient aux entreprises moyennes avec environ 1 million d'adresses
*   Classe C : **192.168.0.0/16**
    *   Plage : **192.168.0.0 à 192.168.255.255** – Parfaite pour les petites entreprises et réseaux domestiques avec 65 000 adresses

# [[NetworkAddressTranslation|Traduction d'Adresses Réseau]] (NAT)

Les adresses privées ne sont pas routables sur Internet. Pour permettre aux appareils utilisant des adresses privées de communiquer avec l'extérieur, nous utilisons la NAT.

### Réseau Interne
Les clients utilisent des adresses privées (ex: 192.168.1.10) pour communiquer localement

### Routeur NAT
Le Routeur [[NetworkAddressTranslation|NAT]] traduit l'Adresse IP Source privée en adresse publique avant transmission

### Internet
Le paquet circule sur Internet avec une adresse publique valide et routable

Cette opération s'effectue généralement sur le routeur qui connecte le Réseau Interne au ISP. Les paquets ayant une adresse privée doivent être traduits avant d'être transmis à un ISP.

# Adresses IPv4 à Usage Spécial

### Adresses de Bouclage
*   **Plage** : 127.0.0.0/8 (127.0.0.1 à 127.255.255.254)
*   L'Adresse de Bouclage **127.0.0.1** est utilisée par un hôte pour diriger le trafic vers lui-même. Utilisée avec la commande Ping pour tester la Configuration IP locale sans envoyer de paquets sur le réseau.

### Adresses Link-Local (APIPA)
*   **Plage** : 169.254.0.0/16 (169.254.0.1 à 169.254.255.254)
*   Appelées APIPA (Automatic Private IP Addressing), ces adresses permettent l'auto-configuration d'un client Windows lorsqu'aucun Serveur DHCP n'est disponible. Utilisables pour connexions peer-to-peer.

### Adresses Réseau et Broadcast
*   **Usage** : Identification et diffusion
*   L'[[NetworkAddress|Adresse Réseau]] (tous les bits hôtes à 0) identifie le réseau lui-même. L'Adresse Broadcast (tous les bits hôtes à 1) permet la diffusion. Ces adresses ne peuvent jamais être attribuées à des hôtes.

# Évolution de l'Adressage : Du Classful au Classless

## Adressage Traditionnel par Classe (1981-1990s)
Défini dans la RFC 790, l'Adressage Classful divisait les adresses en trois classes principales :
*   Classe A (**0.0.0.0/8 à 127.0.0.0/8**) : Préfixe (réseau) /8, plus de 16 millions d'Adresse Hôte par réseau
*   Classe B (**128.0.0.0/16 à 191.255.0.0/16**) : Préfixe /16, environ 65 000 adresses hôtes
*   Classe C (**192.0.0.0/24 à 223.255.255.0/24**) : Préfixe /24, maximum 254 hôtes

Les réseaux de Classe A représentaient 50% des adresses IPv4 disponibles, causant un gaspillage massif.

## Adressage Sans Classe (Actuel)
Au milieu des années 1990, l'adressage classful a été déprécié et remplacé par l'Adressage Sans Classe (CIDR - Classless Inter-Domain Routing).

Cette approche ignore les règles rigides des classes et alloue les adresses selon les besoins réels, permettant une utilisation beaucoup plus efficace de l'Espace d'Adressage IPv4 limité.

**Solution à long terme** : IPv6 résout définitivement le problème d'épuisement des adresses.