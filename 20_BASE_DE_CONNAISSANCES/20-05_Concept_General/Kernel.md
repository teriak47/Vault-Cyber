---
tags:
  - noyau
  - systeme/exploitation
  - logiciel/systeme-exploitation
  - composant/systeme
  - securite/systeme
aliases:
  - Noyau (système d'exploitation)
  - OS Kernel
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Noyau (Kernel)

## 📥 Définition en une phrase
> Le noyau est le programme central d'un système d'exploitation qui gère les ressources du matériel informatique et les intergiciels (middleware), servant de pont entre les applications logicielles et le traitement réel des données au niveau du matériel.

## 🧠 Concepts Clés / Piliers
*   **Gestion des Processus**: Le noyau est responsable de l'ordonnancement et de l'exécution des processus, allouant du temps processeur à chaque tâche et gérant les transitions d'état des processus (démarrage, arrêt, suspension).
*   **Gestion de la Mémoire**: Il attribue et protège les zones de mémoire pour les processus et le système d'exploitation lui-même, en s'assurant qu'aucun processus n'accède à la mémoire d'un autre sans autorisation.
*   **Gestion des Périphériques (Drivers)**: Le noyau interagit avec les différents périphériques matériels (clavier, souris, disque dur, carte réseau) via des pilotes (drivers), facilitant la communication entre le logiciel et le matériel.
*   **Appels Système (System Calls)**: Les applications logicielles utilisent des appels système pour demander des services au noyau, comme la lecture ou l'écriture de données sur un fichier, l'accès au réseau ou la création de nouveaux processus.

## 💡 Importance en Cybersécurité
> Le noyau est le cœur de la sécurité d'un système, car il est le premier point de défense contre les attaques et la dernière ligne de contrôle des ressources. Toute vulnérabilité dans le noyau peut mener à une compromission totale du système, permettant des escalades de privilèges ou l'installation de rootkits qui dissimulent leur présence. La robustesse et l'intégrité du noyau sont donc fondamentales pour la confidentialité, l'intégrité et la disponibilité des données et des services.

## 🔗 Notes Connexes
*   **Concept parent**: Système d'exploitation
*   **Fonction essentielle**: Gestion de la mémoire
*   **Menace majeure**: Kit de racines
*   **Stratégie d'attaque**: Escalade de Privilèges