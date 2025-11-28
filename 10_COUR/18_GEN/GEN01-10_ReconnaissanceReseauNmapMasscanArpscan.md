---
cssclasses:
  - max
aliases:
  - "RECONNAISSANCE RÉSEAU (Nmap • Masscan • ARP-Scan)"
  - "01-10 | RECONNAISSANCE RÉSEAU (Nmap • Masscan • ARP-Scan)"
  - "Network Reconnaissance (Nmap • Masscan • ARP-Scan)"
archetype: cour
module: "GEN (Culture Générale & Hors Cursus)"
tags:
  - pentest/reconnaissance
  - outil/nmap
  - outil/masscan
  - outil/arp-scan
  - protocole/arp
  - reseau/port-scanning
  - detection/service
  - detection/os
  - modele-osi/couche-2
  - protocole/tcp
  - protocole/icmp
  - pare-feu
  - outil/nmap/scan-syn
  - outil/nmap/nse
  - outil/nmap/scan-agressif
  - outil/nmap/scan-tous-ports
  - outil/masscan/scan-rapide
---

# 01-10 | RECONNAISSANCE RÉSEAU (Nmap • Masscan • ARP-Scan)

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1.  Identifier tous les **hôtes en ligne** (Linux, Windows, routeur, serveurs web...).
> 2.  Découvrir les **ports ouverts**, les **services** et leurs **versions**.
> 3.  Comprendre les différents **types de scans** (SYN, version, agressif, complet).
> 4.  Exécuter des **scans rapides** (Masscan) et des **scans complets** (Nmap).
> 5.  Produire une **fiche d'inventaire réseau** utilisable pour l'exploitation.

## 📝 Synthèse du Cours

La **reconnaissance réseau** est une étape cruciale en cybersécurité, tant offensive que défensive. Elle permet de cartographier une infrastructure, d'identifier les systèmes actifs, les services exposés et les vulnérabilités potentielles. Ce module couvre les outils fondamentaux pour construire une image complète d'un réseau inconnu, tel qu'un réseau d'entreprise (par exemple, 192.168.56.0/24).

### 1. Découverte des Hôtes avec ARP-Scan

L'**ARP-Scan** est un outil en ligne de commande qui utilise le protocole ARP (Address Resolution Protocol) pour découvrir les hôtes IPv4 actifs sur un réseau local. Contrairement aux scanners basés sur ICMP (ping) ou TCP/UDP, ARP-Scan opère à la couche 2 du modèle OSI, ce qui lui permet de détecter des appareils qui pourraient bloquer le trafic IP de plus haut niveau, y compris ceux derrière des pare-feu. Cependant, il est limité au sous-réseau local car le protocole ARP n'est pas routable.

*   **Principe de fonctionnement** : ARP-Scan envoie des requêtes ARP à toutes les adresses IP d'une plage spécifiée. Les systèmes actifs répondent avec leur adresse MAC et IP.
*   **Avantages** : Efficace pour identifier tous les dispositifs IPv4 connectés, même ceux configurés pour éviter la détection par des méthodes de scan plus classiques. Fournit une cartographie rapide des adresses IP aux adresses MAC.
*   **Commande essentielle** :
    `sudo arp-scan -l eth1 192.168.56.0/24`
    Cette commande scanne le sous-réseau `192.168.56.0/24` via l'interface `eth1` pour identifier les hôtes en ligne. L'option `-l` permet de générer des adresses à partir de la configuration de l'interface réseau.

### 2. Scan de Ports et Détection de Services/OS avec Nmap

**Nmap** (Network Mapper) est un outil open-source très populaire pour l'exploration réseau, la gestion et l'audit de sécurité. Il permet de découvrir des hôtes, des ports ouverts, les services qui y sont associés et leurs versions, ainsi que le système d'exploitation des machines cibles.

*   **Types de Scans Nmap** :
    *   **Scan SYN (`-sS`)** : C'est le scan par défaut et le plus courant. Aussi appelé "Half-Open" ou "Stealth Scan", il envoie des paquets SYN et observe les réponses sans jamais établir de connexion TCP complète. Un SYN/ACK indique un port ouvert, un RST un port fermé, et l'absence de réponse (après retransmissions) un port filtré. Il est rapide et relativement discret. Nécessite des privilèges root pour envoyer des paquets bruts.
    *   **Détection de Version (`-sV`)** : Permet de sonder les ports ouverts pour déterminer le service et sa version exacte (ex: Apache 2.4).
    *   **Détection d'OS (`-O`)** : Tente d'identifier le système d'exploitation de la cible en analysant les réponses aux sondes TCP/IP.
    *   **Scripts NSE (`-sC` ou `--script`)** : Le Nmap Scripting Engine (NSE) étend les fonctionnalités de Nmap en utilisant des scripts Lua. L'option `-sC` exécute les scripts "safe" et par défaut. Il existe des scripts pour la détection de vulnérabilités (`--script vuln`), l'énumération de services (SMB, DNS, etc.), et bien plus.
    *   **Scan Agressif (`-A`)** : Active la détection d'OS (`-O`), la détection de version (`-sV`), l'exécution de scripts par défaut (`-sC`) et un traceroute. C'est un scan complet mais plus bruyant et plus long.
    *   **Scan de Tous les Ports (`-p-`)** : Scanne l'intégralité des 65535 ports TCP, au lieu des 1000 ports les plus courants par défaut.

*   **Commandes essentielles** :
    *   `nmap 192.168.56.0/24` : Scan basique du réseau.
    *   `nmap -sV -sC 192.168.56.10` : Détection de version et exécution des scripts par défaut pour une cible spécifique.
    *   `sudo nmap -A -p- 192.168.56.20` : Scan agressif de tous les ports pour une cible, nécessitant des privilèges root.
    *   `sudo nmap --script vuln 192.168.56.20` : Recherche de vulnérabilités connues via les scripts NSE "vuln".

### 3. Scan Ultra-Rapide avec Masscan

**Masscan** est un scanner de ports TCP ultra-rapide, capable de scanner l'intégralité d'Internet en quelques minutes grâce à une transmission asynchrone. Il est optimisé pour la vitesse et permet d'identifier très rapidement les ports ouverts sur de très grands réseaux. Masscan se concentre sur la détection des ports ouverts et est moins détaillé que Nmap pour la détection de services ou d'OS. Il est souvent utilisé pour une découverte initiale rapide, les résultats pouvant ensuite être affinés avec Nmap.

*   **Principe de fonctionnement** : Masscan utilise son propre stack TCP/IP pour envoyer des millions de paquets SYN par seconde sans attendre de réponse immédiate, ce qui lui confère une vitesse inégalée.
*   **Avantages** : Vitesse extrême, idéal pour la découverte de ports ouverts sur de vastes plages d'adresses IP.
*   **Inconvénients** : Moins de détails que Nmap, ne détecte pas les services ou versions de manière approfondie. Peut générer un trafic réseau important et être bruyant.
*   **Commande essentielle** :
    `sudo masscan 192.168.56.0/24 -p1-65535 --rate 1000`
    Cette commande scanne tous les ports (`-p1-65535`) du réseau `192.168.56.0/24` à une cadence de 1000 paquets par seconde (`--rate 1000`).

### 4. Analyse Préliminaire de Surface Web avec WhatWeb

**WhatWeb** est un scanner d'applications web qui identifie les technologies utilisées par un site web, incluant les systèmes de gestion de contenu (CMS), les plateformes de blogs, les bibliothèques JavaScript, les serveurs web, les frameworks, et plus encore. Il analyse les en-têtes HTTP, le HTML, le JavaScript, les cookies et d'autres éléments pour identifier plus de 900 plugins de détection.

*   **Principe de fonctionnement** : WhatWeb envoie des requêtes HTTP à la cible et analyse les réponses pour reconnaître les empreintes technologiques.
*   **Avantages** : Fournit rapidement un aperçu des technologies web utilisées, utile pour identifier les cibles d'exploitation potentielles.
*   **Options utiles** : L'option `-v` (verbose) permet d'obtenir une sortie plus détaillée. L'option `-a` (aggression) peut être utilisée pour augmenter la profondeur du scan.
*   **Commande essentielle** :
    `whatweb -v http://192.168.56.50`
    Cette commande effectue un scan verbeux sur l'adresse IP `192.168.56.50` pour découvrir les technologies web.

### 5. Création d'un Inventaire Réseau Complet

Après avoir utilisé ces outils, la dernière étape consiste à consolider toutes les informations recueillies dans un **inventaire réseau** structuré. Cet inventaire est fondamental pour la sécurité, car il permet de connaître précisément les actifs, d'identifier les vulnérabilités et d'évaluer les risques. Un inventaire à jour facilite la réponse aux incidents de sécurité et la mise en œuvre de mesures de protection.

*   **Informations à collecter par machine** :
    *   Adresse IP
    *   Système d'exploitation (OS)
    *   Ports ouverts
    *   Services et versions
    *   Vulnérabilités potentielles
    *   Commentaires (rôle de la machine, priorité, etc.)
*   **Exemple de format** :
    `IP | OS | Ports | Services | Vulnérabilités | Commentaires`
    `192.168.56.20 | Linux | 22/80 | SSH, Apache 2.4 | CVE Apache, directory listing | Cible n°1`

> [!note] Définition Clé
> **Reconnaissance Réseau** : Processus de collecte d'informations sur un réseau ou un système pour comprendre sa structure, ses dispositifs et ses vulnérabilités potentielles, essentielle pour l'audit de sécurité et la planification d'attaques ou de défenses.

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Reconnaissance Réseau] --> B{Objectifs}
    B --> B1[Identifier Hôtes]
    B --> B2[Découvrir Ports/Services]
    B --> B3[Analyser Vulnérabilités]
    B --> B4[Cartographier Réseau]

    A --> C{Outils Clés}
    C --> C1[ARP-Scan]
    C --> C2[Nmap]
    C --> C3[Masscan]
    C --> C4[WhatWeb]

    C1 --> C1_1[Découverte Hôtes Locaux]
    C1 --> C1_2[Couche 2 (ARP)]

    C2 --> C2_1[Scan de Ports (SYN, TCP Connect)]
    C2 --> C2_2[Détection Services/Versions (-sV)]
    C2 --> C2_3[Détection OS (-O)]
    C2 --> C2_4[Scripts NSE (-sC, --script vuln)]
    C2 --> C2_5[Scan Agressif (-A)]

    C3 --> C3_1[Scan Ultra-Rapide]
    C3 --> C3_2[Grands Réseaux]
    C3 --> C3_3[Ports Ouverts Seulement]

    C4 --> C4_1[Analyse Technologies Web]
    C4 --> C4_2[CMS, Serveurs Web, Frameworks]

    A --> D{Processus Général}
    D --> D1[1. Découverte Hôtes (ARP-Scan)]
    D --> D2[2. Scan Ports Classique (Nmap)]
    D --> D3[3. Scan Avancé (Nmap + NSE)]
    D --> D4[4. Scan Ultra-Rapide (Masscan)]
    D --> D5[5. Analyse Surface Web (WhatWeb)]
    D --> D6[6. Inventaire Complet]

    D6 --> E[Fiche Inventaire Réseau]
    E --> E1[IP, OS, Ports, Services, Vulnérabilités, Commentaires]```

## ❓ Quiz de Révision (Active Recall)
> [!question] Question 1
> Quel est l'avantage principal d'utiliser `arp-scan` par rapport à un scan `ping` ou `Nmap` pour la découverte d'hôtes sur un réseau local ?
> > [!success]- Réponse
> > L'avantage principal d'utiliser `arp-scan` est qu'il opère à la couche 2 du modèle OSI (protocole ARP). Cela lui permet de détecter des hôtes qui pourraient bloquer le trafic ICMP (ping) ou TCP/UDP de couche supérieure, y compris ceux protégés par des pare-feu, car tous les dispositifs IPv4 répondent aux requêtes ARP pour communiquer sur le réseau local.

> [!question] Question 2
> Expliquez la différence entre les options `nmap -sV -sC -O` et `nmap -A`. Quand est-il préférable d'utiliser l'une plutôt que l'autre ?
> > [!success]- Réponse
> > Les options `nmap -sV -sC -O` activent spécifiquement la détection de version (`-sV`), l'exécution des scripts par défaut (`-sC`) et la détection d'OS (`-O`). L'option `nmap -A` est un raccourci qui active toutes ces fonctions, plus un traceroute (`--traceroute`).
> >
> > Il peut être préférable d'utiliser `nmap -sV -sC -O` lorsque l'on souhaite un contrôle plus granulaire sur les types de scans exécutés, potentiellement pour réduire le bruit ou le temps de scan sur de grands réseaux en évitant le traceroute, ou pour une meilleure compréhension des actions spécifiques de Nmap. L'option `-A` est pratique pour un scan agressif et complet rapide d'une cible unique ou d'un petit ensemble de cibles, mais elle est plus bruyante et prend plus de temps.

> [!question] Question 3
> Quelle est la principale caractéristique de `Masscan` qui le rend unique parmi les scanners de ports, et quelle est sa limitation par rapport à `Nmap` ?
> > [!success]- Réponse
> > La principale caractéristique de `Masscan` est sa vitesse ultra-rapide, capable de scanner l'ensemble d'Internet en quelques minutes en envoyant des millions de paquets SYN par seconde grâce à une transmission asynchrone.
> >
> > Sa limitation majeure par rapport à `Nmap` est qu'il se concentre uniquement sur l'identification des ports ouverts et fournit peu d'informations supplémentaires sur les services ou leurs versions, contrairement à Nmap qui offre une détection détaillée des services, des versions, des OS et l'exécution de scripts de vulnérabilité.
