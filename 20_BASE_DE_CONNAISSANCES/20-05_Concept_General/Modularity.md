---
tags:
  - concept
  - concept-general
  - conception
  - architecture
  - logiciel
  - systeme
  - approche
  - complexite
  - efficacite
  - maintenance
  - securite/logiciel
aliases:
  - Modularity
  - Modularité
  - Modular Design
  - Conception modulaire
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Modularité

## 📥 Définition en une phrase
> La modularité est un principe de [[SoftwareDesign|conception logicielle]] et [[NetworkArchitecture|d'architecture système]] qui vise à diviser un [[System|système]] en composants discrets et interchangeables, appelés modules, chacun remplissant une fonction spécifique et bien définie.

## 🧠 Concepts Clés / Piliers
*   **Décomposition**: Le [[System|système]] est divisé en unités plus petites et gérables, facilitant la compréhension et la gestion de la [[Complexity|complexité]]. Chaque module est conçu pour accomplir une tâche spécifique sans connaître les détails internes des autres modules.
*   **Indépendance / Faible Couplage**: Les modules sont conçus pour être aussi indépendants que possible, avec un minimum de dépendances entre eux. Un faible couplage signifie que les changements dans un module ont un impact limité sur les autres, améliorant la [[Maintenance|maintenabilité]].
*   **Haute Cohésion**: Les éléments internes d'un module sont fortement liés entre eux et contribuent collectivement à l'objectif unique du module. Une haute cohésion assure que le module est focalisé sur une seule responsabilité.
*   **Interfaces Claires**: Les interactions entre les modules se font via des interfaces bien définies et documentées. Ces interfaces agissent comme des contrats, spécifiant comment les modules peuvent communiquer et échanger des [[Data|données]].

## 💡 Importance en Cybersécurité
> La modularité est un pilier fondamental de la [[SecurityByDesign|sécurité dès la conception]]. En isolant les fonctionnalités dans des modules distincts, elle permet de contenir l'impact d'une [[SoftwareVulnerability|vulnérabilité logicielle]] ou d'une [[Exploitation|exploitation]]. Un [[Attack|attaquant]] qui compromet un module aura plus de difficultés à s'étendre au reste du [[System|système]], ce qui renforce la [[DefenseInDepth|défense en profondeur]]. Elle facilite également la [[CodeReview|revue de code]], le [[Testing|test]] et le [[PatchManagement|patch management]], car les modifications peuvent être appliquées à des modules spécifiques sans affecter l'ensemble du [[SoftwareApplication|logiciel]], améliorant ainsi la [[Reliability|fiabilité]] et la [[Security|sécurité]] globale.

## 🔗 Notes Connexes
*   **Principe de conception**: [[SoftwareDesign|Conception logicielle]]
*   **Approche architecturale**: [[Microservices|Microservices]]
*   **Vulnérabilité atténuée**: [[SoftwareVulnerability|Vulnérabilité logicielle]]
*   **Objectif de sécurité**: [[SecurityByDesign|Sécurité dès la conception]]
*   **Bénéfice secondaire**: [[SystemComplexity|Complexité du système]]