---
tags:
  - concept/general
  - securite/memoire
  - methode/securite
  - protection/buffer-overflow
  - securite/systeme
  - a-completer
aliases:
  - Stack Canary
  - Canari de Pile
archetype: concept-general
source:
  -
cssclasses:
  - max
---

# Stack Canary (Canari de Pile)

## 📥 Définition en une phrase
> Un mécanisme de [[Security|sécurité]] utilisé pour détecter et prévenir les [[BufferOverflow|dépassements de tampon]] sur la [[Stack|pile]] en insérant une valeur sentinelle ("canary") entre les variables locales d'une fonction et son adresse de retour.

## 🧠 Concepts Clés / Piliers
*   **Insertion du Canari**: Une valeur secrète, souvent [[PseudoRandomNumberGeneration|générée de manière pseudo-aléatoire]], est placée sur la [[Stack|pile]] juste avant l'adresse de retour de la fonction. Son emplacement stratégique vise à protéger les données critiques du flux d'exécution.
*   **Vérification de l'[[Integrity|Intégrité]]**: Avant que la fonction ne retourne le contrôle à l'appelant, le [[OperatingSystem|système d'exploitation]] ou le [[Software|compilateur]] insère une instruction pour vérifier si la valeur du canari est restée inchangée. Cette vérification agit comme un [[SecurityControl|contrôle de sécurité]] indispensable avant une opération critique.
*   **Détection d'[[Attack|Attaque]]**: Si la valeur du canari a été modifiée, cela indique qu'un [[BufferOverflow|dépassement de tampon]] s'est produit, généralement dans le but d'écraser l'adresse de retour. Dans ce cas, le [[Software|programme]] déclenche une erreur fatale et se termine de manière anormale pour prévenir l'[[Exploitation|exploitation]] de la [[Vulnerability|vulnérabilité]] et l'[[RemoteCodeExecution|exécution de code à distance]].
*   **Types de Canaris**:
    *   **Terminator Canaries**: Utilisent des octets spécifiques (par exemple, `0x00`, `0x0A`, `0x0D`, `0xFF`) qui peuvent être difficiles à écraser avec certaines fonctions de manipulation de chaînes (comme `strcpy` qui s'arrête au `0x00`).
    *   **Random Canaries**: La valeur du canari est générée [[PseudoRandomNumberGeneration|aléatoirement]] au démarrage du [[Software|programme]] ou du [[OperatingSystem|système]], rendant sa prédiction difficile pour un [[ThreatActor|attaquant]].
    *   **XOR Canaries**: La valeur du canari est XORée avec l'adresse de retour ou d'autres informations importantes sur la [[Stack|pile]]. Cela rend sa falsification plus complexe car l'[[ThreatActor|attaquant]] devrait deviner à la fois la valeur du canari et les données utilisées pour le XOR.

## 💡 Importance en Cybersécurité
> Le [[StackCanary|canari de pile]] est un [[SecurityControl|mécanisme de sécurité]] fondamental dans le domaine de la [[MemorySafety|sécurité mémoire]]. Il permet de détecter efficacement les tentatives d'[[Exploitation|exploitation]] des [[BufferOverflow|dépassements de tampon]], qui représentent une [[Vulnerability|vulnérabilité]] persistante et courante pouvant entraîner la [[MemoryCorruption|corruption de mémoire]] et, ultimement, l'[[RemoteCodeExecution|exécution de code à distance]]. En forçant le [[Process|programme]] à s'interrompre avant qu'une [[Attack|attaque]] ne puisse manipuler l'adresse de retour pour détourner le flux d'exécution, les canaris de pile renforcent considérablement l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[System|systèmes]].

## 🔗 Notes Connexes
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[Stack|Pile]]
*   [[MemorySafety|Sécurité Mémoire]]
*   [[NoExecuteBit|Bit No-Execute (NX Bit)]]
*   [[AddressSpaceLayoutRandomization|Address Space Layout Randomization (ASLR)]]
*   [[Exploitation|Exploitation]]
*   [[RemoteCodeExecution|Exécution de Code à Distance (RCE)]]
*   [[Integrity|Intégrité]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La note pourrait être complétée par des exemples de code simples (en C/C++) montrant l'insertion et la vérification d'un canari pour une meilleure compréhension pratique.
*   Des détails supplémentaires sur les techniques de contournement du [[StackCanary|canari de pile]] (par exemple, attaque par force brute sur les canaris aléatoires, contournement des canaris terminator) seraient pertinents pour une perspective d'[[AttackSurface|surface d'attaque]].
*   Ajouter des informations sur les [[Software|compilateurs]] et [[OperatingSystem|systèmes d'exploitation]] qui implémentent cette protection par défaut.