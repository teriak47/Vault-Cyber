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
> Un modèle de contrôle d'accès où la capacité à accéder à une ressource est déterminée par le propriétaire de cette ressource, qui peut accorder ou révoquer les permissions à sa discrétion.

## 🧠 Concepts Clés / Piliers
*   **Propriété et Attribution**: Le propriétaire d'une ressource (comme un fichier, un répertoire ou un objet) est l'entité qui définit et modifie les permissions d'accès pour d'autres utilisateurs ou groupes.
*   **Mécanismes de Gestion**: Les permissions sont généralement gérées et appliquées via des Listes de Contrôle d'Accès (ACL) ou des bits de permission intégrés aux systèmes d'exploitation.
*   **Flexibilité vs. Risques**: Ce modèle offre une grande flexibilité et une granularité fine dans la gestion des accès, mais cette même flexibilité peut conduire à des vulnérabilités de sécurité dues à une mauvaise configuration ou à des erreurs humaines.
*   **Opposition à MAC**: Le DAC se distingue du Contrôle d'Accès Obligatoire (MAC), où les règles d'accès sont définies par une autorité centrale et non par les propriétaires de ressources.

## 💡 Importance en Cybersécurité
> Le DAC est un modèle de contrôle d'accès fondamental qui permet une gestion flexible et granulaire des permissions sur les ressources. Bien qu'il offre une grande autonomie aux utilisateurs pour partager leurs données, sa dépendance à la diligence des propriétaires peut conduire à des vulnérabilités telles que l'escalade de privilèges ou l'accès non autorisé si les permissions sont mal configurées. Il est crucial pour la compréhension des mécanismes de sécurité de base dans de nombreux systèmes d'exploitation mais nécessite des contrôles de sécurité supplémentaires, comme l'application du Principe du Moindre Privilège, pour atténuer ses risques et garantir une politique de sécurité cohérente.

## 🔗 Notes Connexes
*   Contrôle d'Accès
*   Contrôle d'Accès Basé sur les Rôles (RBAC)
*   Contrôle d'Accès Obligatoire (MAC)
*   Liste de Contrôle d'Accès (ACL)
*   Politique de Sécurité
*   Principe du Moindre Privilège
*   Révision des Accès
*   Surveillance de l'Intégrité des Fichiers
*   Group