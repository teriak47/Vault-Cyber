---
tags:
aliases:
  - DEP
  - Prévention de l'exécution des données
  - Data Execution Prevention
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Prévention de l'exécution des données (DEP)

## 📥 Définition en une phrase
> La [[DataExecutionPrevention|Prévention de l'exécution des données]] ([[DataExecutionPrevention|DEP]]) est une [[SecurityControl|fonctionnalité de sécurité]] d'un [[OperatingSystem|système d'exploitation]] qui marque des zones spécifiques de la [[MemoryManagement|mémoire]] comme non-exécutables afin d'empêcher l'exécution de [[Shellcode|code malveillant]] à partir de ces emplacements.

## 🧠 Concepts Clés / Piliers
*   **Marquage de la Mémoire Non-Exécutable**: Le [[OperatingSystem|système d'exploitation]] et le [[Hardware|matériel]] collaborent pour désigner des régions de la [[MemoryManagement|mémoire]] (telles que la [[Stack|pile]] et le [[Heap|tas]]) comme destinées uniquement aux [[Data|données]], interdisant ainsi toute tentative d'[[Exploitation|exécution de code]] à partir de celles-ci.
*   **[[NoExecuteBit|Bit NX/XD]]**: Les [[Computer|processeurs]] modernes intègrent un [[Bit|bit]] spécifique (le "[[NoExecuteBit|NX bit]]" pour AMD, "[[NoExecuteBit|XD bit]]" pour Intel) dans leurs [[MemoryManagement|tables de pages mémoire]]. Ce [[NoExecuteBit|bit]] permet au [[OperatingSystem|système d'exploitation]] de désigner des pages [[MemoryManagement|mémoire]] comme non-exécutables, déclenchant une exception matérielle si une [[Command|instruction]] y est détectée.
*   **Protection Contre l'[[CodeInjection|Injection de Code]]**: Le principe fondamental de la [[DataExecutionPrevention|DEP]] est de bloquer l'[[Exploitation|exécution]] de [[Shellcode|code injecté]] dans des zones de [[MemoryManagement|mémoire]] prévues pour les [[Data|données]], comme celles ciblées par les [[BufferOverflow|dépassements de tampon]].

## 💡 Importance en Cybersécurité
> La [[DataExecutionPrevention|DEP]] est un [[SecurityControl|contrôle de sécurité]] fondamental qui renforce la [[System|sécurité du système]] en rendant plus difficile pour les [[Malware|logiciels malveillants]] et les [[Exploit|exploits]] (notamment ceux liés aux [[BufferOverflow|dépassements de tampon]] et à l'[[CodeInjection|injection de code]]) de s'exécuter et de prendre le contrôle d'un [[Process|processus]] ou du [[System|système]].

## 🔗 Notes Connexes
*   [[AddressSpaceLayoutRandomization|ASLR]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[CodeInjection|Injection de Code]]
*   [[ExploitMitigation|Atténuation des Exploits]]
*   [[MemoryCorruption|Corruption de mémoire]]
*   [[NoExecuteBit|Bit No-Execute]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[ReturnOrientedProgramming|ROP]]
*   [[StackCanary|Stack Canary]]
*   [[StackSmashing|Stack Smashing]]