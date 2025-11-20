---
tags:
  - memoire
  - développement
aliases:
  - Tas de mémoire
  - Tas
  - Memory Heap
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Tas (Heap)

## 📥 Définition en une phrase
> Le tas (heap) est une zone de mémoire dynamique utilisée par les programmes pour allouer et désallouer de la mémoire à l'exécution, dont la taille et la durée de vie ne sont pas connues au moment de la compilation.

## 🧠 Concepts Clés / Piliers
*   **Allocation de mémoire dynamique** : La mémoire sur le tas est allouée et libérée explicitement par le programmeur (ou automatiquement par un collecteur de déchets) pendant l'exécution, contrairement à la pile (Stack) où l'allocation est statique ou gérée par l'appel de fonctions.
*   **Gestion de la durée de vie** : Les objets alloués sur le tas peuvent persister tant qu'ils sont référencés ou explicitement libérés, permettant une durée de vie qui dépasse celle de la fonction ou du bloc de code qui les a créés.
*   **Fragmentation** : L'allocation et la désallocation irrégulière de blocs de mémoire de différentes tailles peuvent entraîner une fragmentation du tas, rendant plus difficile l'allocation de grands blocs contigus et pouvant affecter les performances du système.
*   **Pointeurs et références** : L'accès aux données stockées sur le tas se fait généralement via des pointeurs ou des références, car leur emplacement exact n'est pas connu au moment de la compilation.

## 💡 Importance en Cybersécurité
> La gestion du tas est critique en cybersécurité car il est une cible fréquente pour les attaques de corruption de mémoire. Une mauvaise gestion peut entraîner des vulnérabilités de sécurité comme les dépassements de tampon, les utilisations après libération ou les doubles libérations, permettant aux attaquants d'exécuter du code arbitraire, d'accéder à des données sensibles ou de provoquer des dénis de service. La compréhension de son fonctionnement et l'application de mesures de sécurité mémoire sont donc essentielles pour protéger les systèmes.

## 🛡️ Risques / Menaces Associés
*   **Dépassement de tampon (Heap Overflow)** : Une vulnérabilité où une application écrit des données au-delà des limites d'un bloc de mémoire alloué sur le tas, pouvant corrompre des données adjacentes, des métadonnées du gestionnaire de tas ou même prendre le contrôle de l'exécution du processus.
*   **Utilisation après libération** : Se produit lorsqu'un programme tente d'accéder à une zone de mémoire qui a déjà été libérée et potentiellement réaffectée à un autre usage. Cela peut entraîner des comportements imprévisibles, des plantages ou l'exécution de code arbitraire.
*   **Double libération** : Tenter de libérer deux fois la même zone de mémoire. Cela peut corrompre la structure interne du gestionnaire de tas, créant des vulnérabilités qui peuvent être exploitées pour l'exécution de code.
*   **Fuite de mémoire** : Oubli de libérer la mémoire allouée sur le tas lorsque celle-ci n'est plus nécessaire. Cela conduit à une consommation excessive de ressources, pouvant entraîner un déni de service pour le système ou l'application affectée.
*   **Pulvérisation de tas** : Une technique d'exploitation visant à remplir de larges portions du tas avec des données contrôlées par l'attaquant (souvent du shellcode), en espérant qu'une autre vulnérabilité redirigera le flux d'exécution vers l'une de ces adresses prévisibles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Programmation sécurisée** : Adopter des pratiques de programmation qui minimisent les risques de corruption de mémoire, comme la vérification systématique des limites de tampon, l'initialisation des pointeurs et la libération correcte des ressources allouées.
*   **Collecte de déchets** : Utiliser des langages de programmation qui intègrent un collecteur de déchets (comme Java, Python) pour automatiser la gestion de la mémoire, réduisant ainsi le risque de fuites de mémoire, utilisations après libération et doubles libérations.
*   **ASLR (Address Space Layout Randomization)** : Une mesure de sécurité qui randomise les emplacements mémoire des zones clés d'un processus (y compris le tas), rendant plus difficile pour les attaquants de prédire les adresses et de cibler des zones spécifiques pour l'exploitation.
*   **DEP (Data Execution Prevention) / NX bit** : Technologies qui marquent certaines zones de mémoire (y compris le tas) comme non-exécutables, empêchant l'exécution de code à partir de ces régions. Cela permet de contrer les attaques de pulvérisation de tas et d'autres techniques d'exploitation.
*   **Stack Canary** : Bien que principalement pour la pile, certains principes s'appliquent pour la détection de corruption avant qu'elle ne soit utilisée pour détourner le flux d'exécution.
*   **Utilisation de bibliothèques et de gestionnaires de tas sécurisés** : Recourir à des implémentations de gestionnaires de tas qui intègrent des protections et des vérifications supplémentaires pour détecter et atténuer les vulnérabilités de corruption de mémoire.

## 🔗 Notes Connexes
*   Pile (Stack)
*   Gestion de la mémoire
*   Corruption de mémoire
*   Dépassement de tampon
*   Sécurité Mémoire
*   Programmation
*   Vulnérabilité