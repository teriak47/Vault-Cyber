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
> Un [[AccessControlModel|Modèle de Contrôle d'Accès]] est un cadre théorique et structurel qui détermine comment les sujets (utilisateurs, processus) peuvent interagir avec les [[Resource|ressources]] (fichiers, bases de données, périphériques) au sein d'un [[System|système]] ou d'un [[Network|réseau]], en définissant les règles et les politiques d'[[AccessControl|accès]].

## 🧠 Concepts Clés / Piliers
*   **[[DiscretionaryAccessControl|Contrôle d'Accès Discrétionnaire (DAC)]]**: Permet au propriétaire d'une [[Resource|ressource]] de définir les permissions d'[[AccessControl|accès]] pour d'autres utilisateurs. C'est le modèle le plus flexible mais potentiellement moins sécurisé car les propriétaires peuvent commettre des erreurs.
*   **[[MandatoryAccessControl|Contrôle d'Accès Obligatoire (MAC)]]**: Applique des règles d'[[AccessControl|accès]] strictes basées sur des classifications de sécurité définies par l'administrateur système. Il est couramment utilisé dans les environnements de haute [[Security|sécurité]] où la [[Confidentiality|confidentialité]] est primordiale, comme les systèmes militaires ou gouvernementaux.
*   **[[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles (RBAC)]]**: L'[[AccessControl|accès]] est attribué aux utilisateurs en fonction de leurs rôles au sein de l'[[Enterprise|organisation]]. Cela simplifie la gestion des permissions, car les droits sont gérés au niveau du rôle plutôt qu'individuellement pour chaque utilisateur.

## 💡 Importance en Cybersécurité
> Les [[AccessControlModel|modèles de contrôle d'accès]] sont fondamentaux pour la [[Cybersecurity|cybersécurité]] car ils garantissent que seuls les utilisateurs et les processus autorisés peuvent accéder, modifier ou supprimer des [[Data|données]] et des [[Resource|ressources]]. Ils sont essentiels pour maintenir la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] (la [[CIATriad|Triade CIA]]) des systèmes d'information en prévenant l'[[UnauthorizedAccess|accès non autorisé]] et en limitant les privilèges au strict nécessaire, réduisant ainsi la [[AttackSurface|surface d'attaque]].

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[Authorization|Autorisation]]
*   [[SecurityPolicy|Politique de sécurité]]
*   [[PrivilegeEscalation|Escalade de Privilèges]]