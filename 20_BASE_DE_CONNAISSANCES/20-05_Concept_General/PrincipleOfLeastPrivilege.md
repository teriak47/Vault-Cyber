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
> Le Principe du Moindre Privilège (PoLP) est un concept de sécurité fondamental qui stipule qu'un utilisateur, un processus ou un système ne devrait avoir accès qu'aux ressources et aux fonctions strictement nécessaires pour accomplir sa tâche désignée, et ce, pour la durée la plus courte possible.

## 🧠 Concepts Clés / Piliers
*   **Granularité des Permissions**: Les autorisations doivent être spécifiques et ne pas accorder un accès plus large que nécessaire à une entité.
*   **Séparation des Fonctions**: Empêcher un seul utilisateur ou processus d'avoir des privilèges qui, s'ils sont compromis, pourraient permettre une compromission étendue de l'environnement.
*   **Révision Régulière**: Les contrôles d'accès et les privilèges doivent être revus et ajustés périodiquement, notamment lors de changements de rôle ou de tâche au sein d'une organisation.
*   **Just-in-Time / Just-Enough Access**: Accorder des privilèges uniquement au moment où ils sont nécessaires et les révoquer dès que la tâche est terminée, minimisant ainsi la fenêtre d'opportunité pour un attaquant.

## 💡 Importance en Cybersécurité
> L'application du Principe du Moindre Privilège réduit considérablement la surface d'attaque d'un système ou d'une organisation. En limitant les privilèges, même en cas de compromission de système ou de compte d'utilisateur, l'attaquant aura un accès limité, ce qui entrave le mouvement latéral et minimise les potentiels pertes financières ou fuites de données. Il est une pierre angulaire de la philosophie Zero Trust et contribue à renforcer la confidentialité, l'intégrité et la disponibilité de l'information.

## 🔗 Notes Connexes
*   **Concept général**: Contrôle d'accès
*   **Modèle associé**: Contrôle d'accès basé sur les rôles (RBAC)
*   **Stratégie de sécurité**: Zero Trust
*   **Domaine de gestion**: Gestion des Identités et des Accès (IAM)
*   **Mesure de mitigation**: Défense en Profondeur