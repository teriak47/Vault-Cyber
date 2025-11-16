---
tags:
  - materiel
aliases:
  - Bit No-Execute
  - Bit d'exécution désactivée
  - No-Execute Bit
  - NX Bit
  - XD Bit
  - EVP
archetype: materiel
source:
cssclasses:
  - max
---

# Bit No-Execute (NX Bit)

## 🎯 Rôle et Fonction
> Le [[NoExecuteBit|Bit No-Execute]] (NX bit) est une fonctionnalité de [[Hardware|sécurité matérielle]] intégrée au [[Computer|processeur]] qui marque des zones spécifiques de la [[Heap|mémoire]] comme non-exécutables. Son rôle est de prévenir l'exécution de [[Malware|code malveillant]] ou non autorisé à partir de ces emplacements, renforçant ainsi la [[MemorySafety|sécurité mémoire]] du [[System|système]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Fonctionnalité de [[Security|sécurité]] matérielle du [[Computer|processeur]], également connue sous le nom de XD Bit (Intel) ou EVP (AMD).
*   **Connectique**: N/A (implémenté au niveau de l'unité de gestion de [[MemoryManagement|mémoire]] (MMU) du [[Computer|processeur]]).
*   **Performances**: Introduit un overhead minime pour une protection substantielle contre certains types d'[[Exploitation|exploits]].
*   **Normes associées**: S'appuie sur l'architecture des [[Computer|processeurs]] modernes et est pris en charge par la plupart des [[OperatingSystem|systèmes d'exploitation]] (par exemple, [[DataExecutionPrevention|DEP]] sous [[Windows|Windows]], intégration au noyau [[Linux|Linux]]).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Renforce considérablement la [[MemorySafety|sécurité mémoire]] en empêchant les [[Attack|attaques]] où du [[Shellcode|code malveillant]] est injecté dans des zones de [[Data|données]] (comme la [[Stack|pile]] ou le [[Heap|tas]]).
    *   Atténue les risques liés aux [[BufferOverflow|dépassements de tampon]].
    *   Implémentation matérielle pour une efficacité et une performance élevées.
*   **Inconvénients**:
    *   Ne protège pas contre toutes les formes d'[[Exploitation|exploitation de mémoire]], notamment les [[ReturnOrientedProgramming|attaques de ROP (Return-Oriented Programming)]] qui manipulent le flux d'exécution sans exécuter de nouveau [[Shellcode|code]].
    *   Nécessite le support et l'activation au niveau du [[Firmware|micrologiciel]] (BIOS/UEFI) et du [[OperatingSystem|système d'exploitation]].

## 🔒 Considérations de Sécurité Physique
*   En tant que caractéristique matérielle intégrée au [[Computer|processeur]], le [[NoExecuteBit|NX bit]] contribue à la [[PhysicalSecurity|sécurité physique]] du [[System|système]] en assurant que le [[Hardware|matériel]] exécute uniquement le [[Software|logiciel]] autorisé et prévu.
*   Son bon fonctionnement dépend de la [[Security|sécurité]] du [[Firmware|micrologiciel]] et de sa configuration, qui peuvent être sujets à des [[Vulnerability|vulnérabilités]] si non protégés physiquement.

## 🔗 Notes Connexes
*   [[DataExecutionPrevention|Data Execution Prevention (DEP)]]
*   [[AddressSpaceLayoutRandomization|Address Space Layout Randomization (ASLR)]]
*   [[MemorySafety|Sécurité mémoire]]
*   [[StackCanary|Stack Canary]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[ReturnOrientedProgramming|Return-Oriented Programming (ROP)]]
*   [[OperatingSystem|Système d'exploitation]]
*   [[Computer|Processeur]]