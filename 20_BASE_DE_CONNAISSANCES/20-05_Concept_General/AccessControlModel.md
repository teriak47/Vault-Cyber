---
aliases:
  - Modèle de Contrôle d'Accès
  - Access Control Model
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Modèle de Contrôle d'Accès

## 📥 Définition en une phrase
> Un Modèle de Contrôle d'Accès est un cadre théorique et structurel qui détermine comment les sujets (utilisateurs, processus) peuvent interagir avec les ressources (fichiers, bases de données, périphériques) au sein d'un système ou d'un réseau, en définissant les règles et les politiques d'accès.

## 🧠 Concepts Clés / Piliers
*   **Contrôle d'Accès Discrétionnaire (DAC)**: Permet au propriétaire d'une ressource de définir les permissions d'accès pour d'autres utilisateurs. C'est le modèle le plus flexible mais potentiellement moins sécurisé car les propriétaires peuvent commettre des erreurs.
*   **Contrôle d'Accès Obligatoire (MAC)**: Applique des règles d'accès strictes basées sur des classifications de sécurité définies par l'administrateur système. Il est couramment utilisé dans les environnements de haute sécurité où la confidentialité est primordiale, comme les systèmes militaires ou gouvernementaux.
*   **Contrôle d'Accès Basé sur les Rôles (RBAC)**: L'accès est attribué aux utilisateurs en fonction de leurs rôles au sein de l'organisation. Cela simplifie la gestion des permissions, car les droits sont gérés au niveau du rôle plutôt qu'individuellement pour chaque utilisateur.

## 💡 Importance en Cybersécurité
> Les modèles de contrôle d'accès sont fondamentaux pour la cybersécurité car ils garantissent que seuls les utilisateurs et les processus autorisés peuvent accéder, modifier ou supprimer des données et des ressources. Ils sont essentiels pour maintenir la confidentialité, l'intégrité et la disponibilité (la Triade CIA) des systèmes d'information en prévenant l'accès non autorisé et en limitant les privilèges au strict nécessaire, réduisant ainsi la surface d'attaque.

## 🔗 Notes Connexes
*   Contrôle d'Accès
*   Autorisation
*   Politique de sécurité
*   Escalade de Privilèges