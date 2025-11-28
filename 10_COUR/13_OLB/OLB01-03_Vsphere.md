---
cssclasses:
  - max
archetype: cour
module: "OLB (Introduction Logiciel et OS)"
aliases:
  - 01-03 | vSphere
tags:
  - labo
  - virtualisation
  - virtualisation/machine-virtuelle
  - logiciel/vmware
  - logiciel/vmware/esxi
  - logiciel/vmware/vcenter-server
  - logiciel/vmware/workstation-player
  - hyperviseur
  - hyperviseur/type-1
  - serveur
  - systeme-exploitation
  - reseau
  - stockage/donnees
  - materiel/peripherique/stockage
  - processeur
  - memoire/vive
---

# 01-03 | vSphere

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Accéder aux machines virtuelles (VM) hébergées sur l'infrastructure vSphere via VMware Workstation ou le client vSphere.
> 2. Gérer les opérations de base des machines virtuelles (démarrage, arrêt).
> 3. Créer une nouvelle machine virtuelle sur l'environnement vSphere en respectant les paramètres définis.

## 📝 Synthèse du Cours

### 1. Accéder et Gérer les Machines Virtuelles (VMs) sous vSphere

Pour interagir avec les machines virtuelles hébergées sur l'infrastructure vSphere du réseau CIDC.be, plusieurs méthodes d'accès sont disponibles, nécessitant au préalable une connexion au réseau **CIDC.be** (en classe ou via VPN).

#### 1.1 Accès via VMware Workstation

*   **Connexion au Serveur** :
    *   Dans VMware Workstation, sélectionnez « Connect To Server ».
    *   Indiquez le nom du serveur : `vcsa.cidc.be`.
    *   Utilisez vos identifiants CIDC pour l'authentification.
*   **Accès aux VMs** : Une fois connecté, vous avez accès à la liste de vos machines virtuelles.
*   **Actualisation** : Après toute modification, il est nécessaire de rafraîchir la vue en sélectionnant « Refresh » pour que les changements soient visibles.

#### 1.2 Accès via le Client vSphere (Interface Web)

L'interface web de vSphere offre un accès plus complet pour la gestion des VMs et la création de nouvelles machines virtuelles.

*   **Connexion à l'Interface Web** :
    *   Ouvrez un navigateur et accédez à l'URL : `https://vcsa.cidc.be/`.
    *   Sur la page d'accueil, cliquez sur « Lancer vSphere Client ».
    *   Authentifiez-vous avec vos identifiants CIDC.
*   **Lancement de la Console VM** :
    *   Une fois dans l'interface, pour interagir directement avec une VM, sélectionnez-la et cliquez sur « Lancer la console ».
    *   Choisissez « VMware Remote Console » (VMRC). L'application VMware Remote Console se lancera et affichera la console de la VM.

#### 1.3 Gestion des VMs

*   **Opérations de base** : Depuis l'interface VMware Workstation ou vSphere Client, vous pouvez allumer ou éteindre vos machines virtuelles en effectuant un clic droit sur la VM et en choisissant l'option d'alimentation appropriée.

> [!note] Définition Clé
> vSphere : Suite logicielle de virtualisation de serveur de VMware qui permet de créer, de gérer et d'exécuter des machines virtuelles sur un serveur physique (hôte ESXi) et de centraliser leur gestion via vCenter Server.

### 2. Création d'une Machine Virtuelle (VM) sous vSphere

La création d'une nouvelle machine virtuelle via l'interface web de vSphere suit un processus guidé.

#### 2.1 Préparation

*   **Création d'un Dossier** : Il est recommandé de créer un dossier dédié à vos VMs si ce n'est pas déjà fait, pour organiser votre inventaire.

#### 2.2 Lancement de l'Assistant de Création

*   Dans votre dossier, ouvrez le menu contextuel (clic droit ou bouton d'action) et sélectionnez « Nouvelle machine Virtuelle ».

#### 2.3 Étapes de la Création

1.  **Type de Création** : Généralement, choisissez "Créer une nouvelle machine virtuelle".
2.  **Nom et Dossier** :
    *   Vérifiez que le dossier cible est bien sélectionné.
    *   Nommez la VM selon le format : `5X79 - Nom Prénom - Nom de l'OS` (ex: `5X79 - Aurelien Cuvelier - Windows 10`).
3.  **Sélectionner une Ressource** : L'assistant vous guidera pour choisir l'hôte ESXi ou le cluster sur lequel la VM sera déployée.
4.  **Sélectionner un Stockage** : Choisissez l'espace de stockage approprié pour les fichiers de la VM :
    *   `DS1-Student`
    *   `DS2-Student`
5.  **Sélectionner une Compatibilité** : Définissez la compatibilité matérielle de la VM.
6.  **Sélectionner un Système d'Exploitation Invité** : Choisissez le type et la version du système d'exploitation que vous comptez installer sur la VM.
7.  **Personnaliser le Matériel** :
    *   **CPU** : Allouez 4 vCPU.
    *   **RAM** : Allouez 8 Go de mémoire vive.
    *   **Disque Dur** : Configurez un disque de 80 Go, de préférence en mode *Dynamique* (thin provisioned).
    *   **Nouveau réseau** : Sélectionnez le réseau `DVS-Lab-Vlan30-DHCP` et assurez-vous qu'il est "Connecté".
    *   **Nouveau lecteur CD/DVD** :
        *   Sélectionnez l'option "Fichier ISO de la bibliothèque de contenu".
        *   Parcourez la bibliothèque pour choisir le fichier ISO du système d'exploitation à installer.
        *   Assurez-vous que l'option "Connecter" est cochée pour le lecteur CD/DVD.
8.  **Prêt à Terminer** : Vérifiez le récapitulatif des configurations et cliquez sur "Terminer" pour créer la VM.

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A[Utilisation de vSphere] --> B(Accès aux VMs)
    A --> C(Création de VMs)

    B --> B1[Accès via VMware Workstation]
    B --> B2[Accès via vSphere Client Web]
    B --> B3[Gestion des VMs]

    B1 --> B1_1[Connect To Server: vcsa.cidc.be]
    B1 --> B1_2[Authentification CIDC]
    B1 --> B1_3[Refresh après modifications]

    B2 --> B2_1[Accéder à https://vcsa.cidc.be/]
    B2 --> B2_2[Lancer vSphere Client]
    B2 --> B2_3[Lancer la console (VMRC)]

    B3 --> B3_1[Allumer/Éteindre VMs (Clic droit)]

    C --> C1[Préparation: Créer Dossier]
    C --> C2[Lancer Assistant "Nouvelle machine virtuelle"]
    C --> C3[Étapes de Configuration]

    C3 --> C3_1[Nom et Dossier (Ex: 5X79 - Nom Prenom - OS)]
    C3 --> C3_2[Sélectionner Ressource]
    C3 --> C3_3[Sélectionner Stockage (DS1/DS2-Student)]
    C3 --> C3_4[Compatibilité]
    C3 --> C3_5[Système d'Exploitation Invité]
    C3 --> C3_6[Personnaliser Matériel]
    C3_6 --> C3_6_1[CPU: 4]
    C3_6 --> C3_6_2[RAM: 8 Go]
    C3_6 --> C3_6_3[Disque Dur: 80 Go Dynamique]
    C3_6 --> C3_6_4[Réseau: DVS-Lab-Vlan30-DHCP (Connecter)]
    C3_6 --> C3_6_5[Lecteur CD/DVD: ISO de la Bibliothèque (Connecter)]
    C3 --> C3_7[Terminer]
```

## ❓ Quiz de Révision (Active Recall)
> [!question] Question 1
> Quel est le nom de serveur à utiliser pour se connecter à l'environnement vSphere CIDC.be via VMware Workstation ?
> > [!success]- Réponse
> > Le nom du serveur est `vcsa.cidc.be`.

> [!question] Question 2
> Lors de la création d'une nouvelle machine virtuelle sous vSphere, quels sont les paramètres recommandés pour le CPU, la RAM et le Disque Dur pour un usage standard en laboratoire ?
> > [!success]- Réponse
> > Les paramètres recommandés sont : 4 vCPU, 8 Go de RAM et un Disque Dur de 80 Go (dynamique).

> [!question] Question 3
> Quel est le réseau à sélectionner pour une nouvelle VM afin d'obtenir une adresse IP via DHCP dans l'environnement de laboratoire CIDC ?
> > [!success]- Réponse
> > Le réseau à sélectionner est `DVS-Lab-Vlan30-DHCP`.

## 🔗 Notes Connexes
*   **Module parent**: [[OLB00-00_Introduction|OLB : Introduction Logiciel et OS]]
*   **Cours précédent**: [[OLB01-02_Cours2WindowsServer2022|01-02 | Cours 2 - Windows Server 2022]]
*   **Cours suivant**: 