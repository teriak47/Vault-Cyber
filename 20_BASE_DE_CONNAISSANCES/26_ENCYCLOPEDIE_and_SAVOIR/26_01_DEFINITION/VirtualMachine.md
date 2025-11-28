---
aliases:
  - Machine virtuelle
  - Virtual Machine
  - machines virtuelles (VMs)
archetype: definition
cssclasses:
  - max
tags:
  - virtualisation
  - virtualisation/machine-virtuelle
  - hyperviseur
  - hyperviseur/type-1
  - hyperviseur/type-2
  - logiciel/vmware
  - logiciel/vmware/esxi
  - logiciel/vmware/workstation-player
  - microsoft/hyper-v
  - logiciel/citrix-xenserver
  - logiciel/oracle-virtualbox
  - logiciel/parallels-desktop
  - systeme-exploitation
  - isolation
  - pra
  - securite/sandboxing
  - developpement/test
  - serveur
  - infrastructure/it
  - virtualisation/consolidation
  - virtualisation/portabilite
  - ressources-virtuelles
  - ibm
---

# Virtual Machine

> [!question] C'est quoi ?
> Une **machine virtuelle** (VM) est une émulation logicielle d'un système informatique physique, exécutant un système d'exploitation invité (guest OS) sur un système hôte (host OS).

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le concept de la **virtualisation** a émergé dans les années 1960 avec les systèmes IBM pour optimiser l'utilisation des mainframes. La popularisation des machines virtuelles pour les architectures x86 a débuté à la fin des années 1990 et au début des années 2000, notamment avec des entreprises comme VMware.

## 💡 Exemples Concrets

### Fonctionnement
Une VM fonctionne grâce à un logiciel appelé **hyperviseur** (ou moniteur de machine virtuelle), qui crée et gère les environnements virtuels. L'hyperviseur alloue les ressources physiques de la machine hôte (CPU, RAM, stockage, réseau) aux différentes machines virtuelles, permettant à chaque VM d'opérer comme un ordinateur indépendant avec son propre système d'exploitation et ses applications.

### Hyperviseur
L'hyperviseur est la couche logicielle qui permet la **virtualisation**. Il agit comme un intermédiaire entre le matériel physique de l'ordinateur hôte et les systèmes d'exploitation invités des VMs.

*   **Types d'hyperviseurs** :
    *   **Type 1 (Bare-Metal)** : Il s'exécute directement sur le matériel physique de l'ordinateur, sans système d'exploitation hôte sous-jacent. Exemples : *VMware ESXi*, *Microsoft Hyper-V*, *Citrix XenServer*. Ces hyperviseurs sont privilégiés dans les environnements de serveurs d'entreprise pour leur performance et leur sécurité.
    *   **Type 2 (Hébergé)** : Il s'exécute comme une application normale au sein d'un système d'exploitation hôte. Exemples : *Oracle VirtualBox*, *VMware Workstation*, *Parallels Desktop*. Ils sont souvent utilisés pour le développement, les tests ou l'utilisation personnelle.

### Composants d'une VM
Chaque machine virtuelle possède ses propres composants virtualisés :
*   **CPU virtuel** : Représente les cœurs de processeur alloués.
*   **RAM virtuelle** : Mémoire vive dédiée.
*   **Stockage virtuel** : Souvent sous forme de fichiers disque virtuels sur le système hôte.
*   **Interface réseau virtuelle** : Permet à la VM de communiquer avec le réseau physique.

### Avantages de la Virtualisation
*   **Consolidation des serveurs** : Réduction du nombre de serveurs physiques, d'où des économies d'énergie et d'espace.
*   **Isolation** : Chaque VM est isolée des autres, ce qui améliore la sécurité et la stabilité.
*   **Portabilité** : Une VM peut être facilement déplacée d'un hôte physique à un autre.
*   **Développement et test** : Création rapide d'environnements pour tester des logiciels ou des configurations sans impacter le système principal.
*   **Reprise après sinistre** : Facilite la sauvegarde et la restauration des systèmes.

### Cas d'Utilisation
*   **Hébergement de multiples services** sur un seul serveur physique.
*   **Environnements de développement et de test** pour des applications web ou logicielles.
*   **Exécution d'applications héritées** qui nécessitent des systèmes d'exploitation plus anciens.
*   **Sandboxing** pour tester des logiciels potentiellement dangereux en toute sécurité.