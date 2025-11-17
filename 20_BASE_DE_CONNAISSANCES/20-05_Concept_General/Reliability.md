---
tags:
  - fiabilite
  - disponibilite
  - integrite
  - securite/systeme
  - continuite-activite
aliases:
  - Fiabilité
  - Durabilité
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Fiabilité

## 📥 Définition en une phrase
> La fiabilité est la capacité d'un [[System|système]], d'un [[Software|logiciel]] ou d'un [[Hardware|matériel]] à fonctionner de manière constante et prévisible, sans défaillance, sur une période donnée ou dans des conditions spécifiées.

## 🧠 Concepts Clés / Piliers
*   **Cohérence Fonctionnelle**: Le système fournit des résultats identiques et attendus lors d'opérations répétées ou dans des conditions stables, garantissant que les [[Process|processus]] se déroulent sans erreurs inattendues.
*   **Robustesse aux Défaillances**: La capacité du système à résister et à se remettre de [[HardwareFailure|pannes matérielles]], [[SoftwareBugs|bugs logiciels]] ou d'autres [[Vulnerability|vulnérabilités]], souvent grâce à des mécanismes de [[Redundancy|redondance]] ou de tolérance aux pannes.
*   **Maintenabilité**: La facilité avec laquelle un système peut être réparé, mis à jour ou ajusté pour corriger des erreurs ou améliorer ses performances, contribuant à sa stabilité à long terme.
*   **Prédictibilité des Performances**: Le système maintient un niveau de [[Throughput|débit]] et de [[Latency|latence]] constant, même sous [[NetworkCongestion|charge]], ce qui est essentiel pour les applications critiques.

## 💡 Importance en Cybersécurité
> La fiabilité est un pilier fondamental de la [[CIATriad|triade CIA]], directement liée à la [[Availability|disponibilité]]. Un système non fiable est une porte ouverte aux [[DenialOfService|dénis de service]], à la [[DataCorruption|corruption de données]] et aux [[ServiceDisruption|interruptions de service]], qui peuvent entraîner des [[FinancialLoss|pertes financières]] et des [[ReputationalDamage|dommages à la réputation]]. Assurer la fiabilité est crucial pour la [[BusinessContinuity|continuité des activités]] et pour maintenir la [[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] des [[Data|données]] en garantissant que les [[System|systèmes]] fonctionnent comme prévu et résistent aux [[Attack|attaques]] et aux [[HumanError|erreurs humaines]].

## 🔗 Notes Connexes
*   **Concept frère**: [[Availability]]
*   **Objectif technique**: [[HighAvailability]]
*   **Mesure d'ingénierie**: [[Redundancy]]
*   **Objectif métier**: [[BusinessContinuity]]
*   **Principe de sécurité**: [[CIATriad|Triade CIA]]