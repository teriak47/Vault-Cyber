---
aliases:
  - "Sous-réseautage IP"
  - "IP Subnetting"
  - "Subnetting"
  - "CIDR"
  - "VLSM"
archetype: concept-reseau
couche_osi:
  - "Couche 3 - Réseau"
technologie:
  - "IP"
  - "CIDR"
  - "VLSM"
cssclasses:
  - max
tags:
  - reseau/sous-reseautage
  - reseau/adressage/ip
  - reseau/masque-de-sous-reseau
  - reseau/cidr
  - reseau/vlsm
  - reseau/segmentation
  - reseau/domaine-de-diffusion
  - reseau/routage
  - securite/reseau
  - architecture/reseau
  - gestion/reseau
  - ip
  - modele/tcp-ip
---

# Ip Subnetting Fundamentals

> [!abstract] Définition
> Le **sous-réseautage IP** est une technique qui consiste à diviser un *grand réseau IP* unique en plusieurs *réseaux logiques plus petits*, appelés sous-réseaux. Cette division est réalisée en empruntant des bits de la partie hôte de l'adresse IP et en les allouant à la partie réseau, grâce à l'utilisation d'un *masque de sous-réseau*. Le but principal est d'optimiser l'utilisation des adresses, de réduire la taille des domaines de diffusion et d'améliorer la sécurité et la gestion du réseau.

## ⚙️ Mécanisme & Fonctionnement
Le sous-réseautage IP repose sur la compréhension de l'architecture d'une adresse IP, composée d'une *partie réseau* et d'une *partie hôte*. Le *masque de sous-réseau* définit la frontière entre ces deux parties.

### Encapsulation / Traitement
*   **Entrée** : Un bloc d'adresses IP initial (par exemple, un réseau /24, /16 ou un super-réseau plus large désigné par CIDR).
*   **Action** : Un ingénieur réseau applique un *masque de sous-réseau* spécifique. Ce masque étend la partie réseau en "empruntant" des bits à la partie hôte, créant ainsi de nouvelles identifications de réseau logique. Chaque nouveau sous-réseau se voit attribuer une *adresse réseau* (le premier identifiant du sous-réseau), une *adresse de diffusion* (le dernier identifiant du sous-réseau) et une plage d'adresses IP utilisables pour les hôtes. Les concepts de *CIDR (Classless Inter-Domain Routing)* et de *VLSM (Variable Length Subnet Mask)* permettent une allocation flexible des masques, optimisant davantage l'utilisation de l'espace d'adressage.
*   **Sortie** : Plusieurs *sous-réseaux IP distincts*, chacun capable de fonctionner comme un domaine de diffusion indépendant et de contenir sa propre plage d'adresses IP pour les périphériques finaux.

```mermaid
graph TD
    A[Réseau IP Initial (ex: 192.168.1.0/24)] --> B{Application du Masque de Sous-réseau};
    B --> C1[Sous-réseau 1 (ex: 192.168.1.0/27)];
    B --> C2[Sous-réseau 2 (ex: 192.168.1.32/27)];
    B --> C3[Sous-réseau 3 (ex: 192.168.1.64/27)];
    C1 --> D1[Plage Hôtes, Adr. Réseau, Adr. Diffusion];
    C2 --> D2[Plage Hôtes, Adr. Réseau, Adr. Diffusion];
    C3 --> D3[Plage Hôtes, Adr. Réseau, Adr. Diffusion];
```

Le calcul des sous-réseaux implique de déterminer le nombre de bits empruntés, le nombre de sous-réseaux créés, le nombre d'hôtes par sous-réseau, et d'identifier les adresses réseau, les adresses de diffusion et les plages d'adresses utilisables pour chaque sous-réseau.

## 💡 Cas d'Usage Typique
Le sous-réseautage est une pratique fondamentale en ingénierie réseau pour plusieurs raisons :
1.  **Optimisation de l'utilisation des adresses IP** : Au lieu d'allouer de grands blocs d'adresses IP à des petits segments de réseau, le sous-réseautage permet de créer des sous-réseaux de tailles appropriées, évitant le gaspillage d'adresses. Cela est particulièrement pertinent avec l'IPv4 où les adresses sont une ressource limitée.
2.  **Réduction du trafic de diffusion** : Chaque sous-réseau constitue un domaine de diffusion séparé. En réduisant la taille des domaines de diffusion, on limite la propagation des messages de diffusion à un segment plus petit, ce qui diminue la charge sur le réseau et les performances des périphériques.
3.  **Amélioration de la sécurité** : La segmentation du réseau en sous-réseaux permet d'isoler les services et les départements. Des politiques de sécurité (comme les listes de contrôle d'accès - *ACLs*) peuvent être appliquées aux interfaces de routage entre les sous-réseaux, contrôlant le flux de trafic et limitant l'accès non autorisé.
4.  **Gestion et organisation du réseau** : Le sous-réseautage facilite l'organisation logique du réseau, rendant plus simple la gestion, le dépannage et la planification de l'expansion. Différents services, départements ou types de trafic peuvent être regroupés dans des sous-réseaux dédiés.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Complexité de la planification** : Une mauvaise planification du sous-réseautage peut entraîner un gaspillage d'adresses, des problèmes de routage ou des difficultés d'expansion future. Les calculs de VLSM peuvent devenir complexes dans les grands réseaux.
> *   **Fragmentation des ressources** : Un sous-réseautage excessif peut créer de très petits sous-réseaux, ce qui pourrait limiter le nombre d'hôtes disponibles et potentiellement compliquer la gestion.
> *   **Impact sur le routage** : Chaque sous-réseau créé nécessite une entrée distincte dans la table de routage des routeurs, ce qui peut augmenter la taille des tables de routage et potentiellement la charge de traitement pour les routeurs si la conception n'est pas agrégée efficacement (supernetting).