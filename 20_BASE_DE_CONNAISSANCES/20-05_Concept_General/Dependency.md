---
tags:
aliases:
  - Dépendance
  - Software Dependency
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Dépendance (Dependency)

## 📥 Définition en une phrase
> Une [[Dependency|dépendance]] est un composant logiciel, une bibliothèque, un module, ou un autre [[Software|logiciel]] ou [[System|système]] externe requis par un programme ou une application pour fonctionner correctement.

## 🧠 Concepts Clés / Piliers
*   **Composants Requis**: Les [[Dependency|dépendances]] sont les blocs de construction nécessaires à une [[SoftwareApplication|application logicielle]] pour fonctionner, incluant souvent des bibliothèques, des frameworks ou des services externes.
*   **Chaîne d'Approvisionnement Logicielle**: Les [[Dependency|dépendances]] forment une "chaîne" où un [[Software|logiciel]] dépend d'un autre, qui à son tour peut dépendre d'un troisième, créant une [[SoftwareSupplyChainSecurity|chaîne d'approvisionnement logicielle]].
*   **Risque de Sécurité**: Chaque [[Dependency|dépendance]] représente une [[Vulnerability|vulnérabilité]] potentielle; si une [[SoftwareVulnerability|vulnérabilité logicielle]] est découverte dans un composant dépendant, l'application qui l'utilise est également compromise.

## 💡 Importance en Cybersécurité
> La gestion des [[Dependency|dépendances]] est fondamentale en [[Cybersecurity|cybersécurité]] car elles constituent une partie significative de la [[AttackSurface|surface d'attaque]] d'une application. Une [[SoftwareVulnerability|vulnérabilité logicielle]] dans une [[Dependency|dépendance]] tierce peut être exploitée pour compromettre l'ensemble du [[System|système]], d'où l'importance de la [[DependencyManagement|gestion des dépendances]] et de la [[SoftwareSupplyChainSecurity|sécurité de la chaîne d'approvisionnement logicielle]].

## 🔗 Notes Connexes
*   [[DependencyManagement|Gestion des Dépendances]]
*   [[SoftwareSupplyChainSecurity|Sécurité de la chaîne d'approvisionnement logicielle]]
*   [[SoftwareVulnerability|Vulnérabilité Logicielle]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Exploit|Exploit]]
*   [[AttackSurface|Surface d'attaque]]
*   [[Software|Logiciel]]
*   [[System|Système]]