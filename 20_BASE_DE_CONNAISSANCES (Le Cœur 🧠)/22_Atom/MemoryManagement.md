---
tags:
  - systeme/gestion-memoire
  - gestion-memoire/fuite
  - architecture/memoire-virtuelle
  - gestion-memoire/automatique
  - depassement-tampon
  - securite/aslr
aliases:
  - Gestion de la mémoire
  - Memory Management
source:
  - null
cssclasses:
  - max
---

# Gestion de la Mémoire

## 📥 Définition en une phrase
> La gestion de la mémoire est un processus fondamental dans les systèmes informatiques et les applications, chargé d'allouer et de libérer efficacement la mémoire vive (RAM) pour les programmes en cours d'exécution.

## 🧠 Concepts Clés / Fonctionnement
*   **Allocation de Mémoire :** Processus par lequel le système d'exploitation ou un programme réserve un bloc de mémoire pour une tâche spécifique.
*   **Désallocation de Mémoire :** Processus de libération d'un bloc de mémoire qui n'est plus utilisé, le rendant disponible pour d'autres programmes.
*   **Mémoire Virtuelle :** Technique permettant aux programmes d'accéder à plus de mémoire qu'il n'y en a de physiquement disponible, en utilisant un espace de stockage secondaire (ex: disque dur) comme extension de la RAM.
*   **Pagining (Pagination) :** Méthode de gestion de la mémoire virtuelle où la mémoire physique et virtuelle est divisée en blocs de taille fixe appelés pages.
*   **Segmentation :** Autre méthode où la mémoire est divisée en segments logiques de taille variable, correspondant aux sections de code, données, ou pile d'un programme.
*   **Garbage Collection (Récupération de Place) :** Mécanisme automatique dans certains langages de programmation (Java, Python) qui identifie et libère la mémoire qui n'est plus référencée.

## 🛡️ Risques / Menaces Associés
*   [[BufferOverflow|Dépassement de Tampon]] : Une vulnérabilité où un programme écrit des données au-delà des limites d'un tampon mémoire, écrasant les données adjacentes.
*   [[MemoryLeak|Fuite de Mémoire]] : Une situation où un programme ne libère pas la mémoire qu'il a allouée mais n'utilise plus, entraînant une consommation excessive et potentiellement un crash.
*   [[UseAfterFree|Utilisation Après Libération]] : Une vulnérabilité critique où un programme tente d'accéder à une portion de mémoire qui a déjà été libérée, pouvant mener à une corruption de données ou à l'exécution de code arbitraire.
*   [[DoubleFree|Double Libération]] : Une vulnérabilité où un programme tente de libérer deux fois la même portion de mémoire, pouvant corrompre le tas et entraîner des exploitations.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecureCoding|Développement Sécurisé]] : Appliquer des pratiques de codage sûres pour prévenir les vulnérabilités liées à la mémoire (ex: vérification des limites, initialisation des pointeurs).
*   [[MemorySafetyLanguage|Langages à Sûreté Mémoire]] : Utiliser des langages de programmation (ex: Rust) qui imposent des règles strictes sur la gestion de la mémoire, réduisant les erreurs courantes.
*   [[AddressSpaceLayoutRandomization|ASLR]] : Une technique de sécurité qui randomise l'emplacement des zones de mémoire clés pour rendre les exploits plus difficiles.
*   [[DataExecutionPrevention|DEP]] : Une fonctionnalité de sécurité qui marque certaines zones de mémoire comme non exécutables pour empêcher l'exécution de code malveillant à partir de ces zones.

## 🔗 Notes Connexes
*   [[OperatingSystem|Système d'Exploitation]]
*   [[ProgrammingLanguage|Langage de Programmation]]
*   [[ProcessManagement|Gestion des Processus]]
*   [[Virtualization|Virtualisation]]