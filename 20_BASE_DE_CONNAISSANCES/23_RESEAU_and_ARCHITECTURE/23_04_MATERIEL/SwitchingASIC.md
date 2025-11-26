---
aliases:
  - "Circuit Intégré Spécifique aux Applications de Commutation"
  - "ASIC de Commutation"
  - "Switching ASIC"
  - "Merchant Silicon"
archetype: materiel
cssclasses:
  - max
couche_osi:
  - "Couche 2 - Liaison"
  - "Couche 3 - Réseau"
tags:
  - materiel
  - materiel/asic
  - materiel/reseau
  - composant/electronique
  - switch
  - routeur
  - reseau/commutation
  - routage
  - traitement-paquets
  - modele-osi/couche-2
  - modele-osi/couche-3
  - latence
  - debit
  - memoire-tampon
  - mac-address-table
  - routage/table
  - listes-controle-acces
  - qualite-de-service
  - encapsulation
  - protocole/gre
  - protocole/vxlan
  - protocole/mpls
  - langage/p4
  - hardware/firmware
  - systeme-exploitation
  - securite/surete-physique
  - surveillance/environnementale
  - maintenance/mise-a-jour
  - redondance
  - processeur
---

# Switching ASIC

> [!info] Rôle Principal
> Un **Switching ASIC** (Application-Specific Integrated Circuit) est un circuit intégré spécialisé conçu pour exécuter les fonctions de commutation de paquets et de routage dans les équipements réseau tels que les commutateurs et les routeurs. Son rôle principal est d'accélérer le traitement du trafic réseau en effectuant ces opérations directement au niveau matériel, déchargeant ainsi le processeur généraliste (CPU) de ces tâches intensives.

## 🛠️ Spécifications Techniques

| Caractéristique | Valeur |
|---|---|
| **Type** | Circuit Intégré Spécifique aux Applications (ASIC) |
| **Débit Max** | Jusqu'à plusieurs dizaines de Térabits par seconde (Tbps) |
| **Paquets par Seconde (PPS)** | Des milliards de paquets par seconde (Bpps), ex: 8 Bpps pour Tomahawk 3 |
| **Mémoire Tampon** | Variable, de 64 Mo (Tomahawk 3) à 8 Go (Jericho2 avec HBM2) |
| **Tables de Forwarding** | TCAM (Content Addressable Memory Ternaire) pour lookups rapides, SRAM pour tables MAC, supporte des millions d'entrées IPv4/IPv6 |
| **Latence** | Extrêmement faible, de l'ordre de la nanoseconde |
| **Couche OSI** | Couche 2 - Liaison, Couche 3 - Réseau |

## ⚙️ Fonctionnement Interne

Le Switching ASIC est le cœur de la transmission de données dans un commutateur réseau. Il est conçu pour traiter les paquets à des vitesses filaires (line rate) en effectuant des opérations spécifiques au réseau directement dans le silicium.

Il intègre plusieurs blocs fonctionnels spécialisés:
*   **Moteur de Lookup**: Effectue des recherches rapides dans les tables d'adresses MAC pour le forwarding de Couche 2 et dans les tables de routage (FIB) pour le routage de Couche 3.
*   **Moteur de Forwarding**: Décide du port de sortie du paquet et applique les modifications nécessaires (ex: décrémentation du TTL, modification des tags VLAN).
*   **Mémoire Tampon (Buffer)**: Stocke temporairement les paquets en attente de traitement ou de transmission pour gérer les surcharges de trafic.
*   **Moteur de Classification et de Filtrage**: Applique des règles de qualité de service (QoS) et des listes de contrôle d'accès (ACL).

Les ASICs modernes peuvent également prendre en charge des fonctionnalités avancées telles que l'encapsulation de protocoles (GRE, VXLAN, MPLS) et peuvent être programmables (utilisant des langages comme P4) pour adapter le traitement des paquets à des besoins spécifiques. Le CPU généraliste du commutateur gère les plans de contrôle et de gestion, tandis que l'ASIC s'occupe du plan de données, garantissant ainsi des performances optimales.

```mermaid
graph LR
    A["Port d'Entrée"] --> B{Parser Packet};
    B --> C{Moteur de Lookup<br>(MAC, IP, ACL)};
    C --> D{Moteur de Forwarding<br>(Décision de port)};
    D --> E[Buffer de Paquets];
    E --> F["Port de Sortie"];

    subgraph Fonctions Avancées
        D -- Encapsulation/DÉcapsulation --> D;
        C -- Programmabilité (P4) --> C;
    end
```

## 🛡️ Sécurité & Risques

> [!warning] Menaces Physiques
> *   **Accès non autorisé**: Un accès physique au commutateur expose l'ASIC et d'autres composants internes à des manipulations malveillantes, pouvant compromettre l'intégrité ou la disponibilité du réseau.
> *   **Environnement**: Les ASICs sont sensibles aux conditions environnementales. Une surchauffe, une humidité excessive ou des chocs physiques peuvent entraîner des défaillances matérielles permanentes.

> [!tip] Bonnes Pratiques
> 1.  **Sécurité physique**: Déployer les commutateurs dans des baies serveurs verrouillées et sécurisées, avec un contrôle d'accès strict.
> 2.  **Surveillance environnementale**: Mettre en place des systèmes de surveillance de la température et de l'humidité dans les datacenters et les armoires réseau pour prévenir les pannes.
> 3.  **Mises à jour logicielles**: Bien que l'ASIC soit matériel, le firmware et le système d'exploitation du commutateur qui l'interfacent doivent être régulièrement mis à jour pour corriger les vulnérabilités logicielles.
> 4.  **Redondance**: Utiliser des commutateurs avec des ASICs redondants ou des configurations de haute disponibilité pour minimiser l'impact d'une défaillance matérielle.