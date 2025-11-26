---
aliases:
  - "Unité de Données de Protocole"
  - "PDU"
  - "Protocol Data Unit"
archetype: concept-reseau
couche_osi:
  - "Couche 1 - Physique"
  - "Couche 2 - Liaison"
  - "Couche 3 - Réseau"
  - "Couche 4 - Transport"
  - "Couche 5 - Session"
  - "Couche 6 - Présentation"
  - "Couche 7 - Application"
technologie:
  - "OSI Model"
cssclasses:
  - max
tags:
  - protocole
  - protocole/pdu
  - modele-osi
  - modele-tcp-ip
  - encapsulation
  - decapsulation
  - reseau
  - communication
  - definition
  - donnee
  - protocole/pdu/segment
  - protocole/pdu/datagramme
  - protocole/pdu/paquet
  - protocole/pdu/trame
  - protocole/pdu/bits
  - controle-erreur
  - routage
  - adresse-ip
  - adresse-mac
  - port
  - chiffrement
  - compression
  - reseau/depannage
  - analyse/trafic-reseau
  - architecture/reseau
---

# Protocol Data Unit (PDU)

> [!abstract] Définition
> Une **Unité de Données de Protocole (PDU)** est une unité d'information unique transmise entre des entités homologues d'un réseau informatique, qui varie à chaque couche du modèle OSI ou TCP/IP. Elle est composée de données utilisateur et d'informations de contrôle spécifiques au protocole de la couche concernée. Le terme PDU est générique et son nom spécifique (segment, paquet, trame, bit) dépend de la couche réseau où elle se trouve.

## ⚙️ Mécanisme & Fonctionnement
Le fonctionnement des PDUs est intrinsèquement lié aux processus d'**encapsulation** et de **décapsulation** dans le modèle OSI. Lors de l'envoi de données, chaque couche ajoute ses propres informations d'en-tête (et parfois de fin de trame) à l'unité de données reçue de la couche supérieure, créant ainsi une PDU pour sa propre couche. Ce processus est appelé encapsulation. À la réception, le processus inverse, la décapsulation, se produit, où chaque couche retire son en-tête et transmet les données restantes à la couche supérieure.

### Encapsulation et Rôle par Couche du Modèle OSI

*   **Couche 7 - Application (PDU: Données / Message)**
    *   **Entrée** : Données brutes de l'application utilisateur (ex: contenu d'un e-mail, fichier).
    *   **Action** : Les données sont formatées pour l'application spécifique (HTTP, FTP, SMTP, etc.). Aucun en-tête OSI n'est ajouté à ce niveau conceptuel pour la PDU elle-même, mais les protocoles applicatifs ont leurs propres structures.
    *   **Sortie** : Les données de l'application sont passées à la couche de Présentation.

*   **Couche 6 - Présentation (PDU: Données)**
    *   **Entrée** : Données de la couche Application.
    *   **Action** : Cette couche gère la traduction, le chiffrement/déchiffrement et la compression/décompression des données pour garantir un format compréhensible par la couche Application du destinataire. La PDU reste des "Données" mais avec un format potentiellement modifié.
    *   **Sortie** : Les données formatées sont passées à la couche Session.

*   **Couche 5 - Session (PDU: Données)**
    *   **Entrée** : Données de la couche Présentation.
    *   **Action** : Établit, gère et termine les sessions entre les applications. La PDU est toujours appelée "Données" à ce niveau, se concentrant sur le dialogue.
    *   **Sortie** : Les données de session sont passées à la couche Transport.

*   **Couche 4 - Transport (PDU: Segment / Datagramme)**
    *   **Entrée** : Données de la couche Session.
    *   **Action** : Les données sont découpées en plus petits morceaux. Un en-tête de transport (par exemple, TCP ou UDP) est ajouté, contenant des informations telles que les numéros de port source et destination, les numéros de séquence et d'acquittement. La PDU est appelée **Segment** (pour TCP, orienté connexion) ou **Datagramme** (pour UDP, sans connexion).
    *   **Sortie** : Le Segment ou Datagramme est passé à la couche Réseau.

*   **Couche 3 - Réseau (PDU: Paquet)**
    *   **Entrée** : Segment ou Datagramme de la couche Transport.
    *   **Action** : Un en-tête de réseau (par exemple, IP) est ajouté au segment/datagramme. Cet en-tête contient les adresses IP source et destination, essentielles pour le routage entre différents réseaux. La PDU est maintenant appelée **Paquet**.
    *   **Sortie** : Le Paquet est passé à la couche Liaison de Données.

*   **Couche 2 - Liaison de Données (PDU: Trame)**
    *   **Entrée** : Paquet de la couche Réseau.
    *   **Action** : Un en-tête de liaison de données et une fin de trame (trailer) sont ajoutés au paquet. L'en-tête contient les adresses MAC source et destination pour la communication au sein d'un même réseau local, et la fin de trame contient généralement un contrôle de redondance cyclique (CRC) pour la détection d'erreurs. La PDU est appelée **Trame**.
    *   **Sortie** : La Trame est passée à la couche Physique.

*   **Couche 1 - Physique (PDU: Bits)**
    *   **Entrée** : Trame de la couche Liaison de Données.
    *   **Action** : La trame est convertie en un flux de signaux électriques, optiques ou radio (bits binaires 0 et 1) qui peuvent être transmis sur le support physique (câble, fibre optique, ondes radio).
    *   **Sortie** : Flux de bits sur le support de transmission.

## 💡 Cas d'Usage Typique
L'unité de Données de Protocole (PDU) est un concept fondamental pour la compréhension et la gestion des réseaux d'entreprise :
1.  **Analyse et Dépannage Réseau** : Comprendre les PDUs permet aux ingénieurs réseau d'analyser le trafic à différents niveaux du modèle OSI. En examinant les en-têtes des segments, paquets ou trames, ils peuvent identifier des problèmes de routage, de connectivité, de performance ou de sécurité.
2.  **Conception et Optimisation de Réseau** : La connaissance des PDUs aide à concevoir des architectures réseau efficaces, à dimensionner les équipements et à optimiser les protocoles. Par exemple, la taille maximale des PDUs (MTU) à la couche Liaison de Données influence les performances.
3.  **Sécurité Réseau** : L'inspection des PDUs est cruciale pour la sécurité. Les pare-feu et les systèmes de détection d'intrusion (IDS) analysent les en-têtes et les charges utiles des PDUs pour détecter des activités malveillantes, des anomalies ou des tentatives d'exploitation de vulnérabilités.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Complexité d'Analyse** : L'analyse des PDUs peut devenir complexe en présence de multiples encapsulations (ex: VPNs, tunnels), rendant difficile l'identification des données originales et des protocoles sous-jacents.
> *   **Performance des Équipements** : Le traitement (encapsulation/décapsulation) des PDUs par les équipements réseau (routeurs, pare-feu) peut avoir un impact significatif sur leurs performances, notamment le CPU et la bande passante, surtout avec des trafics intenses ou des protocoles complexes.
> *   **Interprétation Inadéquate** : Une mauvaise interprétation des champs d'en-tête des PDUs lors du dépannage peut conduire à des diagnostics erronés et à des solutions inefficaces.