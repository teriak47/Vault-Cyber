---
tags:
  - depassement-tampon
  - programmation/securisee
  - cybersécurité/exploitation-vulnerabilite
  - securite/vulnerabilites
aliases:
  - Dépassement de Tampon
  - Buffer Overflow
source:
  - 
cssclasses:
  - max
---

# Dépassement de Tampon

## 📥 Définition en une phrase
> Une vulnérabilité de sécurité où un programme tente d'écrire plus de données dans un tampon mémoire que ce pour quoi il a été alloué, écrasant ainsi les données adjacentes et pouvant mener à un plantage ou à l'exécution de code arbitraire.

## 🧠 Concepts Clés / Fonctionnement
*   Se produit lorsqu'un programme ne vérifie pas les limites d'une zone de mémoire allouée (un [[Buffer|tampon]]) avant d'y écrire des données.
*   Les données en excès débordent du tampon et écrasent les informations stockées dans les adresses mémoire contiguës.
*   Peut affecter différentes zones de mémoire, notamment la [[Stack|pile]] (stack overflow) ou le [[Heap|tas]] (heap overflow).
*   L'écrasement peut cibler des adresses de retour de fonctions, des pointeurs de données, ou d'autres variables, altérant ainsi le comportement normal du programme.
*   Les attaquants peuvent exploiter cette vulnérabilité pour injecter et exécuter du [[Shellcode|code malveillant]] ou provoquer un [[DenialOfService|déni de service]].
*   Principalement associé aux langages de programmation de bas niveau comme C et C++ qui n'ont pas de gestion automatique de la [[MemorySafety|sécurité mémoire]].

## 🛡️ Risques / Menaces Associés
*   [[RemoteCodeExecution|Exécution de Code à Distance]] (RCE)
*   [[DenialOfService|Déni de Service]] (DoS)
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[DataCorruption|Corruption de données]]
*   [[MemoryCorruption|Corruption de mémoire]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Programmation Sécurisée :** Utiliser des fonctions qui vérifient les limites (ex: `strncpy_s`, `snprintf`) et éviter les fonctions dangereuses (ex: `strcpy`, `sprintf`).
*   **Langages Sécurisés :** Préférer des langages de programmation avec une gestion automatique de la mémoire et des vérifications de limites (ex: Python, Java, Rust).
*   **Protections au Niveau OS :**
    *   [[AddressSpaceLayoutRandomization|ASLR]] (Address Space Layout Randomization) : Randomise l'emplacement en mémoire des zones clés pour rendre les exploits plus difficiles.
    *   [[DataExecutionPrevention|DEP]] / [[NoExecuteBit|Bit NX]] : Empêche l'exécution de code à partir de zones mémoire non exécutables (comme la pile ou le tas).
    *   [[StackCanary|Stack Canaries]] : Valeurs sentinelles placées sur la pile qui sont vérifiées avant le retour d'une fonction pour détecter un débordement.
*   **[[CodeReview|Revue de Code]] :** Examiner le code source pour identifier les vulnérabilités potentielles de dépassement de tampon.
*   **[[Fuzzing|Tests de Fuzzing]] :** Alimenter le programme avec de grandes quantités de données aléatoires ou malformées pour déclencher des erreurs et découvrir des vulnérabilités.

## 🔗 Notes Connexes
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[Exploit|Exploit]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Stack|Pile]]
*   [[Heap|Tas]]
*   [[ReturnOrientedProgramming|Programmation Orientée Retour]] (ROP)