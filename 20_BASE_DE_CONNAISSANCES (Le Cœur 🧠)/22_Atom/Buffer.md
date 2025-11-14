---
tags:
  - gestion-memoire/tampon
  - stockage/temporaire-donnees
  - systeme/synchronisation-donnees
  - depassement-tampon
  - impact/execution-code-distance
  - securite/aslr
aliases:
  - Tampon
  - Mémoire tampon
source:
  - null
cssclasses:
  - max
---

# Buffer (Tampon)

## 📥 Définition en une phrase
> Une zone de mémoire temporaire utilisée pour stocker des données en transit, compenser des différences de vitesse entre composants, ou accumuler des informations avant leur traitement ou transmission.

## 🧠 Concepts Clés / Fonctionnement
*   Un buffer est une région physique ou virtuelle de la [[MemoryManagement|mémoire vive]] (RAM) allouée temporairement pour la conservation de données.
*   Il sert de point de collecte ou de dépose pour les données, facilitant la communication et la synchronisation entre des processus ou des périphériques opérant à des vitesses différentes.
*   Les buffers peuvent être de taille fixe, déterminée lors de leur création, ou de taille dynamique, s'adaptant aux besoins en données.
*   Ils sont couramment utilisés dans les opérations d'entrée/sortie (I/O), la mise en cache, la diffusion en continu (streaming) de médias, et la gestion du trafic réseau.
*   Dans la programmation, les variables de type tableau ou les allocations de mémoire dynamique sont souvent utilisées comme buffers.

## 🛡️ Risques / Menaces Associés
*   [[BufferOverflow|Débordement de tampon]] : Une vulnérabilité critique où un programme tente d'écrire plus de données dans un buffer qu'il ne peut en contenir, écrasant les données adjacentes en mémoire.
*   [[RemoteCodeExecution|Exécution de code à distance]] (RCE) : Souvent la conséquence d'un débordement de tampon exploité qui permet à un attaquant d'injecter et d'exécuter son propre code malveillant.
*   [[DenialOfService|Déni de service]] (DoS) : Des attaques peuvent saturer ou corrompre les buffers, provoquant des pannes de système ou d'application.
*   [[InformationDisclosure|Divulgation d'informations]] : Des [[SensitiveData|données sensibles]] résiduelles dans un buffer peuvent être lues accidentellement ou malicieusement.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecureCodingPractices|Pratiques de codage sécurisé]] : Utiliser des fonctions et bibliothèques qui effectuent des vérifications de limites (ex: `strncpy_s` au lieu de `strcpy` en C/C++).
*   [[InputValidation|Validation des entrées]] : S'assurer que toutes les données entrantes respectent les tailles et formats attendus avant d'être écrites dans un buffer.
*   [[AddressSpaceLayoutRandomization|ASLR]] : Une technique de sécurité qui randomise l'emplacement des zones de mémoire clés pour rendre les exploits de débordement de tampon plus difficiles.
*   [[DataExecutionPrevention|DEP]] : Marque des zones de mémoire comme non exécutables, empêchant l'exécution de code à partir de zones prévues pour les données (y compris les buffers).
*   [[StackCanary|Stack Canaries]] : Valeurs sentinelles placées sur la [[Stack|pile]] avant les buffers pour détecter les débordements avant qu'ils ne puissent être exploités.
*   [[StaticCodeAnalysis|Analyse statique de code]] et [[DynamicApplicationSecurityTesting|Tests de sécurité dynamiques]] (DAST) : Pour identifier les vulnérabilités liées aux buffers avant le déploiement.

## 🔗 Notes Connexes
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[Stack|Pile (Mémoire)]]
*   [[Heap|Tas (Mémoire)]]
*   [[Exploit|Exploit]]
*   [[Vulnerability|Vulnérabilité]]