---
tags:
  - labo
  - virtualisation
  - environnement-virtuel
  - vmware
  - linux
  - ubuntu
  - systeme/exploitation
  - installation
  - configuration
aliases:
  - Labo Ubuntu VMware
  - Installation Ubuntu Desktop VMware
archetype: labo
technologies:
  - VMware
  - Ubuntu
cssclasses:
  - max
source:
---

# Labo: Installation d'Ubuntu Desktop sur VMware

## 🎯 Objectif du Labo

> Ce laboratoire vise à fournir une base pratique pour la mise en place d'un environnement [[Virtualization|virtuel]] sécurisé. Il se concentre sur l'installation d'Ubuntu Desktop sur une [[VirtualMachine|machine virtuelle]] VMware, servant de plateforme de [[Testing|tests]] pour des outils de [[Cybersecurity|cybersécurité]] ou des développements.

## 🗺️ Architecture Réseau

> Ce labo implique une seule machine virtuelle [[Ubuntu|Ubuntu Desktop]] fonctionnant sur un hyperviseur [[VMware|VMware]] (Workstation, Fusion ou ESXi). La VM sera configurée en mode réseau NAT par défaut, permettant un accès Internet tout en l'isolant du [[PhysicalNetwork|réseau physique]] hôte.

## 🖥️ Composants

- **Machine Virtuelle Ubuntu**:
  - **OS**: [[Ubuntu|Ubuntu Desktop]] (22.04 LTS ou version ultérieure)
  - **Outils**: Aucun outil spécifique à la cybersécurité n'est installé par défaut à ce stade, l'accent est mis sur le [[OperatingSystem|système d'exploitation]] de base.
  - **Configuration Réseau**: Par défaut via [[DynamicHostConfigurationProtocol|DHCP]].
- **Hyperviseur**:
  - **Logiciel**: [[VMware|VMware]] Workstation, Fusion ou ESXi.
  - **OS Hôte**: Windows, [[Linux|Linux]] ou [[MacOS|macOS]].
- **Réseau Virtuel**:
  - **Type**: NAT (Network Address Translation)
  - **Plage d'adresses**: Généralement gérée automatiquement par VMware (ex: 192.168.x.0/24).

## ⚙️ Étapes de Configuration

1.  **Préparation de l'Hyperviseur**: Assurez-vous que le logiciel [[VMware|VMware]] est installé et fonctionnel sur votre [[Computer|ordinateur]] hôte.
2.  **Téléchargement de l'ISO**: Obtenez l'image ISO officielle d'[[Ubuntu|Ubuntu Desktop]] depuis le site web d'Ubuntu.
3.  **Création de la Machine Virtuelle**:
    - Lancez VMware et créez une nouvelle [[VirtualMachine|machine virtuelle]].
    - Sélectionnez l'ISO d'Ubuntu téléchargée comme support d'[[Installation|installation]].
    - Allouez des ressources suffisantes (RAM, processeurs, espace disque) pour un fonctionnement optimal. (Minimum 4GB RAM, 2 CPU Cores, 25GB HDD recommandé).
    - Configurez le réseau en mode NAT par défaut.
4.  **Installation d'Ubuntu Desktop**:
    - Démarrez la [[VirtualMachine|VM]] et suivez les instructions du processus d'installation graphique d'Ubuntu.
    - Choisissez les options par défaut ou personnalisez selon vos besoins (langue, fuseau horaire, création d'un [[User|utilisateur]]).
5.  **Installation des VMware Tools**: Une fois Ubuntu installé, installez les VMware Tools pour améliorer l'intégration entre la VM et l'hôte (meilleure résolution d'écran, glisser-déposer, copier-coller).
6.  **Snapshot Initial**: Créez un snapshot de la [[VirtualMachine|VM]] après l'installation complète et la mise à jour des packages. Ce `snapshot`vous permettra de revenir rapidement à un état propre en cas de problèmes lors de [[Testing|tests]] ultérieurs.

## 🔬 Scénarios d'Utilisation

- Exploration du [[OperatingSystem|système d'exploitation]] [[Linux|Linux]] dans un environnement sûr.
- [[Testing|Tests]] de [[SoftwareApplication|logiciels]] sans affecter l'hôte.
- Base pour d'autres [[Labo|labos]] de [[Cybersecurity|cybersécurité]], comme l'analyse de [[Malware|malware]] ou la pratique d'[[EthicalHacking|ethical hacking]].

## 🔗 Notes Connexes

- **Technologie clé**: [[Virtualization|Virtualisation]]
- **Plateforme**: [[VMware|VMware]]
- **Système d'exploitation**: [[Ubuntu|Ubuntu Desktop]]
- **Type de système**: [[Linux|Linux]]
- **Processus initial**: [[Installation|Installation]]

---
