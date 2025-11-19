---
tags:
  - cour
  - rib
aliases:
  - Module 7
  - 01-07 | Module 7
archetype: cour
module: "RIB (Introduction au réseau)"
cssclasses:
  - max
---

# 01-07 | Module 7

> [!GOAL] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1.  Comprendre la structure et les champs fondamentaux d'une [[DataFrames|trame Ethernet]].
> 2.  Expliquer le rôle et la nature des [[MediaAccessControlAddress|adresses MAC]] [[SourceMacAddress|source]] et [[DestinationMacAddress|destination]] dans la [[NetworkCommunication|communication réseau]].
> 3.  Décrire le mécanisme d'[[Encoding|encapsulation]] des [[Data|données]] d'[[Application|application]] jusqu'à la [[TrameLiaison|trame de liaison]].
> 4.  Détailler le fonctionnement des [[Switch|commutateurs Ethernet]] en [[NetworkAccessLayer|couche 2]], y compris l'apprentissage dynamique de la [[MacAddressTable|table d'adresses MAC]].
> 5.  Distinguer les comportements de [[TransfertCible|transfert ciblé]] et de [[Flooding|diffusion]] (flooding) des [[Switch|commutateurs]] face aux différents types d'[[DestinationMacAddress|adresses MAC]] de destination.

## 📝 Synthèse du Cours

### 1. Fondement des Réseaux Locaux et Rôle des Adresses MAC

[[EthernetProtocol|Ethernet]] est la [[NetworkStandard|technologie standard]] universellement adoptée pour les [[LocalAreaNetwork|réseaux locaux]] ([[LocalAreaNetwork|LAN]]). Chaque [[NetworkDevice|appareil]] accède au [[Network|réseau]] via une [[NetworkInterfaceCard|carte réseau]] munie d'une [[MediaAccessControlAddress|adresse MAC]] unique.

> [!NOTE] Définition Clé
> **[[MediaAccessControlAddress|Adresse MAC (Media Access Control)]]** : Un identifiant unique de 48 [[Bit|bits]] (6 [[Byte|octets]]), gravé de manière permanente dans la [[NetworkInterfaceCard|carte réseau]] par le fabricant. Elle garantit l'unicité de chaque [[NetworkInterfaceCard|interface réseau]] sur le [[Internet|réseau mondial]].

Les [[MediaAccessControlAddress|adresses MAC]] de [[SourceMacAddress|source]] et de [[DestinationMacAddress|destination]] sont des [[Header|champs]] essentiels dans chaque [[DataFrames|trame Ethernet]]. Elles permettent l'[[Identification|identification]] précise de l'émetteur et du destinataire au niveau de la [[NetworkAccessLayer|couche liaison de données]], formant le fondement de la [[NetworkCommunication|communication]] au sein d'un [[LocalAreaNetwork|réseau local]].

### 2. Anatomie Complète d'une Trame Ethernet

Une [[DataFrames|trame Ethernet]] est composée de plusieurs [[FrameFormat|champs structurés]], chacun ayant un rôle spécifique dans la [[DataTransmission|transmission des données]]. Les valeurs indiquées représentent le nombre d'[[Byte|octets]] (pour obtenir la taille en [[Bit|bits]], multipliez par 8).

*   **Champs de Synchronisation (8 [[Byte|octets]])**
    *   **Préambule (7 [[Byte|octets]])** : Séquence alternée de 0 et 1 (10101010...) permettant à la [[NetworkInterfaceCard|carte réseau]] réceptrice de se synchroniser avec le [[BinaryDigit|flux de bits]] et d'établir le timing pour la réception des [[Data|données]].
    *   **[[StartFrameDelimiter|Délimiteur de Trame de Début (SFD)]] (1 [[Byte|octet]])** : Séquence 10101011 qui signale la fin du préambule et le début de l'information réelle de la [[DataFrames|trame]].

*   **Adresses de Communication (12 [[Byte|octets]])**
    *   **[[DestinationMacAddress|Adresse MAC de Destination]] (6 [[Byte|octets]])** : Identifie le [[Host|destinataire]] final de la [[DataFrames|trame]] sur le [[LocalAreaNetwork|réseau local]]. Elle peut être:
        *   [[OneToOneCommunications|Unicast]] : Pour un [[Host|destinataire]] unique.
        *   [[Multicast|Multicast]] : Pour un groupe de [[Host|hôtes]].
        *   [[Broadcast|Broadcast]] : Pour tous les [[Host|hôtes]] du [[Network|réseau]] ([[HexadecimalValues|FF:FF:FF:FF:FF:FF]]).
    *   **[[SourceMacAddress|Adresse MAC Source]] (6 [[Byte|octets]])** : Identifie l'[[NetworkDevice|appareil]] émetteur de la [[DataFrames|trame]]. Essentiel pour la construction des [[MacAddressTable|tables d'adresses MAC]] des [[Switch|commutateurs]].

*   **Longueur/Type et [[Payload|Données Encapsulées]] (48-1502 [[Byte|octets]])**
    *   **Champ Longueur/Type (2 [[Byte|octets]])** : Polyvalent, indique soit la taille du [[Payload|payload]] ([[LongueurChamp|Longueur]]) en [[Byte|octets]], soit le [[Protocol|protocole]] de [[Header|couche supérieure]] [[Encoding|encapsulé]] ([[TypeChamp|Type]]). Ex: [[InternetProtocolVersion4|0x0800]] pour [[InternetProtocolVersion4|IPv4]], [[InternetProtocolVersion6|0x86DD]] pour [[InternetProtocolVersion6|IPv6]], [[AddressResolutionProtocol|0x0806]] pour [[AddressResolutionProtocol|ARP]].
    *   **[[Payload|Données Encapsulées]] (46-1500 [[Byte|octets]])** : Contient les informations transportées, comme un [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]] avec des [[Protocol|protocoles]] de [[Header|couches supérieures]] ([[HypertextTransferProtocol|HTTP]], [[FileTransferProtocol|FTP]], etc.). Le rôle d'[[EthernetProtocol|Ethernet]] est simplement de transporter ces [[Data|données]] de manière fiable.

*   **Contrôle d'Intégrité (4 [[Byte|octets]])**
    *   **[[FrameCheckSequence|FCS (Frame Check Sequence)]] (4 [[Byte|octets]])** : Le dernier [[Header|champ]] de la [[DataFrames|trame]]. Il contient une valeur de [[Checksum|contrôle de redondance cyclique]] ([[CyclicRedundancyCheck|CRC-32]]) calculée sur l'ensemble des [[Header|champs]] de la [[DataFrames|trame]]. Le dispositif récepteur recalcule le [[CyclicRedundancyCheck|CRC]] et le compare au [[FrameCheckSequence|FCS]] reçu. Si les valeurs ne correspondent pas, la [[DataFrames|trame]] est considérée comme corrompue et rejetée, garantissant l'[[Integrity|intégrité des données]].

### 3. Le Concept d'Encapsulation Réseau

L'[[Encoding|encapsulation]] est le processus de placement d'un [[MessageFormatting|format de message]] dans un autre, comme une lettre dans une enveloppe. Chaque [[Message|message]] informatique est [[Encoding|encapsulé]] dans une [[DataFrames|trame]] spécifique avant d'être transmis sur le [[Network|réseau]].

1.  **[[DonneesApplication|Données d'Application]]** : Le [[Message|message]] original créé par l'[[Application|application]] ([[HypertextTransferProtocol|HTTP]], [[FileTransferProtocol|FTP]], etc.).
2.  **[[SegmentTransport|Segment Transport]]** : Ajout de l'[[Header|en-tête]] [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] avec les [[PortNumber|ports]].
3.  **[[Packet|Paquet Réseau]]** : [[Encoding|Encapsulation]] dans un [[Packet|paquet]] [[InternetProtocol|IP]] avec les [[IPAddressing|adresses IP]] [[InternetProtocolAddress|source]] et [[DestinationInternetProtocolAddress|destination]].
4.  **[[TrameLiaison|Trame Liaison]]** : [[Encoding|Encapsulation]] finale dans la [[DataFrames|trame Ethernet]] avec les [[MediaAccessControlAddress|adresses MAC]] [[SourceMacAddress|source]] et [[DestinationMacAddress|destination]].

La [[DataFrames|trame]] agit comme une enveloppe, fournissant l'adresse de [[Destination|destination]] et celle de la [[Source|source]]. Les [[Message|messages]] mal formatés sont rejetés.

### 4. Le Paquet IPv6 : Vue Détaillée

Le [[InternetProtocol|protocole Internet]] ([[InternetProtocol|IP]]) agit comme une enveloppe postale. Les [[Header|champs]] du [[Packet|paquet]] [[InternetProtocolVersion6|IPv6]] identifient la [[Source|source]] et la [[Destination|destination]], et [[InternetProtocol|IP]] est responsable de l'[[Routing|acheminement]] du [[Message|message]] à travers plusieurs [[IntermediateDevice|réseaux intermédiaires]].

1.  **[[Header|En-tête Fixe]] (40 [[Byte|octets]])** : Contient la version, la classe de [[NetworkTraffic|trafic]], l'étiquette de [[NetworkTraffic|flux]], la longueur des [[Payload|données utiles]], l'[[Header|en-tête]] suivant, et la limite du nombre de tronçons.
2.  **[[AdresseIPSource|Adresse IP Source]] (16 [[Byte|octets]])** : Identifie l'[[NetworkDevice|appareil]] émetteur du [[Packet|paquet]] au niveau [[InternetLayer|réseau]].
3.  **[[AdresseIPDestination|Adresse IP Destination]] (16 [[Byte|octets]])** : Identifie l'[[NetworkDevice|appareil]] destinataire final du [[Packet|paquet]].
4.  **[[Payload|Données Encapsulées]]** : Contient le [[SegmentTransport|segment de couche transport]] ([[TransmissionControlProtocol|TCP]]/[[UserDatagramProtocol|UDP]]) et les [[DonneesApplication|données d'application]].

### 5. Les Commutateurs Ethernet : Fonctionnement en Couche 2

Les [[Switch|commutateurs Ethernet]] opèrent au niveau de la [[NetworkAccessLayer|couche 2]] ([[LiaisonDeDonnees|liaison de données]]) du [[OSIModel|modèle OSI]]. Contrairement aux [[Router|routeurs]] qui utilisent les [[IPAddressing|adresses IP]], les [[Switch|commutateurs]] prennent leurs décisions de [[Routing|transfert]] en se basant exclusivement sur les informations de l'[[Header|en-tête Ethernet]], notamment les [[MediaAccessControlAddress|adresses MAC]].

> [!NOTE] Définition Clé
> **[[MacAddressTable|Table d'adresses MAC]]** : Une table maintenue par chaque [[Switch|commutateur]] qui associe les [[MediaAccessControlAddress|adresses MAC]] des [[NetworkDevice|appareils]] connectés à ses [[EthernetPorts|ports physiques]]. Elle est construite dynamiquement par un processus d'[[ApprentissageDynamique|apprentissage intelligent]].

**Processus d'Apprentissage et de Transfert d'une Trame :**

1.  **Apprentissage par la [[Source|Source]]** : Lorsqu'un [[Switch|commutateur]] reçoit une [[DataFrames|trame]] sur un [[LANPort|port]] (ex: FA 0/1) avec une [[SourceMacAddress|MAC source]] (ex: AAAA), il enregistre dans sa [[MacAddressTable|table MAC]] que "AAAA est accessible via le [[LANPort|port]] FA 0/1".
2.  **[[UnicastInconnu|Unicast Inconnu]] ([[Flooding|Flooding]])** : Si la [[DestinationMacAddress|MAC de destination]] (ex: DDDD) n'est pas encore dans la [[MacAddressTable|table MAC]] du [[Switch|commutateur]], celui-ci effectue un "[[Flooding|flooding]]" : il envoie la [[DataFrames|trame]] sur tous les [[LANPort|ports]] sauf le [[LANPort|port]] d'entrée.
3.  **Filtrage par les [[Host|Hôtes]]** : Tous les [[Host|hôtes]] connectés aux [[LANPort|ports]] de [[OutputDevices|sortie]] reçoivent la [[DataFrames|trame]]. Seul l'[[Host|hôte]] dont la [[MediaAccessControlAddress|MAC]] correspond à la [[DestinationMacAddress|MAC de destination]] accepte et traite la [[DataFrames|trame]]. Les autres [[Host|hôtes]] l'ignorent.
4.  **Apprentissage Bidirectionnel** : Lorsque l'[[Host|hôte]] destinataire (ex: H4 avec MAC DDDD) répond à l'[[Host|hôte]] [[Source|source]], sa [[SourceMacAddress|MAC source]] (DDDD) est apprise par le [[Switch|commutateur]] sur le [[LANPort|port]] où la réponse est reçue (ex: FA 0/4). Le [[Switch|commutateur]] peut alors effectuer un [[TransfertCible|transfert ciblé]] vers DDDD via FA 0/4 pour les [[TransmissionSuivantes|communications futures]].

Ce processus de [[Commutation|commutation]] évite les [[Collision|collisions]] et optimise l'[[Bandwidth|utilisation de la bande passante]] en n'envoyant les [[DataFrames|trames]] que vers leur [[Destination|destination]] réelle.

### 6. Gestion Dynamique de la Table MAC

*   **Durée de Vie des Entrées ([[AgingTime|Aging Time]])** : Les [[Switch|commutateurs]] conservent les entrées [[MediaAccessControlAddress|MAC]] pendant environ **5 minutes (300 [[Seconde|secondes]])** par défaut. Ce [[Timer|minuteur]] est réinitialisé à chaque fois qu'une [[DataFrames|trame]] est reçue avec la [[MediaAccessControlAddress|MAC source]] correspondante. Si aucune [[DataFrames|trame]] n'est reçue pendant ce délai, l'entrée est supprimée pour libérer de la [[Memory|mémoire]] et s'adapter aux changements de [[NetworkTopology|topologie]].

*   **Capacité de la [[MacAddressTable|Table]]** : Les [[Switch|commutateurs]] modernes peuvent stocker de milliers à des dizaines de milliers d'[[MediaAccessControlAddress|adresses MAC]] simultanément, selon leur modèle. Lorsque la [[MacAddressTable|table]] est pleine, certains [[Switch|commutateurs]] peuvent basculer vers un comportement de [[Flooding|flooding]] pour les nouvelles [[MediaAccessControlAddress|adresses]] jusqu'à ce que de l'espace soit libéré.

*   **Comportements de [[Transfert|Transfert]] (`Unicast`, `Multicast`, `Broadcast`)** :
    *   **[[UnicastConnu|Unicast connu]]** : [[TransfertCible|Transfert ciblé]] vers un seul [[LANPort|port]].
    *   **[[UnicastInconnu|Unicast inconnu]]** : [[Flooding|Flooding]] sur tous les [[LANPort|ports]] sauf le [[LANPort|port]] d'entrée.
    *   **[[Broadcast|Broadcast]]** (([[HexadecimalValues|FF:FF:FF:FF:FF:FF]])) : Toujours envoyé sur tous les [[LANPort|ports]].
    *   **[[Multicast|Multicast]]** : Selon la configuration (par exemple, [[IGMPSnooping|IGMP snooping]] pour diriger le [[Multicast|multidiffusion]] uniquement vers les [[Host|hôtes]] membres, ou [[Flooding|flooding]] par défaut).

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Trame Ethernet] --> B[Champs de Synchronisation]
    A --> C[Adresses de Communication]
    A --> D[Longueur/Type & Données]
    A --> E[Contrôle d'Intégrité (FCS)]

    B --> B1[Préambule (7 octets)]
    B --> B2[Délimiteur de Trame (SFD) (1 octet)]

    C --> C1[Adresse MAC Dest. (6 octets)]
    C --> C2[Adresse MAC Source (6 octets)]
    C1 --> C1a[Unicast]
    C1 --> C1b[Multicast]
    C1 --> C1c[Broadcast (FF:FF:FF:FF:FF:FF)]

    D --> D1[Champ Longueur/Type (2 octets)]
    D --> D2[Données Encapsulées (46-1500 octets)]
    D1 --> D1a[Indique taille du payload]
    D1 --> D1b[Spécifie protocole supérieur (IPv4, IPv6, ARP)]

    E --> E1[CRC-32]
    E1 --> E2[Détection d'erreurs, intégrité des données]

    F[Commutateur Ethernet (Couche 2)] --> G[Table d'Adresses MAC]
    G --> H[Apprentissage Dynamique]
    G --> I[Décisions de Transfert]

    H --> H1[Apprentissage Source]
    H --> H2[Apprentissage Bidirectionnel]

    I --> I1[Unicast connu --> Transfert Ciblé]
    I --> I2[Unicast inconnu --> Flooding]
    I --> I3[Broadcast --> Flooding]
    I --> I4[Multicast --> Selon config. (IGMP Snooping ou Flooding)]

    J[Encapsulation Réseau] --> J1[Données d'Application]
    J1 --> J2[Segment Transport (TCP/UDP)]
    J2 --> J3[Paquet Réseau (IP)]
    J3 --> J4[Trame Liaison (Ethernet)]
```

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Quels sont les deux champs de synchronisation au début d'une [[DataFrames|trame Ethernet]] et quel est leur rôle principal?
> > [!success]- Réponse
> > 1.  **Préambule (7 [[Byte|octets]])** : Permet à la [[NetworkInterfaceCard|carte réseau]] réceptrice de se synchroniser avec le [[BinaryDigit|flux de bits]] et d'établir le timing.
> > 2.  **[[StartFrameDelimiter|Délimiteur de Trame de Début (SFD)]] (1 [[Byte|octet]])** : Signale la fin du préambule et le début des [[Data|données]] utiles de la [[DataFrames|trame]].

> [!QUESTION] Question 2
> Expliquez la différence entre une [[DestinationMacAddress|adresse MAC]] de [[Destination|destination]] [[OneToOneCommunications|Unicast]], [[Multicast|Multicast]] et [[Broadcast|Broadcast]].
> > [!success]- Réponse
> > *   **[[OneToOneCommunications|Unicast]]** : La [[DataFrames|trame]] est destinée à un [[Host|hôte]] spécifique sur le [[Network|réseau]]. L'[[DestinationMacAddress|adresse MAC]] est celle d'une [[NetworkInterfaceCard|interface réseau]] unique.
> > *   **[[Multicast|Multicast]]** : La [[DataFrames|trame]] est destinée à un groupe spécifique de [[Host|hôtes]] qui se sont inscrits pour recevoir ces [[Message|messages]].
> > *   **[[Broadcast|Broadcast]]** : La [[DataFrames|trame]] est destinée à tous les [[Host|hôtes]] sur le [[BroadcastDomain|segment de réseau local]]. L'[[DestinationMacAddress|adresse MAC]] de [[Destination|destination]] est [[HexadecimalValues|FF:FF:FF:FF:FF:FF]].

> [!QUESTION] Question 3
> Quel est le double rôle du champ Longueur/Type dans une [[DataFrames|trame Ethernet]]? Citez deux valeurs typiques pour la fonction "Type".
> > [!success]- Réponse
> > Le champ Longueur/Type (2 [[Byte|octets]]) peut avoir deux fonctions distinctes selon sa valeur numérique :
> > 1.  **Longueur** : Si sa valeur est inférieure ou égale à 1500, elle indique la taille en [[Byte|octets]] des [[Payload|données utiles]] (payload) de la [[DataFrames|trame]].
> > 2.  **Type** : Si sa valeur est supérieure à 1500, elle spécifie le [[Protocol|protocole]] de [[Header|couche supérieure]] [[Encoding|encapsulé]] dans les [[Payload|données]].
> >     *   Valeurs typiques :
> >         *   `0x0800` pour [[InternetProtocolVersion4|IPv4]]
> >         *   `0x0806` pour [[AddressResolutionProtocol|ARP]]
> >         *   `0x86DD` pour [[InternetProtocolVersion6|IPv6]]

> [!QUESTION] Question 4
> Décrivez les étapes du mécanisme d'apprentissage de la [[MacAddressTable|table MAC]] d'un [[Switch|commutateur]] lorsque la [[MediaAccessControlAddress|MAC]] de [[Destination|destination]] d'une [[DataFrames|trame]] est initialement inconnue.
> > [!success]- Réponse
> > 1.  **Réception et Apprentissage [[Source|Source]]** : Le [[Switch|commutateur]] reçoit une [[DataFrames|trame]] sur un [[LANPort|port]]. Il examine la [[SourceMacAddress|MAC source]] de la [[DataFrames|trame]] et l'ajoute à sa [[MacAddressTable|table MAC]] en l'associant au [[LANPort|port]] d'entrée.
> > 2.  **[[UnicastInconnu|Unicast Inconnu]] ([[Flooding|Flooding]])** : Le [[Switch|commutateur]] vérifie sa [[MacAddressTable|table MAC]] pour la [[DestinationMacAddress|MAC de destination]]. Si cette [[MediaAccessControlAddress|MAC]] est inconnue, le [[Switch|commutateur]] envoie la [[DataFrames|trame]] sur tous ses [[LANPort|ports]] (sauf le [[LANPort|port]] d'où elle provient).
> > 3.  **Filtrage par les [[Host|Hôtes]]** : Tous les [[Host|hôtes]] sur le [[NetworkSegment|segment réseau]] reçoivent la [[DataFrames|trame]]. Seul l'[[Host|hôte]] avec la [[DestinationMacAddress|MAC de destination]] correspondante accepte et traite la [[DataFrames|trame]].
> > 4.  **Apprentissage Bidirectionnel** : Lorsque le [[Host|hôte]] destinataire répond, le [[Switch|commutateur]] apprend cette nouvelle [[MediaAccessControlAddress|MAC]] ([[SourceMacAddress|MAC source]] de la réponse) et l'associe au [[LANPort|port]] par lequel la réponse est reçue, complétant ainsi sa [[MacAddressTable|table MAC]] pour cette [[NetworkDevice|paire d'appareils]].

> [!QUESTION] Question 5
> Pourquoi le champ [[FrameCheckSequence|Frame Check Sequence (FCS)]] est-il essentiel dans une [[DataFrames|trame Ethernet]]?
> > [!success]- Réponse
> > Le champ [[FrameCheckSequence|FCS]] est essentiel pour la [[Integrity|détection d'erreurs]] de [[DataTransmission|transmission]] au niveau de la [[NetworkAccessLayer|couche liaison de données]]. Il contient une valeur [[CyclicRedundancyCheck|CRC-32]] calculée sur l'ensemble des [[Header|champs]] de la [[DataFrames|trame]]. Le dispositif récepteur effectue le même calcul et compare le résultat au [[FrameCheckSequence|FCS]] reçu. Si les valeurs ne correspondent pas, cela indique que la [[DataFrames|trame]] a été corrompue pendant la [[DataTransmission|transmission]], et elle est alors rejetée. Cela garantit que seules les [[DataFrames|trames]] intègres sont traitées, assurant la fiabilité des [[Data|données]].

## 🔗 Liens du Module
*   **Précédent** : [[RIB01-06_Module6]]
*   **Suivant** :[[RIB01-08_Module8]]