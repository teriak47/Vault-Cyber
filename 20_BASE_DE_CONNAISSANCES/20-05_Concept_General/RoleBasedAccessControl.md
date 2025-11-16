---
tags:
  - gestion/privileges
  - securite/informations
  - controle/acces/rbac
  - securite/application
  - principe-moindre-privilege
  - gestion/identite/acces
aliases:
  - RBAC
  - Contrôle d'accès basé sur les rôles
  - Role-Based Access Control
  - Contrôle d'Accès par Rôles
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Contrôle d'Accès Basé sur les Rôles (RBAC)

## 📥 Définition en une phrase
> Le [[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles]] est une méthode de [[AccessControl|gestion des accès]] où les [[Permissions|permissions]] sont attribuées aux [[Role|rôles]] endossés par les [[User|utilisateurs]] au sein d'une [[Enterprise|organisation]], plutôt que directement aux [[User|utilisateurs]].

## 🧠 Concepts Clés / Piliers
*   **[[Role|Rôles]]**: Définitions de fonctions au sein de l'[[Enterprise|organisation]] (ex: "Administrateur Système", "Comptable", "Utilisateur standard"). Chaque [[Role|rôle]] est associé à un ensemble spécifique de [[Permissions|permissions]].
*   **[[Permissions|Permissions]]**: Les [[Authorization|autorisations]] spécifiques à effectuer des [[Task|actions]] sur des [[Resource|ressources]] (ex: "lire [[FileServer|fichier]] X", "modifier [[Database|base de données]] Y", "exécuter [[SoftwareApplication|programme]] Z").
*   **[[User|Utilisateurs]]**: Les [[User|individus]] qui se voient attribuer un ou plusieurs [[Role|rôles]] en fonction de leurs [[Task|responsabilités]].
*   **[[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]**: Le [[RoleBasedAccessControl|RBAC]] facilite l'application de ce [[Principle|principe]] en garantissant que les [[User|utilisateurs]] n'ont que les [[Permissions|permissions]] nécessaires pour accomplir leurs [[Task|tâches]].
*   **[[CentralizedAdministration|Gestion Simplifiée]]**: Au lieu de gérer les [[Permissions|permissions]] pour chaque [[User|utilisateur]], l'[[CentralizedAdministration|administration]] se concentre sur la définition des [[Role|rôles]] et l'attribution de ces [[Role|rôles]] aux [[User|utilisateurs]], ce qui simplifie grandement la [[IdentityAndAccessManagement|gestion]] des [[AccessControl|accès]] à grande [[Scalability|échelle]].
*   **[[SeparationOfDuties|Séparation des Fonctions]]**: Permet de s'assurer qu'aucun [[Role|rôle]] unique ne détient toutes les [[Permissions|permissions]] nécessaires pour commettre une [[Fraud|fraude]] ou une [[CriticalError|erreur critique]].

## 💡 Importance en Cybersécurité
> Le [[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles]] est fondamental pour la [[InformationSecurity|sécurité des systèmes d'information]] en offrant une approche structurée et granulaire de la [[AccessControl|gestion des accès]]. Il renforce le [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]], réduisant ainsi les risques d'[[PrivilegeEscalation|élévation de privilèges]] et d'[[UnauthorizedAccess|accès non autorisés]]. Sa capacité à simplifier la [[IdentityAndAccessManagement|gestion des droits]] à grande [[Scalability|échelle]] minimise les [[HumanError|erreurs de configuration]] et la [[AttackSurface|surface d'attaque]], tout en facilitant la [[LegalCompliance|conformité réglementaire]] et les [[SecurityAudit|audits de sécurité]].

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[ZeroTrust|Confiance Zéro]]
*   [[DiscretionaryAccessControl|Contrôle d'Accès Discrétionnaire (DAC)]]
*   [[MandatoryAccessControl|Contrôle d'Accès Obligatoire (MAC)]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[InsiderThreat|Menace interne]]
*   [[Misconfiguration|Mauvaise configuration]]
*   [[SeparationOfDuties|Séparation des Fonctions]]
*   [[SecurityAudit|Audit de Sécurité]]
*   [[SecurityPolicy|Politique de sécurité]]
*   [[Role|Rôle]]
*   [[Permissions|Permissions]]