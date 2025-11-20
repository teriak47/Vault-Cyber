---
tags:
  - logiciel
  - domain-controller
  - active-directory
  - annuaire
  - authentification
  - gestion/identite/acces
  - serveur
  - architecture-reseau
  - infrastructure
aliases:
  - Contrôleur de Domaine
  - Active Directory Domain Controller
  - DC
archetype: logiciel
version:
cssclasses:
  - max
source:
---

# Contrôleur de Domaine (Domain Controller)

## 🎯 Rôle et Fonction
> Un Contrôleur de Domaine est un serveur qui héberge l'Active Directory et gère l'authentification et l'autorisation des utilisateurs et des ressources au sein d'un environnement Windows. Il est l'épine dorsale de la gestion des identités et des accès dans les entreprises utilisant Active Directory. Il stocke des informations sur les utilisateurs, les ordinateurs et d'autres ressources réseau, permettant aux administrateurs de gérer de manière centralisée les politiques de sécurité, les mots de passe et les permissions.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   Base de données Active Directory (NTDS.DIT)
    *   Stratégies de groupe (Group Policy Objects - GPO)
    *   Fichiers de journalisation des événements
*   **Modules importants**:
    *   Services de domaine Active Directory (AD DS)
    *   Services DNS
    *   Services LDAP
    *   Centre de distribution de clés Kerberos (KDC)
*   **Dépendances**:
    *   Windows Server
    *   DNS
    *   Réseau stable et performant

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Application du Principe du Moindre Privilège**: Limiter strictement les droits d'administration sur les Contrôleurs de Domaine.
*   **Gestion des mises à jour rigoureuse**: Appliquer rapidement les correctifs de sécurité pour l'OS et Active Directory.
*   **Authentification Multi-Facteurs (MFA)**: Exiger la MFA pour tous les comptes administratifs.
*   **Segmentation réseau**: Isoler les Contrôleurs de Domaine sur un segment réseau dédié avec des règles de pare-feu strictes.
*   **Désactivation des services inutiles**: Réduire la surface d'attaque en désactivant tous les services non essentiels.
*   **Sécurisation physique**: Assurer la sécurité physique des serveurs hébergeant les Contrôleurs de Domaine.

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   Journal des événements de sécurité (Log d'audit de connexion, accès aux objets)
    *   Journal des services d'annuaire (événements liés à Active Directory)
    *   Journal DNS (activités de résolution de noms)
*   **Commandes d'audit**:
```bash
# Vérifier la santé du contrôleur de domaine
dcdiag /q

# Vérifier la réplication Active Directory
repadmin /showrepl

# Lister les membres d'un groupe d'administration sensible (exemple)
net group "Domain Admins" /domain
```
*   **Outils de surveillance**: SIEM pour la corrélation des logs et la détection d'anomalies.

## 🔗 Notes Connexes
*   **Concept parent**: Active Directory
*   **Protocole d'authentification clé**: Kerberos
*   **Protocole de services d'annuaire**: LDAP
*   **Principe de sécurisation essentiel**: Principe du Moindre Privilège
*   **Vulnérabilité typique**: Prise de contrôle de compte