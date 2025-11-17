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
> [[ActiveDirectory|Active Directory Domain Services]] (AD DS) est un service d'annuaire développé par Microsoft pour les réseaux de [[Windows|systèmes d'exploitation Windows]]. Il fournit un moyen centralisé de gérer et de sécuriser les ressources d'une [[Enterprise|entreprise]], incluant les [[User|utilisateurs]], les [[Computer|ordinateurs]] et les [[SoftwareApplication|applications]]. AD DS est le fondement de la [[IdentityAndAccessManagement|gestion des identités et des accès]] (IAM) dans les environnements [[Windows|Windows]], permettant l'[[Authentication|authentification]] et l'[[Authorization|autorisation]] des [[User|utilisateurs]] et des [[Process|processus]] au sein du [[CorporateNetwork|réseau d'entreprise]].

## ⚙️ Configuration
*   **Fichiers et outils de configuration clés**:
    *   Le schéma [[ActiveDirectory|Active Directory]] définit la structure de l'annuaire.
    *   Les [[GroupPolicyObject|Objets de Stratégie de Groupe]] (GPO) sont utilisés pour configurer et appliquer des paramètres de sécurité et des stratégies aux [[User|utilisateurs]] et aux [[Computer|ordinateurs]] liés au [[DomainController|domaine]].
    *   Les outils de gestion [[ActiveDirectory|Active Directory]] (Utilisateurs et ordinateurs, Sites et services, Domaines et approbations) sont utilisés pour l'administration.
*   **Composants importants**:
    *   [[DomainController|Contrôleurs de Domaine]] : [[Server|Serveurs]] qui hébergent les copies de l'annuaire [[ActiveDirectory|Active Directory]].
    *   [[DomainNameSystem|DNS]] (Domain Name System) : Essentiel pour la résolution des noms et la localisation des services au sein d'un [[ActiveDirectory|domaine Active Directory]].
    *   Catalogue Global : Une copie partielle de toutes les partitions d'annuaire de chaque [[DomainController|domaine]] dans la forêt, permettant des recherches rapides.
*   **Dépendances**:
    *   [[DomainNameSystem|DNS]]
    *   [[Kerberos]] (protocole d'authentification par défaut)

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Application du [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]**: Accorder aux [[User|utilisateurs]] et aux [[Process|services]] uniquement les [[PrivilegeEscalation|privilèges]] nécessaires à l'exécution de leurs tâches.
*   **Sécurisation des [[DomainController|Contrôleurs de Domaine]]**: Renforcer la [[Security|sécurité]] physique et logique des [[DomainController|DCs]], car leur compromission peut entraîner une [[SystemCompromise|compromission complète du système]].
*   **Mise en œuvre de [[StrongPasswordPolicy|politiques de mots de passe forts]] via les [[GroupPolicyObject|GPO]]**: Appliquer des exigences de [[Password|mots de passe]] complexes, des rotations régulières et des politiques de [[AccountLockout|verrouillage de compte]].
*   **[[PatchManagement|Gestion des Patchs]] régulière**: Maintenir à jour tous les [[Server|serveurs]] [[ActiveDirectory|Active Directory]] et les [[Computer|ordinateurs]] membres pour se protéger contre les [[SoftwareVulnerability|vulnérabilités logicielles]] connues, y compris les [[ZeroDay|zero-days]].
*   **Implémentation de [[MultiFactorAuthentication|MFA]]**: Renforcer l'[[Authentication|authentification]] pour les [[Account|comptes]] privilégiés afin de prévenir les [[AccountTakeover|prises de contrôle de compte]].
*   **[[NetworkSegmentation|Segmentation réseau]]**: Isoler les [[DomainController|contrôleurs de domaine]] dans un [[NetworkSegment|segment réseau]] hautement sécurisé pour limiter le [[LateralMovement|mouvement latéral]] en cas de [[Attack|cyberattaque]].

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   Journaux d'événements de [[Security|sécurité]] [[Windows|Windows]] (`Security.evtx`) pour les tentatives d'[[Authentication|authentification]], les modifications de [[GroupPolicyObject|GPO]], et les accès aux [[Resource|ressources]].
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
*   Utilisation de [[SecurityInformationAndEventManagement|SIEM]] pour la collecte et l'[[AnomalyDetection|analyse d'anomalies]] des [[Log|journaux]].

## 🔗 Notes Connexes
*   **Concept parent**: [[ActiveDirectory]]
*   **Composant central**: [[DomainController]]
*   **Outil de gestion de la sécurité**: [[GroupPolicyObject|Objet de Stratégie de Groupe (GPO)]]
*   **Mécanisme d'authentification**: [[Authentication]]
*   **Vulnérabilité exploitée**: [[PrivilegeEscalation|Escalade de Privilèges]]