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
> 3. Comprendre le rôle du [[SubnetMask|SubnetMask]] dans la détermination de ces parties.
> 4. Expliquer pourquoi l'[[HierarchicalAddressing|adressage hiérarchique]] est essentiel pour l'efficacité du [[Routing|Routage]] et la [[Scalability|scalabilité]] des [[Network|réseaux]].
> 5. Différencier les [[LogicalNetwork|réseaux logiques]] des [[PhysicalNetwork|réseaux physiques]] et leurs implications.

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
*   **[[NetworkPrinter|Périphériques Réseau]]** : [[NetworkPrinter|Imprimantes réseau]], téléphones IP et autres [[EndDevices|équipements connectés]] utilisent des [[InternetProtocolVersion4|adresses IPv4]] pour [[NetworkCommunication|communiquer]].
*   **[[Router|Routeurs]]** : Chaque [[LANPort|interface]] d'un [[Router|routeur]] connectant différents [[InternetProtocol|réseaux IP]] possède sa propre [[InternetProtocolVersion4|adresse IPv4]], agissant comme [[Gateway|passerelle]] entre les [[Network|réseaux]].

### 4. Anatomie d'un Paquet IPv4
Chaque [[Packet|paquet]] [[NetworkCommunication|circulant]] sur [[Internet|Internet]] contient des informations critiques :
*   **[[SourceInternetProtocolVersion4Address|Adresse Source]]** : Identifie l'[[EndDevices|appareil]] qui envoie les [[Data|données]].
*   **[[Data|Données du Paquet]]** : Le contenu réel transporté à travers le [[Network|réseau]].
*   **[[DestinationInternetProtocolVersion4Address|Adresse de Destination]]** : Indique où les [[Data|données]] doivent arriver.
Ces [[AddressingInformation|adresses]] permettent aux [[NetworkDevice|équipements réseau]] d'[[Routing|acheminer]] les [[Data|données]] et de garantir que les réponses reviennent à l'expéditeur.

### 5. Du [[BinaryDigit|Binaire]] au Décimal : La [[InternetProtocolVersion4|Structure IPv4]]
*   Les [[InternetProtocolVersion4|adresses IPv4]] sont composées de **[[Bit|32 bits]]**.
*   Une [[Bit|séquence de 32 bits]] est difficile à mémoriser et sujette aux erreurs pour les humains (ex: `11010001101001011100100000000001`).
*   Pour faciliter la lecture et la manipulation, la [[InternetProtocolVersion4|notation décimale pointée]] a été créée.

### 6. La Notation Décimale Pointée
Le [[BinaryDigit|format binaire complet]] est regroupé et converti :
1.  **[[BinaryDigit|Format Binaire Complet]]** ([[Bit|32 bits]]) : Ex. `11010001101001011100100000000001`. Difficile à lire.
2.  **[[Byte|Regroupement en Octets]]** ([[Byte|4 x 8 bits]]) : Ex. `11010001.10100101.11001000.00000001`. Organisation en quatre groupes de 8 bits.
3.  **Conversion en Décimal** : Chaque [[Byte|octet]] est converti en valeur décimale de 0 à 255. Ex. `209.165.200.1`. Format final lisible.
*   Cette notation décimale pointée est le [[NetworkStandard|format standard]] utilisé pour [[Configuration|configurer]] et [[Identification|identifier]] les [[NetworkDevice|appareils réseau]].

### 7. Communication Multi-Réseaux et [[HierarchicalAddressing|Structure Hiérarchique]]
Pour la communication entre différents réseaux, l'[[InternetProtocolVersion4|adresse IPv4]] est divisée en deux composants essentiels :
*   **[[NetworkPortion|Partie Réseau]]** : Identifie le [[NetworkSegment|segment de réseau]] auquel l'[[EndDevices|appareil]] appartient. Tous les [[EndDevices|appareils]] d'un même [[Network|réseau]] partagent cette partie.
    *   Ex: Dans `192.168.3.X`, `192.168.3` est la [[NetworkPortion|partie réseau]].
*   **[[HostPortion|Partie Hôte]]** : Identifie l'[[HostAddress|appareil individuel]] sur le [[Network|réseau]] spécifique. Cette valeur doit être unique pour chaque [[HostAddress|hôte]] du même [[Network|réseau]].
    *   Ex: Dans `192.168.3.X`, `X` est la [[HostPortion|partie hôte]].

> [!NOTE] Règle d'Or
> Sur un [[LocalAreaNetwork|réseau local]], la [[NetworkPortion|partie réseau]] doit être identique pour tous les [[EndDevices|appareils]], tandis que la [[HostPortion|partie hôte]] doit être unique pour chacun.

### 8. Exemple : Départements sur [[NetworkSegment|Réseaux Séparés]]
Des départements (Management, Comptabilité, Ventes) peuvent être configurés sur des [[NetworkSegment|réseaux logiques distincts]] :
*   Management : `192.168.1.X`
*   Comptabilité : `192.168.2.X`
*   Ventes : `192.168.3.X`
Si un [[EndDevices|appareil]] du département Ventes (`192.168.3.X`) veut [[NetworkCommunication|communiquer]] avec un [[EndDevices|appareil]] de la Comptabilité (`192.168.2.X`), la [[NetworkCommunication|communication]] doit passer par un [[Router|routeur]], car ils sont sur des [[NetworkPortion|parties réseau]] différentes.

### 9. Le Rôle du [[SubnetMask|SubnetMask]]
Le [[SubnetMask|masque de sous-réseau]] est l'[[Tool|outil]] qui permet à un [[EndDevices|appareil]] de déterminer quelle partie d'une [[InternetProtocolVersion4|adresse IPv4]] représente le [[Network|réseau]] et quelle partie représente l'[[HostPortion|hôte]].
*   **Exemple** :
    *   [[InternetProtocolVersion4|Adresse]] : `192.168.5.11`
    *   [[SubnetMask|Masque]] : `255.255.255.0`
    *   Les trois premiers [[Byte|octets]] du [[SubnetMask|masque]] (`255.255.255`) identifient la [[NetworkPortion|partie réseau]] (`192.168.5`).
    *   Le dernier [[Byte|octet]] du [[SubnetMask|masque]] (`0`) identifie la [[HostPortion|partie hôte]] (`11`).

### 10. Pourquoi l'[[HierarchicalAddressing|Adressage Hiérarchique]] ?
L'[[HierarchicalAddressing|adressage hiérarchique]] est crucial pour :
*   **Efficacité du Routage** : Les [[Router|routeurs]] n'ont besoin de connaître que les chemins vers les [[Network|réseaux]], pas l'emplacement de chaque [[HostAddress|hôte individuel]]. Cela réduit la taille des [[RoutingTable|tables de routage]].
*   **[[Scalability|Scalabilité]]** : Permet à [[Internet|Internet]] de croître en organisant des millions d'[[EndDevices|appareils]] en [[LogicalNetwork|réseaux logiques]] gérables.
*   **Organisation** : Facilite la gestion et la [[NetworkSegmentation|segmentation des réseaux]] par département, fonction ou [[LocationData|localisation]].

### 11. [[LogicalNetwork|Réseaux Logiques]] vs [[PhysicalNetwork|Réseaux Physiques]]
Un concept puissant de l'[[IPAddressing|adressage IPv4]] est la possibilité de créer plusieurs [[LogicalNetwork|réseaux logiques]] sur une même [[PhysicalNetwork|infrastructure physique]].
*   **Scénario** : Six [[Client|ordinateurs]] connectés au même commutateur physique, mais configurés sur deux [[LogicalNetwork|réseaux logiques]] différents (ex. : `192.168.18.X` et `192.168.5.X`).
*   **Résultat** : Les [[HostAddress|hôtes]] du réseau `192.168.18` peuvent [[NetworkCommunication|communiquer]] entre eux, et ceux du réseau `192.168.5` peuvent [[NetworkCommunication|communiquer]] entre eux. Cependant, les deux groupes **ne peuvent pas** [[NetworkCommunication|communiquer]] directement sans un [[Router|routeur]].

> [!IMPORTANT]
> Un seul réseau physique peut héberger plusieurs réseaux IPv4 logiques, offrant flexibilité et segmentation pour des raisons de sécurité ou d'organisation.

### 12. Analogie : Le Système Téléphonique
L'adressage IPv4 peut être comparé au système téléphonique :
*   **Indicatif de Pays** (+33 pour la France) : Équivalent à l'identifiant de réseau principal.
*   **Indicatif Régional** (01 pour Paris) : Affine la localisation du réseau.
*   **Central Téléphonique** (XX XX) : Identifie le réseau local spécifique.
*   **Numéro Local** (XX XX) : Correspond à l'hôte individuel sur le réseau.
Cette structure hiérarchique permet d'acheminer efficacement les données à travers Internet.

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Pourquoi l'adresse IPv4 est-elle considérée comme une identité numérique essentielle dans le réseau ?
> > [!success]- Réponse
> > L'adresse IPv4 fournit une identité numérique unique à chaque appareil connecté, permettant ainsi la communication et l'acheminement correct des données de leur source à leur destination sur Internet et les réseaux locaux. Sans elle, les appareils seraient isolés.

> [!QUESTION] Question 2
> Décrivez la notation décimale pointée des adresses IPv4 et expliquez son avantage par rapport à la notation binaire complète.
> > [!success]- Réponse
> > Une adresse IPv4 est un nombre de 32 bits. La notation décimale pointée divise ces 32 bits en quatre groupes de 8 bits (octets), séparés par des points. Chaque octet est ensuite converti en sa valeur décimale correspondante, allant de 0 à 255. L'avantage est qu'elle est beaucoup plus facile à lire, à mémoriser et à manipuler pour les humains que la longue séquence binaire complète.

> [!QUESTION] Question 3
> Quelle est la "Règle d'Or" concernant les parties réseau et hôte d'une adresse IPv4 sur un réseau local ?
> > [!success]- Réponse
> > Sur un réseau local, la partie réseau de l'adresse IPv4 doit être identique pour tous les appareils afin qu'ils soient reconnus comme appartenant au même réseau. En revanche, la partie hôte doit être unique pour chaque appareil individuel sur ce réseau pour éviter les conflits.

> [!QUESTION] Question 4
> Expliquez le rôle du masque de sous-réseau dans l'adressage IPv4. Donnez un exemple.
> > [!success]- Réponse
> > Le masque de sous-réseau est un outil qui indique à un appareil quelle partie de son adresse IPv4 correspond à la partie réseau et quelle partie correspond à la partie hôte. Il est essentiel pour le appareil afin de déterminer si un autre appareil est sur le même réseau local ou sur un réseau distant. Par exemple, avec l'adresse `192.168.1.10` et un masque `255.255.255.0`, les trois premiers octets (`192.168.1`) identifient la partie réseau, et le dernier octet (`10`) identifie la partie hôte.

> [!QUESTION] Question 5
> Pourquoi l'adressage hiérarchique est-il important pour le fonctionnement d'Internet ? Citez au moins deux raisons.
> > [!success]- Réponse
> > L'adressage hiérarchique est crucial pour plusieurs raisons :
> > 1.  **Efficacité du Routage** : Il permet aux routeurs de router les paquets en se basant uniquement sur la partie réseau de l'adresse de destination, sans avoir à connaître l'emplacement de chaque hôte individuel. Cela réduit considérablement la taille des tables de routage.
> > 2.  **Scalabilité** : En organisant les millions d'appareils connectés à Internet en réseaux logiques gérables, l'adressage hiérarchique permet à Internet de croître de manière ordonnée.
> > 3.  **Organisation** : Il facilite la gestion et la segmentation des réseaux, améliorant la sécurité et la performance.

## 🔗 Liens du Module
*   **Précédent** : [[RIB01-07_Module7|01-07 | Module 7]]
*   **Suivant** : [[RIB01-09_Module9|01-09 | Module 9]] 