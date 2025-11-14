---
tags:
  - memoire/tas
  - gestion-memoire/allocation-dynamique
  - exploitation/pulverisation-tas
  - depassement-tampon
  - gestion-memoire/fuite
  - vulnerabilite/utilisation-apres-liberation
aliases:
  - Tas de mémoire
  - Tas
source:
  - null
cssclasses:
  - max
---

# Tas (Heap)

## 📥 Définition en une phrase
> Le tas (heap) est une zone de mémoire dynamique utilisée par les programmes pour allouer et désallouer de la mémoire à l'exécution, dont la taille et la durée de vie ne sont pas connues au moment de la compilation.

## 🧠 Concepts Clés / Fonctionnement
*   **[[MemoryAllocation|Allocation de mémoire]] dynamique** : La mémoire sur le tas est allouée et libérée explicitement par le programmeur (ou automatiquement par un [[GarbageCollection|collecteur de déchets]]) pendant l'exécution, contrairement à la [[Stack|Pile (Stack)]] où l'allocation est statique ou gérée par l'appel de fonctions.
*   **Gestion explicite ou automatique** : En C/C++, l'allocation se fait via des fonctions comme `malloc`/`free` ou `new`/`delete`. Dans des langages comme Java ou Python, un [[GarbageCollection|collecteur de déchets]] gère la libération de la mémoire de manière automatique.
*   **Durée de vie variable** : Les objets alloués sur le tas persistent tant qu'ils sont référencés ou explicitement libérés, même après la fin de la fonction qui les a créés.
*   **Fragmentation** : L'allocation et la désallocation irrégulière de blocs de mémoire de différentes tailles peuvent entraîner une fragmentation du tas, rendant plus difficile l'allocation de grands blocs contigus.

## 🛡️ Risques / Menaces Associés
*   [[BufferOverflow|Dépassement de tampon]] (Heap Overflow) : Écriture de données au-delà des limites d'un bloc alloué sur le tas, pouvant corrompre des données adjacentes ou des métadonnées du gestionnaire de tas.
*   [[UseAfterFree|Utilisation après libération]] : Tenter d'accéder à une zone de mémoire qui a déjà été libérée et potentiellement réaffectée à un autre usage, conduisant à des comportements imprévisibles ou à l'exécution de code arbitraire.
*   [[DoubleFree|Double libération]] : Tenter de libérer deux fois la même zone de mémoire, ce qui peut corrompre la structure interne du gestionnaire de tas et entraîner des vulnérabilités ou des plantages.
*   [[MemoryLeak|Fuite de mémoire]] : Oubli de libérer la mémoire allouée sur le tas lorsqu'elle n'est plus nécessaire, ce qui entraîne une consommation excessive de ressources et potentiellement un déni de service.
*   [[HeapSpray|Pulvérisation de tas]] : Une technique d'exploitation visant à placer des données malveillantes (souvent du shellcode) à des adresses mémoire prévisibles sur le tas.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MemorySafety|Programmation sécurisée]] : Utilisation de bonnes pratiques de gestion de la mémoire, comme la vérification des limites de tampon, l'initialisation des pointeurs et la libération correcte des ressources.
*   Utilisation de langages avec [[GarbageCollection|collecte de déchets]] : Réduit le risque de fuites de mémoire et d'erreurs de libération en automatisant la gestion de la mémoire.
*   [[AddressSpaceLayoutRandomization|ASLR]] (Address Space Layout Randomization) : Rend plus difficile pour les attaquants de prédire les adresses des allocations sur le tas.
*   [[DataExecutionPrevention|DEP]] (Data Execution Prevention) / [[NoExecute|NX bit]] : Empêche l'exécution de code à partir de zones mémoire non exécutables, y compris le tas, pour contrer les attaques de pulvérisation de tas.
*   Utilisation de bibliothèques et de gestionnaires de tas sécurisés : Certains gestionnaires de tas intègrent des protections contre les exploits courants (ex: glibc malloc protections).

## 🔗 Notes Connexes
*   [[Stack|Pile (Stack)]]
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[BufferOverflow|Dépassement de tampon]]
*   [[Pointer|Pointeur]]
*   [[GarbageCollection|Collecte de déchets]]