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
> La stack (pile) est une région de la mémoire vive utilisée par les programmes pour stocker temporairement des données de manière ordonnée, fonctionnant selon le principe "dernier entré, premier sorti" (LIFO).

## 🧠 Concepts Clés / Piliers
*   **Structure Last-In, First-Out**: La pile fonctionne sur le principe du Dernier Entré, Premier Sorti (Last-In, First-Out - LIFO), signifiant que le dernier élément ajouté est toujours le premier à être retiré.
*   **Gestion des Appels de Fonctions**: Elle est principalement utilisée pour gérer les appels de fonctions et les retours. Lors d'un appel, les adresses de retour, les arguments de la fonction, les variables locales et l'état des registres du processeur sont "empilés".
*   **Cadres de Pile**: Chaque appel de fonction entraîne la création d'un cadre de pile (ou cadre d'activation) sur le dessus de la pile. Ce cadre contient toutes les données spécifiques à l'exécution de cette fonction.
*   **Pointeur de Pile**: Un pointeur de pile est un registre (comme `ESP` ou `RSP` sur les architectures x86/x64) qui pointe constamment vers le sommet de la pile, indiquant la donnée la plus récemment ajoutée et la prochaine à être potentiellement retirée.
*   **Direction de Croissance**: Sur la plupart des architectures (comme x86/x64), la pile croît vers les adresses mémoire plus basses, ce qui signifie que de nouveaux éléments sont ajoutés à des adresses inférieures à celles des éléments précédents.

## 💡 Importance en Cybersécurité
> La pile est un élément critique de la gestion de la mémoire et représente une surface d'attaque majeure en cybersécurité. Une manipulation incorrecte de la pile peut entraîner des vulnérabilités logicielles telles que les dépassements de tampon, les débordements de tampon de pile, ou les sous-débordements de pile. Ces vulnérabilités peuvent être exploitées par des acteurs de menace pour injecter du code malveillant, exécuter des codes à distance, ou provoquer des dénis de service. Les techniques de sécurité mémoire et les contrôles de sécurité comme le Stack Canary, la DEP (Prévention de l'Exécution des Données), et l'ASLR visent à protéger l'intégrité de la pile et à mitiger ces exploits.

## 🔗 Notes Connexes
*   Corruption de mémoire
*   Dépassement de Tampon
*   Tas de mémoire
*   Programmation
*   Système d'exploitation
*   Prévention de l'exécution des données
*   Stack Canary
*   Programmation Orientée Retour

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   [Raison 1 : Le concept de LIFO mériterait une note dédiée pour expliquer en détail son fonctionnement. Il en va de même pour FunctionCall, StackFrame et StackPointer.]
*   [Raison 2 : La section "Importance en Cybersécurité" pourrait être enrichie avec des exemples plus concrets d'exploits de pile ou des scénarios d'attaque spécifiques.]