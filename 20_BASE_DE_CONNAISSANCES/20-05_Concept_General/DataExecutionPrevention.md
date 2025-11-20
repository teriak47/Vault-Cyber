---
tags:
aliases:
  - DEP
  - Prévention de l'exécution des données
  - Data Execution Prevention
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Prévention de l'exécution des données (DEP)

## 📥 Définition en une phrase
> La Prévention de l'exécution des données (DEP) est une fonctionnalité de sécurité d'un système d'exploitation qui marque des zones spécifiques de la mémoire comme non-exécutables afin d'empêcher l'exécution de code malveillant à partir de ces emplacements.

## 🧠 Concepts Clés / Piliers
*   **Marquage de la Mémoire Non-Exécutable**: Le système d'exploitation et le matériel collaborent pour désigner des régions de la mémoire (telles que la pile et le tas) comme destinées uniquement aux données, interdisant ainsi toute tentative d'exécution de code à partir de celles-ci.
*   **Bit NX/XD**: Les processeurs modernes intègrent un bit spécifique (le "NX bit" pour AMD, "XD bit" pour Intel) dans leurs tables de pages mémoire. Ce bit permet au système d'exploitation de désigner des pages mémoire comme non-exécutables, déclenchant une exception matérielle si une instruction y est détectée.
*   **Protection Contre l'Injection de Code**: Le principe fondamental de la DEP est de bloquer l'exécution de code injecté dans des zones de mémoire prévues pour les données, comme celles ciblées par les dépassements de tampon.

## 💡 Importance en Cybersécurité
> La DEP est un contrôle de sécurité fondamental qui renforce la sécurité du système en rendant plus difficile pour les logiciels malveillants et les exploits (notamment ceux liés aux dépassements de tampon et à l'injection de code) de s'exécuter et de prendre le contrôle d'un processus ou du système.

## 🔗 Notes Connexes
*   ASLR
*   Dépassement de Tampon
*   Injection de Code
*   Atténuation des Exploits
*   Corruption de mémoire
*   Bit No-Execute
*   Système d'exploitation
*   ROP
*   Stack Canary
*   Stack Smashing