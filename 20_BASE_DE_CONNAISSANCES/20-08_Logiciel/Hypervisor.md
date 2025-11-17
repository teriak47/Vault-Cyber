---
tags:
  - logiciel
  - hyperviseur
  - virtualisation
  - securite/virtualisation
  - environnement-virtuel
  - architecture
  - composant
  - technologie
aliases:
  - Hyperviseur
  - Virtual Machine Monitor
  - VMM
archetype: logiciel
version:
cssclasses:
  - max
source:
---

# Hyperviseur

## 🎯 Rôle et Fonction
> Un hyperviseur, également connu sous le nom de Virtual Machine Monitor (VMM), est un [[Software|logiciel]], [[Firmware|micrologiciel]] ou [[Hardware|matériel]] qui crée et exécute des [[VirtualMachine|machines virtuelles]] (VMs). Il permet à plusieurs [[OperatingSystem|systèmes d'exploitation]] de partager une seule plateforme [[Hardware|matérielle]] hôte en isolant les environnements et en gérant les ressources de chaque VM.

## ⚙️ Configuration
* **Fichiers de configuration clés**:
  * `hypervisor.conf` (exemple générique)
  * `vms_config.xml` (pour la définition des VMs)
* **Modules importants**: Gestion de la [[Virtualization|virtualisation]] CPU/mémoire, gestion du réseau virtuel, gestion du stockage virtuel.
* **Dépendances**: [[Hardware|Matériel]] compatible avec la virtualisation (Intel VT-x, AMD-V), [[OperatingSystem|Système d'exploitation]] hôte (pour les hyperviseurs de Type 2).

## 🔒 Sécurisation (Durcissement / Hardening)
* **Mise à jour régulière**: Appliquer les [[PatchManagement|patchs]] de sécurité pour l'hyperviseur et les [[VirtualMachine|VMs]] afin de corriger les [[Vulnerability|vulnérabilités]].
* **[[AccessControl|Contrôle d'accès]] strict**: Mettre en œuvre le [[PrincipleOfLeastPrivilege|principe de moindre privilège]] pour les comptes administrateurs de l'hyperviseur et des VMs.
* **[[NetworkSegmentation|Segmentation réseau]]**: Isoler les réseaux des [[VirtualMachine|VMs]] les uns des autres et du réseau de gestion de l'hyperviseur pour prévenir la [[LateralMovement|propagation latérale]] d'attaques.
* **Durcissement de l'hôte**: Sécuriser le [[OperatingSystem|système d'exploitation]] hôte (pour les hyperviseurs de Type 2) ou la base de l'hyperviseur (pour Type 1) en désactivant les services inutiles et en configurant des [[SecurityPolicy|politiques de sécurité]] robustes.

## 🔍 Audit et Surveillance
* **Logs importants**:
  * Journaux d'événements de l'hyperviseur (création/suppression de VMs, changements de configuration, alertes de sécurité).
  * Journaux d'accès aux interfaces de gestion de l'hyperviseur.
* **Commandes d'audit**:
```bash
# Vérifier l'état des VMs (exemple générique)
virsh list --all
# Vérifier la configuration réseau de l'hyperviseur (exemple Open vSwitch)
ovs-vsctl show
# Afficher les journaux de l'hyperviseur (exemple Linux)
journalctl -u hypervisor_service
```

## 🔗 Notes Connexes
* **Concept parent**: [[Virtualization|Virtualisation]]
* **Élément géré**: [[VirtualMachine|Machine Virtuelle]]
* **Contexte d'application**: [[CloudSecurity|Sécurité du Cloud]]
* **Menace associée**: [[SystemCompromise|Compromission de Système]]
* **Technologie de base**: [[Hardware|Matériel]]