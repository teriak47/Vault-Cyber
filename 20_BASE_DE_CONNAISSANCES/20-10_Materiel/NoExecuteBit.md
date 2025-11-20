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
> Le Bit No-Execute (NX bit) est une fonctionnalité de sécurité matérielle intégrée au processeur qui marque des zones spécifiques de la mémoire comme non-exécutables. Son rôle est de prévenir l'exécution de code malveillant ou non autorisé à partir de ces emplacements, renforçant ainsi la sécurité mémoire du système.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Fonctionnalité de sécurité matérielle du processeur, également connue sous le nom de XD Bit (Intel) ou EVP (AMD).
*   **Connectique**: N/A (implémenté au niveau de l'unité de gestion de mémoire (MMU) du processeur).
*   **Performances**: Introduit un overhead minime pour une protection substantielle contre certains types d'exploits.
*   **Normes associées**: S'appuie sur l'architecture des processeurs modernes et est pris en charge par la plupart des systèmes d'exploitation (par exemple, DEP sous Windows, intégration au noyau Linux).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Renforce considérablement la sécurité mémoire en empêchant les attaques où du code malveillant est injecté dans des zones de données (comme la pile ou le tas).
    *   Atténue les risques liés aux dépassements de tampon.
    *   Implémentation matérielle pour une efficacité et une performance élevées.
*   **Inconvénients**:
    *   Ne protège pas contre toutes les formes d'exploitation de mémoire, notamment les attaques de ROP (Return-Oriented Programming) qui manipulent le flux d'exécution sans exécuter de nouveau code.
    *   Nécessite le support et l'activation au niveau du micrologiciel (BIOS/UEFI) et du système d'exploitation.

## 🔒 Considérations de Sécurité Physique
*   En tant que caractéristique matérielle intégrée au processeur, le NX bit contribue à la sécurité physique du système en assurant que le matériel exécute uniquement le logiciel autorisé et prévu.
*   Son bon fonctionnement dépend de la sécurité du micrologiciel et de sa configuration, qui peuvent être sujets à des vulnérabilités si non protégés physiquement.

## 🔗 Notes Connexes
*   Data Execution Prevention (DEP)
*   Address Space Layout Randomization (ASLR)
*   Sécurité mémoire
*   Stack Canary
*   Dépassement de Tampon
*   Return-Oriented Programming (ROP)
*   Système d'exploitation
*   Processeur