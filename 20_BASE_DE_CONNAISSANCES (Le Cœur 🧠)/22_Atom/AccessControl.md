---
tags:
  - autorisation
  - controle-acces/base-roles
  - gestion-identites/gestion-acces
  - securite/controle-acces
  - principe-moindre-privilege
  - authentification
aliases:
  - Contrôle d'accès
  - Access Control
source:
  - null
cssclasses:
  - max
---

# Contrôle d'Accès

## 📥 Définition en une phrase
> Le contrôle d'accès est un mécanisme de sécurité qui régule qui ou quoi peut voir ou utiliser une ressource dans un environnement informatique, basé sur l'identité et les autorisations définies.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification & Authentification :** Vérification de l'identité d'un utilisateur ou d'un système. L'[[Authentication|authentification]] confirme que l'entité est bien celle qu'elle prétend être.
*   **Autorisation :** Détermination des actions qu'une entité authentifiée est autorisée à effectuer sur une ressource spécifique.
*   **Modèles de Contrôle d'Accès :**
    *   [[RoleBasedAccessControl|RBAC]] (Role-Based Access Control) : Les permissions sont basées sur les rôles attribués aux utilisateurs.
    *   [[DiscretionaryAccessControl|DAC]] (Discretionary Access Control) : Le propriétaire d'une ressource peut en gérer les permissions.
    *   [[MandatoryAccessControl|MAC]] (Mandatory Access Control) : Basé sur des niveaux de sécurité pré-définis, souvent utilisé dans des environnements de haute sécurité.
*   **[[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]] :** Accorder uniquement les permissions minimales nécessaires pour accomplir une tâche, réduisant ainsi la surface d'attaque potentielle.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]] : Un individu ou un système accède à des ressources sans les permissions requises.
*   [[PrivilegeEscalation|Escalade de privilèges]] : Un attaquant obtient des privilèges plus élevés que ceux initialement attribués, souvent en exploitant des faiblesses dans le contrôle d'accès.
*   [[InsiderThreat|Menace interne]] : Des utilisateurs légitimes avec des accès abusent de leurs privilèges pour causer des dommages ou voler des données.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémentation de l'[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour renforcer la vérification d'identité.
*   Application rigoureuse du [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]].
*   Utilisation de solutions de [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]] pour centraliser et automatiser la gestion des permissions.
*   Révision régulière des permissions et des rôles des utilisateurs pour s'assurer qu'ils restent pertinents et sécurisés.
*   Mise en place de journaux d'audit pour surveiller les accès aux ressources critiques.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[ZeroTrust|Zero Trust]]