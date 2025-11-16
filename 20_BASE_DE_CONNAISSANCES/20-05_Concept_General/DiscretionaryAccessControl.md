---
tags:
aliases:
  - Contrôle d'accès discrétionnaire
  - DAC
  - Discretionary Access Control
  - DAC (sécurité)
  - Contrôle d'Accès Discrétionnaire (sécurité)
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Contrôle d'Accès Discrétionnaire (DAC)

## 📥 Définition en une phrase
> Un [[AccessControlModel|modèle de contrôle d'accès]] où la capacité à accéder à une [[Resource|ressource]] est déterminée par le propriétaire de cette [[Resource|ressource]], qui peut accorder ou révoquer les [[AccessControl|permissions]] à sa discrétion.

## 🧠 Concepts Clés / Piliers
*   **Propriété et Attribution**: Le propriétaire d'une [[Resource|ressource]] (comme un [[FileServer|fichier]], un répertoire ou un objet) est l'entité qui définit et modifie les [[AccessControl|permissions]] d'accès pour d'autres [[User|utilisateurs]] ou [[Group|groupes]].
*   **Mécanismes de Gestion**: Les [[AccessControl|permissions]] sont généralement gérées et appliquées via des [[AccessControlList|Listes de Contrôle d'Accès (ACL)]] ou des bits de permission intégrés aux [[OperatingSystem|systèmes d'exploitation]].
*   **Flexibilité vs. Risques**: Ce modèle offre une grande flexibilité et une granularité fine dans la gestion des accès, mais cette même flexibilité peut conduire à des [[SecurityVulnerabilities|vulnérabilités de sécurité]] dues à une mauvaise configuration ou à des [[HumanError|erreurs humaines]].
*   **Opposition à MAC**: Le [[DiscretionaryAccessControl|DAC]] se distingue du [[MandatoryAccessControl|Contrôle d'Accès Obligatoire (MAC)]], où les règles d'accès sont définies par une autorité centrale et non par les propriétaires de [[Resource|ressources]].

## 💡 Importance en Cybersécurité
> Le [[DiscretionaryAccessControl|DAC]] est un [[AccessControlModel|modèle de contrôle d'accès]] fondamental qui permet une gestion flexible et granulaire des [[AccessControl|permissions]] sur les [[Resource|ressources]]. Bien qu'il offre une grande autonomie aux [[User|utilisateurs]] pour partager leurs données, sa dépendance à la diligence des propriétaires peut conduire à des [[SecurityVulnerabilities|vulnérabilités]] telles que l'[[PrivilegeEscalation|escalade de privilèges]] ou l'[[UnauthorizedAccess|accès non autorisé]] si les [[AccessControl|permissions]] sont mal configurées. Il est crucial pour la compréhension des mécanismes de [[Security|sécurité]] de base dans de nombreux [[OperatingSystem|systèmes d'exploitation]] mais nécessite des [[SecurityControl|contrôles de sécurité]] supplémentaires, comme l'application du [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]], pour atténuer ses risques et garantir une [[SecurityPolicy|politique de sécurité]] cohérente.

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles (RBAC)]]
*   [[MandatoryAccessControl|Contrôle d'Accès Obligatoire (MAC)]]
*   [[AccessControlList|Liste de Contrôle d'Accès (ACL)]]
*   [[SecurityPolicy|Politique de Sécurité]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[AccessReview|Révision des Accès]]
*   [[FileIntegrityMonitoring|Surveillance de l'Intégrité des Fichiers]]
*   [[Group]]