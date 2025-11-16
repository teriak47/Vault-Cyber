---
module: RIB
cssclasses:
  - max
title: L'Adressage IPv4
---

# L'Adressage IPv4

Comprendre les Fondamentaux des Adresses Réseau

## Pourquoi l'Adresse IPv4 Est-elle Essentielle ?

Dans notre monde hyperconnecté, chaque appareil a besoin d'une identité numérique unique pour communiquer. 
L'adresse IPv4 est cette identité fondamentale qui permet à votre ordinateur, smartphone ou serveur d'interagir sur Internet et sur les réseaux locaux.

Tout comme votre adresse postale permet au facteur de vous livrer du courrier, l'adresse IPv4 permet aux données de voyager de leur source à leur destination correcte. Sans cette adresse unique et correctement configurée, un appareil reste isolé, incapable de participer aux communications numériques qui définissent notre époque.

## L'Adresse IPv4 En Action

### Sur Le Réseau Local

L'adresse doit être **unique** parmi tous les appareils connectés au même réseau local. Cette unicité garantit que les communications locales se déroulent sans confusion ni collision de données.

### Sur Internet

L'adresse doit être **unique au niveau mondial** pour permettre les communications à distance. C'est ainsi qu'un serveur en France peut communiquer avec un utilisateur au Japon.

## Où Trouve-t-on Les Adresses IPv4 ?

### Stations De Travail

Chaque ordinateur possède une Carte Réseau (NIC) à laquelle est attribuée une adresse IPv4. Cette interface physique est le point de connexion entre l'appareil et le réseau.

### Serveurs

Les serveurs peuvent disposer de plusieurs cartes réseau, chacune avec sa propre adresse IPv4, permettant des connexions multiples et une redondance.

### Périphériques Réseau

Imprimantes réseau, téléphones IP et autres équipements connectés possèdent également leurs propres adresses IPv4 pour communiquer sur le réseau.

### Routeurs

Chaque interface d'un routeur qui connecte différents réseaux IP dispose de sa propre adresse IPv4, servant de [[Gateway|passerelle]] entre les réseaux.

## Anatomie D'un Paquet IPv4

-   **Adresse Source**
    Identifie l'appareil qui envoie les données
-   **Données du Paquet**
    Le contenu réel transporté à travers le réseau
-   **Adresse de Destination**
    Indique où les données doivent arriver

Chaque paquet IPv4 circulant sur Internet contient ces informations critiques. Les équipements réseau utilisent ces adresses pour acheminer les données vers leur destination et garantir que les réponses reviennent à l'expéditeur. C'est le mécanisme fondamental qui permet à Internet de fonctionner.

## Du Binaire Au Décimal : La Structure IPv4

Les adresses IPv4 sont composées de **32 bits** au niveau le plus fondamental. Imaginez devoir configurer chaque appareil avec une séquence comme celle-ci :

`11010001010010110110010000000001`

Impossible à mémoriser et extrêmement sujet aux erreurs ! C'est pourquoi les concepteurs d'IPv4 ont créé un système de notation plus convivial pour les humains.

## La Notation Décimale Pointée

### 1. Format Binaire Complet (32 bits)

`11010001010010110110010000000001`

Difficile à lire et à manipuler

### 2. Regroupement En Octets (4 × 8 bits)

`11010001.10100101.11001000.00000001`

Organisation en quatre groupes de 8 bits

### 3. Conversion En Décimal

`209.165.200.1`

Format final lisible et utilisable

Chaque groupe de 8 bits (octet) peut représenter une valeur décimale de 0 à 255. Cette notation décimale pointée est le format standard que nous utilisons quotidiennement pour configurer et identifier les appareils réseau.

## Communication Multi-Réseaux

Lorsque nous étendons notre perspective au-delà d'un simple réseau local, une question cruciale se pose : Comment un appareil sait-il si un autre appareil se trouve sur le même réseau ou sur un réseau différent ?

La réponse réside dans la structure hiérarchique des adresses IPv4. Chaque adresse contient deux composants essentiels qui permettent cette distinction : une partie réseau et une partie hôte individuel sur ce réseau.

## Structure Hiérarchique : Réseau Et Hôte

### Partie Réseau

`192.168.3.X`

Les trois premiers octets identifient le réseau local. Tous les appareils d'un même réseau partagent cette partie commune de leur adresse.

### Partie Hôte

`192.168.3.X`

Le dernier octet identifie l'appareil individuel sur le réseau. Cette valeur doit être unique pour chaque appareil du même réseau local.

> **Règle d'Or :** Sur un réseau local, la partie réseau doit être identique pour tous les appareils, tandis que la partie hôte doit être unique pour chacun.

## Exemple : Départements Sur Réseaux Séparés

### Management

`192.168.1.X`

-   PC Manager : `192.168.1.10`
-   Imprimante : `192.168.1.20`

### Comptabilité

`192.168.2.X`

-   PC Comptable : `192.168.2.10`
-   Serveur : `192.168.2.5`

### Ventes

`192.168.3.X`

-   PC Commercial : `192.168.3.10`
-   Téléphone IP : `192.168.3.25`

Chaque département fonctionne sur un réseau logique distinct, identifié par les trois premiers octets de l'adresse. Si un appareil du département des ventes (`192.168.3.X`) souhaite communiquer avec un appareil de la comptabilité (`192.168.2.X`), il devra passer par un routeur.

## Le Rôle Du Masque De Sous-Réseau

Le masque de sous-réseau (par exemple, `255.255.255.0`) est l'outil qui permet à un appareil de déterminer quelle partie de l'adresse IPv4 représente le réseau et quelle partie représente l'hôte.

### Exemple Pratique

Adresse : `192.168.5.11`
Masque : `255.255.255.0`

---

Réseau : `192.168.5`
Hôte : `11`

Dans notre exemple avec le masque `255.255.255.0` :

-   Les trois premiers octets (`255.255.255`) identifient la partie réseau
-   Le dernier octet (`0`) identifie la partie hôte

## Pourquoi l'Adressage Hiérarchique ?

1.  **Efficacité du Routage**
    Les routeurs n'ont besoin de connaître que les chemins vers les réseaux, pas l'emplacement de chaque hôte individuel.
2.  **Scalabilité**
    Permet à Internet de croître en organisant des millions d'appareils en réseaux logiques gérables.
3.  **Organisation**
    Facilite la gestion et la segmentation des réseaux par département, fonction ou localisation.

## Réseaux Logiques Vs Réseaux Physiques

Un concept puissant de l'adressage IPv4 est la possibilité de créer plusieurs réseaux logiques sur une même infrastructure physique.

### Scénario

Six ordinateurs connectés au même commutateur physique, mais configurés sur deux réseaux logiques différents :

-   Trois hôtes : `192.168.1.X`
-   Trois hôtes : `192.168.5.X`

### Résultat

Les hôtes du réseau `192.168.1` peuvent communiquer entre eux. Les hôtes du réseau `192.168.5` peuvent communiquer entre eux. Mais les deux groupes **ne peuvent pas** communiquer directement sans routeur.

> **Important :** Un seul réseau physique peut héberger plusieurs réseaux IPv4 logiques, offrant flexibilité et segmentation pour des raisons de sécurité ou d'organisation.

## Analogie : Le Système Téléphonique

### Indicatif De Pays

+33 pour la France
Équivalent à l'identifiant de réseau principal

### Indicatif Régional

01 pour Paris

Affine la localisation du réseau

### Central Téléphonique

XX XX

Identifie le réseau local spécifique

### Numéro Local

XX XX

Correspond à l'hôte individuel sur le réseau

Tout comme le système téléphonique utilise une structure hiérarchique pour acheminer les appels du pays à la région puis au numéro local, IPv4 utilise sa structure réseau/hôte pour acheminer efficacement les données à travers Internet.

## Points Clés à Retenir

-   **Unicité**
    Chaque adresse IPv4 doit être unique sur son réseau (local) ou sur Internet (global).
-   **Structure Hiérarchique**
    Toute adresse IPv4 se compose d'une partie réseau et d'une partie hôte.
-   **32 Bits Organisés**
    4 octets de 8 bits chacun, notés en décimal pointé pour faciliter la lecture.
-   **Masque de Sous-Réseau**
    Définit la frontière entre la partie réseau et la partie hôte de l'adresse.
-   **Routage Inter-Réseaux**
    La communication entre réseaux différents nécessite un routeur.
-   **Flexibilité Logique**
    Plusieurs réseaux logiques peuvent coexister sur une même infrastructure physique.