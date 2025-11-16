---
aliases:
  - Randomisation de l'Espace d'Adressage
  - Aléatorisation de l'Espace d'Adressage
  - ASLR
  - Address Space Layout Randomization
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Randomisation de l'Espace d'Adressage (ASLR)

## 📥 Définition en une phrase
> L'[[AddressSpaceLayoutRandomization|ASLR]] (Address Space Layout Randomization) est une technique de [[Security|sécurité]] informatique qui vise à randomiser l'emplacement des zones de [[MemoryManagement|mémoire]] importantes (comme la [[Stack|pile]], le [[Heap|tas]] et les bibliothèques partagées) dans l'[[AddressSpace|espace d'adressage]] d'un [[Process|processus]], rendant ainsi plus difficile l'[[Exploitation|exploitation]] de [[SoftwareVulnerability|vulnérabilités logicielles]] liées à la [[MemoryCorruption|corruption de mémoire]].

## 🧠 Concepts Clés / Piliers
*   **Objectif**: L'[[AddressSpaceLayoutRandomization|ASLR]] est conçue pour empêcher les [[ThreatActor|attaquants]] de prédire l'emplacement d'adresses [[Memory|mémoire]] spécifiques, cruciales pour réaliser des [[Exploit|exploits]] comme les [[BufferOverflow|dépassements de tampon]] ou les [[ReturnOrientedProgramming|attaques ROP]].
*   **Mécanisme d'Aléatorisation**: Au démarrage d'un [[SoftwareApplication|programme]], le [[OperatingSystem|système d'exploitation]] attribue aléatoirement des adresses de base pour des segments de [[MemoryManagement|mémoire]] clés (la [[Stack|pile]], le [[Heap|tas]], les [[DynamicLinkLibraries|bibliothèques dynamiquement liées]], etc.), modifiant l'agencement [[Memory|mémoire]] à chaque exécution et rendant la prédiction des adresses difficile.
*   **[[Entropy|Entropie]]**: L'efficacité de l'[[AddressSpaceLayoutRandomization|ASLR]] est directement liée à la quantité d'[[Entropy|aléatoire]] (entropie) utilisée pour les adresses. Une plus grande [[Entropy|entropie]] augmente le temps et la complexité nécessaires pour réussir une [[BruteForceAttack|attaque par force brute]] sur les adresses [[Memory|mémoire]].
*   **Segments de Mémoire Concernés**: Les zones typiquement randomisées incluent la [[Stack|pile]] (pour les variables locales et les appels de fonctions), le [[Heap|tas]] (pour la mémoire allouée dynamiquement) et les [[DynamicLinkLibraries|bibliothèques dynamiquement liées]] (telles que `libc`). Le binaire exécutable lui-même peut aussi être randomisé.
*   **Limitations**: Bien que l'[[AddressSpaceLayoutRandomization|ASLR]] augmente considérablement la difficulté d'[[Exploitation|exploitation]], elle n'élimine pas les [[SoftwareVulnerability|vulnérabilités]] sous-jacentes. Elle peut être contournée par des techniques comme la [[InformationDisclosure|divulgation d'informations]] ou combinée avec des [[HeapSpray|attaques par "Heap Spray"]].

## 💡 Importance en Cybersécurité
> L'[[AddressSpaceLayoutRandomization|ASLR]] est un [[SecurityControl|contrôle de sécurité]] fondamental qui joue un rôle essentiel dans la [[MemorySafety|sécurité mémoire]] moderne. En introduisant de l'imprévisibilité dans l'[[AddressSpace|espace d'adressage]] des [[Process|processus]], elle élève considérablement la barre pour les [[ThreatActor|attaquants]] tentant d'exécuter du [[Shellcode|code malveillant]] ou de détourner le flux d'exécution d'un [[SoftwareApplication|programme]], transformant des [[Exploit|exploits]] autrefois fiables en opérations coûteuses et souvent infructueuses sans informations supplémentaires.

## 🔗 Notes Connexes
*   [[MemoryCorruption|Corruption de mémoire]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[ReturnOrientedProgramming|Programmation Orientée Retour (ROP)]]
*   [[DataExecutionPrevention|Prévention de l'exécution des données (DEP)]]
*   [[StackCanary|Stack Canary]]
*   [[Exploit|Exploit]]
*   [[Vulnerability|Vulnérabilité]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[OperatingSystemSecurity|Sécurité du Système d'Exploitation]]
*   [[SecureCodingPractices|Pratiques de codage sécurisées]]
*   [[InformationDisclosure|Divulgation d'informations]]
*   [[MemoryExploitation|Exploitation de Mémoire]]
*   [[HeapSpray|Heap Spray]]