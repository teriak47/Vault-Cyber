---
tags:
  - concept
  - concept/general
  - memoire
  - a-completer
aliases:
  - Pile
  - Memory Stack
  - Call Stack
  - Stack
archetype: concept-general
source:
  -
cssclasses:
  - max
---

# Stack (Pile)

## 📥 Définition en une phrase
> La [[Stack|stack]] (pile) est une région de la [[MemoryManagement|mémoire vive]] utilisée par les [[Software|programmes]] pour stocker temporairement des [[Data|données]] de manière ordonnée, fonctionnant selon le principe "dernier entré, premier sorti" ([[LIFO|LIFO]]).

## 🧠 Concepts Clés / Piliers
*   **Structure [[LIFO|Last-In, First-Out]]**: La [[Stack|pile]] fonctionne sur le principe du Dernier Entré, Premier Sorti (Last-In, First-Out - [[LIFO|LIFO]]), signifiant que le dernier élément ajouté est toujours le premier à être retiré.
*   **Gestion des [[FunctionCall|Appels de Fonctions]]**: Elle est principalement utilisée pour gérer les [[FunctionCall|appels de fonctions]] et les retours. Lors d'un appel, les adresses de retour, les arguments de la fonction, les [[Variable|variables locales]] et l'état des [[Register|registres du processeur]] sont "empilés".
*   **[[StackFrame|Cadres de Pile]]**: Chaque [[FunctionCall|appel de fonction]] entraîne la création d'un [[StackFrame|cadre de pile]] (ou cadre d'activation) sur le dessus de la [[Stack|pile]]. Ce [[StackFrame|cadre]] contient toutes les [[Data|données]] spécifiques à l'exécution de cette fonction.
*   **[[StackPointer|Pointeur de Pile]]**: Un [[StackPointer|pointeur de pile]] est un [[Register|registre]] (comme `ESP` ou `RSP` sur les architectures x86/x64) qui pointe constamment vers le sommet de la [[Stack|pile]], indiquant la [[Data|donnée]] la plus récemment ajoutée et la prochaine à être potentiellement retirée.
*   **Direction de Croissance**: Sur la plupart des architectures (comme x86/x64), la [[Stack|pile]] croît vers les adresses [[MemoryAddress|mémoire]] plus basses, ce qui signifie que de nouveaux éléments sont ajoutés à des adresses inférieures à celles des éléments précédents.

## 💡 Importance en Cybersécurité
> La [[Stack|pile]] est un élément critique de la [[MemoryManagement|gestion de la mémoire]] et représente une [[AttackSurface|surface d'attaque]] majeure en [[Cybersecurity|cybersécurité]]. Une manipulation incorrecte de la [[Stack|pile]] peut entraîner des [[SoftwareVulnerability|vulnérabilités logicielles]] telles que les [[BufferOverflow|dépassements de tampon]], les [[StackBufferOverflow|débordements de tampon de pile]], ou les [[StackUnderflow|sous-débordements de pile]]. Ces [[SoftwareVulnerability|vulnérabilités]] peuvent être exploitées par des [[ThreatActor|acteurs de menace]] pour injecter du [[Shellcode|code malveillant]], exécuter des [[RemoteCodeExecution|codes à distance]], ou provoquer des [[DenialOfService|dénis de service]]. Les techniques de [[MemorySafety|sécurité mémoire]] et les [[SecurityControl|contrôles de sécurité]] comme le [[StackCanary|Stack Canary]], la [[DataExecutionPrevention|DEP]] (Prévention de l'Exécution des Données), et l'[[AddressSpaceLayoutRandomization|ASLR]] visent à protéger l'intégrité de la [[Stack|pile]] et à mitiger ces [[Exploitation|exploits]].

## 🔗 Notes Connexes
*   [[MemoryCorruption|Corruption de mémoire]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[Heap|Tas de mémoire]]
*   [[Programming|Programmation]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[DataExecutionPrevention|Prévention de l'exécution des données]]
*   [[StackCanary|Stack Canary]]
*   [[ReturnOrientedProgramming|Programmation Orientée Retour]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   [Raison 1 : Le concept de [[LIFO|LIFO]] mériterait une note dédiée pour expliquer en détail son fonctionnement. Il en va de même pour [[FunctionCall]], [[StackFrame]] et [[StackPointer]].]
*   [Raison 2 : La section "Importance en Cybersécurité" pourrait être enrichie avec des exemples plus concrets d'exploits de pile ou des scénarios d'attaque spécifiques.]