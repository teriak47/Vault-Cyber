---
tags:
aliases:
  - Disaster Recovery
  - Plan de Reprise d'Activité
  - PRA
  - Disaster Recovery Planning
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Reprise Après Sinistre (PRA)

## 📥 Définition en une phrase
> Stratégie et processus mis en œuvre pour restaurer les opérations informatiques et l'accès aux données après un événement perturbateur majeur comme une catastrophe naturelle, une cyberattaque ou une défaillance système grave.

## 🧠 Concepts Clés / Piliers
*   **Objectifs de Récupération (RPO & RTO)**: Le RPO (Objectif de Point de Récupération) définit la quantité maximale de données qu'une organisation est prête à perdre, mesurée en temps depuis le dernier point de sauvegarde. Le RTO (Objectif de Temps de Récupération) spécifie la durée maximale admissible pendant laquelle un système ou une application peut être hors service avant que l'impact ne devienne inacceptable. Ces métriques sont fondamentales pour dimensionner la stratégie de reprise après sinistre.
*   **Plan de Reprise d'Activité (DRP)**: Le DRP est un document structuré et détaillé qui formalise les procédures, les rôles et les responsabilités pour restaurer les systèmes et services critiques post-sinistre. Il est le cœur de toute initiative de reprise d'activité et doit être intégré dans le planification globale de la continuité des activités.
*   **Stratégies de Réplication et de Sauvegarde**: La redondance des données et des systèmes est atteinte via la mise en place de sites de secours (chauds, tièdes, froids), la réplication des données en temps réel ou quasi-réel, et des sauvegardes régulières et robustes (souvent selon la règle 3-2-1). L'utilisation de la virtualisation et du cloud computing peut grandement faciliter ces processus en offrant flexibilité et évolutivité.
*   **Tests et Mises à Jour Réguliers**: Un plan de reprise d'activité n'est efficace que s'il est testé régulièrement et mis à jour pour s'adapter à l'évolution de l'infrastructure, des logiciels et des menaces. Ces tests (par exemple, des simulations de sinistre) permettent d'identifier les lacunes, de valider les procédures et de s'assurer de l'atteinte des objectifs RPO/RTO.

## 💡 Importance en Cybersécurité
> Le Plan de Reprise d'Activité est une composante essentielle de la cybersécurité et de la continuité des activités. Il assure la disponibilité et l'intégrité des systèmes et des données face à des menaces majeures, qu'elles soient d'origine naturelle, accidentelle (comme une erreur humaine) ou malveillante (comme une cyberattaque telle que le rançongiciel ou le déni de service distribué). En minimisant les interruptions de service et la perte de données, le PRA protège l'organisation contre des pertes financières importantes et des dommages réputationnels, tout en garantissant la conformité légale et réglementaire.

## 🔗 Notes Connexes
*   Continuité d'Activité
*   Planification de la Continuité des Activités
*   Réponse aux Incidents
*   Sauvegarde et Récupération
*   Objectif de Point de Récupération (RPO)
*   Objectif de Temps de Récupération (RTO)
*   Planification de la Reprise après Sinistre
*   Gestion des Risques
*   Disponibilité
*   Intégrité
*   Cloud Computing
*   Virtualisation
*   Catastrophe naturelle