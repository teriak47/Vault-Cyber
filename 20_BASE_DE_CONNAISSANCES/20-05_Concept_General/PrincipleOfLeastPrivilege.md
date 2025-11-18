---
tags:
  - principe-du-moindre-privilege
  - principe-de-securite
  - controle/acces
  - gestion/privileges
  - securite/systeme
aliases:
  - Principe du Moindre Privilège
  - Principle of Least Privilege
  - Least Privilege
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Principe du Moindre Privilège (PoLP)

## 📥 Définition en une phrase
> Le [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]] (PoLP) est un concept de sécurité fondamental qui stipule qu'un utilisateur, un processus ou un système ne devrait avoir accès qu'aux ressources et aux fonctions strictement nécessaires pour accomplir sa tâche désignée, et ce, pour la durée la plus courte possible.

## 🧠 Concepts Clés / Piliers
*   **Granularité des Permissions**: Les [[Authorization|autorisations]] doivent être spécifiques et ne pas accorder un accès plus large que nécessaire à une entité.
*   **Séparation des Fonctions**: Empêcher un seul utilisateur ou processus d'avoir des [[PrivilegeEscalation|privilèges]] qui, s'ils sont compromis, pourraient permettre une compromission étendue de l'environnement.
*   **Révision Régulière**: Les [[AccessControl|contrôles d'accès]] et les privilèges doivent être revus et ajustés périodiquement, notamment lors de changements de rôle ou de tâche au sein d'une organisation.
*   **Just-in-Time / Just-Enough Access**: Accorder des privilèges uniquement au moment où ils sont nécessaires et les révoquer dès que la tâche est terminée, minimisant ainsi la fenêtre d'opportunité pour un [[ThreatActor|attaquant]].

## 💡 Importance en Cybersécurité
> L'application du [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]] réduit considérablement la [[AttackSurface|surface d'attaque]] d'un système ou d'une organisation. En limitant les privilèges, même en cas de [[SystemCompromise|compromission de système]] ou de [[Account|compte d'utilisateur]], l'attaquant aura un accès limité, ce qui entrave le [[LateralMovement|mouvement latéral]] et minimise les potentiels pertes financières ou [[DataBreach|fuites de données]]. Il est une pierre angulaire de la [[ZeroTrust|philosophie Zero Trust]] et contribue à renforcer la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] de l'information.

## 🔗 Notes Connexes
*   **Concept général**: [[AccessControl|Contrôle d'accès]]
*   **Modèle associé**: [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles (RBAC)]]
*   **Stratégie de sécurité**: [[ZeroTrust|Zero Trust]]
*   **Domaine de gestion**: [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   **Mesure de mitigation**: [[DefenseInDepth|Défense en Profondeur]]