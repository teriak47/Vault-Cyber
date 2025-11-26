---
aliases:
  - Routage Inter-VLAN
  - Inter-VLAN Routing
  - Router on a Stick
  - Layer 3 Switch Routing
  - Routage de niveau 3 entre VLAN
archetype: concept-reseau
couche_osi:
  - "Couche 3 - Réseau"
technologie:
  - VLAN
  - Routage
  - IEEE 802.1Q
cssclasses:
  - max
tags:
  - reseau/vlan
  - routage
  - routage-reseau
  - routeur
  - switch
  - switch/multicouche
  - routage/router-on-a-stick
  - protocole/ieee-802-1q
  - modele-osi/couche-3
  - reseau/segmentation
  - encapsulation
  - reseau/adressage/ip
  - reseau/performance
  - securite/segmentation
  - reseau/vlan/svi
  - reseau/domaine-de-diffusion
  - reseau/passerelle-par-defaut
  - reseau/trunk-port
---

# InterVLAN Routing

> [!abstract] Définition
> Le **routage Inter-VLAN** est un processus qui permet la communication entre différents **Virtual Local Area Networks (VLANs)** au sein d'un réseau. Par défaut, les appareils situés dans des VLAN distincts ne peuvent pas échanger de données sans un dispositif de couche 3 (réseau), tel qu'un routeur ou un commutateur multicouche, car chaque VLAN représente un domaine de diffusion unique et est isolé logiquement.

## ⚙️ Mécanisme & Fonctionnement
Le routage Inter-VLAN permet à des hôtes appartenant à des sous-réseaux IP différents (chaque VLAN étant associé à un sous-réseau unique) de communiquer entre eux en acheminant le trafic au niveau de la couche réseau (Couche 3 de l'OSI).

Il existe deux méthodes principales pour implémenter le routage Inter-VLAN :

### 1. Routeur sur une patte (Router-on-a-Stick)
Cette méthode utilise une seule interface physique sur un routeur, divisée en plusieurs sous-interfaces virtuelles. Chaque sous-interface est configurée avec une adresse IP qui sert de passerelle par défaut pour un VLAN spécifique et est associée à un numéro de VLAN via l'encapsulation IEEE 802.1Q.

*   **Encapsulation / Traitement** :
    *   **Entrée** : Une trame Ethernet provenant d'un hôte d'un VLAN donné arrive au commutateur de couche 2. Si le trafic est destiné à un autre VLAN, le commutateur l'envoie vers l'interface trunk connectée au routeur, ajoutant une balise **802.1Q** contenant l'ID du VLAN d'origine.
    *   **Action** : Le routeur reçoit la trame tagguée sur son interface physique. La sous-interface correspondant à l'ID du VLAN d'origine décapsule la trame (retire la balise 802.1Q), examine l'adresse IP de destination, prend une décision de routage, puis ré-encapsule le paquet avec la balise 802.1Q du VLAN de destination avant de le renvoyer via la même interface physique vers le commutateur.
    *   **Sortie** : Le commutateur reçoit la trame tagguée du routeur, identifie le VLAN de destination grâce à la balise, et transfère la trame (après avoir retiré la balise pour un port d'accès) à l'hôte destinataire.

### 2. Commutateur multicouche (Layer 3 Switch)
Un **commutateur multicouche** est un appareil capable d'effectuer à la fois la commutation (Couche 2) et le routage (Couche 3). Il utilise des **Interfaces VLAN virtuelles (SVIs - Switched Virtual Interfaces)**, qui sont des interfaces logiques configurées avec une adresse IP pour chaque VLAN, agissant comme la passerelle par défaut pour ce VLAN. Le routage est effectué directement au niveau matériel, ce qui est généralement plus rapide que le "router-on-a-stick".

*   **Encapsulation / Traitement** :
    *   **Entrée** : Une trame Ethernet provenant d'un hôte arrive au commutateur multicouche. Si le trafic est destiné à un autre VLAN, le commutateur reconnaît que la destination est sur un autre sous-réseau/VLAN.
    *   **Action** : Le commutateur multicouche route le paquet entre les SVIs correspondantes. L'encapsulation (ajout/retrait de la balise 802.1Q) est gérée en interne par le matériel du commutateur sans avoir besoin de faire transiter le trafic par une interface physique externe.
    *   **Sortie** : Le commutateur multicouche transfère la trame (potentiellement détagguée si le port est en mode accès) à l'hôte de destination dans le VLAN cible.

```mermaid
graph TD
    subgraph VLAN_10
        PC_A[PC A (VLAN 10)]
    end

    subgraph VLAN_20
        PC_B[PC B (VLAN 20)]
    end

    subgraph Core
        SW_L2[Switch L2]
        ROUTER[Routeur (Router-on-a-Stick)]
        SW_L3[Switch Multicouche (L3)]
    end

    PC_A -- Trafic untagged --> SW_L2
    SW_L2 -- Trame tagged (VLAN 10) --> ROUTER
    ROUTER -- Route entre sous-interfaces --> ROUTER
    ROUTER -- Trame tagged (VLAN 20) --> SW_L2
    SW_L2 -- Trafic untagged --> PC_B

    PC_A -- Trafic untagged --> SW_L3
    SW_L3 -- Routage Interne (SVI) --> SW_L3
    SW_L3 -- Trafic untagged --> PC_B

    style ROUTER fill:#f9f,stroke:#333,stroke-width:2px
    style SW_L3 fill:#9cf,stroke:#333,stroke-width:2px
```

## 💡 Cas d'Usage Typique
Le routage Inter-VLAN est essentiel pour la flexibilité, la sécurité et l'optimisation des réseaux d'entreprise.
1.  **Sécurité et Isolation** : Isoler les départements (ex: Comptabilité, RH, IT) ou les types de trafic (ex: voix, données, gestion) dans des VLANs distincts pour limiter les domaines de diffusion et améliorer la sécurité en contrôlant les communications entre eux via des politiques de routage.
2.  **Optimisation des performances réseau** : En segmentant le réseau, on réduit la taille des domaines de diffusion, ce qui diminue le trafic inutile et améliore les performances globales du réseau. Le routage direct par un commutateur L3 est plus rapide que de faire transiter le trafic par un routeur externe.
3.  **Gestion et Flexibilité** : Faciliter la gestion du réseau et permettre aux utilisateurs de différents VLANs d'accéder à des ressources partagées (serveurs, imprimantes) situées dans d'autres VLANs, tout en conservant une séparation logique.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Performance (Router-on-a-Stick)** : L'utilisation d'une seule liaison physique pour tout le trafic Inter-VLAN via un routeur peut créer un goulot d'étranglement (single point of failure et de congestion), surtout dans les grands réseaux avec un trafic Inter-VLAN élevé.
> *   **Coût** : Les commutateurs multicouches, bien que plus performants, sont généralement plus coûteux que les commutateurs de Couche 2 et les routeurs bas de gamme.
> *   **Complexité de configuration** : La configuration des sous-interfaces sur un routeur ou des SVIs sur un commutateur multicouche nécessite une bonne compréhension des concepts VLAN et routage.
> *   **Sécurité** : Une mauvaise configuration peut entraîner des vulnérabilités, permettant potentiellement l'accès non autorisé entre VLANs si les listes de contrôle d'accès (ACLs) ne sont pas correctement appliquées.