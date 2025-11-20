---
tags:
aliases:
  - Contrôle d'Accès Obligatoire
  - MAC
  - Mandatory Access Control
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Contrôle d'Accès Obligatoire (MAC)

## 📥 Définition en une phrase
> Un modèle de contrôle d'accès strict où les règles d'accès sont définies et appliquées de manière centralisée par un système d'exploitation ou un administrateur de sécurité, et les utilisateurs ne peuvent pas modifier ces règles, garantissant une forte sécurité et une stricte séparation des privilèges.

## 🧠 Concepts Clés / Piliers
*   **Politique Centrale**: Les décisions d'accès sont basées sur des politiques de sécurité prédéfinies par une autorité centrale, souvent le système d'exploitation.
*   **Étiquettes de Sécurité**: Les sujets (par exemple, utilisateurs, processus) et les objets (par exemple, fichiers, ressources) se voient attribuer des étiquettes de sécurité (ex: niveau de confidentialité, catégorie) qui déterminent les interactions permises.
*   **Règles Strictes**: Des règles immuables dictent quelles étiquettes peuvent accéder à quelles autres, empêchant toute modification ou contournement par les utilisateurs finaux.
*   **Implémentations Courantes**: Souvent mis en œuvre dans des environnements nécessitant une haute sécurité ou une conformité réglementaire stricte, avec des outils tels que SELinux ou AppArmor.

## 💡 Importance en Cybersécurité
> Le MAC est fondamental en cybersécurité car il permet d'appliquer une politique de sécurité rigide et centralisée, essentielle pour protéger les données sensibles et les systèmes critiques contre les accès non autorisés et les violations de données. Il est particulièrement important dans les environnements où la confidentialité et l'intégrité sont primordiales, comme les organismes gouvernementaux ou les entreprises traitant des informations hautement classifiées, en imposant le principe du moindre privilège et en réduisant la surface d'attaque.

## 🔗 Notes Connexes
*   Contrôle d'Accès
*   Contrôle d'Accès Discrétionnaire (DAC)
*   Contrôle d'Accès Basé sur les Rôles (RBAC)
*   Principe du Moindre Privilège
*   Sécurité de l'Information