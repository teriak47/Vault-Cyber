---
aliases:
  - Autorisation
  - Authorization
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Autorisation

## 📥 Définition en une phrase
> L'[[Authorization|autorisation]] est le processus de détermination si une entité (utilisateur, programme, processus) est autorisée à effectuer une action ou à accéder à une ressource spécifique après que son [[Authentication|identité]] ait été vérifiée.

## 🧠 Concepts Clés / Piliers
*   **Identification et [[Authentication|Authentification]]**: L'[[Authorization|autorisation]] est toujours précédée de l'[[Authentication|authentification]], qui vérifie l'[[Identification|identité]] de l'entité. Sans une [[Authentication|authentification]] fiable, l'[[Authorization|autorisation]] ne peut pas être efficace.
*   **[[AccessControl|Contrôle d'Accès]]**: L'[[Authorization|autorisation]] est la mise en œuvre des politiques de [[AccessControl|contrôle d'accès]], déterminant quels [[Account|comptes]] ou [[System|systèmes]] peuvent accéder à quelles [[Data|données]] ou fonctions. Elle s'appuie sur des modèles tels que le [[RoleBasedAccessControl|RBAC]], le [[DiscretionaryAccessControl|DAC]] ou le [[MandatoryAccessControl|MAC]].
*   **Permissions et Privilèges**: Il s'agit des droits spécifiques accordés à une entité. Ils définissent ce que l'entité est autorisée à faire (lire, écrire, exécuter, supprimer) sur des ressources particulières (fichiers, bases de [[Database|données]], fonctions d'[[SoftwareApplication|application]]).

## 💡 Importance en Cybersécurité
> L'[[Authorization|autorisation]] est un [[SecurityControl|contrôle de sécurité]] fondamental qui garantit la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]] et des [[System|systèmes]] en empêchant l'[[UnauthorizedAccess|accès non autorisé]] et l'exécution d'actions non permises. Une [[Vulnerability|vulnérabilité]] dans l'[[Authorization|autorisation]] peut conduire à des problèmes graves comme l'[[PrivilegeEscalation|escalade de privilèges]], la [[DataExfiltration|fuite de données]] ou la [[SystemCompromise|compromission de système]], rendant ce processus indispensable à une [[Cybersecurity|cybersécurité]] robuste.

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'Accès]]
*   [[Authentication|Authentification]]
*   [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles]]
*   [[SecurityPolicy|Politique de sécurité]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]