---
tags:
  - controle-acces/obligatoire
  - securite/etiquettes
  - administration/surprivileges
  - securite/controle-acces
  - principe-moindre-privilege
  - gestion/politiques-securite
aliases:
  - Contrôle d'Accès Obligatoire
  - MAC
  - Mandatory Access Control
source:
  - null
cssclasses:
  - max
---

# Contrôle d'Accès Obligatoire (MAC)

## 📥 Définition en une phrase
> Un modèle de contrôle d'accès où les règles d'accès sont définies et appliquées de manière centralisée par un administrateur système ou une autorité de sécurité, et les utilisateurs ne peuvent pas modifier ces règles, garantissant une forte sécurité et une stricte séparation des privilèges.

## 🧠 Concepts Clés / Fonctionnement
*   **Politique Centrale**: Les décisions d'accès sont basées sur des politiques de sécurité définies par une autorité centrale, souvent le système d'exploitation ou un administrateur de sécurité.
*   **Étiquettes de Sécurité**: Les sujets (utilisateurs, processus) et les objets (fichiers, ressources) se voient attribuer des étiquettes de sécurité (ex: niveau de confidentialité, catégorie) qui déterminent les interactions permises.
*   **Règles Strictes**: Les règles prédéfinies dictent quelles étiquettes peuvent accéder à quelles autres, empêchant toute modification ou contournement par les utilisateurs finaux.
*   **Modèles Courants**: Souvent implémenté dans des environnements nécessitant une haute sécurité ou une conformité réglementaire stricte (ex: militaire, gouvernemental).

## 🛡️ Risques / Menaces Associés
*   [[Misconfiguration|Mauvaise configuration]] : Une erreur dans la définition des politiques MAC peut entraîner des dénis de service ou des brèches de sécurité.
*   [[OverPrivilege|Surprivilèges]] : Si les administrateurs attribuent des droits excessifs, la granularité de MAC peut être compromise.
*   Complexité de gestion: La gestion d'un grand nombre de politiques et d'étiquettes peut devenir complexe et source d'erreurs.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[LeastPrivilege|Principe du Moindre Privilège]] : S'assurer que les sujets n'ont que le niveau d'accès minimal requis pour effectuer leurs tâches.
*   Conception Granulaire : Définir des étiquettes et des politiques précises pour chaque ressource et utilisateur afin de maximiser la sécurité.
*   Revue et Audit Réguliers : Effectuer des audits réguliers des politiques MAC et des journaux d'accès pour identifier et corriger les vulnérabilités.
*   Outils de Gestion Spécifiques : Utiliser des outils comme [[SELinux]] ou [[AppArmor]] pour implémenter et gérer les politiques MAC de manière efficace.

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[DiscretionaryAccessControl|Contrôle d'Accès Discrétionnaire (DAC)]]
*   [[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles (RBAC)]]
*   [[InformationSecurity|Sécurité de l'Information]]