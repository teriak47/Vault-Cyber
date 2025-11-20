---
tags:
aliases:
  - Test de Fuzzing
  - Fuzz Testing
  - Fuzzing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Fuzzing

## 📥 Définition en une phrase
> Le Fuzzing est une technique de test logiciel qui consiste à injecter des données aléatoires, inattendues ou malformées dans une application, un système ou un protocole pour provoquer des erreurs, des plantages et révéler des vulnérabilités latentes.

## 🧠 Concepts Clés / Piliers
*   **Génération de Données**: Crée des entrées non valides, semi-valides ou aléatoires qui sortent des spécifications attendues du programme, exploitant les faiblesses potentielles dans la validation des entrées.
*   **Injection Ciblée**: Ces données sont ensuite injectées dans différents points d'entrée de la application cible, tels que les champs de formulaire, les API, les paramètres réseau, ou les fichiers d'entrée.
*   **Surveillance et Détection**: Le système ou l'application est rigoureusement surveillé pour détecter les comportements anormaux, incluant les plantages, les fuites de mémoire, les violations d'accès, les assertions ratées ou les boucles infinies.
*   **Découverte de Vulnérabilités**: L'objectif principal est d'identifier des failles de sécurité telles que les dépassements de tampon, les dépassements d'entiers, les injections SQL, les attaques XSS ou les dénis de service.
*   **Types de Fuzzing**: Le fuzzing peut être basé sur des mutations (modifiant des entrées existantes), des générateurs (créant des entrées à partir de zéro selon un modèle) ou être intelligent (guidé par la couverture de code via des outils comme Code Coverage).

## 💡 Importance en Cybersécurité
> Le fuzzing est fondamental en cybersécurité car il permet de découvrir de manière proactive des vulnérabilités inconnues, y compris des potentielles vulnérabilités Zero-Day, avant qu'elles ne soient exploitées par des acteurs de menace. En identifiant et en corrigeant ces failles tôt dans le cycle de vie de développement sécurisé (SDLC), il contribue significativement à la robustesse et à la sécurité des logiciels et des systèmes, réduisant ainsi la surface d'attaque et le risque de cyberattaques telles que les fuites de données ou les compromissions de système.

## 🔗 Notes Connexes
*   Tests d'intrusion
*   Gestion des vulnérabilités
*   Exploitation de vulnérabilités
*   Pratiques de codage sécurisé
*   Tests logiciels
*   SAST
*   DAST
*   Cycle de Vie de Développement Sécurisé