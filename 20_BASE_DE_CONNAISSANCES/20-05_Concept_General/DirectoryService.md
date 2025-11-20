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
> Un Service d'Annuaire est un service réseau qui stocke des informations structurées sur les objets d'un système ou d'un réseau, telles que les identités des utilisateurs, les ordinateurs, et les ressources, les rendant disponibles pour la recherche et l'authentification.

## 🧠 Concepts Clés / Piliers
*   **Stockage Centralisé**: Il s'agit d'une base de données optimisée pour la lecture, gérant les informations de manière hiérarchique et facilitant l'administration centralisée des ressources et des comptes au sein d'une entreprise.
*   **Authentification et Autorisation**: Les Services d'Annuaire fournissent les mécanismes nécessaires pour vérifier l'identité des utilisateurs et des ordinateurs, puis pour déterminer leurs droits d'accès aux différentes ressources.
*   **LDAP (Lightweight Directory Access Protocol)**: C'est un protocole standardisé de l'IETF qui permet d'interroger et de modifier les informations dans un service d'annuaire.
*   **Active Directory**: L'implémentation de Microsoft d'un service d'annuaire, largement utilisée dans les environnements Windows pour la gestion des domaines, des utilisateurs et des ressources.

## 💡 Importance en Cybersécurité
Les Services d'Annuaire sont fondamentaux pour la sécurité réseau car ils constituent le cœur de l'Identity and Access Management (IAM). Ils permettent de centraliser les identités des utilisateurs, d'appliquer des politiques de sécurité strictes et de faciliter le login et l'autorisation des utilisateurs sur le réseau. Une gestion efficace d'un Service d'Annuaire est essentielle pour le respect du principe du moindre privilège et la mise en œuvre de la Zéro Confiance, réduisant ainsi la surface d'attaque. Toute compromission d'un Service d'Annuaire peut entraîner un accès non autorisé étendu et des fuites de données majeures.

## 🔗 Notes Connexes
*   **Modèle de sécurité**: Zéro Confiance
*   **Composant clé**: Contrôleur de Domaine
*   **Principe lié**: Principe du Moindre Privilège
*   **Protocole d'authentification**: Kerberos
*   **Gestion des droits**: Objet de Stratégie de Groupe (GPO)