---
tags:
  - logiciel
  - active-directory
  - annuaire
  - gestion/identite/acces
  - authentification
  - domain-controller
  - infrastructure
  - securite/systeme
  - logiciel/windows
  - reseau
  - gestion/privileges
aliases:
  - AD DS
  - Active Directory Domain Services
  - Services de Domaine Active Directory
archetype: logiciel
version:
cssclasses:
  - max
---

# Active Directory Domain Services (AD DS)

## 🎯 Rôle et Fonction
> Active Directory Domain Services (AD DS) est un service d'annuaire développé par Microsoft pour les réseaux de systèmes d'exploitation Windows. Il fournit un moyen centralisé de gérer et de sécuriser les ressources d'une entreprise, incluant les utilisateurs, les ordinateurs et les applications. AD DS est le fondement de la gestion des identités et des accès (IAM) dans les environnements Windows, permettant l'authentification et l'autorisation des utilisateurs et des processus au sein du réseau d'entreprise.

## ⚙️ Configuration
*   **Fichiers et outils de configuration clés**:
    *   Le schéma Active Directory définit la structure de l'annuaire.
    *   Les Objets de Stratégie de Groupe (GPO) sont utilisés pour configurer et appliquer des paramètres de sécurité et des stratégies aux utilisateurs et aux ordinateurs liés au domaine.
    *   Les outils de gestion Active Directory (Utilisateurs et ordinateurs, Sites et services, Domaines et approbations) sont utilisés pour l'administration.
*   **Composants importants**:
    *   Contrôleurs de Domaine : Serveurs qui hébergent les copies de l'annuaire Active Directory.
    *   DNS (Domain Name System) : Essentiel pour la résolution des noms et la localisation des services au sein d'un domaine Active Directory.
    *   Catalogue Global : Une copie partielle de toutes les partitions d'annuaire de chaque domaine dans la forêt, permettant des recherches rapides.
*   **Dépendances**:
    *   DNS
    *   Kerberos (protocole d'authentification par défaut)

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Application du Principe du Moindre Privilège**: Accorder aux utilisateurs et aux services uniquement les privilèges nécessaires à l'exécution de leurs tâches.
*   **Sécurisation des Contrôleurs de Domaine**: Renforcer la sécurité physique et logique des DCs, car leur compromission peut entraîner une compromission complète du système.
*   **Mise en œuvre de politiques de mots de passe forts via les GPO**: Appliquer des exigences de mots de passe complexes, des rotations régulières et des politiques de verrouillage de compte.
*   **Gestion des Patchs régulière**: Maintenir à jour tous les serveurs Active Directory et les ordinateurs membres pour se protéger contre les vulnérabilités logicielles connues, y compris les zero-days.
*   **Implémentation de MFA**: Renforcer l'authentification pour les comptes privilégiés afin de prévenir les prises de contrôle de compte.
*   **Segmentation réseau**: Isoler les contrôleurs de domaine dans un segment réseau hautement sécurisé pour limiter le mouvement latéral en cas de cyberattaque.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   Journaux d'événements de sécurité Windows (`Security.evtx`) pour les tentatives d'authentification, les modifications de GPO, et les accès aux ressources.
    *   Journaux des services d'annuaire pour les événements liés à la réplication et à l'intégrité de l'annuaire.
*   **Commandes et outils d'audit**:
```bash
# Vérifier la réplication Active Directory
repadmin /showrepl

# Lister les GPO appliquées à un utilisateur ou un ordinateur
gpresult /r

# Vérifier l'état des services liés à Active Directory
Get-Service -DisplayName *Active* | Select-Object Name, Status
```
*   Utilisation de SIEM pour la collecte et l'analyse d'anomalies des journaux.

## 🔗 Notes Connexes
*   **Concept parent**: ActiveDirectory
*   **Composant central**: DomainController
*   **Outil de gestion de la sécurité**: Objet de Stratégie de Groupe (GPO)
*   **Mécanisme d'authentification**: Authentication
*   **Vulnérabilité exploitée**: Escalade de Privilèges