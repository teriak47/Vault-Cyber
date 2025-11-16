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
> Un [[AccessControlModel|modèle de contrôle d'accès]] strict où les règles d'accès sont définies et appliquées de manière centralisée par un [[OperatingSystem|système d'exploitation]] ou un [[SecurityPolicy|administrateur de sécurité]], et les [[User|utilisateurs]] ne peuvent pas modifier ces règles, garantissant une forte [[Security|sécurité]] et une stricte séparation des [[PrivilegeEscalation|privilèges]].

## 🧠 Concepts Clés / Piliers
*   **Politique Centrale**: Les décisions d'[[AccessControl|accès]] sont basées sur des [[SecurityPolicy|politiques de sécurité]] prédéfinies par une autorité centrale, souvent le [[OperatingSystem|système d'exploitation]].
*   **Étiquettes de Sécurité**: Les [[Process|sujets]] (par exemple, [[User|utilisateurs]], [[Process|processus]]) et les [[Resource|objets]] (par exemple, [[Data|fichiers]], [[Resource|ressources]]) se voient attribuer des étiquettes de [[Confidentiality|sécurité]] (ex: niveau de [[Confidentiality|confidentialité]], catégorie) qui déterminent les interactions permises.
*   **Règles Strictes**: Des règles immuables dictent quelles étiquettes peuvent accéder à quelles autres, empêchant toute modification ou contournement par les [[User|utilisateurs]] finaux.
*   **Implémentations Courantes**: Souvent mis en œuvre dans des environnements nécessitant une haute [[Security|sécurité]] ou une [[LegalCompliance|conformité réglementaire]] stricte, avec des outils tels que [[SELinux]] ou [[AppArmor]].

## 💡 Importance en Cybersécurité
> Le [[MandatoryAccessControl|MAC]] est fondamental en [[Cybersecurity|cybersécurité]] car il permet d'appliquer une [[SecurityPolicy|politique de sécurité]] rigide et centralisée, essentielle pour protéger les [[SensitiveData|données sensibles]] et les [[System|systèmes]] critiques contre les [[UnauthorizedAccess|accès non autorisés]] et les [[DataBreach|violations de données]]. Il est particulièrement important dans les environnements où la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] sont primordiales, comme les organismes [[Government|gouvernementaux]] ou [[Enterprise|les entreprises]] traitant des informations hautement classifiées, en imposant le [[PrincipleOfLeastPrivilege|principe du moindre privilège]] et en réduisant la [[AttackSurface|surface d'attaque]].

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[DiscretionaryAccessControl|Contrôle d'Accès Discrétionnaire (DAC)]]
*   [[RoleBasedAccessControl|Contrôle d'Accès Basé sur les Rôles (RBAC)]]
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]
*   [[InformationSecurity|Sécurité de l'Information]]