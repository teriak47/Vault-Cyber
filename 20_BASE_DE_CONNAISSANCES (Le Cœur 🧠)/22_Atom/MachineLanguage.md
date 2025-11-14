---
tags:
  - programmation/langage-machine
  - architecture/jeu-instructions
  - programmation
aliases:
  - Langage Machine
  - Machine Language
source:
  - 
cssclasses:
  - max
---

# Langage Machine

## 📥 Définition en une phrase
> Le langage machine est le langage de programmation de plus bas niveau, directement exécutable par le [[CentralProcessingUnit|processeur]] d'un ordinateur, composé d'instructions binaires (séquences de 0 et de 1).

## 🧠 Concepts Clés / Fonctionnement
*   **Représentation Binaire**: Chaque instruction est un code opération (opcode) suivi d'opérandes, tous encodés en [[BinaryCode|binaire]].
*   **Exécution Directe**: C'est le seul langage que le [[CentralProcessingUnit|CPU]] peut comprendre et exécuter nativement sans nécessiter de [[Interpreter|traduction]] ou d'[[Compiler|compilation]] préalable par un logiciel intermédiaire.
*   **Spécifique à l'Architecture**: Le langage machine est fortement lié à l'[[InstructionSetArchitecture|architecture de jeu d'instructions]] (ISA) d'un processeur donné (par exemple, x86, ARM), le rendant non portable entre différentes architectures.
*   **Génération**: Il est généralement le résultat de la [[Compilation|compilation]] de [[HighLevelProgrammingLanguage|langages de programmation de haut niveau]] (comme C++, Java) ou de l'[[AssemblyLanguage|assemblage]] de code en langage d'assemblage.
*   **Difficulté Humaine**: Il est extrêmement difficile pour les humains de lire, écrire ou comprendre directement le langage machine en raison de sa nature abstraite et binaire.

## 🛡️ Risques / Menaces Associés
*   [[SoftwareVulnerability|Vulnérabilités logicielles]] : Des erreurs dans le code source (écrit en langage de haut niveau) peuvent se traduire par des failles exploitables au niveau du langage machine (ex: [[BufferOverflow|dépassement de tampon]], [[CodeInjection|injection de code]]).
*   [[Malware|Malwares]] : Les logiciels malveillants sont finalement exécutés en langage machine, permettant aux attaquants d'interagir directement avec le matériel et le système d'exploitation.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecureCodingPractices|Pratiques de codage sécurisé]] : Réduire les vulnérabilités au niveau du code source afin d'éviter qu'elles ne se manifestent en langage machine exploitable.
*   [[BinaryAnalysis|Analyse binaire]] et [[StaticApplicationSecurityTesting|tests statiques/dynamiques]] : Utiliser des outils pour détecter les failles au niveau du code machine ou compilé.
*   [[OperatingSystemSecurity|Fonctionnalités de sécurité du système d'exploitation]] : Utiliser des mécanismes comme l'[[AddressSpaceLayoutRandomization|ASLR]] et la [[DataExecutionPrevention|DEP]] pour atténuer les exploits basés sur le code machine.
*   [[CodeReview|Revue de code]] : Examiner attentivement le code source pour identifier les erreurs logiques qui pourraient mener à des vulnérabilités de bas niveau.

## 🔗 Notes Connexes
*   [[AssemblyLanguage|Langage d'assemblage]]
*   [[CentralProcessingUnit|CPU]]
*   [[Compiler|Compilateur]]
*   [[BinaryCode|Code Binaire]]
*   [[InstructionSetArchitecture|Architecture de jeu d'instructions]]
*   [[HighLevelProgrammingLanguage|Langage de programmation de haut niveau]]