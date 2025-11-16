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
> Le tas (heap) est une zone de [[MemoryManagement|mémoire dynamique]] utilisée par les [[Programming|programmes]] pour allouer et désallouer de la mémoire à l'exécution, dont la taille et la durée de vie ne sont pas connues au moment de la compilation.

## 🧠 Concepts Clés / Piliers
*   **[[MemoryAllocation|Allocation de mémoire]] dynamique** : La mémoire sur le tas est allouée et libérée explicitement par le [[Programmation|programmeur]] (ou automatiquement par un [[GarbageCollection|collecteur de déchets]]) pendant l'exécution, contrairement à la [[Stack|pile (Stack)]] où l'allocation est statique ou gérée par l'appel de fonctions.
*   **Gestion de la durée de vie** : Les [[Resource|objets]] alloués sur le tas peuvent persister tant qu'ils sont référencés ou explicitement libérés, permettant une durée de vie qui dépasse celle de la fonction ou du bloc de code qui les a créés.
*   **Fragmentation** : L'allocation et la désallocation irrégulière de blocs de mémoire de différentes tailles peuvent entraîner une fragmentation du tas, rendant plus difficile l'allocation de grands blocs contigus et pouvant affecter les [[NetworkPerformance|performances du système]].
*   **[[Pointer|Pointeur]]s et références** : L'accès aux données stockées sur le tas se fait généralement via des [[Pointer|pointeurs]] ou des références, car leur emplacement exact n'est pas connu au moment de la [[Programming|compilation]].

## 💡 Importance en Cybersécurité
> La gestion du tas est critique en [[Cybersecurity|cybersécurité]] car il est une cible fréquente pour les [[MemoryCorruption|attaques de corruption de mémoire]]. Une mauvaise gestion peut entraîner des [[SecurityVulnerabilities|vulnérabilités de sécurité]] comme les [[BufferOverflow|dépassements de tampon]], les [[UseAfterFree|utilisations après libération]] ou les [[DoubleFree|doubles libérations]], permettant aux [[ThreatActor|attaquants]] d'exécuter du code arbitraire, d'accéder à des [[SensitiveData|données sensibles]] ou de provoquer des [[ServiceDisruption|dénis de service]]. La compréhension de son fonctionnement et l'application de mesures de [[MemorySafety|sécurité mémoire]] sont donc essentielles pour protéger les [[System|systèmes]].

## 🛡️ Risques / Menaces Associés
*   **[[BufferOverflow|Dépassement de tampon]] (Heap Overflow)** : Une [[Vulnerability|vulnérabilité]] où une [[SoftwareApplication|application]] écrit des données au-delà des limites d'un bloc de mémoire alloué sur le tas, pouvant corrompre des données adjacentes, des métadonnées du gestionnaire de tas ou même prendre le contrôle de l'exécution du [[Process|processus]].
*   **[[UseAfterFree|Utilisation après libération]]** : Se produit lorsqu'un [[SoftwareApplication|programme]] tente d'accéder à une zone de mémoire qui a déjà été libérée et potentiellement réaffectée à un autre usage. Cela peut entraîner des comportements imprévisibles, des [[System|plantages]] ou l'[[RemoteCodeExecution|exécution de code arbitraire]].
*   **[[DoubleFree|Double libération]]** : Tenter de libérer deux fois la même zone de mémoire. Cela peut corrompre la structure interne du gestionnaire de tas, créant des [[SecurityVulnerabilities|vulnérabilités]] qui peuvent être exploitées pour l'[[Exploitation|exécution de code]].
*   **[[MemoryLeak|Fuite de mémoire]]** : Oubli de libérer la mémoire allouée sur le tas lorsque celle-ci n'est plus nécessaire. Cela conduit à une consommation excessive de [[Resource|ressources]], pouvant entraîner un [[DenialOfService|déni de service]] pour le [[System|système]] ou l'[[SoftwareApplication|application]] affectée.
*   **[[HeapSpray|Pulvérisation de tas]]** : Une technique d'[[Exploitation|exploitation]] visant à remplir de larges portions du tas avec des données contrôlées par l'attaquant (souvent du [[Shellcode|shellcode]]), en espérant qu'une autre [[Vulnerability|vulnérabilité]] redirigera le flux d'exécution vers l'une de ces adresses prévisibles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[MemorySafety|Programmation sécurisée]]** : Adopter des pratiques de [[Programming|programmation]] qui minimisent les risques de [[MemoryCorruption|corruption de mémoire]], comme la vérification systématique des limites de [[Buffer|tampon]], l'initialisation des [[Pointer|pointeurs]] et la libération correcte des [[Resource|ressources]] allouées.
*   **[[GarbageCollection|Collecte de déchets]]** : Utiliser des [[Programming|langages de programmation]] qui intègrent un [[GarbageCollection|collecteur de déchets]] (comme Java, Python) pour automatiser la gestion de la mémoire, réduisant ainsi le risque de [[MemoryLeak|fuites de mémoire]], [[UseAfterFree|utilisations après libération]] et [[DoubleFree|doubles libérations]].
*   **[[AddressSpaceLayoutRandomization|ASLR]] (Address Space Layout Randomization)** : Une [[SecurityControl|mesure de sécurité]] qui randomise les emplacements mémoire des zones clés d'un [[Process|processus]] (y compris le tas), rendant plus difficile pour les [[ThreatActor|attaquants]] de prédire les adresses et de cibler des zones spécifiques pour l'[[Exploitation|exploitation]].
*   **[[DataExecutionPrevention|DEP]] (Data Execution Prevention) / [[NoExecuteBit|NX bit]]** : Technologies qui marquent certaines zones de mémoire (y compris le tas) comme non-exécutables, empêchant l'[[Exploitation|exécution]] de code à partir de ces régions. Cela permet de contrer les [[HeapSpray|attaques de pulvérisation de tas]] et d'autres techniques d'[[Exploitation|exploitation]].
*   **[[StackCanary|Stack Canary]]** : Bien que principalement pour la [[Stack|pile]], certains principes s'appliquent pour la détection de corruption avant qu'elle ne soit utilisée pour détourner le flux d'exécution.
*   **Utilisation de bibliothèques et de gestionnaires de tas sécurisés** : Recourir à des implémentations de gestionnaires de tas qui intègrent des protections et des vérifications supplémentaires pour détecter et atténuer les [[MemoryCorruption|vulnérabilités de corruption de mémoire]].

## 🔗 Notes Connexes
*   [[Stack|Pile (Stack)]]
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[MemoryCorruption|Corruption de mémoire]]
*   [[BufferOverflow|Dépassement de tampon]]
*   [[MemorySafety|Sécurité Mémoire]]
*   [[Programming|Programmation]]
*   [[Vulnerability|Vulnérabilité]]