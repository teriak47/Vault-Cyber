---
aliases:
  - Hyperviseur
  - Hypervisor
  - Type 1 Hypervisor
  - Type 2 Hypervisor
  - Bare-Metal Hypervisor
  - Hosted Hypervisor
archetype: definition
cssclasses:
  - max
tags:
  - hyperviseur
  - virtualisation
  - virtualisation/machine-virtuelle
  - hyperviseur/type-1
  - logiciel/vmware/esxi
  - microsoft/hyper-v
  - logiciel/kvm
  - hyperviseur/type-2
  - logiciel/oracle-virtualbox
  - logiciel/vmware/workstation-player
  - histoire/virtualisation
---

# Hypervisor

> [!question] C'est quoi ?
> Un *hyperviseur* est un logiciel, un firmware ou un matériel qui crée et gère des machines virtuelles (VM), permettant à plusieurs systèmes d'exploitation invités de fonctionner simultanément sur une seule machine physique.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le concept d'*hyperviseur*, initialement appelé "Control Program" (CP), est apparu dans les années 1960 avec le système IBM CP-40, évoluant plus tard vers CP-67 et VM/370. Le terme "hyperviseur" lui-même est une évolution du mot "superviseur", qui désignait les noyaux de système d'exploitation traditionnels, "hyper" suggérant un niveau de contrôle supérieur.

## 💡 Exemples Concrets
*   **Exemple 1 (Hyperviseur de Type 1 - Bare-Metal)** : Un serveur d'entreprise exécutant *VMware ESXi*, *Microsoft Hyper-V* ou *KVM* (Kernel-based Virtual Machine) directement sur son matériel physique, où l'hyperviseur est le premier logiciel à démarrer et gère toutes les ressources matérielles pour les machines virtuelles invitées.
*   **Exemple 2 (Hyperviseur de Type 2 - Hosted)** : Un utilisateur installant *VirtualBox* ou *VMware Workstation* sur son ordinateur portable (qui exécute déjà un système d'exploitation comme Windows ou macOS) pour créer et exécuter des machines virtuelles, l'hyperviseur s'exécutant alors comme une application au-dessus du système d'exploitation hôte.