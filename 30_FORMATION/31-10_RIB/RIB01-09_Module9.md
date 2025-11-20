---
tags:
  - cour
  - rib
aliases:
  - Module 9
  - 01-09 | Module 9
archetype: cour
module: "RIB (Introduction au réseau)"
cssclasses:
  - max
---

# 01-09 | Module 9

> [!GOAL] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Expliquer les mécanismes fondamentaux de la [[Unicast|transmission IP unicast]], [[Broadcast|broadcast]] et [[Multicast|multicast]].
> 2. Identifier et décrire les différents types d'[[InternetProtocolVersion4.md|adressage IPv4]], y compris les [[PublicIPAddress|adresses publiques]], [[PrivateIPAddress|privées]] et à usage spécial.
> 3. Comprendre la structure hiérarchique de l'attribution mondiale des [[InternetProtocolAddressBlocks|adresses IP]] par l'[[InternetAssignedNumbersAuthority|IANA]] et les [[RegionalInternetRegistry|RIR]].
> 4. Expliquer le rôle des [[Router|routeurs]] dans la [[NetworkSegmentation|segmentation réseau]] et la gestion des [[BroadcastDomain|domaines de diffusion]].
> 5. Expliquer la problématique des grands [[BroadcastDomain|domaines de diffusion]] et les avantages du [[NetworkSegmentation|sous-réseautage]] ([[Subnetting|subnetting]]).

## 📝 Synthèse du Cours

### 1. Types de Transmission IP

Les [[Packet|paquets IP]] peuvent être transmis selon trois modes principaux :

#### A. [[Unicast|Transmission Unicast]]
- **Définition** : Communication [[OneToOneCommunications|un-à-un]], où un [[HostAddress|périphérique]] envoie un [[Message|message]] à un seul autre [[HostAddress|périphérique]] spécifique.
- **Fonctionnement** : Un [[Packet|paquet unicast]] a une [[DestinationInternetProtocolVersion4Address|adresse IP de destination]] unique. Seul le destinataire ciblé reçoit et traite le [[Packet|paquet]].
- **Point clé** : L'[[HostAddress|adresse IP source]] d'un [[Packet|paquet]] est **toujours** [[Unicast|unicast]], car un [[Packet|paquet]] ne peut provenir que d'une seule source, quelle que soit la [[DestinationInternetProtocolVersion4Address|destination]].
- **Exemple** : Un ordinateur 172.16.4.1 envoie un [[Packet|paquet]] à une [[NetworkPrinter|imprimante]] 172.16.4.253. Seule l'[[NetworkPrinter|imprimante]] reçoit.

#### B. [[Broadcast|Diffusion IPv4 (Broadcast)]]
- **Définition** : Communication un-à-tous, où un [[HostAddress|périphérique]] envoie un [[Message|message]] simultanément à **tous** les autres [[NetworkDevice|appareils]] au sein du même [[BroadcastDomain|domaine de diffusion]] ([[NetworkSegment|segment réseau]] local).
- **Adresse Spéciale** : Utilise l'[[BroadcastAddress|adresse de diffusion]] 255.255.255.255 (tous les bits à 1).
- **Inondation du Réseau** : Les [[IntermediateDevice|commutateurs Ethernet]] reçoivent le [[Packet|paquet]] et le propagent sur tous les ports (sauf celui d'entrée).
- **[[Router|Limitation des Routeurs]]** : Les [[Router|routeurs]] ne transmettent pas les [[Broadcast|paquets de diffusion]] au-delà du [[BroadcastDomain|domaine local]].
- **Types de Diffusion** :
    - **[[DirectedBroadcast|Diffusion dirigée]]** : Envoyée à tous les hôtes d'un [[NetworkSegment|réseau]] spécifique (ex: 172.16.4.255 sur le réseau 172.16.4.0/24).
    - **[[LimitedBroadcast|Diffusion limitée]]** : Envoyée à 255.255.255.255, reste confinée au [[LocalAreaNetwork|réseau local]] immédiat et ne traverse pas les [[Router|routeurs]].
- **Important** : [[InternetProtocolVersion4.md|IPv4]] utilise la [[Broadcast|diffusion]], mais [[InternetProtocolVersion6.md|IPv6]] n'a pas de paquets de [[Broadcast|diffusion]].

#### C. [[Multicast|Multidiffusion IPv4 (Multicast)]]
- **Définition** : Approche optimisée un-à-groupe, où un [[HostAddress|hôte]] envoie un seul [[Packet|paquet]] à un groupe spécifique d'[[HostAddress|hôtes]] qui se sont abonnés à ce groupe.
- **Plage Réservée** : [[InternetProtocolVersion4|IPv4]] réserve les adresses de 224.0.0.0 à 239.255.255.255 pour la [[Multicast|multidiffusion]].
- **Adresse Unique de Groupe** : Chaque groupe est représenté par une adresse de destination multicast unique.
- **Inscription au Groupe** : Les [[HostAddress|hôtes]] deviennent clients de multidiffusion en s'abonnant à un groupe spécifique.
- **Traitement Sélectif** : Seuls les membres du groupe traitent les [[Packet|paquets]], les autres [[NetworkDevice|périphériques]] les ignorent, optimisant l'utilisation des [[Resource|ressources]].
- **Applications** : Essentielle pour les [[SecureRoutingProtocols|protocoles de routage]] comme OSPF (ex: 224.0.0.5) pour communiquer efficacement entre [[Router|routeurs]].

### 2. Adressage IPv4

#### A. [[PublicIPAddress|Adresses IPv4 Publiques et Privées]]
- **[[PublicIPAddress|Adresses Publiques]]** :
    - Sont routables sur l'[[Internet|Internet]] et globalement uniques.
    - Acheminées par les [[InternetServiceProvider|fournisseurs d'accès à Internet]] (FAI) entre les [[Router|routeurs]].
    - Permettent la [[NetworkCommunication|communication mondiale]].
- **[[PrivateIPAddress|Adresses Privées]]** :
    - Définies dans la [[RequestForComments|RFC 1918]].
    - Non routables sur l'[[Internet|Internet]], utilisées pour les [[InternalNetwork|réseaux internes]] des [[Enterprise|entreprises]].
    - Peuvent être réutilisées par différentes organisations car elles ne sont pas vues de l'[[Internet|extérieur]].
    - **Plages d'adresses privées ([[RequestForComments|RFC 1918]])** :
        - **Classe A** : 10.0.0.0/8 (10.0.0.0 à 10.255.255.255) - Plus de 16 millions d'adresses.
        - **Classe B** : 172.16.0.0/12 (172.16.0.0 à 172.31.255.255) - Environ 1 million d'adresses.
        - **Classe C** : 192.168.0.0/16 (192.168.0.0 à 192.168.255.255) - Environ 65 000 adresses.
- **[[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]]** :
    - Permet aux [[HostAddress|appareils]] avec des [[PrivateIPAddress|adresses privées]] de communiquer avec l'[[Internet|extérieur]].
    - Le [[Router|routeur NAT]] traduit l'[[PrivateIPAddress|adresse source privée]] en une [[PublicIPAddress|adresse publique]] routable avant transmission.

#### B. [[LinkLocalAddress|Adresses IPv4 à Usage Spécial]]
- **[[LoopbackAddress|Adresses de Bouclage]]** :
    - Plage : 127.0.0.0/8 (127.0.0.1 à 127.255.255.254).
    - L'[[LoopbackAddress|adresse 127.0.0.1]] est utilisée par un [[HostAddress|hôte]] pour diriger le [[NetworkTraffic|trafic]] vers lui-même.
    - Sert à tester la configuration IP locale sans envoyer de [[Packet|paquets]] sur le [[Network|réseau]].
- **[[AutomaticPrivateIPAddressing|Adresses Link-Local (APIPA)]]** :
    - Plage : 169.254.0.0/16 (169.254.0.1 à 169.254.255.254).
    - Permettent l'auto-configuration d'un [[DynamicHostConfigurationProtocolClient|client]] [[OperatingSystem|Windows]] lorsqu'aucun [[DHCPServer|serveur DHCP]] n'est disponible.
    - Utilisables pour des connexions [[PeerToPeer|peer-to-peer]] simples.
- **[[NetworkAddress|Adresses Réseau]] et [[BroadcastAddress|Broadcast]]** :
    - L'[[NetworkAddress|adresse réseau]] (tous les bits [[HostPortion|hôtes]] à 0) identifie le [[Network|réseau]] lui-même.
    - L'[[BroadcastAddress|adresse de diffusion]] (tous les bits [[HostPortion|hôtes]] à 1) permet la [[Broadcast|diffusion]] à tous les [[HostAddress|hôtes]] du [[NetworkSegment|segment]].
    - Ces adresses ne peuvent **jamais** être attribuées à des [[HostAddress|hôtes]].

#### C. [[ClassfulAddressing|Évolution de l'Adressage : Du Classful au Classless]]
- **[[ClassfulAddressing|Adressage Traditionnel par Classe]] (1981-1990s)** :
    - Défini par la [[RequestForComments|RFC 790]], divisait les adresses en classes A, B et C avec des préfixes fixes (/8, /16, /24).
    - A mené à un [[Resource|gaspillage massif]] d'[[InternetProtocolVersion4|adresses IPv4]], notamment avec la classe A.
- **[[ClasslessInterDomainRouting|Adressage Sans Classe (CIDR)]] (Actuel)** :
    - Introduit au milieu des années 1990 pour remplacer l'[[ClassfulAddressing|adressage classful]].
    - Ignore les règles de classes et alloue les adresses selon les besoins réels grâce à des masques de sous-réseau de longueur variable.
    - A permis une utilisation beaucoup plus efficace de l'espace d'[[InternetProtocolVersion4|adressage IPv4]] limité.
    - La solution à long terme pour l'épuisement des adresses est l'[[InternetProtocolVersion6|IPv6]].

### 3. Architecture Mondiale de Distribution des Adresses IP

- L'[[InternetAssignedNumbersAuthority|IANA]] (Internet Assigned Numbers Authority) est l'autorité suprême.
- L'[[InternetAssignedNumbersAuthority|IANA]] attribue de grands blocs d'[[InternetProtocolAddressBlocks|adresses IP]] aux cinq [[RegionalInternetRegistry|Registres Internet Régionaux]] (RIR) :
    - **ARIN** (Amérique du Nord)
    - **RIPE NCC** (Europe, Moyen-Orient, Asie centrale)
    - **APNIC** (Asie-Pacifique)
    - **LACNIC** (Amérique Latine et Caraïbes)
    - **AFRINIC** (Afrique)
- Les [[RegionalInternetRegistry|RIR]] redistribuent ensuite ces blocs aux [[InternetServiceProvider|fournisseurs d'accès Internet]] (FAI) et aux organisations de leur région géographique.

### 4. [[NetworkSegmentation|Segmentation du Réseau]] et [[BroadcastDomain|Domaines de Diffusion]]

- **Principe de la [[Broadcast|Diffusion Ethernet]]** : Dans un [[LocalAreaNetwork|réseau local Ethernet]], les [[HostAddress|appareils]] utilisent la [[Broadcast|diffusion]] pour des protocoles comme [[AddressResolutionProtocol|ARP]] et [[DynamicHostConfigurationProtocol|DHCP]].
- **[[BroadcastDomain|Domaine de Diffusion]]** : Représente l'ensemble des [[NetworkDevice|périphériques]] qui reçoivent les [[DataFrames|trames de diffusion]] émises par n'importe quel [[HostAddress|appareil]] du groupe.
- **Rôle des [[Router|Routeurs]]** :
    - Les [[Router|routeurs]] sont cruciaux pour la [[NetworkSegmentation|segmentation réseau]] car ils ne propagent pas les messages de [[Broadcast|diffusion]] d'une interface à une autre.
    - Chaque interface d'un [[Router|routeur]] délimite un [[BroadcastDomain|domaine de diffusion]] distinct.

#### A. Problématiques des Grands Domaines de Diffusion
- **[[NetworkPerformance|Impact sur les Performances Réseau]]** : Un volume excessif de [[Broadcast|trafic de diffusion]] ralentit les [[Network|opérations réseau]].
- **Charge de Traitement des [[NetworkDevice|Périphériques]]** : Chaque [[NetworkDevice|appareil]] doit traiter tous les [[Packet|paquets de diffusion]], consommant [[Resource|CPU]] et [[Resource|mémoire]].
- **Dégradation de l'Expérience Utilisateur** : [[NetworkCongestion|Congestion du réseau]] entraînant des lenteurs et une perte de productivité.

#### B. [[Subnetting|Solution : La Création de Sous-Réseaux]]
- **[[Subnetting|Sous-réseautage]]** : Division d'un grand [[LogicalNetwork|réseau logique]] en plusieurs [[NetworkSegment|sous-réseaux]] plus petits.
- **Avantages de la [[NetworkSegmentation|Segmentation en Sous-Réseaux]]** :
    - **[[NetworkPerformance|Amélioration des Performances]]** : Réduit le [[NetworkTraffic|trafic global]] et limite la propagation des [[Broadcast|diffusions]].
    - **[[SecurityPolicy|Politiques de Sécurité]]** : Permet de définir des politiques granulaires de [[NetworkSecurity|sécurité]] et de contrôler la [[NetworkCommunication|communication]] entre [[NetworkSegment|segments]].
    - **[[Isolation|Isolation des Problèmes]]** : Limite l'impact du trafic anormal ou des activités malveillantes.
- **Stratégies de Découpage** :
    - Par emplacement géographique (bâtiments, étages).
    - Par groupe ou fonction (départements, services).
    - Par type de périphérique (serveurs, imprimantes, IoT).
    - Par niveau de sécurité (réseau invité, zone DMZ).

> [!NOTE] Définition Clé
> **[[NetworkAddressTranslation|NAT (Network Address Translation)]]** : Processus par lequel une [[Router|passerelle]] (généralement un [[Router|routeur]]) modifie l'[[InternetProtocolAddressBlocks|information d'adressage IP]] dans l'[[Header|en-tête]] d'un [[Packet|paquet]] pendant qu'il transite un [[NetworkTraffic|trafic]] d'un [[NetworkSegment|segment réseau]] à un autre, généralement pour permettre à plusieurs [[HostAddress|appareils]] sur un [[PrivateNetwork|réseau privé]] de partager une seule [[PublicIPAddress|adresse IP publique]] pour accéder à l'[[Internet|Internet]].

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Transmission IP] --> B[Unicast]
    A --> C[Broadcast IPv4]
    A --> D[Multicast IPv4]

    B --> B1[Un-à-un]
    B --> B2[Adresse de destination unique]
    B --> B3[Ex: 172.16.4.1 à 172.16.4.253]

    C --> C1[Un-à-tous (segment)]
    C --> C2[Adresse: 255.255.255.255]
    C --> C3[Commutateurs inondent]
    C --> C4[Routeurs bloquent (domaine)]
    C --> C5[Types: Dirigée, Limitée]

    D --> D1[Un-à-groupe]
    D --> D2[Plage: 224.0.0.0 - 239.255.255.255]
    D --> D3[Membres s'abonnent]
    D --> D4[Traitement sélectif]
    D --> D5[Ex: OSPF 224.0.0.5]

    E[Adressage IPv4] --> E1[Publiques]
    E --> E2[Privées (RFC 1918)]
    E --> E3[Usage Spécial]
    E --> E4[Traduction d'Adresses (NAT)]

    E1 --> E1a[Routables sur Internet]
    E1 --> E1b[Globalement uniques]

    E2 --> E2a[Non routables sur Internet]
    E2 --> E2b[Réutilisables localement]
    E2 --> E2c[Plages: 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16]

    E3 --> E3a[Bouclage (127.0.0.0/8)]
    E3 --> E3b[Link-Local (APIPA 169.254.0.0/16)]
    E3 --> E3c[Réseau et Broadcast]

    F[Architecture IP Mondiale] --> F1[IANA]
    F --> F2[RIR (ARIN, RIPE NCC, etc.)]
    F2 --> F3[FAI / Organisations]

    G[Segmentation Réseau] --> G1[Domaines de Diffusion]
    G --> G2[Rôle des Routeurs]
    G --> G3[Problématiques (Grands Domaines)]
    G --> G4[Solution (Sous-Réseaux)]

    G1 --> G1a[Définition (Couche 2)]
    G1 --> G1b[Protocoles (ARP, DHCP)]

    G2 --> G2a[Bloquent la diffusion]
    G2 --> G2b[Chaque interface = limite de domaine]

    G3 --> G3a[Impact Performances]
    G3 --> G3b[Charge Périphériques]
    G3 --> G3c[Dégradation Expérience Utilisateur]

    G4 --> G4a[Avantages]
    G4 --> G4b[Stratégies de Découpage]
    G4a --> G4a1[Meilleures Performances]
    G4a --> G4a2[Politiques Sécurité]
    G4a --> G4a3[Isolation Problèmes]

    G4b --> G4b1[Géographique]
    G4b --> G4b2[Fonction]
    G4b --> G4b3[Type de Périphérique]
    G4b --> G4b4[Niveau de Sécurité]
```

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Décrivez la principale différence entre la [[Unicast|transmission unicast]] et la [[Broadcast|transmission broadcast]] en termes de destinataires et d'efficacité.
> > [!success]- Réponse
> > La [[Unicast|transmission unicast]] cible un **seul destinataire spécifique** ([[OneToOneCommunications|un-à-un]]) et est très efficace pour les communications ciblées. La [[Broadcast|transmission broadcast]] envoie un [[Message|message]] à **tous les appareils** sur un [[BroadcastDomain|segment réseau]] ([[OneToManyCommunications|un-à-tous]]), consommant plus de [[Resource|ressources]] car tous les [[HostAddress|hôtes]] doivent traiter le [[Packet|paquet]], même s'il ne les concerne pas.

> [!QUESTION] Question 2
> Pourquoi les [[Router|routeurs]] ne transmettent-ils pas les [[Broadcast|paquets de diffusion]] au-delà de leur [[NetworkSegment|segment réseau]] immédiat ? Quel est l'impact de cette caractéristique sur les [[BroadcastDomain|domaines de diffusion]] ?
> > [!success]- Réponse
> > Les [[Router|routeurs]] agissent comme des frontières de [[BroadcastDomain|domaines de diffusion]]. Ils bloquent les [[Broadcast|paquets de diffusion]] pour éviter qu'ils ne saturent l'ensemble du [[Network|réseau]] interconnecté. Chaque interface de [[Router|routeur]] définit la limite d'un [[BroadcastDomain|domaine de diffusion]] distinct, ce qui permet de segmenter le [[Network|réseau]] et de confiner le [[Broadcast|trafic de diffusion]] à des zones plus petites.

> [!QUESTION] Question 3
> Quelles sont les trois plages d'[[PrivateIPAddress|adresses IPv4 privées]] définies par la [[RequestForComments|RFC 1918]] ? Donnez un exemple de contexte d'utilisation pour ces adresses.
> > [!success]- Réponse
> > Les trois plages d'[[PrivateIPAddress|adresses IPv4 privées]] sont :
> > 1. **Classe A** : 10.0.0.0/8 (10.0.0.0 à 10.255.255.255)
> > 2. **Classe B** : 172.16.0.0/12 (172.16.0.0 à 172.31.255.255)
> > 3. **Classe C** : 192.168.0.0/16 (192.168.0.0 à 192.168.255.255)
> > Ces adresses sont utilisées dans les [[InternalNetwork|réseaux internes]] des [[Enterprise|entreprises]] ou à domicile, car elles ne sont pas routables sur l'[[Internet|Internet]] et peuvent être réutilisées localement sans conflit global.

> [!QUESTION] Question 4
> Expliquez le concept de [[ClasslessInterDomainRouting|CIDR]] et pourquoi il a remplacé l'[[ClassfulAddressing|adressage par classe]] pour [[InternetProtocolVersion4|IPv4]].
> > [!success]- Réponse
> > Le [[ClasslessInterDomainRouting|CIDR]] (Classless Inter-Domain Routing) est une méthode d'[[IPAddressing|adressage IP]] qui ignore les règles rigides des classes A, B et C et utilise un masque de sous-réseau de longueur variable. Il a remplacé l'[[ClassfulAddressing|adressage par classe]] car ce dernier entraînait un [[Resource|gaspillage]] considérable d'[[InternetProtocolVersion4|adresses IPv4]] en raison de ses divisions fixes et inefficaces. Le [[ClasslessInterDomainRouting|CIDR]] permet une allocation plus flexible et efficace des adresses, réduisant ainsi le problème d'épuisement de l'espace d'[[InternetProtocolVersion4|adressage IPv4]].

> [!QUESTION] Question 5
> Quels sont les principaux avantages de la [[NetworkSegmentation|segmentation réseau]] en [[NetworkSegment|sous-réseaux]] ? Citez au moins trois points.
> > [!success]- Réponse
> > Les principaux avantages de la [[NetworkSegmentation|segmentation réseau]] sont :
> > 1. **[[NetworkPerformance|Amélioration des performances]]** : Réduit le [[NetworkTraffic|trafic]] de [[Broadcast|diffusion]] et le [[NetworkTraffic|trafic global]], ce qui améliore la vitesse et la réactivité du [[Network|réseau]].
> > 2. **[[SecurityPolicy|Politiques de sécurité]] accrues** : Permet de définir des règles de sécurité granulaires pour contrôler la [[NetworkCommunication|communication]] entre différents [[NetworkSegment|sous-réseaux]].
> > 3. **[[Isolation|Isolation des problèmes]]** : Limite l'impact des pannes, des erreurs de configuration ou des activités malveillantes à un seul [[NetworkSegment|segment]], évitant qu'elles ne se propagent à l'ensemble du [[Network|réseau]].

## 🔗 Liens du Module
* **Précédent** : [[RIB01-08_Module8]]
* **Suivant** : [[RIB01-10_Module10]] 
* **Ressource Externe** : [RFC 1918 - Address Allocation for Private Internets](https://datatracker.ietf.org/doc/html/rfc1918)
