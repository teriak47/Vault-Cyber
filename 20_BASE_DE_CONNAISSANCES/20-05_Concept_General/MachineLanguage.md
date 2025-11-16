---
tags:
aliases:
  - Langage Machine
  - Machine Language
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Langage Machine

## 📥 Définition en une phrase
> Le [[MachineLanguage|langage machine]] est le [[Programming|langage de programmation]] de plus bas niveau, directement exécutable par le [[CentralProcessingUnit|processeur]] d'un [[Computer|ordinateur]], composé d'instructions binaires.

## 🧠 Concepts Clés / Piliers
*   **Représentation Binaire**: Chaque instruction est un code opération (opcode) et des opérandes encodés en [[BinaryDigit|binaire]] (séquences de 0 et de 1).
*   **Exécution Directe**: C'est le seul langage que le [[CentralProcessingUnit|CPU]] peut comprendre et exécuter nativement, sans nécessiter de [[Compiler|compilation]] ou d'[[Interpreter|interprétation]] préalable par un [[Software|logiciel]] intermédiaire.
*   **Spécificité Architecturale**: Le langage machine est intrinsèquement lié à l'[[InstructionSetArchitecture|architecture de jeu d'instructions]] (ISA) d'un [[CentralProcessingUnit|processeur]] donné (ex: x86, ARM), le rendant non portable et limitant son [[Interoperability|interopérabilité]] entre différentes plateformes.
*   **Génération**: Il est généralement le résultat de la [[Compilation|compilation]] de [[HighLevelProgrammingLanguage|langages de programmation de haut niveau]] (comme C++, Java) ou de l'[[AssemblyLanguage|assemblage]] de code en langage d'assemblage.
*   **Difficulté Humaine**: Extrêmement difficile à lire, écrire ou comprendre directement pour les [[User|humains]] en raison de sa nature abstraite et [[BinaryDigit|binaire]].

## 💡 Importance en Cybersécurité
> Le [[MachineLanguage|langage machine]] est le fondement de l'exécution de tout [[Software|logiciel]] sur un [[Computer|ordinateur]]. Sa compréhension est cruciale en [[Cybersecurity|cybersécurité]] car il représente le point d'interaction direct avec le [[Hardware|matériel]]. Les [[SoftwareVulnerability|vulnérabilités logicielles]], qu'elles soient intentionnelles (comme les [[Malware|malwares]]) ou accidentelles (comme les [[BufferOverflow|dépassements de tampon]]), se manifestent au niveau du langage machine. L'analyse de ce langage permet de comprendre comment les [[Exploitation|exploits]] fonctionnent et comment les [[SecurityControl|mesures de sécurité]] comme l'[[AddressSpaceLayoutRandomization|ASLR]] et la [[DataExecutionPrevention|DEP]] protègent les [[System|systèmes]] à leur niveau le plus bas. C'est le champ de bataille ultime où les [[ThreatActor|acteurs de menace]] tentent de contourner les défenses.

## 🔗 Notes Connexes
*   [[AssemblyLanguage|Langage d'assemblage]]
*   [[CentralProcessingUnit|CPU]]
*   [[InstructionSetArchitecture|Architecture de jeu d'instructions]]
*   [[HighLevelProgrammingLanguage|Langage de programmation de haut niveau]]
*   [[Compiler|Compilateur]]
*   [[BinaryDigit|Binaire]]
*   [[BufferOverflow|Buffer Overflow]]
*   [[AddressSpaceLayoutRandomization|ASLR]]
*   [[DataExecutionPrevention|DEP]]
*   [[ReverseEngineering|Ingénierie inverse]]
*   [[OperatingSystem|Système d'exploitation]]