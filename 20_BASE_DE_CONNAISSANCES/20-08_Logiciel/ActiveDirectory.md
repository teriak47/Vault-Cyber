---
tags:
  - logiciel
  - active-directory
  - annuaire
  - domain-controller
  - logiciel/windows
aliases:
  - Active Directory
  - AD
  - Annuaire Active Directory
archetype: logiciel
source:
  - 
cssclasses:
  - max
---

# Active Directory (AD)

## 📥 Définition en une phrase
> L'[[ActiveDirectory|Active Directory]] (AD) est un service d'annuaire développé par Microsoft, qui gère les ressources réseau dans les environnements [[Windows|Windows]] pour l'[[Authentication|authentification]] et l'[[Authorization|autorisation]] des [[User|utilisateurs]] et des [[Computer|ordinateurs]].

## 🧠 Concepts Clés / Piliers
*   **Services de Domaine (AD DS)**: Le composant central de l'[[ActiveDirectory|AD]] qui stocke les informations sur les [[User|utilisateurs]], les [[GroupPolicyObject|groupes]], les [[Computer|ordinateurs]] et d'autres [[Resource|ressources]] réseau, et qui gère l'accès et la [[Security|sécurité]] via l'[[Authentication|authentification]] et l'[[Authorization|autorisation]].
*   **Objets**: Représentent des entités spécifiques dans l'annuaire, telles que les [[User|utilisateurs]], les [[Computer|ordinateurs]], les [[Server|serveurs]], les groupes, les [[PrinterSharing|imprimantes partagées]] et d'autres [[NetworkDevice|périphériques réseau]].
*   **Stratégies de Groupe (GPO)**: Des ensembles de règles configurables qui permettent aux administrateurs de contrôler l'environnement de travail des [[User|utilisateurs]] et des [[Computer|ordinateurs]] dans un [[DomainController|domaine Active Directory]], incluant des paramètres de [[Security|sécurité]], de déploiement de [[Software|logiciels]] et de configuration système.
*   **Contrôleurs de Domaine (DC)**: Des [[Server|serveurs]] qui exécutent l'[[ActiveDirectoryDomainServices|AD DS]] et stockent une copie de la base de données de l'annuaire, facilitant les demandes d'[[Authentication|authentification]] et d'[[Authorization|autorisation]] pour les [[User|utilisateurs]] et les [[Computer|ordinateurs]] dans le [[DomainController|domaine]].
*   **Structure Hiérarchique**: Organisée en [[DomainController|domaines]], arbres et forêts pour une gestion structurée et [[Scalability|évolutive]] des [[Resource|ressources]] au sein d'une [[Enterprise|entreprise]].

## 💡 Importance en Cybersécurité
> L'[[ActiveDirectory|Active Directory]] est un pilier fondamental de la [[Cybersecurity|cybersécurité]] pour de nombreuses [[Enterprise|organisations]], car il centralise la [[IdentityAndAccessManagement|gestion des identités et des accès]]. Sa compromission représente une [[Threat|menace]] majeure, pouvant offrir aux [[ThreatActor|acteurs de menace]] un contrôle étendu sur l'[[EnterpriseNetwork|ensemble du réseau]], des capacités de [[PrivilegeEscalation|escalade de privilèges]] et un [[LateralMovement|mouvement latéral]] aisé, aboutissant souvent à une [[SystemCompromise|compromission complète du système]]. Une configuration sécurisée, une [[SecurityMonitoring|surveillance]] continue et des stratégies de [[DefenseInDepth|défense en profondeur]] sont donc essentielles pour protéger l'AD contre les [[Attack|attaques]].

## 🔗 Notes Connexes
*   **Gestion d'identité**: [[IdentityAndAccessManagement|Identity and Access Management]]
*   **Composant clé**: [[DomainController|Contrôleur de Domaine]]
*   **Vulnérabilité potentielle**: [[PrivilegeEscalation|Escalade de Privilèges]]
*   **Cible d'attaque**: [[LateralMovement|Mouvement Latéral]]
*   **Système d'exploitation associé**: [[Windows]]