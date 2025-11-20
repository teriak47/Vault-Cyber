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
> Le Contrôle d'Accès Basé sur les Rôles est une méthode de gestion des accès où les permissions sont attribuées aux rôles endossés par les utilisateurs au sein d'une organisation, plutôt que directement aux utilisateurs.

## 🧠 Concepts Clés / Piliers
*   **Rôles**: Définitions de fonctions au sein de l'organisation (ex: "Administrateur Système", "Comptable", "Utilisateur standard"). Chaque rôle est associé à un ensemble spécifique de permissions.
*   **Permissions**: Les autorisations spécifiques à effectuer des actions sur des ressources (ex: "lire fichier X", "modifier base de données Y", "exécuter programme Z").
*   **Utilisateurs**: Les individus qui se voient attribuer un ou plusieurs rôles en fonction de leurs responsabilités.
*   **Principe du Moindre Privilège**: Le RBAC facilite l'application de ce principe en garantissant que les utilisateurs n'ont que les permissions nécessaires pour accomplir leurs tâches.
*   **Gestion Simplifiée**: Au lieu de gérer les permissions pour chaque utilisateur, l'administration se concentre sur la définition des rôles et l'attribution de ces rôles aux utilisateurs, ce qui simplifie grandement la gestion des accès à grande échelle.
*   **Séparation des Fonctions**: Permet de s'assurer qu'aucun rôle unique ne détient toutes les permissions nécessaires pour commettre une fraude ou une erreur critique.

## 💡 Importance en Cybersécurité
> Le Contrôle d'Accès Basé sur les Rôles est fondamental pour la sécurité des systèmes d'information en offrant une approche structurée et granulaire de la gestion des accès. Il renforce le Principe du Moindre Privilège, réduisant ainsi les risques d'élévation de privilèges et d'accès non autorisés. Sa capacité à simplifier la gestion des droits à grande échelle minimise les erreurs de configuration et la surface d'attaque, tout en facilitant la conformité réglementaire et les audits de sécurité.

## 🔗 Notes Connexes
*   Contrôle d'Accès
*   Gestion des Identités et des Accès (IAM)
*   Confiance Zéro
*   Contrôle d'Accès Discrétionnaire (DAC)
*   Contrôle d'Accès Obligatoire (MAC)
*   Principe du Moindre Privilège
*   Élévation de privilèges
*   Menace interne
*   Mauvaise configuration
*   Séparation des Fonctions
*   Audit de Sécurité
*   Politique de sécurité
*   Rôle
*   Permissions