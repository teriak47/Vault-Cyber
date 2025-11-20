---
tags:
aliases:
  - Sécurité Mémoire
  - Memory Safety
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sécurité Mémoire (Memory Safety)

## 📥 Définition en une phrase
> La **sécurité mémoire** désigne l'ensemble des techniques et pratiques visant à prévenir les erreurs d’accès à la mémoire qui peuvent entraîner des vulnérabilités comme des corruptions mémoire ou des exécutions de code arbitraire.

## 🧠 Concepts Clés / Piliers
*   **Erreurs Fondamentales**: Identification des types d'erreurs d'accès mémoire qui compromettent la sécurité, telles que les débordements de tampon, les utilisations après libération, et les accès hors limites (out-of-bounds access).
*   **Approches Linguistiques**: Distinction entre les langages de programmation sûrs (ex: Rust, Go, Java) qui intègrent des mécanismes de sécurité mémoire au niveau du compilateur ou de la machine virtuelle, et les langages comme C/C++ nécessitant une gestion explicite des pointeurs.
*   **Mécanismes de Défense**: Présentation des contrôles de sécurité d'intégrité mémoire tels que les canaris de pile, la randomisation de l'espace d'adressage (ASLR), et la prévention de l'exécution des données (DEP), ainsi que les techniques de gestion automatique de la mémoire (comme le garbage collector).
*   **Outillage et Bonnes Pratiques**: Importance de l'application de pratiques de codage sécurisé, de l'analyse statique et dynamique du code, ainsi que du fuzzing pour identifier et prévenir les erreurs logicielles et les vulnérabilités liées à la mémoire.

## 💡 Importance en Cybersécurité
> La sécurité mémoire est un pilier fondamental de la cybersécurité car les vulnérabilités liées à la mémoire (comme la corruption mémoire) sont des vecteurs d'attaque parmi les plus couramment exploités par les acteurs de menace. Elles permettent souvent des exécutions de code à distance (RCE), des escalades de privilèges, ou d'autres formes de compromission de système, impactant directement l'intégrité, la confidentialité et l'disponibilité des systèmes. Prévenir ces erreurs est donc essentiel pour construire des logiciels robustes et sécurisés.

## 🔗 Notes Connexes
*   Débordement de tampon
*   Usage après libération
*   Corruption mémoire
*   Exécution de code à distance
*   Escalade de privilèges
*   Exploit
*   Stack Canary
*   ASLR
*   DEP
*   Programmation sécurisée
*   Analyse statique
*   Analyse dynamique
*   Fuzzing
*   Langages de programmation sûrs
*   Rust
*   Go
*   Java
*   Sandboxing
*   Vulnérabilité Logicielle