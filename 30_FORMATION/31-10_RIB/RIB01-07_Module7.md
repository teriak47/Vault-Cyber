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
> 3.  Décrire le mécanisme d'[[Encoding|encapsulation]] des [[Data|données]] d'[[SoftwareApplication|application]] jusqu'à la trame de liaison.
> 4.  Détailler le fonctionnement des [[NetworkSwitch|commutateurs Ethernet]] en [[NetworkAccessLayer|couche 2]], y compris l'apprentissage dynamique de la [[MacAddressTable|table d'adresses MAC]].
> 5.  Distinguer les comportements de transfert ciblé et de diffusion (flooding) des [[NetworkSwitch|commutateurs]] face aux différents types d'[[DestinationMacAddress|adresses MAC]] de destination.

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
    *   **[[SourceMacAddress|Adresse MAC Source]] (6 [[Byte|octets]])** : Identifie l'[[NetworkDevice|appareil]] émetteur de la [[DataFrames|trame]]. Essentiel pour la construction des [[MacAddressTable|tables d'adresses MAC]] des [[NetworkSwitch|commutateurs]].

*   **Longueur/Type et [[Payload|Données Encapsulées]] (48-1502 [[Byte|octets]])**
    *   **Champ Longueur/Type (2 [[Byte|octets]])** : Polyvalent, indique soit la taille du [[Payload|payload]] (Longueur) en [[Byte|octets]], soit le [[Protocol|protocole]] de [[Header|couche supérieure]] [[Encoding|encapsulé]] (Type). Ex: [[InternetProtocolVersion4|0x0800]] pour [[InternetProtocolVersion4|IPv4]], [[InternetProtocolVersion6|0x86DD]] pour [[InternetProtocolVersion6|IPv6]], [[AddressResolutionProtocol|0x0806]] pour [[AddressResolutionProtocol|ARP]].
    *   **[[Payload|Données Encapsulées]] (46-1500 [[Byte|octets]])** : Contient les informations transportées, comme un [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]] avec des [[Protocol|protocoles]] de [[Header|couches supérieures]] ([[HypertextTransferProtocol|HTTP]], [[FileTransferProtocol|FTP]], etc.). Le rôle d'[[EthernetProtocol|Ethernet]] est simplement de transporter ces [[Data|données]] de manière fiable.

*   **Contrôle d'Intégrité (4 [[Byte|octets]])**
    *   **[[FrameCheckSequence|FCS (Frame Check Sequence)]] (4 [[Byte|octets]])** : Le dernier [[Header|champ]] de la [[DataFrames|trame]]. Il contient une valeur de [[Checksum|contrôle de redondance cyclique]] ([[CyclicRedundancyCheck|CRC-32]]) calculée sur l'ensemble des [[Header|champs]] de la [[DataFrames|trame]]. Le dispositif récepteur recalcule le [[CyclicRedundancyCheck|CRC]] et le compare au [[FrameCheckSequence|FCS]] reçu. Si les valeurs ne correspondent pas, la [[DataFrames|trame]] est considérée comme corrompue et rejetée, garantissant l'[[Integrity|intégrité des données]].

### 3. Le Concept d'Encapsulation Réseau

L'[[Encoding|encapsulation]] est le processus de placement d'un [[MessageFormatting|format de message]] dans un autre, comme une lettre dans une enveloppe. Chaque [[Message|message]] informatique est [[Encoding|encapsulé]] dans une [[DataFrames|trame]] spécifique avant d'être transmis sur le [[Network|réseau]].

1.  **[[ApplicationData|Données d'Application]]** : Le [[Message|message]] original créé par l'[[SoftwareApplication|application]] ([[HypertextTransferProtocol|HTTP]], [[FileTransferProtocol|FTP]], etc.).
2.  **[[SegmentTransport|Segment Transport]]** : Ajout de l'[[Header|en-tête]] [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] avec les [[PortNumber|ports]].
3.  **[[Packet|Paquet Réseau]]** : [[Encoding|Encapsulation]] dans un [[Packet|paquet]] [[InternetProtocol|IP]] avec les [[IPAddressing|adresses IP]] [[InternetProtocolAddress|source]] et [[DestinationInternetProtocolAddress|destination]].
4.  **[[DataLinkLayerFrame|Trame Liaison]]** : [[Encoding|Encapsulation]] finale dans la [[DataFrames|trame Ethernet]] avec les [[MediaAccessControlAddress|adresses MAC]] [[SourceMacAddress|source]] et [[DestinationMacAddress|destination]].

La [[DataFrames|trame]] agit comme une enveloppe, fournissant l'adresse de destination et celle de la source. Les [[Message|messages]] mal formatés sont rejetés.

### 4. Le Paquet IPv6 : Vue Détaillée

Le [[InternetProtocol|protocole Internet]] ([[InternetProtocol|IP]]) agit comme une enveloppe postale. Les [[Header|champs]] du [[Packet|paquet]] [[InternetProtocolVersion6|IPv6]] identifient la source et la destination, et [[InternetProtocol|IP]] est responsable de l'[[Routing|acheminement]] du [[Message|message]] à travers plusieurs [[IntermediateDevice|réseaux intermédiaires]].

1.  **[[Header|En-tête Fixe]] (40 [[Byte|octets]])** : Contient la version, la classe de [[NetworkTraffic|trafic]], l'étiquette de [[NetworkTraffic|flux]], la longueur des [[Payload|données utiles]], l'[[Header|en-tête]] suivant, et la limite du nombre de tronçons.
2.  **Adresse IP Source (16 [[Byte|octets]])** : Identifie l'[[NetworkDevice|appareil]] émetteur du [[Packet|paquet]] au niveau [[InternetLayer|réseau]].
3.  **Adresse IP Destination (16 [[Byte|octets]])** : Identifie l'[[NetworkDevice|appareil]] destinataire final du [[Packet|paquet]].
4.  **[[Payload|Données Encapsulées]]** : Contient le [[SegmentTransport|segment de couche transport]] ([[TransmissionControlProtocol|TCP]]/[[UserDatagramProtocol|UDP]]) et les [[ApplicationData|données d'application]].

### 5. Les Commutateurs Ethernet : Fonctionnement en Couche 2

Les [[NetworkSwitch|commutateurs Ethernet]] opèrent au niveau de la [[NetworkAccessLayer|couche 2]] (liaison de données) du modèle OSI. Contrairement aux [[Router|routeurs]] qui utilisent les [[IPAddressing|adresses IP]], les [[NetworkSwitch|commutateurs]] prennent leurs décisions de [[Routing|transfert]] en se basant exclusivement sur les informations de l'[[Header|en-tête Ethernet]], notamment les [[MediaAccessControlAddress|adresses MAC]].

> [!NOTE] Définition Clé
> **[[MacAddressTable|Table d'adresses MAC]]** : Une table maintenue par chaque [[NetworkSwitch|commutateur]] qui associe les [[MediaAccessControlAddress|adresses MAC]] des [[NetworkDevice|appareils]] connectés à ses [[EthernetPorts|ports physiques]]. Elle est construite dynamiquement par un processus d'apprentissage intelligent.

**Processus d'Apprentissage et de Transfert d'une Trame :**

1.  **Apprentissage par la Source** : Lorsqu'un commutateur reçoit une trame sur un port (ex: FA 0/1) avec une MAC source (ex: AAAA), il enregistre dans sa table MAC que "AAAA est accessible via le port FA 0/1".
2.  **Unicast Inconnu (Flooding)** : Si la MAC de destination (ex: DDDD) n'est pas encore dans la table MAC du commutateur, celui-ci effectue un "flooding" : il envoie la trame sur tous les ports sauf le port d'entrée.
3.  **Filtrage par les Hôtes** : Tous les hôtes connectés aux ports de sortie reçoivent la trame. Seul l'hôte dont la MAC correspond à la MAC de destination accepte et traite la trame. Les autres hôtes l'ignorent.
4.  **Apprentissage Bidirectionnel** : Lorsque l'hôte destinataire (ex: H4 avec MAC DDDD) répond à l'hôte source, sa MAC source (DDDD) est apprise par le commutateur sur le port où la réponse est reçue (ex: FA 0/4). Le commutateur peut alors effectuer un transfert ciblé vers DDDD via FA 0/4 pour les communications futures.

Ce processus de commutation évite les collisions et optimise l'utilisation de la bande passante en n'envoyant les trames que vers leur destination réelle.

### 6. Gestion Dynamique de la Table MAC

*   **Durée de Vie des Entrées (Aging Time)** : Les commutateurs conservent les entrées MAC pendant environ **5 minutes (300 secondes)** par défaut. Ce minuteur est réinitialisé à chaque fois qu'une trame est reçue avec la MAC source correspondante. Si aucune trame n'est reçue pendant ce délai, l'entrée est supprimée pour libérer de la mémoire et s'adapter aux changements de topologie.

*   **Capacité de la Table** : Les commutateurs modernes peuvent stocker de milliers à des dizaines de milliers d'adresses MAC simultanément, selon leur modèle. Lorsque la table est pleine, certains commutateurs peuvent basculer vers un comportement de flooding pour les nouvelles adresses jusqu'à ce que de l'espace soit libéré.

*   **Comportements de Transfert (`Unicast`, `Multicast`, `Broadcast`)** :
    *   **Unicast connu** : Transfert ciblé vers un seul port.
    *   **Unicast inconnu** : Flooding sur tous les ports sauf le port d'entrée.
    *   **Broadcast** ((FF:FF:FF:FF:FF:FF)) : Toujours envoyé sur tous les ports.
    *   **Multicast** : Selon la configuration (par exemple, IGMP snooping pour diriger le multidiffusion uniquement vers les hôtes membres, ou flooding par défaut).

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Quels sont les deux champs de synchronisation au début d'une trame Ethernet et quel est leur rôle principal?
> > [!success]- Réponse
> > 1.  **Préambule (7 octets)** : Permet à la carte réseau réceptrice de se synchroniser avec le flux de bits et d'établir le timing.
> > 2.  **Délimiteur de Trame de Début (SFD) (1 octet)** : Signale la fin du préambule et le début des données utiles de la trame.

> [!QUESTION] Question 2
> Expliquez la différence entre une adresse MAC de destination Unicast, Multicast et Broadcast.
> > [!success]- Réponse
> > *   **Unicast** : La trame est destinée à un hôte spécifique sur le réseau. L'adresse MAC est celle d'une interface réseau unique.
> > *   **Multicast** : La trame est destinée à un groupe spécifique de hôtes qui se sont inscrits pour recevoir ces messages.
> > *   **Broadcast** : La trame est destinée à tous les hôtes sur le segment de réseau local. L'adresse MAC de destination est FF:FF:FF:FF:FF:FF.

> [!QUESTION] Question 3
> Quel est le double rôle du champ Longueur/Type dans une trame Ethernet? Citez deux valeurs typiques pour la fonction "Type".
> > [!success]- Réponse
> > Le champ Longueur/Type (2 octets) peut avoir deux fonctions distinctes selon sa valeur numérique :
> > 1.  **Longueur** : Si sa valeur est inférieure ou égale à 1500, elle indique la taille en octets des données utiles (payload) de la trame.
> > 2.  **Type** : Si sa valeur est supérieure à 1500, elle spécifie le protocole de couche supérieure encapsulé dans les données.
> >     *   Valeurs typiques :
> >         *   `0x0800` pour IPv4
> >         *   `0x0806` pour ARP
> >         *   `0x86DD` pour IPv6

> [!QUESTION] Question 4
> Décrivez les étapes du mécanisme d'apprentissage de la table MAC d'un commutateur lorsque la MAC de destination d'une trame est initialement inconnue.
> > [!success]- Réponse
> > 1.  **Réception et Apprentissage Source** : Le commutateur reçoit une trame sur un port. Il examine la MAC source de la trame et l'ajoute à sa table MAC en l'associant au port d'entrée.
> > 2.  **Unicast Inconnu (Flooding)** : Le commutateur vérifie sa table MAC pour la MAC de destination. Si cette MAC est inconnue, le commutateur envoie la trame sur tous ses ports (sauf le port d'où elle provient).
> > 3.  **Filtrage par les Hôtes** : Tous les hôtes sur le segment réseau reçoivent la trame. Seul l'hôte avec la MAC de destination correspondante accepte et traite la trame.
> > 4.  **Apprentissage Bidirectionnel** : Lorsque le hôte destinataire répond, le commutateur apprend cette nouvelle MAC (MAC source de la réponse) et l'associe au port par lequel la réponse est reçue, complétant ainsi sa table MAC pour cette paire d'appareils.

> [!QUESTION] Question 5
> Pourquoi le champ Frame Check Sequence (FCS) est-il essentiel dans une trame Ethernet?
> > [!success]- Réponse
> > Le champ FCS est essentiel pour la détection d'erreurs de transmission au niveau de la couche liaison de données. Il contient une valeur CRC-32 calculée sur l'ensemble des champs de la trame. Le dispositif récepteur effectue le même calcul et compare le résultat au FCS reçu. Si les valeurs ne correspondent pas, cela indique que la trame a été corrompue pendant la transmission, et elle est alors rejetée. Cela garantit que seules les trames intègres sont traitées, assurant la fiabilité des données.

## 🔗 Liens du Module
*   **Précédent** : [[RIB01-06_Module6]]
*   **Suivant** :[[RIB01-08_Module8]]