---
tags:
  - modele
  - modele/osi
  - modele/reference
  - reseau
  - communication
  - couche
aliases:
  - Modèle OSI
  - OSI Model
  - OSI
  - Open Systems Interconnection Model
archetype: modele
source:
  - 
cssclasses:
  - max
---

# Modèle : Interconnexion de Systèmes Ouverts (OSI)

## 🎯 Principe Fondamental

> Le [[OpenSystemsInterconnectionModel|Modèle OSI]] (Open Systems Interconnection) est un [[ReferenceModel|modèle de référence]] conceptuel développé par l'[[InternationalOrganizationForStandardization|ISO]] qui décrit la [[NetworkCommunication|communication réseau]] en la décomposant en sept couches distinctes et interdépendantes. 
> Son but est de fournir un cadre universel pour la standardisation des [[Protocol|protocoles]] de communication, facilitant ainsi l'[[Interoperability|interopérabilité]] entre différents [[System|systèmes]] et [[NetworkDevice|équipements réseau]].

## 🧩 Composants / Éléments Clés

Le [[OpenSystemsInterconnectionModel|Modèle OSI]] est composé de sept [[ProtocolStack|couches de protocole]] superposées, chacune ayant une fonction spécifique :

*   **7. [[ApplicationLayer|Couche Application]]**: Interface directe avec les [[SoftwareApplication|applications]] [[User|utilisateur]]. Elle fournit des [[OnlineServices|services réseau]] aux applications (ex: HTTP, FTP, SMTP).
*   **6. [[PresentationLayer|Couche Présentation]]**: Gère la représentation des [[Data|données]], y compris l'[[Encoding|encodage]], le [[Encryption|chiffrement]]/déchiffrement et la compression pour assurer que les données sont compréhensibles par la couche application du destinataire.
*   **5. [[SessionLayer|Couche Session]]**: Établit, gère et termine les sessions de [[NetworkCommunication|communication]] entre les [[SoftwareApplication|applications]]. Elle assure le dialogue et la synchronisation.
*   **4. [[TransportLayer|Couche Transport]]**: Responsable de la segmentation, du transfert et de la réassemblage des données pour des [[EndDevices|applications]] spécifiques. Elle assure la [[Reliability|fiabilité]] de la [[DataTransmission|transmission de données]] et le [[FlowControl|contrôle de flux]] (ex: [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]).
*   **3. [[NetworkLayer|Couche Réseau]]**: Gère l'[[Routing|adressage logique]] et le routage des [[Packet|paquets]] de données entre différents [[NetworkSegment|réseaux]]. Elle détermine le meilleur chemin pour les données (ex: [[InternetProtocol|IP]]).
*   **2. [[DataLinkLayer|Couche Liaison de Données]]**: Fournit un transfert de données fiable sur une [[PhysicalNetwork|liaison physique]] directe. Elle gère l'[[AccessControl|accès au support physique]], le [[Frame|formatage de trame]] et la [[ErrorDetectionAndCorrection|détection d'erreurs]] (ex: [[Ethernet]]).
*   **1. [[PhysicalLayer|Couche Physique]]**: Définit les spécifications électriques, mécaniques, fonctionnelles et procédurales pour l'activation, le maintien et la désactivation des [[PhysicalNetwork|liaisons physiques]] entre les [[NetworkDevice|dispositifs réseau]]. Elle gère la transmission des [[Bit|bits]] (ex: [[Ethernet]], [[FiberOpticCable|fibre optique]]).

## 📜 Règles de Fonctionnement

> Le [[OpenSystemsInterconnectionModel|Modèle OSI]] opère selon plusieurs règles fondamentales :

*   **[[Encapsulation|Encapsulation]] et [[Decapsulation|Décapsulation]]**: À chaque couche émettrice, les données reçoivent un [[Header|en-tête]] (et parfois un pied de page) spécifique à la couche, processus appelé encapsulation. À la réception, le processus inverse (décapsulation) se produit, où chaque couche retire son en-tête.
*   **Communication de couche à couche**: Chaque couche ne communique qu'avec la couche directement supérieure ou inférieure, et logiquement, avec la couche homologue sur le [[RemoteNetwork|système distant]].
*   **Indépendance des couches**: Les couches sont conçues pour être indépendantes les unes des autres, permettant à une couche d'être modifiée sans affecter les autres, tant que son interface avec les couches adjacentes reste inchangée.

## 📊 Diagramme Conceptuel

```mermaid
graph TD
    classDef layer fill:#e8f8ff,stroke:#2980b9,stroke-width:2px;
    classDef odd fill:#fff2cc,stroke:#b8860b,stroke-width:2px;
    classDef even fill:#e9ffe0,stroke:#27ae60,stroke-width:2px;

    L7["🟦 Couche 7<br/>Application"]:::layer
    L6["🟨 Couche 6<br/>Présentation"]:::odd
    L5["🟩 Couche 5<br/>Session"]:::even
    L4["🟦 Couche 4<br/>Transport"]:::layer
    L3["🟨 Couche 3<br/>Réseau"]:::odd
    L2["🟩 Couche 2<br/>Liaison de Données"]:::even
    L1["🟦 Couche 1<br/>Physique"]:::layer

    L7 --> L6 --> L5 --> L4 --> L3 --> L2 --> L1

```
---


```mermaid
graph TD
    classDef layer1 fill:#e8f8ff,stroke:#2980b9,stroke-width:2px;
    classDef layer2 fill:#fff2cc,stroke:#b8860b,stroke-width:2px;
    classDef layer3 fill:#e9ffe0,stroke:#27ae60,stroke-width:2px;

    L7["🟦 Couche 7 : Application<br/>HTTP, DNS, SMTP"]:::layer1
    L6["🟨 Couche 6 : Présentation<br/>Encodage, Compression, TLS"]:::layer2
    L5["🟩 Couche 5 : Session<br/>Handshake, Sync, Dialogue"]:::layer3
    L4["🟦 Couche 4 : Transport<br/>TCP, UDP, Ports"]:::layer1
    L3["🟨 Couche 3 : Réseau<br/>IP, Routage, IPv4/6"]:::layer2
    L2["🟩 Couche 2 : Liaison<br/>MAC, ARP, Trame Ethernet"]:::layer3
    L1["🟦 Couche 1 : Physique<br/>Bits, Signaux, Médium"]:::layer1

    L7 --> L6 --> L5 --> L4 --> L3 --> L2 --> L1

```

---

## 💡 Applications Pratiques

*   **Enseignement et Compréhension**: Largement utilisé comme outil pédagogique pour expliquer le fonctionnement des [[Network|réseaux informatiques]] et des [[NetworkCommunication|communications de données]].
*   **[[NetworkArchitecture|Conception de réseau]]**: Sert de guide pour la [[NetworkArchitecture|conception]] et le développement de [[NetworkProtocol|protocoles réseau]] et de [[NetworkDevice|dispositifs]].
*   **[[Troubleshooting|Dépannage]]**: Les administrateurs réseau utilisent le modèle pour isoler et résoudre les [[SoftwareBugs|problèmes réseau]] en identifiant la couche affectée.
*   **Standardisation**: Bien que le [[InternetProtocolSuite|modèle TCP/IP]] soit plus couramment implémenté, le [[OpenSystemsInterconnectionModel|Modèle OSI]] a influencé de nombreux [[NetworkStandard|standards réseau]] et le développement de [[NetworkProtocol|protocoles]].

## ✅ Avantages et Limites

*   **Avantages**:
    *   **Modularité**: Facilite le développement et le [[Testing|test]] des [[NetworkProtocol|protocoles]] en les décomposant en fonctions plus petites.
    *   **Standardisation**: Favorise l'[[Interoperability|interopérabilité]] en fournissant un langage et un cadre commun pour les fabricants et les développeurs.
    *   **[[Troubleshooting|Dépannage]]**: Simplifie la [[Troubleshooting|résolution de problèmes]] en permettant d'isoler les dysfonctionnements à une couche spécifique.
    *   **Flexibilité**: Permet à différentes [[NetworkTechnology|technologies réseau]] de coexister et de communiquer.
*   **Limites**:
    *   **Complexité**: Le modèle est très détaillé, ce qui peut rendre son implémentation directe difficile et moins flexible que le [[InternetProtocolSuite|modèle TCP/IP]].
    *   **Chevauchement de fonctions**: Certaines fonctions peuvent se chevaucher entre les couches, comme le [[Encryption|chiffrement]] qui peut se produire à plusieurs niveaux (présentation, session, transport).
    *   **Inadéquation pratique**: Dans la pratique, le [[InternetProtocolSuite|modèle TCP/IP]] est devenu le standard de facto pour l'[[Internet]], étant plus simple et plus adapté aux implémentations réelles.

## 🔗 Notes Connexes
*   **Modèle concurrent**: [[InternetProtocolSuite|Suite de Protocoles Internet (TCP/IP)]]
*   **Concept général**: [[ProtocolStack|Pile de Protocoles]]
*   **Mécanisme clé**: [[Encapsulation|Encapsulation de données]]
*   **Application réseau**: [[NetworkMonitoring|Surveillance réseau]]
*   **Organisme de normalisation**: [[InternationalOrganizationForStandardization|ISO]]