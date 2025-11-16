---
module: RIB
cssclasses:
  - max
---
# Les Champs de la Trame Ethernet

Une exploration technique approfondie de la structure et du fonctionnement des trames Ethernet dans les réseaux locaux

# [[Ethernet]] : Le Fondement des Réseaux Locaux

## Technologie Standard

Ethernet est la technologie universellement adoptée pour les réseaux locaux ([[LocalAreaNetwork]]). Chaque appareil accède au réseau via une Carte Réseau (NIC) Ethernet équipée d'une Adresse MAC unique.

Cette Adresse MAC (Media Access Control) est intégrée de manière permanente lors de la fabrication de la Carte Réseau (NIC), garantissant l'unicité de chaque interface sur le réseau mondial.

## Rôle des Adresses MAC

Les adresses MAC de la source et de la destination constituent des champs essentiels dans chaque Trame Ethernet. Elles permettent l'identification précise de l'émetteur et du destinataire au niveau de la Couche Liaison de Données.

Ces adresses sont le fondement de la communication au sein d'un même Réseau Local, permettant aux commutateurs de router efficacement les trames.

# Anatomie Complète d'une Trame Ethernet

Une Trame Ethernet est composée de plusieurs champs structurés, chacun ayant un rôle spécifique dans la transmission des données. Les valeurs indiquées sous chaque champ représentent le nombre d'octets. Pour obtenir la taille en bits, multipliez simplement ces valeurs par 8.

Comprendre cette structure est fondamental pour diagnostiquer les problèmes réseau, optimiser les performances et saisir le fonctionnement de la communication au niveau de la Couche Liaison de Données du Modèle OSI.

# Les Champs de Synchronisation

## Préambule (7 octets)

Le préambule permet à la Carte Réseau (NIC) réceptrice de se synchroniser avec le flux de bits qui arrive par le câble. Il est composé d'une séquence alternée de 0 et 1 (10101010...) qui aide l'Interface Réseau à établir le timing et à se préparer à recevoir les données réelles.

Sans cette synchronisation, la NIC pourrait mal interpréter les bits de données.

## Délimiteur de Trame de Début (1 octet)

Ce champ signale à la carte d'interface réseau réceptrice que, après ce délimiteur (SFD - Start Frame Delimiter), commencera l'information réelle associée à la Trame Ethernet.

Il se termine par la séquence 10101011, marquant clairement la fin du préambule et le début des Données Utiles. C'est le signal de départ pour le traitement de la trame.

# Les Adresses de Communication

## Adresse MAC de Destination (6 octets)

L'adresse MAC de destination identifie l'hôte destinataire sur le Réseau Local. C'est l'Adresse MAC de la carte NIC où cette Trame Ethernet va arriver.

*   Unicast : pour un destinataire unique
*   Multicast : pour un groupe d'hôtes
*   Broadcast : pour tous les hôtes du réseau (FF:FF:FF:FF:FF:FF)

## Adresse MAC Source (6 octets)

L'adresse MAC source identifie l'appareil qui a créé et envoyé cette Trame Ethernet. C'est l'Adresse MAC de la Carte Réseau (NIC) Ethernet à l'origine de la transmission.

Cette information permet au destinataire de connaître l'expéditeur et facilite la construction des Table d'Adresses MAC par les commutateurs pour l'apprentissage dynamique du réseau.

# Champ Longueur/Type et Données Encapsulées

## Champ Longueur/Type (2 octets)

Ce champ polyvalent peut servir deux fonctions distinctes selon sa valeur numérique :

*   Longueur : Indique la taille des Données Utiles (Payload) en octets, c'est-à-dire combien d'octets se trouvent dans la partie données de la trame
*   Type : Spécifie le protocole de couche supérieure encapsulé (IPv4 = 0x0800, IPv6 = 0x86DD, ARP = 0x0806)

## Données Encapsulées (46-1500 octets)

Ce champ contient les informations transportées par la trame. Il peut s'agir d'un paquet IPv4 ou IPv6, accompagné d'autres protocoles de couches supérieures. Par exemple, un paquet IPv4 peut contenir un Segment TCP qui lui-même transporte des données HTTP. Ethernet ne se préoccupe pas du contenu spécifique : son rôle est simplement de transporter ces données d'une Interface Réseau à une autre de manière fiable.

# Contrôle d'Intégrité : Frame Check Sequence

## FCS - Frame Check Sequence (4 octets)

Le FCS (Frame Check Sequence) constitue le dernier champ de la Trame Ethernet et joue un rôle critique dans la détection d'erreurs de transmission.

Ce champ contient une valeur de Contrôle de Redondance Cyclique (CRC-32) calculée sur l'ensemble des champs de la trame. Le dispositif récepteur recalcule le CRC et le compare au FCS reçu.

Si les valeurs ne correspondent pas, cela indique que la trame a été corrompue pendant la transmission, et elle est alors rejetée. Ce mécanisme garantit l'intégrité des données au niveau de la Couche Liaison de Données.

# Le Concept d'Encapsulation Réseau

L'Encapsulation est le processus consistant à placer un format de message dans un autre, semblable à une lettre placée dans une enveloppe. Chaque message informatique est encapsulé dans un format spécifique appelé **Trame** avant d'être transmis sur le réseau.

1.  Données d'Application
    Le message original créé par l'application (HTTP, FTP, etc.)
2.  Segment Transport
    Ajout de l'En-tête TCP ou UDP avec les ports
3.  Paquet Réseau
    Encapsulation dans un Paquet IP avec les adresses IP
4.  Trame Liaison
    Encapsulation finale dans la Trame Ethernet avec les adresses MAC

La Trame fait office d'enveloppe : elle fournit l'adresse de la destination souhaitée et celle de l'hôte source. Les messages mal formatés ne sont ni livrés ni traités par l'hôte de destination.

# Le Paquet IPv6 : Vue Détaillée

Le protocole Internet (IP) a une fonction similaire à celle d'une enveloppe postale. Les champs du Paquet IPv6 identifient la source et la destination du paquet. IP est responsable de l'acheminement du message de la source vers la destination, potentiellement à travers plusieurs réseaux intermédiaires.

1.  En-tête Fixe (40 octets)
    Version, classe de trafic, étiquette de flux, longueur des Données Utiles, en-tête suivant, limite de nombre de tronçons
2.  Adresse IP Source (16 octets)
    Identifie l'appareil émetteur du paquet au niveau réseau
3.  Adresse IP de Destination (16 octets)
    Identifie l'appareil destinataire final du paquet
4.  Données Encapsulées
    Contient le segment de couche transport (TCP/UDP) et les Données d'Application

# Les Commutateurs Ethernet : Fonctionnement en Couche Liaison de Données

## Principe de Fonctionnement

Les commutateurs Ethernet opèrent au niveau de la **Couche Liaison de Données (Couche Liaison de Données)** du Modèle OSI. Contrairement aux routeurs qui utilisent les adresses IP, les commutateurs prennent leurs décisions de transfert en se basant exclusivement sur les informations de l'En-tête Ethernet.

Chaque Switch (Commutateur) maintient une Table d'Adresses MAC qui associe les adresses MAC aux ports physiques du commutateur. Cette table est construite dynamiquement par apprentissage.

# Transfert d'une Trame : Exemple Pratique

Considérons un réseau avec quatre hôtes (H1, H2, H3, H4) connectés à un Switch (Commutateur). Chaque hôte possède une Adresse MAC unique (simplifiées ici en AAAA, BBBB, CCCC, DDDD).

*   **Étape 1 : Création de la Trame**
    H1 crée une Trame avec Adresse MAC Source = AAAA et Adresse MAC de Destination = DDDD pour communiquer avec H4
*   **Étape 2 : Réception par le Switch (Commutateur)**
    La Trame arrive sur le port Fast Ethernet 0/1 du Switch (Commutateur)
*   **Étape 3 : Consultation de la Table**
    Le Switch (Commutateur) consulte sa table MAC et trouve que DDDD est sur le port FA 0/4
*   **Étape 4 : Transfert Ciblé**
    La Trame est transmise uniquement vers le port FA 0/4, atteignant directement H4

Ce processus de commutation permet d'éviter les collisions et d'optimiser l'utilisation de la bande passante, car les trames ne sont envoyées que vers leur destination réelle.

# Construction de la Table d'Adresses MAC

Un Switch (Commutateur) construit sa Table d'Adresses MAC de manière dynamique par un processus d'apprentissage intelligent. Examinons ce mécanisme en détail.

## Apprentissage par la Source

Quand le Switch (Commutateur) reçoit une Trame sur le port FA 0/1 avec Adresse MAC Source = AAAA, il enregistre : "AAAA est accessible via le port FA 0/1"

## Unicast Inconnu

Si la MAC destination (DDDD) n'est pas dans la table, le Switch (Commutateur) effectue un "Flooding" : envoi sur tous les ports sauf le port entrant

## Filtrage par les Hôtes

H2 et H3 reçoivent la Trame mais l'ignorent (MAC destination ≠ leur Adresse MAC). Seul H4 (Adresse MAC = DDDD) accepte et traite la Trame

## Apprentissage Bidirectionnel

Quand H4 répond, le Switch (Commutateur) apprend "DDDD sur port FA 0/4" et peut désormais router directement vers H4

# Évolution d'une Communication : De l'Inondation au Routage Ciblé

## Première Transmission (Table Vide)

### H1 -> H4 (Trame 1)

*   MAC source AAAA apprise sur FA 0/1
*   MAC destination DDDD inconnue
*   Action : **Flooding** sur tous les ports (FA 0/2, 0/3, 0/4)
*   Résultat : H2, H3, H4 reçoivent la Trame

### H4 -> H1 (réponse)

*   MAC source DDDD apprise sur FA 0/4
*   MAC destination AAAA connue (FA 0/1)
*   Action : **Transfert ciblé** uniquement vers FA 0/1

## Transmissions Suivantes (Table Remplie)

### H1 -> H4 (Trame 2)

*   MAC source AAAA déjà connue (rafraîchissement du timer ~5 minutes)
*   MAC destination DDDD connue (FA 0/4)
*   Action : **Transfert direct** vers FA 0/4 uniquement
*   Optimisation : Aucune Trame parasite sur les ports FA 0/2 et 0/3

Le Switch (Commutateur) a donc évolué d'un comportement de Hub (diffusion) vers un comportement intelligent de commutation (filtrage et transfert ciblé), optimisant l'efficacité du réseau.

# Gestion Dynamique de la Table d'Adresses MAC

## Durée de Vie des Entrées

Les commutateurs conservent généralement les entrées MAC pendant environ **5 minutes (300 secondes)** par défaut. Ce timer, appelé *Aging Time*, est réinitialisé chaque fois qu'une Trame est reçue avec cette adresse MAC source.

Si aucune Trame n'est reçue pendant ce délai, l'entrée est supprimée pour libérer de la mémoire et s'adapter aux changements de topologie.

## Capacité de la Table

Les commutateurs modernes peuvent stocker des **milliers à dizaines de milliers** d'adresses MAC simultanément, selon le modèle et la catégorie (accès, distribution, cœur de réseau).

Lorsque la table est pleine, certains commutateurs peuvent adopter un comportement de Flooding pour les nouvelles adresses jusqu'à ce que de l'espace soit libéré.

## Unicast, Multicast, Broadcast

*   Unicast connu : transfert ciblé vers un seul port
*   Unicast inconnu : Flooding sur tous les ports sauf l'entrant
*   Broadcast (FF:FF:FF:FF:FF:FF) : toujours envoyé sur tous les ports
*   Multicast : selon la configuration (IGMP Snooping ou Flooding)

# Synthèse : La Trame Ethernet et les Commutateurs

## Structure Hiérarchique

Une Trame Ethernet est composée de champs structurés (préambule, adresses MAC, données, FCS) qui garantissent une transmission fiable et contrôlée des données au niveau de la Couche Liaison de Données.

## Identification Unique

Les adresses MAC permettent l'identification unique de chaque Interface Réseau. Elles sont essentielles pour la communication au sein d'un Réseau Local et pour le fonctionnement des commutateurs.

## Apprentissage Intelligent

Les commutateurs construisent dynamiquement leurs tables d'adresses MAC par apprentissage, optimisant progressivement le transfert des trames de la diffusion généralisée vers un routage ciblé et efficace.

## Intégrité des Données

Le champ FCS (Frame Check Sequence) assure la détection d'erreurs de transmission, garantissant que seules les trames intègres sont acceptées et traitées par les destinataires.

## Encapsulation en Couches

Ethernet encapsule les protocoles de couches supérieures (IP, TCP, HTTP) dans ses trames, permettant une architecture réseau modulaire et hiérarchisée selon le Modèle OSI.

## Optimisation Réseau

Grâce à la commutation intelligente, seules les trames nécessaires transitent sur chaque segment du réseau, réduisant les collisions et maximisant l'utilisation efficace de la bande passante disponible.

La maîtrise de la structure des trames Ethernet et du fonctionnement des commutateurs est fondamentale pour comprendre, concevoir, dépanner et optimiser les réseaux locaux modernes.