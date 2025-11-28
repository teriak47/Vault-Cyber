---
aliases:
  - VMware
  - VMware Inc.
  - Virtualisation VMware
archetype: logiciel
cssclasses:
  - max
tags:
  - logiciel/vmware
  - logiciel/vmware/esxi
  - logiciel/vmware/vcenter-server
  - logiciel/vmware/vsphere
  - hyperviseur
  - virtualisation
  - cloud
  - infrastructure/data-center
  - infrastructure/it
  - systeme/exploitation
  - systeme/configuration
  - gestion-configuration
  - port
  - port/443
  - port/902
  - port/427
  - port/80
  - port/389
  - port/636
  - log
  - log/gestion
  - log/syslog
  - outil/powercli
  - logiciel/vcenter-log-insight
  - web/api
  - hardening
  - checklist
  - securite/checklist
  - securite/correctif
  - vulnerabilite
  - cve
  - cve/2021-21974
  - cve/2021-21985
  - cve/2024-37079
  - cve/2024-37080
  - vulnerabilite/mauvaise-configuration
  - vulnerabilite/buffer-overflow/heap-based
  - vulnerabilite/execution-code-distance
  - attaque
  - malware/ransomware
  - attaque/lateralisation
  - protocole/openslp
  - protocole/ldap
  - protocole/dce-rpc
  - protocole/http
  - protocole/https
  - segmentation/micro-segmentation
  - logiciel/vmware-nsx
  - logiciel/vsan
---

# VMware

> [!summary] À quoi ça sert ?
> **VMware** est une entreprise pionnière et leader dans le domaine de la **virtualisation**, offrant des solutions logicielles qui permettent l'exécution de multiples systèmes d'exploitation sur une seule machine physique. Ses produits principaux, tels qu'**ESXi** et **vSphere**, sont fondamentaux pour le _cloud computing_, la gestion de _datacenters_ et l'optimisation des infrastructures IT, en offrant flexibilité, efficacité et résilience aux entreprises.

## ⚙️ Configuration Clé
*   **Fichiers de conf (Exemples)** :
    *   Pour ESXi : Les fichiers de configuration peuvent être modifiés via `/bin/configstorecli` dans le _ConfigStore_ d'ESXi. Des fichiers de logs spécifiques comme `/etc/vmware/hostd/proxy.xml` peuvent être édités pour changer les ports.
    *   Pour vCenter Server : Les configurations sont souvent gérées via l'interface web ou des scripts _PowerCLI_. Les paramètres avancés sont accessibles via les outils de gestion.
*   **Ports par défaut (Exemples)** :
    *   **ESXi** :
        *   **443** (TCP) : Interface de gestion _vSphere Client_ et API.
        *   **902** (TCP & UDP) : Communication avec _vCenter Server_ et accès à la console des VMs.
        *   **427** (TCP) : _OpenSLP_, cible de vulnérabilités passées.
    *   **vCenter Server** :
        *   **80** (TCP) : Redirection HTTP vers HTTPS.
        *   **443** (TCP) : HTTPS pour l'accès _vSphere Web Client_ et API.
        *   **389** (TCP) : _vCenter_ requiert ce port pour l'authentification (_LDAP_).
        *   **636** (TCP) : SSL pour le mode lié (_Linked Mode_).
*   **Logs** :
    *   **ESXi** : Les fichiers de journaux sont généralement stockés dans `/var/log/` (ou sur une _Scratch Partition_ si configurée). Des exemples incluent `/var/log/hostd.log` (gestion hôte), `/var/log/vmkernel.log` (_Core VMkernel_), `/var/log/auth.log` (authentification).
    *   **vCenter Server** : Les journaux sont regroupés par composant et accessibles via l'interface (_vSphere Client_) ou dans des répertoires spécifiques. Le fichier `vpxd.log` est le principal journal du _vCenter Server_.

## 🔒 Guide de Durcissement (Hardening)
> [!check] Checklist Sécurité
> - [ ] **Appliquer régulièrement les correctifs de sécurité (patchs)** : C'est une action critique pour se protéger contre les vulnérabilités connues (ex: CVE-2021-21974, CVE-2021-21985).
> - [ ] **Changer les mots de passe par défaut et renforcer les politiques de mots de passe** : Utiliser des mots de passe complexes et uniques pour les comptes _root_ et administrateurs.
> - [ ] **Désactiver les services et fonctionnalités inutiles** : Minimiser la surface d'attaque en désactivant les services non essentiels, notamment _OpenSLP_ si non utilisé.
> - [ ] **Restreindre l'accès réseau aux interfaces de gestion** : Isoler le réseau de gestion et implémenter des règles de pare-feu pour autoriser uniquement les IPs et ports nécessaires (ex: 443, 902).
> - [ ] **Utiliser des comptes dédiés (non-root) avec des privilèges moindres** : Ne pas utiliser le compte _root_ pour les opérations quotidiennes.
> - [ ] **Activer la journalisation détaillée (logs verbeux) et centraliser les logs** : S'assurer que les logs sont conservés de manière persistante et consultés régulièrement via un système _syslog_ centralisé ou _vCenter Log Insight_.
> - [ ] **Implémenter la micro-segmentation avec des outils comme VMware NSX** : Pour isoler les machines virtuelles et restreindre la communication entre elles.
> - [ ] **Suivre les guides de durcissement officiels de VMware** : VMware publie des guides de configuration et de durcissement pour vSphere.

## ⚠️ Surfaces d'Attaque Communes
*   **Mauvaise configuration** : Des configurations laxistes des droits d'accès, des réseaux non segmentés, ou des services non sécurisés peuvent exposer l'infrastructure. Un exemple est la mauvaise gestion des paramètres _vCenter Server_.
*   **Vulnérabilités logicielles (CVEs fréquentes)** :
    *   **CVE-2021-21974 / CVE-2020-3992** : Vulnérabilités dans le service _OpenSLP_ d'ESXi, permettant l'exécution de code à distance et exploitées par des _ransomwares_.
    *   **CVE-2021-21985** : Vulnérabilité critique dans le plug-in _Virtual SAN (vSAN) Health Check_ de _vCenter Server_, permettant l'exécution de commandes à distance sans authentification via le port 443.
    *   **CVE-2024-37079 et CVE-2024-37080** : Failles de débordement de tas (_heap overflow_) dans l'implémentation du protocole _DCE/RPC_ de _vSphere ESXi_, pouvant mener à l'exécution de code malveillant à distance.
*   **Attaques par rançongiciel (Ransomware)** : Les infrastructures de virtualisation, y compris _VMware ESXi_, sont des cibles privilégiées en raison de la concentration de machines virtuelles, ce qui maximise l'impact d'une attaque.
*   **Latéralisation depuis l'environnement bureautique ou un sous-traitant** : Une compromission initiale peut conduire à une propagation vers l'infrastructure de virtualisation.
*   **Accès non autorisé ou escalade de privilèges** : L'utilisation de comptes par défaut, de mots de passe faibles ou l'exploitation de failles (comme CVE-2024-37081) peut permettre à un attaquant d'obtenir un accès privilégié.