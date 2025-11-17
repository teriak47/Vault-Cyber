---
tags:
  - annuaire
  - service
  - gestion/identite/acces
  - authentification
  - active-directory
  - protocole/ldap
  - infrastructure
  - securite/acces
  - centralisation
aliases:
  - Service d'annuaire
  - Répertoire de services
  - Annuaire réseau
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Service d'Annuaire (Directory Service)

## 📥 Définition en une phrase
> Un Service d'Annuaire est un [[NetworkService|service réseau]] qui stocke des informations structurées sur les objets d'un [[System|système]] ou d'un [[Network|réseau]], telles que les [[UserIdentity|identités des utilisateurs]], les [[Computer|ordinateurs]], et les [[Resource|ressources]], les rendant disponibles pour la recherche et l'[[Authentication|authentification]].

## 🧠 Concepts Clés / Piliers
*   **Stockage Centralisé**: Il s'agit d'une base de données optimisée pour la lecture, gérant les informations de manière hiérarchique et facilitant l'[[CentralizedAdministration|administration centralisée]] des ressources et des [[Account|comptes]] au sein d'une [[EnterpriseNetwork|entreprise]].
*   **[[Authentication|Authentification]] et [[Authorization|Autorisation]]**: Les Services d'Annuaire fournissent les mécanismes nécessaires pour vérifier l'identité des [[User|utilisateurs]] et des [[Computer|ordinateurs]], puis pour déterminer leurs droits d'[[AccessControl|accès]] aux différentes ressources.
*   **[[LightweightDirectoryAccessProtocol|LDAP]] (Lightweight Directory Access Protocol)**: C'est un [[Protocol|protocole]] standardisé de l'[[InternetEngineeringTaskForce|IETF]] qui permet d'interroger et de modifier les informations dans un service d'annuaire.
*   **[[ActiveDirectory|Active Directory]]**: L'implémentation de [[Microsoft|Microsoft]] d'un service d'annuaire, largement utilisée dans les environnements [[Windows|Windows]] pour la gestion des domaines, des [[User|utilisateurs]] et des ressources.

## 💡 Importance en Cybersécurité
Les Services d'Annuaire sont fondamentaux pour la [[NetworkSecurity|sécurité réseau]] car ils constituent le cœur de l'[[IdentityAndAccessManagement|Identity and Access Management (IAM)]]. Ils permettent de centraliser les [[UserIdentity|identités des utilisateurs]], d'appliquer des [[SecurityPolicy|politiques de sécurité]] strictes et de faciliter le [[Login|login]] et l'[[Authorization|autorisation]] des [[User|utilisateurs]] sur le [[Network|réseau]]. Une gestion efficace d'un Service d'Annuaire est essentielle pour le respect du [[PrincipleOfLeastPrivilege|principe du moindre privilège]] et la mise en œuvre de la [[ZeroTrust|Zéro Confiance]], réduisant ainsi la [[AttackSurface|surface d'attaque]]. Toute [[SystemCompromise|compromission]] d'un Service d'Annuaire peut entraîner un [[UnauthorizedAccess|accès non autorisé]] étendu et des [[DataBreach|fuites de données]] majeures.

## 🔗 Notes Connexes
*   **Modèle de sécurité**: [[ZeroTrust|Zéro Confiance]]
*   **Composant clé**: [[DomainController|Contrôleur de Domaine]]
*   **Principe lié**: [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   **Protocole d'authentification**: [[Kerberos|Kerberos]]
*   **Gestion des droits**: [[GroupPolicyObject|Objet de Stratégie de Groupe (GPO)]]