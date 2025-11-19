---
tags:
  - cour
  - rib
aliases:
  - Module 6
  - 01-06 | Module 6
archetype: cour
module: "RIB (Introduction au réseau)"
cssclasses:
  - max
---

# 01-06 | Module 6

> [!GOAL] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Expliquer ce qu'est un [[Switch|Switch]] réseau, son rôle et ses fonctions principales.
> 2. Décrire les trois principes fondamentaux du fonctionnement d'un [[Switch|Switch]] (écoute, apprentissage, aiguillage).
> 3. Comprendre la différence entre une [[MacAddressTable|table d'adresses MAC]] et une [[AddressResolutionProtocol|table ARP]].
> 4. Expliquer le processus par lequel un [[Switch|Switch]] remplit sa [[MacAddressTable|table d'adresses MAC]] et gère le [[Broadcast|flooding]].
> 5. Différencier un [[Switch|Switch]] d'un [[Router|routeur]] et connaître les types de [[Switch|Switches]] (non managé, managé).

## 📝 Synthèse du Cours

### 1. Le Switch Réseau : Le Standardiste Intelligent de Votre LAN

Le [[Switch|Switch]] est un [[NetworkDevice|équipement réseau]] essentiel pour les [[LocalAreaNetwork|réseaux locaux]] (LAN). Il agit comme un "standardiste intelligent" qui organise et optimise la [[NetworkCommunication|communication]] entre les [[NetworkDevice|appareils]].

*   **Description** : C'est un boîtier muni de plusieurs prises, appelées [[LANPort|ports]], où se connectent les [[EthernetPatchCable|câbles Ethernet]] de vos [[OperatingSystem|ordinateurs]], [[NetworkPrinter|imprimantes]], [[Server|serveurs]] et autres [[NetworkDevice|périphériques réseau]].
*   **Rôle essentiel** :
    *   Recevoir les [[DataFrames|messages numériques]] (appelés "trames") d'un [[NetworkDevice|appareil]].
    *   Les rediriger intelligemment et *uniquement* vers le [[NetworkDevice|périphérique]] destinataire.
    *   Assurer une [[NetworkCommunication|communication]] [[Efficiency|efficace]] et [[NetworkSecurity|sécurisée]] au sein de votre [[NetworkInfrastructure|infrastructure]].

### 2. Comment Fonctionne un Switch ? Le Principe de Base

Un [[Switch|Switch]] réseau opère selon trois principes fondamentaux, ce qui le rend bien plus intelligent qu'un simple [[BroadcastDomain|hub]] traditionnel :

1.  **Il écoute en permanence (Learning)** :
    *   Dès qu'un [[NetworkDevice|appareil]] est branché et allumé, le [[Switch|switch]] "écoute" activement les [[Message|messages]] qui transitent sur chaque [[LANPort|port]].
    *   Cela lui permet d'apprendre la [[NetworkTopology|topologie du réseau]] et de savoir quels [[NetworkDevice|appareils]] sont connectés à quels [[LANPort|ports]].
2.  **Il apprend par cœur (Building MAC Table)** :
    *   Le [[Switch|switch]] construit et maintient automatiquement une [[MacAddressTable|table d'adresses MAC]] (parfois appelée table de commutation).
    *   Cette table est un annuaire qui cartographie chaque [[MediaAccessControlAddress|adresse MAC]] d'un [[NetworkDevice|appareil]] avec le [[LANPort|port]] physique du [[Switch|switch]] auquel il est connecté.
3.  **Il aiguille intelligemment (Forwarding)** :
    *   Lorsqu'il reçoit une [[DataFrames|trame]], le [[Switch|switch]] consulte sa [[MacAddressTable|table d'adresses MAC]].
    *   Il identifie le [[DestinationMacAddress|destinataire]] et envoie la [[DataFrames|trame]] *uniquement* par le [[LANPort|port]] où se trouve le [[NetworkDevice|périphérique]] destinataire.

> [!NOTE] Switch vs Hub
> Un [[BroadcastDomain|hub]] transmet toutes les [[Data|données]] à tous les [[LANPort|ports]], générant du trafic inutile et des [[Collision|collisions]]. Un [[Switch|switch]], grâce à son intelligence, permet une [[OneToOneCommunications|communication un à un]], optimisant la [[Bandwidth|bande passante]] et la [[NetworkPerformance|performance du réseau]].

### 3. Le Cœur de l'Intelligence : La Table d'Adresses MAC

Une confusion courante est de confondre la [[MacAddressTable|table d'adresses MAC]] du [[Switch|switch]] avec la [[AddressResolutionProtocol|table ARP]]. Elles sont différentes :

*   **[[AddressResolutionProtocol|Table ARP]]** :
    *   Gérée par les [[OperatingSystem|ordinateurs]] eux-mêmes.
    *   Fait le lien entre une [[InternetProtocol|adresse IP]] (logique, couche 3 du [[InternationalOrganizationForStandardization|modèle OSI]]) et une [[MediaAccessControlAddress|adresse MAC]] (physique, couche 2).
*   **[[MacAddressTable|Table MAC du Switch]]** :
    *   Sa propre carte interne gérée par le [[Switch|switch]].
    *   Fait le lien entre une [[MediaAccessControlAddress|adresse MAC]] (physique) et un [[LANPort|port physique]] du [[Switch|switch]]. C'est son annuaire personnel.

#### Comment le Switch Remplit-il sa Table ? Un Processus Automatique

Le [[Switch|switch]] apprend dynamiquement les [[MediaAccessControlAddress|adresses MAC]] et leurs [[LANPort|ports]] associés via trois étapes clés :

1.  **Apprentissage (Learning)**
    *   Lorsqu'un [[NetworkDevice|appareil]] (ex: [[NetworkDevice|Ordinateur]] A avec [[MediaAccessControlAddress|MAC]] `AA-AA-AA-AA-AA-AA`) est connecté au [[LANPort|Port]] 1 du [[Switch|switch]] et envoie sa première [[DataFrames|trame]].
    *   Le [[Switch|switch]] reçoit cette [[DataFrames|trame]] sur le [[LANPort|Port]] 1 et enregistre : "L'[[MediaAccessControlAddress|adresse MAC]] `AA-AA-AA-AA-AA-AA` est sur le [[LANPort|Port]] 1".
    *   Cette entrée est ajoutée à la [[MacAddressTable|table d'adresses MAC]].

2.  **Filtrage et Forwarding (Aiguillage)**
    *   Si un [[NetworkDevice|appareil]] B (connecté au [[LANPort|Port]] 2) envoie une [[DataFrames|trame]] destinée à l'[[NetworkDevice|Ordinateur]] A (`AA-AA-AA-AA-AA-AA`).
    *   Le [[Switch|switch]] reçoit la [[DataFrames|trame]] sur le [[LANPort|Port]] 2.
    *   Il consulte sa [[MacAddressTable|table]] et découvre que l'[[MediaAccessControlAddress|adresse MAC]] `AA-AA-AA-AA-AA-AA` est associée au [[LANPort|Port]] 1.
    *   Le [[Switch|switch]] envoie alors la [[DataFrames|trame]] *uniquement* par le [[LANPort|Port]] 1. Les autres [[LANPort|ports]] (3, 4, 5, etc.) ne reçoivent rien, économisant ainsi la [[Bandwidth|bande passante]].

3.  **Gestion de l'Inconnu (Flooding)**
    *   Si le [[Switch|switch]] reçoit une [[DataFrames|trame]] destinée à une [[MediaAccessControlAddress|adresse MAC]] qu'il ne connaît pas (absente de sa [[MacAddressTable|table]]).
    *   Il se comporte temporairement comme un [[BroadcastDomain|hub]] : il envoie la [[DataFrames|trame]] par *tous* les [[LANPort|ports]] sauf celui d'origine. C'est le [[Broadcast|flooding]] (inondation).
    *   Si le [[NetworkDevice|destinataire]] existe sur le [[NetworkSegment|segment]], il répondra, permettant au [[Switch|switch]] d'apprendre son emplacement et de mettre à jour sa [[MacAddressTable|table]].

**Exemple de [[MacAddressTable|Table MAC]]**

| Adresse MAC (Appareil) | Port du Switch |
| :--------------------- | :------------- |
| AA-AA-AA-AA-AA-AA      | 1              |
| BB-BB-BB-BB-BB-BB      | 2              |
| CC-CC-CC-CC-CC-CC      | 3              |
| DD-DD-DD-DD-DD-DD      | 5              |

### 4. Compléments sur le Switch

#### Différence Fondamentale : [[Switch|Switch]] vs [[Router|Routeur]]

*   **[[Switch|Le Switch]]** :
    *   Travaille au [[NetworkAccessLayer|niveau 2]] (couche de liaison de [[Data|données]]) du [[InternationalOrganizationForStandardization|modèle OSI]].
    *   Gère les [[NetworkCommunication|communications]] *[[InternalNetwork|à l'intérieur]]* d'un même [[LocalAreaNetwork|réseau local]] (ex: entre les [[OperatingSystem|ordinateurs]] de votre bureau).
*   **[[Router|Le Routeur]]** :
    *   Travaille au [[InternetLayer|niveau 3]] (couche [[Network|réseau]]) du [[InternationalOrganizationForStandardization|modèle OSI]].
    *   Sert de [[Gateway|passerelle]] entre différents [[Network|réseaux]] (ex: entre votre [[HomeNetwork|réseau domestique]] et l'[[Internet|Internet]]).

#### Les Types de [[Switch|Switches]]

1.  **Non Managé (Unmanaged)** :
    *   "Branchez et ça marche" : aucune [[ConfigurationDrift|configuration]] possible ou nécessaire.
    *   Idéal pour les petites installations [[HomeNetwork|domestiques]] ou les [[Enterprise|bureaux]] simples.
    *   [[Efficiency|Économique]] et facile d'utilisation.

2.  **Managé (Managed)** :
    *   Offre un [[CentralizedAdministration|contrôle avancé]] sur le [[Network|réseau]].
    *   Permet de créer des [[QualityOfService|VLANs]] (réseaux virtuels séparés), de configurer la [[QualityOfService|Qualité de Service]] ([[QualityOfService|QoS]]) pour prioriser certains [[NetworkTrafficAnalysis|trafics]].
    *   Permet de surveiller les [[NetworkPerformance|performances]] en temps réel et d'appliquer des [[SecurityPolicy|politiques de sécurité]] sophistiquées.
    *   Utilisé principalement en [[Enterprise|environnement professionnel]] et [[Enterprise|entreprise]].

#### Avantages Clés d'un [[Switch|Switch]]

*   **[[NetworkPerformance|Performance]]** :
    *   Le [[NetworkTrafficAnalysis|trafic]] est [[Isolation|isolé]] entre les [[LANPort|ports]], ce qui réduit drastiquement les [[Collision|collisions de données]].
    *   Améliore significativement la vitesse de [[DataTransmission|transmission]] sur le [[Network|réseau]].
*   **[[NetworkSecurity|Sécurité]]** :
    *   Les [[NetworkDevice|appareils]] ne "voient" que le [[NetworkTrafficAnalysis|trafic]] qui leur est destiné ou le [[Broadcast|trafic broadcast]].
    *   Ceci rend l'[[Eavesdropping|écoute passive]] du [[Network|réseau]] ([[Wireshark|sniffing]]) beaucoup plus difficile.
*   **[[Efficiency|Efficacité]]** :
    *   La [[Bandwidth|bande passante]] est optimisée car elle n'est pas gaspillée à [[Broadcast|diffuser des données]] à tous les [[NetworkDevice|appareils]].
    *   Chaque [[NetworkCommunication|communication]] utilise uniquement les [[Resource|ressources]] nécessaires.

### 5. Récapitulatif en Image Mentale

Votre [[LocalAreaNetwork|réseau local]] est une petite ville. Chaque [[NetworkDevice|appareil]] est une maison avec une [[MediaAccessControlAddress|adresse postale unique (l'adresse MAC)]]. Le [[Switch|switch]] est le centre de tri postal intelligent. Il apprend quelle maison ([[MediaAccessControlAddress|adresse MAC]]) se trouve sur quelle rue ([[LANPort|port du switch]]). Quand une [[DataFrames|lettre (trame)]] arrive pour une maison, le centre de tri la met directement dans le camion de livraison de la bonne rue, au lieu de déposer une copie de la lettre dans toutes les boîtes aux lettres de la ville.

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Switch Réseau] --> B[Rôle: Standardiste Intelligent LAN]
    B --> C[Reçoit Trames]
    B --> D[Redirige Intelligemment]
    D --> E[Communication Efficace & Sécurisée]

    A --> F[3 Principes de Fonctionnement]
    F --> F1[1. Écoute Permanente]
    F --> F2[2. Apprend par Cœur]
    F --> F3[3. Aiguille Intelligemment]

    F2 --> G[Construit Table MAC]
    G --> G1[Lien MAC <--> Port Switch]
    G1 --> G2[Différent de Table ARP (IP <--> MAC)]

    F3 --> H[Processus d'Aiguillage]
    H --> H1[Apprentissage: Enregistre MAC/Port]
    H --> H2[Filtrage/Forwarding: Envoie vers Port Spécifique]
    H --> H3[Flooding: Gère Adresses MAC Inconnues]

    A --> I[Types de Switches]
    I --> I1[Non Managé: Plug & Play, simple]
    I --> I2[Managé: Contrôle avancé (VLAN, QoS, Sécurité)]

    A --> J[Avantages Clés]
    J --> J1[Performance: Moins de Collisions, Vitesse Accrue]
    J --> J2[Sécurité: Trafic Isolé, Difficile d'Écoute Passive]
    J --> J3[Efficacité: Bande Passante Optimisée]

    A --> K[Switch vs Routeur]
    K --> K1[Switch: Couche 2, Interne LAN]
    K --> K2[Routeur: Couche 3, Inter-Réseaux (ex: Internet)]
```

## ❓ Quiz de Révision (Active Recall)
> [!QUESTION] Question 1
> Quel est le rôle principal d'un [[Switch|Switch]] réseau et comment se différencie-t-il d'un [[BroadcastDomain|hub]] traditionnel dans la gestion du [[NetworkTrafficAnalysis|trafic]] ?
> > [!success]- Réponse
> > Le rôle principal d'un [[Switch|Switch]] est de recevoir des [[DataFrames|trames]] et de les rediriger *intelligemment* vers leur [[NetworkDevice|destinataire]] spécifique en se basant sur la [[MacAddressTable|table d'adresses MAC]]. Il se différencie d'un [[BroadcastDomain|hub]] car le [[BroadcastDomain|hub]] diffuse toutes les [[Data|données]] à tous les [[LANPort|ports]], gaspillant la [[Bandwidth|bande passante]] et créant des [[Collision|collisions]], tandis que le [[Switch|Switch]] envoie les [[Data|données]] uniquement au [[NetworkDevice|destinataire]] voulu, optimisant ainsi la [[NetworkPerformance|performance]] et la [[NetworkSecurity|sécurité]].

> [!QUESTION] Question 2
> Expliquez la différence fondamentale entre une [[MacAddressTable|table d'adresses MAC]] (utilisée par un [[Switch|Switch]]) et une [[AddressResolutionProtocol|table ARP]] (gérée par les [[OperatingSystem|ordinateurs]]) en précisant les informations qu'elles contiennent et leur niveau [[InternationalOrganizationForStandardization|OSI]] respectif.
> > [!success]- Réponse
> > La [[MacAddressTable|table d'adresses MAC]] du [[Switch|Switch]] fait le lien entre une [[MediaAccessControlAddress|adresse MAC]] (physique, couche 2 [[InternationalOrganizationForStandardization|OSI]]) et le [[LANPort|port physique]] du [[Switch|switch]] sur lequel l'[[NetworkDevice|appareil]] est connecté. La [[AddressResolutionProtocol|table ARP]], gérée par les [[OperatingSystem|ordinateurs]], fait le lien entre une [[InternetProtocol|adresse IP]] (logique, couche 3 [[InternationalOrganizationForStandardization|OSI]]) et l'[[MediaAccessControlAddress|adresse MAC]] correspondante d'un [[NetworkDevice|appareil]] sur le même [[NetworkSegment|segment réseau]].

> [!QUESTION] Question 3
> Décrivez les trois étapes par lesquelles un [[Switch|Switch]] remplit et utilise sa [[MacAddressTable|table d'adresses MAC]], y compris comment il gère les [[MediaAccessControlAddress|adresses MAC]] inconnues.
> > [!success]- Réponse
> > 1.  **Apprentissage (Learning)** : Le [[Switch|switch]] enregistre l'[[MediaAccessControlAddress|adresse MAC]] source de chaque [[DataFrames|trame]] entrante et le [[LANPort|port]] par lequel elle est arrivée, ajoutant cette association à sa [[MacAddressTable|table]].
> > 2.  **Filtrage et Forwarding (Aiguillage)** : Lorsqu'une [[DataFrames|trame]] arrive, le [[Switch|switch]] consulte sa [[MacAddressTable|table]] pour l'[[DestinationMacAddress|adresse MAC de destination]]. S'il trouve une correspondance, il envoie la [[DataFrames|trame]] *uniquement* par le [[LANPort|port]] associé, filtrant le trafic pour les autres [[LANPort|ports]].
> > 3.  **Gestion de l'Inconnu ([[Broadcast|Flooding]])** : Si l'[[DestinationMacAddress|adresse MAC de destination]] est inconnue (pas dans la [[MacAddressTable|table]]), le [[Switch|switch]] agit comme un [[BroadcastDomain|hub]] et diffuse la [[DataFrames|trame]] par tous les [[LANPort|ports]] sauf celui d'où elle provient. Si le [[NetworkDevice|destinataire]] répond, le [[Switch|switch]] apprend son emplacement et met à jour sa [[MacAddressTable|table]].

## 🔗 Liens du Module
*   **Précédent** : [[RIB01-05_Module5Partie2|01-05 | Module 5 partie 2]]
*   **Suivant** : [[RIB01-07_Module7|01-07 | Module 7]]
*   **Ressource Externe** : [Comprendre le fonctionnement d'un Switch Ethernet - Tech2Tech](https://www.youtube.com/watch?v=k_B8kRzB_uY)