---
tags:
  - concept/general
  - securite/memoire
  - methode/securite
  - protection/buffer-overflow
  - securite/systeme
  - a-completer
aliases:
  - Stack Canary
  - Canari de Pile
archetype: concept-general
source:
  -
cssclasses:
  - max
---

# Stack Canary (Canari de Pile)

## 📥 Définition en une phrase
> Un mécanisme de sécurité utilisé pour détecter et prévenir les dépassements de tampon sur la pile en insérant une valeur sentinelle ("canary") entre les variables locales d'une fonction et son adresse de retour.

## 🧠 Concepts Clés / Piliers
*   **Insertion du Canari**: Une valeur secrète, souvent générée de manière pseudo-aléatoire, est placée sur la pile juste avant l'adresse de retour de la fonction. Son emplacement stratégique vise à protéger les données critiques du flux d'exécution.
*   **Vérification de l'Intégrité**: Avant que la fonction ne retourne le contrôle à l'appelant, le système d'exploitation ou le compilateur insère une instruction pour vérifier si la valeur du canari est restée inchangée. Cette vérification agit comme un contrôle de sécurité indispensable avant une opération critique.
*   **Détection d'Attaque**: Si la valeur du canari a été modifiée, cela indique qu'un dépassement de tampon s'est produit, généralement dans le but d'écraser l'adresse de retour. Dans ce cas, le programme déclenche une erreur fatale et se termine de manière anormale pour prévenir l'exploitation de la vulnérabilité et l'exécution de code à distance.
*   **Types de Canaris**:
    *   **Terminator Canaries**: Utilisent des octets spécifiques (par exemple, `0x00`, `0x0A`, `0x0D`, `0xFF`) qui peuvent être difficiles à écraser avec certaines fonctions de manipulation de chaînes (comme `strcpy` qui s'arrête au `0x00`).
    *   **Random Canaries**: La valeur du canari est générée aléatoirement au démarrage du programme ou du système, rendant sa prédiction difficile pour un attaquant.
    *   **XOR Canaries**: La valeur du canari est XORée avec l'adresse de retour ou d'autres informations importantes sur la pile. Cela rend sa falsification plus complexe car l'attaquant devrait deviner à la fois la valeur du canari et les données utilisées pour le XOR.

## 💡 Importance en Cybersécurité
> Le canari de pile est un mécanisme de sécurité fondamental dans le domaine de la sécurité mémoire. Il permet de détecter efficacement les tentatives d'exploitation des dépassements de tampon, qui représentent une vulnérabilité persistante et courante pouvant entraîner la corruption de mémoire et, ultimement, l'exécution de code à distance. En forçant le programme à s'interrompre avant qu'une attaque ne puisse manipuler l'adresse de retour pour détourner le flux d'exécution, les canaris de pile renforcent considérablement l'intégrité et la disponibilité des systèmes.

## 🔗 Notes Connexes
*   Dépassement de Tampon
*   Pile
*   Sécurité Mémoire
*   Bit No-Execute (NX Bit)
*   Address Space Layout Randomization (ASLR)
*   Exploitation
*   Exécution de Code à Distance (RCE)
*   Intégrité

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La note pourrait être complétée par des exemples de code simples (en C/C++) montrant l'insertion et la vérification d'un canari pour une meilleure compréhension pratique.
*   Des détails supplémentaires sur les techniques de contournement du canari de pile (par exemple, attaque par force brute sur les canaris aléatoires, contournement des canaris terminator) seraient pertinents pour une perspective d'surface d'attaque.
*   Ajouter des informations sur les compilateurs et systèmes d'exploitation qui implémentent cette protection par défaut.