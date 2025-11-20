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
> L'Active Directory (AD) est un service d'annuaire développé par Microsoft, qui gère les ressources réseau dans les environnements Windows pour l'authentification et l'autorisation des utilisateurs et des ordinateurs.

## 🧠 Concepts Clés / Piliers
*   **Services de Domaine (AD DS)**: Le composant central de l'AD qui stocke les informations sur les utilisateurs, les groupes, les ordinateurs et d'autres ressources réseau, et qui gère l'accès et la sécurité via l'authentification et l'autorisation.
*   **Objets**: Représentent des entités spécifiques dans l'annuaire, telles que les utilisateurs, les ordinateurs, les serveurs, les groupes, les imprimantes partagées et d'autres périphériques réseau.
*   **Stratégies de Groupe (GPO)**: Des ensembles de règles configurables qui permettent aux administrateurs de contrôler l'environnement de travail des utilisateurs et des ordinateurs dans un domaine Active Directory, incluant des paramètres de sécurité, de déploiement de logiciels et de configuration système.
*   **Contrôleurs de Domaine (DC)**: Des serveurs qui exécutent l'AD DS et stockent une copie de la base de données de l'annuaire, facilitant les demandes d'authentification et d'autorisation pour les utilisateurs et les ordinateurs dans le domaine.
*   **Structure Hiérarchique**: Organisée en domaines, arbres et forêts pour une gestion structurée et évolutive des ressources au sein d'une entreprise.

## 💡 Importance en Cybersécurité
> L'Active Directory est un pilier fondamental de la cybersécurité pour de nombreuses organisations, car il centralise la gestion des identités et des accès. Sa compromission représente une menace majeure, pouvant offrir aux acteurs de menace un contrôle étendu sur l'ensemble du réseau, des capacités de escalade de privilèges et un mouvement latéral aisé, aboutissant souvent à une compromission complète du système. Une configuration sécurisée, une surveillance continue et des stratégies de défense en profondeur sont donc essentielles pour protéger l'AD contre les attaques.

## 🔗 Notes Connexes
*   **Gestion d'identité**: Identity and Access Management
*   **Composant clé**: Contrôleur de Domaine
*   **Vulnérabilité potentielle**: Escalade de Privilèges
*   **Cible d'attaque**: Mouvement Latéral
*   **Système d'exploitation associé**: Windows