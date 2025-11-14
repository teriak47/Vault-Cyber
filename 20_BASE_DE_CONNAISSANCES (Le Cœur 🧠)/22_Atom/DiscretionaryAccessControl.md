---
tags:
  - controle-acces/discretionnaire
  - controle-acces/liste-acl
  - gestion-acces/proprietaire-ressource
  - principe-moindre-privilege
  - cybersécurité/escalade-privileges
  - acces/non-autorise
aliases:
  - Contrôle d'accès discrétionnaire
  - DAC
  - Discretionary Access Control
source:
  - null
cssclasses:
  - max
---

# Contrôle d'Accès Discrétionnaire (DAC)

## 📥 Définition en une phrase
> Un modèle de contrôle d'accès où la capacité à accéder à une ressource est déterminée par le propriétaire de cette ressource, qui peut accorder ou révoquer les permissions à sa discrétion.

## 🧠 Concepts Clés / Fonctionnement
*   Le propriétaire d'une ressource (fichier, répertoire, objet) est l'entité qui définit les permissions d'accès pour d'autres utilisateurs ou groupes.
*   Les permissions sont généralement gérées via des [[AccessControlList|Listes de Contrôle d'Accès (ACL)]] ou des bits de permission sur les systèmes de fichiers.
*   Permet une grande flexibilité et une granularité fine des permissions, mais peut être complexe à gérer dans de grands environnements et sujet aux erreurs humaines.
*   Contrasté par le [[MandatoryAccessControl|Contrôle d'Accès Obligatoire (MAC)]] où les permissions sont définies par une autorité centrale ou des politiques système.
*   S'applique à la fois aux systèmes de fichiers, aux bases de données et à d'autres objets du système d'exploitation.

## 🛡️ Risques / Menaces Associés
*   [[PrivilegeEscalation|Escalade de privilèges]] due à une mauvaise configuration des permissions.
*   [[UnauthorizedAccess|Accès non autorisé]] si un propriétaire accorde accidentellement ou intentionnellement des permissions excessives.
*   [[InsiderThreat|Menace interne]] où un propriétaire de ressource malveillant ou négligent peut exposer des données.
*   Difficulté à garantir la cohérence des politiques de sécurité à travers l'organisation.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Appliquer le [[LeastPrivilege|Principe du moindre privilège]] : accorder uniquement les permissions strictement nécessaires aux utilisateurs.
*   Mettre en œuvre des [[AccessReview|Révisions régulières des accès]] pour s'assurer que les permissions sont toujours appropriées.
*   Sensibiliser les propriétaires de données aux meilleures pratiques de gestion des permissions.
*   Combiner le DAC avec d'autres modèles de contrôle d'accès comme le [[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles (RBAC)]] pour simplifier la gestion.
*   Utiliser des [[FileIntegrityMonitoring|outils de surveillance de l'intégrité des fichiers]] pour détecter les modifications non autorisées des permissions.

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles (RBAC)]]
*   [[MandatoryAccessControl|Contrôle d'Accès Obligatoire (MAC)]]
*   [[AccessControlList|Liste de Contrôle d'Accès (ACL)]]
*   [[SecurityPolicy|Politique de Sécurité]]