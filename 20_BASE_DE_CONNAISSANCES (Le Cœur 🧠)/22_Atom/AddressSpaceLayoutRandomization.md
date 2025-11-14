---
tags:
  - adressage/aleatoire
  - protection/memoire
  - exploit/contournement
  - securite/aslr
  - depassement-tampon
  - securite/corruption-memoire
aliases:
  - Randomisation de l'Espace d'Adressage
  - Aléatorisation de l'Espace d'Adressage
  - ASLR
  - Address Space Layout Randomization
source:
  - null
cssclasses:
  - max
---

# Randomisation de l'Espace d'Adressage (ASLR)

## 📥 Définition en une phrase
> L'[[AddressSpaceLayoutRandomization|ASLR]] est une technique de sécurité informatique qui consiste à randomiser l'emplacement des zones de mémoire importantes (pile, tas, bibliothèques partagées) dans l'espace d'adressage d'un processus pour rendre les attaques par exploitation de mémoire plus difficiles à réaliser.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif Principal** : Empêcher les attaquants de prédire l'emplacement d'adresses mémoire spécifiques (par exemple, des fonctions système ou des données de l'utilisateur) qui sont essentielles pour exécuter des exploits comme les [[BufferOverflow|dépassements de tampon]] ou les [[ReturnOrientedProgramming|attaques ROP]].
*   **Mécanisme** : Au démarrage d'un programme, le système d'exploitation attribue aléatoirement des adresses de base pour la pile, le tas et les bibliothèques partagées (`libc`). Cela signifie que l'agencement mémoire change à chaque exécution du programme.
*   **Entropie** : L'efficacité de l'[[AddressSpaceLayoutRandomization|ASLR]] dépend de la quantité d'aléatoire (entropie) utilisée pour les adresses. Une plus grande entropie rend la prédiction plus difficile et le "brute-forcing" plus long.
*   **Types de segments randomisés** :
    *   **Pile (Stack)** : L'emplacement de la pile du programme.
    *   **Tas (Heap)** : L'emplacement du tas dynamique.
    *   **Bibliothèques partagées (Libraries)** : L'emplacement des bibliothèques dynamiquement liées (ex: `libc.so`).
    *   **Exécutable principal** : Moins courant, mais le binaire lui-même peut aussi être randomisé.
*   **Limitation** : L'[[AddressSpaceLayoutRandomization|ASLR]] n'élimine pas les [[Vulnerability|vulnérabilités]] d'exploitation de mémoire, mais augmente considérablement la difficulté de les exploiter en transformant les exploits fiables en exploits non fiables qui nécessitent généralement des tentatives multiples ou une [[InformationDisclosure|divulgation d'informations]] préalable.

## 🛡️ Risques / Menaces Associés
*   [[MemoryExploitation|Exploitation de Mémoire]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[ReturnOrientedProgramming|Attaques ROP]]
*   [[InformationDisclosure|Divulgation d'informations]] (peut être utilisée pour contourner l'ASLR)
*   [[HeapSpray|Attaque par "Heap Spray"]] (peut être combinée avec d'autres techniques pour contourner l'ASLR)

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Activation par défaut** : S'assurer que l'[[AddressSpaceLayoutRandomization|ASLR]] est activée sur les systèmes d'exploitation (généralement le cas sur les systèmes modernes).
*   **Combiner avec d'autres protections** : L'[[AddressSpaceLayoutRandomization|ASLR]] est plus efficace lorsqu'elle est combinée avec d'autres mécanismes de protection comme la [[DataExecutionPrevention|prévention de l'exécution des données (DEP)]] et les [[StackCanary|Stack Canaries]].
*   [[SecureCodingPractices|Pratiques de codage sécurisées]] : Réduire les [[Vulnerability|vulnérabilités]] sous-jacentes d'exploitation de mémoire par des pratiques de développement robustes.

## 🔗 Notes Connexes
*   [[OperatingSystemSecurity|Sécurité du Système d'Exploitation]]
*   [[Exploit|Exploit]]
*   [[Vulnerability|Vulnérabilité]]
*   [[SecurityControl|Contrôle de Sécurité]]