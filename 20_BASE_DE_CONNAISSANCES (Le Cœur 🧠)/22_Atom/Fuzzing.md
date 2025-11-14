---
tags:
  - test/fuzzing
  - generation/donnees-malformees
  - test/injection-donnees
  - analyse-vulnerabilite
  - securite-application
  - depassement-tampon
aliases:
  - Test de Fuzzing
  - Fuzz Testing
source:
  - null
cssclasses:
  - max
---

# Fuzzing

## 📥 Définition en une phrase
> Le Fuzzing est une technique de [[SoftwareTesting|test logiciel]] consistant à injecter des données aléatoires, inattendues ou malformées dans une application, un système ou un [[Protocols|protocole]] pour provoquer des erreurs, des plantages ou révéler des [[Vulnerability|vulnérabilités]] latentes.

## 🧠 Concepts Clés / Fonctionnement
*   **Génération de Données**: Crée des entrées non valides, semi-valides ou aléatoires qui sortent des spécifications attendues du programme.
*   **Injection Ciblée**: Ces données sont ensuite injectées dans différents points d'entrée de l'application (champs de formulaire, API, paramètres réseau, fichiers d'entrée, etc.).
*   **Surveillance du Comportement**: Le système est observé pour détecter les comportements anormaux tels que les plantages, les fuites de mémoire, les violations d'accès, les assertions ratées ou les boucles infinies.
*   **Découverte de Vulnérabilités**: L'objectif est de trouver des failles comme les [[BufferOverflow|dépassements de tampon]], les [[IntegerOverflow|dépassements d'entiers]], les [[SQLInjection|injections SQL]], les [[CrossSiteScripting|XSS]] ou les [[DenialOfService|dénis de service]].
*   **Types de Fuzzing**: Peut être basé sur des mutations (modifiant des entrées existantes), des générateurs (créant des entrées à partir de zéro selon un modèle) ou être intelligent (guidé par la couverture de code).

## 🛡️ Risques / Menaces Associés
*   [[ZeroDayVulnerability|Vulnérabilité Zero-Day]]: Peut révéler des failles inconnues.
*   [[Cyberattack|Cyberattaque]]: Les vulnérabilités découvertes par fuzzing peuvent être exploitées par des acteurs malveillants.
*   [[DataBreach|Fuite de données]]: Une vulnérabilité exploitée peut entraîner un accès non autorisé à des [[SensitiveData|informations sensibles]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecureCodingPractices|Pratiques de codage sécurisé]]: Implémenter une validation d'entrée robuste, une gestion des erreurs appropriée et une gestion sécurisée de la mémoire.
*   [[SoftwareTesting|Tests logiciels]] exhaustifs: Intégrer le fuzzing comme une partie régulière du cycle de développement logiciel (SDL).
*   [[StaticApplicationSecurityTesting|SAST]] et [[DynamicApplicationSecurityTesting|DAST]]: Combiner le fuzzing avec d'autres outils d'analyse de sécurité.
*   [[VulnerabilityManagementProgram|Programme de gestion des vulnérabilités]]: Mettre en place un processus pour identifier, trier et corriger rapidement les failles découvertes.

## 🔗 Notes Connexes
*   [[PenetrationTesting|Tests d'intrusion]]
*   [[VulnerabilityAssessment|Évaluation des vulnérabilités]]
*   [[Exploitation|Exploitation de vulnérabilités]]
*   [[SecureDevelopmentLifecycle|Cycle de Vie de Développement Sécurisé (SDLC)]]