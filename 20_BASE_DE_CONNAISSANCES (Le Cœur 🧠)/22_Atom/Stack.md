---
tags:
  - securite/aslr
  - securite/canaris-pile
  - structure-donnees/lifo
  - depassement-tampon
  - memoire/pile
  - programmation/securisee
aliases:
  - Pile
  - Memory Stack
  - Call Stack
source:
  - null
cssclasses:
  - max
---

# Stack (Pile)

## 📥 Définition en une phrase
> La "stack" (pile) est une région de la mémoire vive utilisée par les programmes pour stocker temporairement des données de manière ordonnée, fonctionnant selon le principe "dernier entré, premier sorti" (LIFO).

## 🧠 Concepts Clés / Fonctionnement
*   **Structure LIFO** : Fonctionne sur le principe [[LIFO|Last-In, First-Out]] (Dernier entré, premier sorti), où le dernier élément ajouté est le premier à être retiré.
*   **Utilisation Principale** : Sert à gérer les [[FunctionCall|appels de fonctions]], stockant les adresses de retour, les arguments de fonctions, les variables locales et l'état des registres.
*   **[[StackFrame|Cadre de Pile]]** : À chaque appel de fonction, un nouveau [[StackFrame|cadre de pile]] est créé et "empilé" sur la pile, contenant les données spécifiques à cette invocation de fonction.
*   **[[StackPointer|Pointeur de Pile]]** : Le [[StackPointer|pointeur de pile]] (souvent `ESP` ou `RSP` sur les architectures x86/x64) pointe toujours vers le sommet de la pile, indiquant la dernière donnée empilée.
*   **Direction de Croissance** : La pile croît généralement vers les adresses mémoire plus basses sur la plupart des architectures (comme x86/x64).

## 🛡️ Risques / Menaces Associés
*   [[BufferOverflow|Dépassement de Tampon]] : Écriture de données au-delà des limites d'un tampon alloué sur la pile, pouvant corrompre l'[[StackFrame|intégrité du cadre de pile]], y compris l'adresse de retour, et potentiellement permettre l'[[CodeExecution|exécution de code arbitraire]].
*   [[StackOverflow|Débordement de Pile]] : Situation où toute la mémoire allouée à la pile est consommée, souvent due à une [[Recursion|récursion]] infinie ou à l'allocation excessive de grandes variables locales, menant à un [[DenialOfService|déni de service]] (plantage du programme).
*   [[ReturnOrientedProgramming|Return-Oriented Programming (ROP)]] : Technique d'[[Exploit|exploitation]] avancée qui manipule les adresses de retour sur la pile pour enchaîner de petits fragments de code existants (gadgets) et ainsi exécuter une logique malveillante sans injecter de nouveau code.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[StackCanary|Stack Canaries]] : Valeurs aléatoires insérées sur la pile avant l'adresse de retour pour détecter les [[BufferOverflow|dépassements de tampon]] avant qu'ils ne puissent corrompre les données critiques.
*   [[DataExecutionPrevention|Data Execution Prevention (DEP)]] / [[NoExecuteBit|NX bit]] : Empêche l'exécution de code à partir de régions de la mémoire désignées comme des zones de données (comme la pile), rendant plus difficile l'[[CodeInjection|injection]] et l'exécution de shellcode sur la pile.
*   [[AddressSpaceLayoutRandomization|Address Space Layout Randomization (ASLR)]] : Randomise l'emplacement de la pile en mémoire au démarrage du programme, rendant les adresses de retour plus difficiles à prédire pour les [[Exploit|attaquants]].
*   **Programmation Sécurisée** : Utiliser des fonctions sûres (`strncpy_s`, `snprintf`), valider les entrées et s'assurer que les tampons sont alloués avec des tailles suffisantes pour éviter les [[BufferOverflow|dépassements]].
*   **[[Compiler|Compilateur]] Protections** : Activer les options de sécurité du [[Compiler|compilateur]] (ex: `-fstack-protector` dans GCC) pour inclure des [[StackCanary|canaris de pile]] et d'autres protections automatiques.

## 🔗 Notes Connexes
*   [[Heap|Heap (Tas)]]
*   [[MemoryManagement|Gestion de la Mémoire]]
*   [[ProgramExecution|Exécution de Programme]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Exploit|Exploitation]]