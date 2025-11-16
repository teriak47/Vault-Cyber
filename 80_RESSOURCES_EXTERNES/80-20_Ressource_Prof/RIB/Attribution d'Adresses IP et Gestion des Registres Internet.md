---
aliases:
  - Attribution d'Adresses IP Et Gestion Des Registres Internet
module: RIB
cssclasses:
  - max
title: Attribution d'Adresses IP Et Gestion Des Registres Internet
---

# Attribution d'Adresses IP Et Gestion Des Registres Internet

Comprendre la distribution mondiale des adresses IP et le rôle crucial des organismes de régulation dans l'architecture Internet moderne.

## L'Architecture Mondiale De Distribution Des Adresses IP

Les adresses IPv4 publiques constituent l'épine dorsale de la communication Internet mondiale. Ces adresses, qui doivent être globalement uniques pour garantir un acheminement correct, sont gérées par un système hiérarchique sophistiqué qui assure leur distribution équitable à travers le monde.

L'IANA (Internet Assigned Numbers Authority) occupe le sommet de cette hiérarchie en tant qu'autorité suprême responsable de la gestion des blocs d'adresses IP. Cette organisation attribue de grands blocs d'adresses aux Registres Internet Régionaux (RIR), qui les redistribuent ensuite aux fournisseurs d'accès Internet et aux organisations de leur région géographique respective.

## Les Cinq Registres Internet Régionaux (RIR)

-   **ARIN**
    American Registry for Internet Numbers - Dessert l'Amérique du Nord
-   **RIPE NCC**
    Réseaux IP Européens - Couvre l'Europe, le Moyen-Orient et l'Asie centrale
-   **APNIC**
    Asia-Pacific Network Information Centre - Région Asie-Pacifique
-   **LACNIC**
    Latin America and Caribbean Network Information Centre
-   **AFRINIC**
    African Network Information Centre
    - Continent africain

Ces RIR attribuent des adresses IP aux ISP, qui fournissent ensuite des blocs d'adresses aux entreprises et aux petits fournisseurs.

Les grandes organisations peuvent également obtenir leurs adresses directement auprès d'un RIR.

## Segmentation du Réseau Et Domaines de Diffusion

### Principe De la Diffusion Ethernet

Dans un réseau local Ethernet, les appareils utilisent la diffusion pour communiquer avec tous les périphériques du même segment réseau. Cette méthode est essentielle pour des protocoles fondamentaux comme ARP et DHCP.

Les Commutateur propagent les diffusions sur toutes leurs interfaces, sauf celle d'où provient le message. Cette propagation peut rapidement saturer un réseau si elle n'est pas contrôlée.

Un domaine de diffusion de couche 2 représente l'ensemble des périphériques qui reçoivent les trames de diffusion émises par n'importe quel appareil du groupe. La taille de ces domaines a un impact direct sur les performances du réseau.

## Le Rôle Crucial Des Routeurs Dans la Segmentation

-   **Domaine de Diffusion 1**
    Les commutateurs propagent toutes les diffusions au sein du segment
-   **Routeur**
    Bloque les diffusions et segmente les domaines
-   **Domaine de Diffusion 2**
    Segment isolé avec son propre trafic de diffusion

Les routeurs ne propagent pas les messages de diffusion. Lorsqu'un routeur reçoit une diffusion sur une interface, il ne la transmet jamais vers d'autres interfaces. Cette caractéristique fondamentale permet de créer des domaines de diffusion distincts, chaque interface de routeur définissant la limite d'un domaine.

## Protocoles Utilisant la Diffusion

-   **Protocole ARP**
    Address Resolution Protocol - Envoie des diffusions de couche 2 pour découvrir l'adresse MAC associée à une adresse IPv4 connue sur le réseau local
-   **Protocole DHCP**
    Dynamic Host Configuration Protocol - Utilise des messages de découverte en diffusion pour localiser un serveur DHCP et obtenir une configuration d'adresse IPv4 automatique

Ces deux protocoles sont essentiels au fonctionnement quotidien des réseaux modernes. Ils dépendent de la capacité à diffuser des messages à tous les périphériques d'un segment réseau pour accomplir leurs fonctions respectives de résolution d'adresses et de configuration automatique.

## Problématiques Des Grands Domaines De Diffusion

-   **Impact sur les Performances Réseau**
    Un domaine connectant de nombreux hôtes (par exemple 400 utilisateurs) génère un volume excessif de trafic de diffusion, ralentissant considérablement les opérations réseau
-   **Charge de Traitement des Périphériques**
    Chaque appareil doit accepter et traiter tous les paquets de diffusion, même ceux qui ne le concernent pas, ce qui consomme des ressources CPU et mémoire précieuses
-   **Dégradation de l'Expérience Utilisateur**
    Les opérations deviennent lentes, les temps de réponse augmentent et la productivité diminue en raison de la congestion du réseau

## Solution : La Création De Sous-Réseaux (Subnetting)

### Avant Le Sous-Réseau

-   Réseau unique **172.16.0.0/16**
-   400 utilisateurs dans un seul domaine de diffusion massif
-   Trafic de diffusion excessif affectant tous les périphériques

### Après Le Sous-Réseau

-   Deux sous-réseaux :
    -   172.16.0.0/24 - 200 utilisateurs
    -   172.16.1.0/24 - 200 utilisateurs
-   Les diffusions restent confinées à leur domaine respectif

Remarquez comment la longueur du préfixe passe de /16 à /24, utilisant des bits d'hôte supplémentaires pour créer des sous-réseaux distincts.

## Avantages De la Segmentation En Sous-Réseaux

-   **Amélioration des Performances**
    Réduit le trafic global et améliore significativement les performances du réseau en limitant la propagation des diffusions
-   **Politiques de Sécurité**
    Permet aux administrateurs de définir des politiques granulaires pour contrôler la communication entre différents sous-réseaux et segments
-   **Isolation des Problèmes**
    Limite l'impact du trafic anormal causé par des erreurs de configuration, des problèmes matériels/logiciels ou des activités malveillantes

## Stratégies De Découpage En Sous-Réseaux

Les administrateurs réseau peuvent organiser leurs sous-réseaux selon plusieurs critères pour optimiser la gestion et la sécurité :

1.  **Par Emplacement Géographique**
    Segmentation basée sur les sites physiques : bâtiments, étages, campus
2.  **Par Groupe ou Fonction**
    Organisation selon les départements : ventes, marketing, finance, RH
3.  **Par Type de Périphérique**
    Séparation des équipements : serveurs, postes de travail, imprimantes, [[InternetofThings|IoT]]
4.  **Par Niveau de Sécurité**
    Isolation selon la sensibilité : réseau invité, réseau interne, zone DMZ

> **Compétence Fondamentale :**
> Comprendre le découpage en sous-réseaux est essentiel pour tout administrateur réseau. Bien que complexe au début, cette compétence devient plus intuitive avec la pratique et l'attention aux détails. Diverses méthodes et outils existent pour faciliter ce processus d'apprentissage.
