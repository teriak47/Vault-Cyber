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
> Un [[DomainController|Contrôleur de Domaine]] est un [[Server|serveur]] qui héberge l'[[ActiveDirectory|Active Directory]] et gère l'[[Authentication|authentification]] et l'[[Authorization|autorisation]] des utilisateurs et des ressources au sein d'un [[Windows|environnement Windows]]. Il est l'épine dorsale de la gestion des identités et des accès dans les [[Enterprise|entreprises]] utilisant [[ActiveDirectory|Active Directory]]. Il stocke des informations sur les utilisateurs, les [[Computer|ordinateurs]] et d'autres [[Resource|ressources]] réseau, permettant aux administrateurs de gérer de manière centralisée les politiques de [[Security|sécurité]], les [[Password|mots de passe]] et les permissions.

## ⚙️ Configuration
*   **Fichiers de configuration clés**:
    *   Base de données [[ActiveDirectory|Active Directory]] (NTDS.DIT)
    *   Stratégies de groupe (Group Policy Objects - GPO)
    *   Fichiers de journalisation des événements
*   **Modules importants**:
    *   Services de domaine [[ActiveDirectory|Active Directory]] (AD DS)
    *   Services [[DomainNameSystem|DNS]]
    *   Services [[LightweightDirectoryAccessProtocol|LDAP]]
    *   Centre de distribution de clés [[Kerberos]] (KDC)
*   **Dépendances**:
    *   [[Windows|Windows Server]]
    *   [[DomainNameSystem|DNS]]
    *   [[Network|Réseau]] stable et performant

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Application du [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]**: Limiter strictement les droits d'administration sur les [[DomainController|Contrôleurs de Domaine]].
*   **[[PatchManagement|Gestion des mises à jour]] rigoureuse**: Appliquer rapidement les correctifs de [[Security|sécurité]] pour l'[[OperatingSystem|OS]] et [[ActiveDirectory|Active Directory]].
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]**: Exiger la [[MultiFactorAuthentication|MFA]] pour tous les [[Account|comptes]] administratifs.
*   **[[NetworkSegmentation|Segmentation réseau]]**: Isoler les [[DomainController|Contrôleurs de Domaine]] sur un [[NetworkSegment|segment réseau]] dédié avec des règles de [[Firewall|pare-feu]] strictes.
*   **Désactivation des services inutiles**: Réduire la [[AttackSurface|surface d'attaque]] en désactivant tous les services non essentiels.
*   **Sécurisation physique**: Assurer la [[PhysicalSecurity|sécurité physique]] des [[Server|serveurs]] hébergeant les [[DomainController|Contrôleurs de Domaine]].

## 🔍 Audit et Surveillance
*   **Logs importants**:
    *   Journal des événements de sécurité ([[Log|Log]] d'audit de [[Authentication|connexion]], accès aux objets)
    *   Journal des services d'annuaire (événements liés à [[ActiveDirectory|Active Directory]])
    *   Journal [[DomainNameSystem|DNS]] (activités de résolution de noms)
*   **Commandes d'audit**:
```bash
# Vérifier la santé du contrôleur de domaine
dcdiag /q

# Vérifier la réplication Active Directory
repadmin /showrepl

# Lister les membres d'un groupe d'administration sensible (exemple)
net group "Domain Admins" /domain
```
*   **Outils de surveillance**: [[SecurityInformationAndEventManagement|SIEM]] pour la corrélation des [[Log|logs]] et la détection d'[[AnomalyDetection|anomalies]].

## 🔗 Notes Connexes
*   **Concept parent**: [[ActiveDirectory|Active Directory]]
*   **Protocole d'authentification clé**: [[Kerberos]]
*   **Protocole de services d'annuaire**: [[LightweightDirectoryAccessProtocol|LDAP]]
*   **Principe de sécurisation essentiel**: [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   **Vulnérabilité typique**: [[AccountTakeover|Prise de contrôle de compte]]