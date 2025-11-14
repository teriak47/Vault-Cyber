---
tags:
  - gestion-acces/audit-roles
  - securite/autorisation/permissions
  - gouvernance/definition-roles
  - controle-acces/base-roles
  - gestion-identites/controle-acces
  - principe-moindre-privilege
aliases:
  - RBAC
  - Contrôle d'accès basé sur les rôles
source:
  - null
cssclasses:
  - max
---

# Contrôle d'Accès Basé sur les Rôles (RBAC)

## 📥 Définition en une phrase
> Le Contrôle d'Accès Basé sur les Rôles (RBAC) est une méthode de gestion des accès où les permissions sont attribuées non pas directement aux utilisateurs, mais aux rôles que ces utilisateurs endossent au sein d'une organisation.

## 🧠 Concepts Clés / Fonctionnement
*   **Rôles**: Définitions de fonctions au sein de l'organisation (ex: "Administrateur Système", "Comptable", "Utilisateur standard"). Chaque rôle est associé à un ensemble spécifique de permissions.
*   **Permissions**: Les autorisations spécifiques à effectuer des actions sur des ressources (ex: "lire fichier X", "modifier base de données Y", "exécuter programme Z").
*   **Utilisateurs**: Les individus qui se voient attribuer un ou plusieurs rôles en fonction de leurs responsabilités.
*   **Principe de Moindre Privilège**: Le RBAC facilite l'application de ce principe en garantissant que les utilisateurs n'ont que les permissions nécessaires pour accomplir leurs tâches.
*   **Gestion Simplifiée**: Au lieu de gérer les permissions pour chaque utilisateur, l'administration se concentre sur la définition des rôles et l'attribution de ces rôles aux utilisateurs, ce qui simplifie grandement la gestion à grande échelle.

## 🛡️ Risques / Menaces Associés
*   [[PrivilegeEscalation|Élévation de privilèges]] si les rôles sont mal définis ou si un utilisateur se voit attribuer un rôle avec des permissions excessives.
*   [[Misconfiguration|Mauvaise configuration]] des rôles ou des attributions, conduisant à des accès non autorisés ou des refus d'accès légitimes.
*   [[InsiderThreat|Menaces internes]] si un rôle privilégié est compromis ou utilisé abusivement par un employé.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PrincipleOfLeastPrivilege|Appliquer le Principe de Moindre Privilège]] lors de la définition des rôles et de l'attribution des permissions.
*   [[AccessControl|Mettre en œuvre des contrôles d'accès]] stricts basés sur les rôles.
*   **Audit Régulier**: Examiner et ajuster périodiquement les rôles et les attributions pour s'assurer qu'ils restent pertinents et sécurisés.
*   **Séparation des Fonctions**: S'assurer qu'aucun rôle unique ne détient toutes les permissions nécessaires pour commettre une fraude ou une erreur critique.
*   **Documentation Claire**: Maintenir une documentation à jour des rôles, de leurs permissions et des processus d'attribution.

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[ZeroTrust|Confiance Zéro]]
*   [[DiscretionaryAccessControl|DAC (Contrôle d'Accès Discrétionnaire)]]
*   [[MandatoryAccessControl|MAC (Contrôle d'Accès Obligatoire)]]