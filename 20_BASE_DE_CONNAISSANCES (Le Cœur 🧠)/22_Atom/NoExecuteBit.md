---
tags:
  - protection-memoire
  - processeur/nx-bit
  - systeme/execution-code
  - depassement-tampon
  - securite/materielle
  - securite/prevention-execution-donnees
aliases:
  - Bit No-Execute
  - Bit d'exécution désactivée
  - No-Execute Bit
  - NX Bit
  - XD Bit
  - EVP
source:
  - null
cssclasses:
  - max
---

# Bit No-Execute (NX Bit)

## 📥 Définition en une phrase
> Le bit No-Execute (NX bit), également connu sous le nom de XD Bit chez Intel ou EVP chez AMD, est une fonctionnalité de sécurité matérielle du processeur qui marque certaines zones de la mémoire d'un ordinateur comme non-exécutables, empêchant ainsi l'exécution de code malveillant à partir de ces emplacements.

## 🧠 Concepts Clés / Fonctionnement
*   **Protection Matérielle** : Implémenté directement au niveau du processeur et de l'unité de gestion de mémoire (MMU), il ajoute un bit aux entrées de la table de pages de la mémoire pour indiquer si une page mémoire est exécutable ou non.
*   **Prévention des Dépassements de Tampon** : Sa fonction principale est de contrer les attaques par [[BufferOverflow|dépassement de tampon]] (buffer overflow) qui tentent d'injecter et d'exécuter du code malveillant dans des zones de mémoire censées contenir uniquement des données (comme la pile ou le tas).
*   **Interaction avec le Système d'Exploitation** : Le [[OperatingSystem|système d'exploitation]] doit prendre en charge et activer le NX bit. Sous Windows, cela est connu sous le nom de [[DataExecutionPrevention|Data Execution Prevention (DEP)]]. Sous Linux, le support est intégré dans le noyau.
*   **Fonctionnement** : Lorsqu'un programme tente d'exécuter du code à partir d'une page mémoire marquée comme non-exécutable, le processeur génère une exception, généralement une erreur de violation d'accès, stoppant ainsi le processus.

## 🛡️ Risques / Menaces Associés
*   [[BufferOverflow|Dépassement de tampon]]
*   [[Malware|Logiciels malveillants]] (spécifiquement ceux qui utilisent l'injection de code dans des zones de données)
*   [[ReturnOrientedProgramming|Attaques de ROP (Return-Oriented Programming)]] (bien que le NX bit atténue les attaques d'exécution directe, le ROP peut contourner cette protection dans certains scénarios)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SystemHardening|Durcissement du système]] : S'assurer que le NX bit (ou DEP/W^X) est activé et configuré correctement au niveau du BIOS/UEFI et du système d'exploitation.
*   [[PatchManagement|Gestion des correctifs]] : Maintenir le système d'exploitation et les pilotes à jour pour garantir une exploitation optimale du NX bit.
*   [[SecureCoding|Développement sécurisé]] : Bien que le NX bit soit une protection importante, de bonnes pratiques de codage qui évitent les dépassements de tampon restent essentielles.

## 🔗 Notes Connexes
*   [[DataExecutionPrevention|Data Execution Prevention (DEP)]]
*   [[AddressSpaceLayoutRandomization|ASLR]]
*   [[MemorySafety|Sécurité mémoire]]
*   [[StackSmashingProtection|Protection contre l'écrasement de la pile]]