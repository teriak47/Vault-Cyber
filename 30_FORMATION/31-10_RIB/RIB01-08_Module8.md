---
tags:
  - cour
  - rib
aliases:
  - Module 8
  - 01-08 | Module 8
archetype: cour
module: "RIB (Introduction au réseau)"
cssclasses:
  - max
---

# 01-08 | Module 8

> [!GOAL] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Expliquer l'importance fondamentale de l'[[InternetProtocolVersion4|Adressage IPv4]] dans la communication réseau.
> 2. Décrire la structure hiérarchique d'une [[InternetProtocolVersion4|Adresse IPv4]], distinguant la partie réseau de la partie hôte.
> 3. Comprendre le rôle du [[Masque de Sous-Réseau|Masque de Sous-Réseau]] dans la détermination de ces parties.
> 4. Expliquer pourquoi l'[[Adressage Hiérarchique|adressage hiérarchique]] est essentiel pour l'efficacité du [[Routing|Routage]] et la [[Scalability|scalabilité]] des [[Network|réseaux]].
> 5. Différencier les [[Réseau Logique|réseaux logiques]] des [[Réseau Physique|réseaux physiques]] et leurs implications.

## 📝 Synthèse du Cours

### 1. L'[[InternetProtocolVersion4|Adresse IPv4]] : Une Identité Numérique Essentielle
Dans un monde hyperconnecté, chaque [[EndDevices|appareil]] a besoin d'une identité numérique unique pour communiquer. L'[[InternetProtocolVersion4|Adresse IPv4]] est cette identité fondamentale qui permet aux [[EndDevices|ordinateurs]], [[Android|smartphones]] ou [[Server|serveurs]] d'[[NetworkCommunication|interagir]] sur [[Internet|Internet]] et les [[LocalAreaNetwork|réseaux locaux]].
*   Elle agit comme une [[AddressingInformation|adresse postale]] pour les données, assurant leur livraison de la source à la destination correcte.
*   Sans une [[InternetProtocolVersion4|adresse IPv4]] unique et configurée correctement, un [[EndDevices|appareil]] reste isolé.

### 2. [[InternetProtocolVersion4|IPv4]] en Action
*   **Sur le [[LocalAreaNetwork|Réseau Local]] ([[LocalAreaNetwork|LAN]])** : L'[[InternetProtocolVersion4|adresse IPv4]] doit être unique parmi tous les [[EndDevices|appareils]] connectés au même [[LocalAreaNetwork|LAN]] pour éviter les [[Collision|collisions]] et assurer des [[NetworkCommunication|communications locales]] claires.
*   **Sur [[Internet|Internet]]** : L'[[InternetProtocolVersion4|adresse IPv4]] doit être unique au niveau [[Internet|mondial]] pour permettre les [[NetworkCommunication|communications à distance]] (ex. : un [[Server|serveur]] en France et un [[Client|utilisateur]] au Japon).

### 3. Où Trouve-t-on les [[InternetProtocolVersion4|Adresses IPv4]] ?
Les [[InternetProtocolVersion4|adresses IPv4]] sont attribuées à de nombreux types de [[NetworkDevice|périphériques réseau]] :
*   **Stations de Travail** : Chaque [[Client|ordinateur]] possède une [[NetworkInterfaceCard|carte réseau]] ([[NetworkInterfaceCard|NIC]]) avec une [[InternetProtocolVersion4|adresse IPv4]], servant de point de connexion au [[Network|réseau]].
*   **[[Server|Serveurs]]** : Les [[Server|serveurs]] peuvent avoir plusieurs [[NetworkInterfaceCard|cartes réseau]], chacune avec sa propre [[InternetProtocolVersion4|adresse IPv4]] pour des [[NetworkCommunication|connexions multiples]] et la [[HighAvailability|redondance]].
*   **[[NetworkPrinter|Périphériques Réseau]]** : [[NetworkPrinter|Imprimantes réseau]], [[VoiceOverInternetProtocol|téléphones IP]] et autres [[EndDevices|équipements connectés]] utilisent des [[InternetProtocolVersion4|adresses IPv4]] pour [[NetworkCommunication|communiquer]].
*   **[[Router|Routeurs]]** : Chaque [[LANPort|interface]] d'un [[Router|routeur]] connectant différents [[InternetProtocol|réseaux IP]] possède sa propre [[InternetProtocolVersion4|adresse IPv4]], agissant comme [[Gateway|passerelle]] entre les [[Network|réseaux]].

### 4. [[Anatomie d'un Paquet IPv4|Anatomie d'un Paquet IPv4]]
Chaque [[Packet|paquet]] [[NetworkCommunication|circulant]] sur [[Internet|Internet]] contient des informations critiques :
*   **[[Source Internet Protocol Version 4 Address|Adresse Source]]** : Identifie l'[[EndDevices|appareil]] qui envoie les [[Data|données]].
*   **[[Data|Données du Paquet]]** : Le contenu réel transporté à travers le [[Network|réseau]].
*   **[[DestinationInternetProtocolVersion4Address|Adresse de Destination]]** : Indique où les [[Data|données]] doivent arriver.
Ces [[AddressingInformation|adresses]] permettent aux [[NetworkDevice|équipements réseau]] d'[[Routing|acheminer]] les [[Data|données]] et de garantir que les réponses reviennent à l'expéditeur.

### 5. Du [[BinaryDigit|Binaire]] au [[Décimal|Décimal]] : La [[InternetProtocolVersion4|Structure IPv4]]
*   Les [[InternetProtocolVersion4|adresses IPv4]] sont composées de **[[Bit|32 bits]]**.
*   Une [[Bit|séquence de 32 bits]] est difficile à mémoriser et sujette aux erreurs pour les humains (ex: `11010001101001011100100000000001`).
*   Pour faciliter la lecture et la manipulation, la [[InternetProtocolVersion4|notation décimale pointée]] a été créée.

### 6. La [[Notation Décimale Pointée IPv4|Notation Décimale Pointée]]
Le [[BinaryDigit|format binaire complet]] est regroupé et converti :
1.  **[[BinaryDigit|Format Binaire Complet]]** ([[Bit|32 bits]]) : Ex. `11010001101001011100100000000001`. Difficile à lire.
2.  **[[Octet|Regroupement en Octets]]** ([[Octet|4 x 8 bits]]) : Ex. `11010001.10100101.11001000.00000001`. Organisation en quatre groupes de 8 bits.
3.  **[[Décimal|Conversion en Décimal]]** : Chaque [[Octet|octet]] est converti en valeur décimale de 0 à 255. Ex. `209.165.200.1`. Format final lisible.
*   Cette [[Notation Décimale Pointée IPv4|notation décimale pointée]] est le [[NetworkStandard|format standard]] utilisé pour [[Configuration|configurer]] et [[Identification|identifier]] les [[NetworkDevice|appareils réseau]].

### 7. [[Communication Multi-Réseaux|Communication Multi-Réseaux]] et [[Adressage Hiérarchique|Structure Hiérarchique]]
Pour la [[Communication Multi-Réseaux|communication entre différents réseaux]], l'[[InternetProtocolVersion4|adresse IPv4]] est divisée en deux composants essentiels :
*   **[[NetworkPortion|Partie Réseau]]** : Identifie le [[NetworkSegment|segment de réseau]] auquel l'[[EndDevices|appareil]] appartient. Tous les [[EndDevices|appareils]] d'un même [[Network|réseau]] partagent cette partie.
    *   Ex: Dans `192.168.3.X`, `192.168.3` est la [[NetworkPortion|partie réseau]].
*   **[[HostPortion|Partie Hôte]]** : Identifie l'[[HostAddress|appareil individuel]] sur le [[Network|réseau]] spécifique. Cette valeur doit être unique pour chaque [[HostAddress|hôte]] du même [[Network|réseau]].
    *   Ex: Dans `192.168.3.X`, `X` est la [[HostPortion|partie hôte]].

> [!NOTE] Règle d'Or
> Sur un [[LocalAreaNetwork|réseau local]], la [[NetworkPortion|partie réseau]] doit être identique pour tous les [[EndDevices|appareils]], tandis que la [[HostPortion|partie hôte]] doit être unique pour chacun.

### 8. Exemple : Départements sur [[Network Segment|Réseaux Séparés]]
Des départements (Management, Comptabilité, Ventes) peuvent être configurés sur des [[Network Segment|réseaux logiques distincts]] :
*   Management : `192.168.1.X`
*   Comptabilité : `192.168.2.X`
*   Ventes : `192.168.3.X`
Si un [[EndDevices|appareil]] du département Ventes (`192.168.3.X`) veut [[NetworkCommunication|communiquer]] avec un [[EndDevices|appareil]] de la Comptabilité (`192.168.2.X`), la [[NetworkCommunication|communication]] doit passer par un [[Router|routeur]], car ils sont sur des [[NetworkPortion|parties réseau]] différentes.

### 9. Le Rôle du [[Masque de Sous-Réseau|Masque de Sous-Réseau]]
Le [[Masque de Sous-Réseau|masque de sous-réseau]] est l'[[Tool|outil]] qui permet à un [[EndDevices|appareil]] de déterminer quelle partie d'une [[InternetProtocolVersion4|adresse IPv4]] représente le [[Network|réseau]] et quelle partie représente l'[[HostPortion|hôte]].
*   **Exemple** :
    *   [[InternetProtocolVersion4|Adresse]] : `192.168.5.11`
    *   [[Masque de Sous-Réseau|Masque]] : `255.255.255.0`
    *   Les trois premiers [[Octet|octets]] du [[Masque de Sous-Réseau|masque]] (`255.255.255`) identifient la [[NetworkPortion|partie réseau]] (`192.168.5`).
    *   Le dernier [[Octet|octet]] du [[Masque de Sous-Réseau|masque]] (`0`) identifie la [[HostPortion|partie hôte]] (`11`).

### 10. Pourquoi l'[[Adressage Hiérarchique|Adressage Hiérarchique]] ?
L'[[Adressage Hiérarchique|adressage hiérarchique]] est crucial pour :
*   **[[Efficacité du Routage|Efficacité du Routage]]** : Les [[Router|routeurs]] n'ont besoin de connaître que les chemins vers les [[Network|réseaux]], pas l'emplacement de chaque [[HostAddress|hôte individuel]]. Cela réduit la taille des [[RoutingTable|tables de routage]].
*   **[[Scalability|Scalabilité]]** : Permet à [[Internet|Internet]] de croître en organisant des millions d'[[EndDevices|appareils]] en [[Réseau Logique|réseaux logiques]] gérables.
*   **[[Organisation Réseau|Organisation]]** : Facilite la [[Gestion Réseau|gestion]] et la [[NetworkSegmentation|segmentation des réseaux]] par département, fonction ou [[LocationData|localisation]].

### 11. [[Réseau Logique|Réseaux Logiques]] vs [[Réseau Physique|Réseaux Physiques]]
Un concept puissant de l'[[IPAddressing|adressage IPv4]] est la possibilité de créer plusieurs [[Réseau Logique|réseaux logiques]] sur une même [[Réseau Physique|infrastructure physique]].
*   **Scénario** : Six [[Client|ordinateurs]] connectés au même [[Commutateur|commutateur physique]], mais configurés sur deux [[Réseau Logique|réseaux logiques]] différents (ex. : `192.168.18.X` et `192.168.5.X`).
*   **Résultat** : Les [[HostAddress|hôtes]] du réseau `192.168.18` peuvent [[NetworkCommunication|communiquer]] entre eux, et ceux du réseau `192.168.5` peuvent [[NetworkCommunication|communiquer]] entre eux. Cependant, les deux groupes **ne peuvent pas** [[NetworkCommunication|communiquer]] directement sans un [[Router|routeur]].

> [!IMPORTANT]
> Un seul [[Réseau Physique|réseau physique]] peut héberger plusieurs [[Réseau Logique|réseaux IPv4 logiques]], offrant [[Flexibilité Réseau|flexibilité]] et [[NetworkSegmentation|segmentation]] pour des raisons de [[Security|sécurité]] ou d'[[Organisation Réseau|organisation]].

### 12. Analogie : Le [[Système Téléphonique|Système Téléphonique]]
L'[[Adressage Hiérarchique|adressage IPv4]] peut être comparé au [[Système Téléphonique|système téléphonique]] :
*   **[[Indicatif de Pays|Indicatif de Pays]]** (+33 pour la France) : Équivalent à l'[[NetworkAddress|identifiant de réseau principal]].
*   **[[Indicatif Régional|Indicatif Régional]]** (01 pour Paris) : Affine la [[LocationData|localisation du réseau]].
*   **[[Central Téléphonique|Central Téléphonique]]** (XX XX) : Identifie le [[LocalAreaNetwork|réseau local]] spécifique.
*   **[[Numéro Local|Numéro Local]]** (XX XX) : Correspond à l'[[HostAddress|hôte individuel]] sur le [[Network|réseau]].
Cette [[Adressage Hiérarchique|structure hiérarchique]] permet d'[[Routing|acheminer]] efficacement les [[Data|données]] à travers [[Internet|Internet]].

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Adressage IPv4] --> B[Pourquoi Essentiel?]
    B --> B1[Identité Numérique Unique]
    B --> B2[Livraison des Données]

    A --> C[IPv4 en Action]
    C --> C1[Sur Réseau Local: Unique localement]
    C --> C2[Sur Internet: Unique mondialement]

    A --> D[Où Trouve-t-on IPv4?]
    D --> D1[Stations de Travail]
    D --> D2[Serveurs]
    D --> D3[Périphériques Réseau]
    D --> D4[Routeurs]

    A --> E[Anatomie d'un Paquet IPv4]
    E --> E1[Adresse Source]
    E --> E2[Données du Paquet]
    E --> E3[Adresse de Destination]

    A --> F[Structure IPv4: Binaire au Décimal]
    F --> F1[32 bits binaires]
    F1 --> F2[Notation Décimale Pointée]
    F2 --> F3[4 Octets (0-255)]

    A --> G[Communication Multi-Réseaux]
    G --> G1[Partie Réseau]
    G --> G2[Partie Hôte]
    G1 & G2 --> H[Rôle du Masque de Sous-Réseau]
    H --> H1[Délimite Réseau/Hôte]

    A --> I[Pourquoi Adressage Hiérarchique?]
    I --> I1[Efficacité du Routage]
    I --> I2[Scalabilité]
    I --> I3[Organisation]

    A --> J[Réseaux Logiques vs Physiques]
    J --> J1[Plusieurs Logiques sur 1 Physique]
    J1 --> J2[Nécessite Routeur pour comm. inter-réseaux]

    A --> K[Analogie: Système Téléphonique]
    K --> K1[Indicatif Pays (Réseau Principal)]
    K --> K2[Indicatif Régional (Localisation Réseau)]
    K --> K3[Central Téléphonique (Réseau Local)]
    K --> K4[Numéro Local (Hôte Individuel)]
```

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Pourquoi l'[[InternetProtocolVersion4|adresse IPv4]] est-elle considérée comme une identité numérique essentielle dans le [[Network|réseau]] ?
> > [!success]- Réponse
> > L'[[InternetProtocolVersion4|adresse IPv4]] fournit une identité numérique unique à chaque [[EndDevices|appareil]] connecté, permettant ainsi la [[NetworkCommunication|communication]] et l'[[Routing|acheminement]] correct des [[Data|données]] de leur [[Source|source]] à leur [[Destination|destination]] sur [[Internet|Internet]] et les [[LocalAreaNetwork|réseaux locaux]]. Sans elle, les [[EndDevices|appareils]] seraient isolés.

> [!QUESTION] Question 2
> Décrivez la [[Notation Décimale Pointée IPv4|notation décimale pointée]] des [[InternetProtocolVersion4|adresses IPv4]] et expliquez son avantage par rapport à la [[BinaryDigit|notation binaire]] complète.
> > [!success]- Réponse
> > Une [[InternetProtocolVersion4|adresse IPv4]] est un nombre de [[Bit|32 bits]]. La [[Notation Décimale Pointée IPv4|notation décimale pointée]] divise ces [[Bit|32 bits]] en quatre groupes de [[Octet|8 bits]] ([[Octet|octets]]), séparés par des points. Chaque [[Octet|octet]] est ensuite converti en sa valeur décimale correspondante, allant de 0 à 255. L'avantage est qu'elle est beaucoup plus facile à lire, à mémoriser et à manipuler pour les humains que la longue [[BinaryDigit|séquence binaire]] complète.

> [!QUESTION] Question 3
> Quelle est la "Règle d'Or" concernant les parties [[NetworkPortion|réseau]] et [[HostPortion|hôte]] d'une [[InternetProtocolVersion4|adresse IPv4]] sur un [[LocalAreaNetwork|réseau local]] ?
> > [!success]- Réponse
> > Sur un [[LocalAreaNetwork|réseau local]], la [[NetworkPortion|partie réseau]] de l'[[InternetProtocolVersion4|adresse IPv4]] doit être identique pour tous les [[EndDevices|appareils]] afin qu'ils soient reconnus comme appartenant au même [[Network|réseau]]. En revanche, la [[HostPortion|partie hôte]] doit être unique pour chaque [[HostAddress|appareil individuel]] sur ce [[Network|réseau]] pour éviter les conflits.

> [!QUESTION] Question 4
> Expliquez le rôle du [[Masque de Sous-Réseau|masque de sous-réseau]] dans l'[[IPAddressing|adressage IPv4]]. Donnez un exemple.
> > [!success]- Réponse
> > Le [[Masque de Sous-Réseau|masque de sous-réseau]] est un [[Tool|outil]] qui indique à un [[EndDevices|appareil]] quelle partie de son [[InternetProtocolVersion4|adresse IPv4]] correspond à la [[NetworkPortion|partie réseau]] et quelle partie correspond à la [[HostPortion|partie hôte]]. Il est essentiel pour le [[EndDevices|appareil]] afin de déterminer si un autre [[EndDevices|appareil]] est sur le même [[Network|réseau]] local ou sur un [[RemoteNetwork|réseau distant]]. Par exemple, avec l'[[InternetProtocolVersion4|adresse]] `192.168.1.10` et un [[Masque de Sous-Réseau|masque]] `255.255.255.0`, les trois premiers [[Octet|octets]] (`192.168.1`) identifient la [[NetworkPortion|partie réseau]], et le dernier [[Octet|octet]] (`10`) identifie la [[HostPortion|partie hôte]].

> [!QUESTION] Question 5
> Pourquoi l'[[Adressage Hiérarchique|adressage hiérarchique]] est-il important pour le fonctionnement d'[[Internet|Internet]] ? Citez au moins deux raisons.
> > [!success]- Réponse
> > L'[[Adressage Hiérarchique|adressage hiérarchique]] est crucial pour plusieurs raisons :
> > 1.  **[[Efficacité du Routage|Efficacité du Routage]]** : Il permet aux [[Router|routeurs]] de [[Routing|router]] les [[Packet|paquets]] en se basant uniquement sur la [[NetworkPortion|partie réseau]] de l'[[InternetProtocolVersion4|adresse de destination]], sans avoir à connaître l'emplacement de chaque [[HostAddress|hôte individuel]]. Cela réduit considérablement la taille des [[RoutingTable|tables de routage]].
> > 2.  **[[Scalability|Scalabilité]]** : En organisant les millions d'[[EndDevices|appareils]] connectés à [[Internet|Internet]] en [[Réseau Logique|réseaux logiques]] gérables, l'[[Adressage Hiérarchique|adressage hiérarchique]] permet à [[Internet|Internet]] de croître de manière ordonnée.
> > 3.  **[[Organisation Réseau|Organisation]]** : Il facilite la [[Gestion Réseau|gestion]] et la [[NetworkSegmentation|segmentation des réseaux]], améliorant la [[Security|sécurité]] et la [[NetworkPerformance|performance]].

## 🔗 Liens du Module
*   **Précédent** : [[RIB01-07_Module7|01-07 | Module 7]]
*   **Suivant** : [[RIB01-09_Module9|01-09 | Module 9]] 