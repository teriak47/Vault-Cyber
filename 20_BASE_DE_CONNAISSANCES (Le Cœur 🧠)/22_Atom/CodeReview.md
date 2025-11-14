---
tags:
  - analyse/securite/statique
  - qualite-code
  - developpement/workflow/collaboration
  - developpement/revision-code
  - developpement/securise
  - securite-application
aliases:
  - Revue de Code
  - Code Review
source:
  - null
cssclasses:
  - max
---

# Revue de Code (Code Review)

## 📥 Définition en une phrase
> La revue de code est un examen systématique du code source d'un programme par une ou plusieurs personnes, principalement pour détecter des erreurs, améliorer la qualité du code et identifier des vulnérabilités de sécurité.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectifs Multiples** : Vise l'amélioration de la qualité, la détection des bugs, la conformité aux standards de codage, et surtout l'identification des failles de sécurité.
*   **Processus Collaboratif** : Implique généralement des pairs (développeurs) qui examinent le code écrit par un collègue avant son intégration dans la base de code principale.
*   **Types de Revue** : Peut être formelle (réunions dédiées, checklists) ou informelle (lecture rapide, pair programming, pull request reviews).
*   **Outils de Support** : Des outils de gestion de version (comme Git avec des plateformes comme GitHub, GitLab) facilitent les revues de code en permettant des commentaires directs sur des lignes de code spécifiques.

## 🛡️ Risques / Menaces Associés
*   [[Vulnerability|Vulnérabilités]] non détectées dans le code applicatif, menant à des failles de sécurité exploitables.
*   Mauvaise qualité de code, rendant la maintenance et l'évolution plus difficiles et coûteuses.
*   Non-respect des [[SecurityBestPractices|bonnes pratiques de sécurité]] et des normes de codage.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Intégrer la [[CodeReview|revue de code]] comme étape obligatoire dans le [[SecureSoftwareDevelopmentLifeCycle|cycle de vie de développement logiciel sécurisé]].
*   Former les développeurs aux [[SecureCoding|bonnes pratiques de codage sécurisé]] et aux méthodologies de revue.
*   Utiliser des [[StaticApplicationSecurityTesting|outils d'analyse statique de code (SAST)]] pour identifier automatiquement les problèmes courants avant la revue manuelle.
*   Définir des [[SecurityPolicy|politiques]] et des checklists claires pour la revue de code, y compris des critères de sécurité spécifiques.

## 🔗 Notes Connexes
*   [[SecureCoding|Codage Sécurisé]]
*   [[SoftwareDevelopmentLifeCycle|SDLC]]
*   [[StaticApplicationSecurityTesting|SAST]]
*   [[DynamicApplicationSecurityTesting|DAST]]
*   [[PenetrationTesting|Tests d'intrusion]]