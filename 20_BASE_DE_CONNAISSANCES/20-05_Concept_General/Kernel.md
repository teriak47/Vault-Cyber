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
> Le [[Kernel|noyau]] est le programme central d'un [[OperatingSystem|système d'exploitation]] qui gère les ressources du [[Computer|matériel informatique]] et les intergiciels (middleware), servant de pont entre les applications logicielles et le traitement réel des données au niveau du matériel.

## 🧠 Concepts Clés / Piliers
*   **Gestion des [[Process|Processus]]**: Le [[Kernel|noyau]] est responsable de l'ordonnancement et de l'exécution des [[Process|processus]], allouant du temps processeur à chaque tâche et gérant les transitions d'état des [[Process|processus]] (démarrage, arrêt, suspension).
*   **[[MemoryManagement|Gestion de la Mémoire]]**: Il attribue et protège les zones de [[MemoryManagement|mémoire]] pour les [[Process|processus]] et le [[OperatingSystem|système d'exploitation]] lui-même, en s'assurant qu'aucun [[Process|processus]] n'accède à la [[MemoryManagement|mémoire]] d'un autre sans autorisation.
*   **Gestion des Périphériques (Drivers)**: Le [[Kernel|noyau]] interagit avec les différents [[Device|périphériques]] [[Hardware|matériels]] (clavier, souris, disque dur, [[NetworkInterfaceCard|carte réseau]]) via des pilotes ([[Driver|drivers]]), facilitant la [[Communication|communication]] entre le [[Software|logiciel]] et le [[Hardware|matériel]].
*   **Appels Système (System Calls)**: Les [[SoftwareApplication|applications logicielles]] utilisent des appels système pour demander des services au [[Kernel|noyau]], comme la lecture ou l'écriture de [[Data|données]] sur un [[FileServer|fichier]], l'accès au [[Network|réseau]] ou la création de nouveaux [[Process|processus]].

## 💡 Importance en [[Cybersecurity|Cybersécurité]]
> Le [[Kernel|noyau]] est le cœur de la [[Security|sécurité]] d'un [[System|système]], car il est le premier point de défense contre les [[Attack|attaques]] et la dernière ligne de contrôle des ressources. Toute [[Vulnerability|vulnérabilité]] dans le [[Kernel|noyau]] peut mener à une [[SystemCompromise|compromission totale du système]], permettant des [[PrivilegeEscalation|escalades de privilèges]] ou l'installation de [[Rootkit|rootkits]] qui dissimulent leur présence. La robustesse et l'[[Integrity|intégrité]] du [[Kernel|noyau]] sont donc fondamentales pour la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des [[Data|données]] et des [[Service|services]].

## 🔗 Notes Connexes
*   **Concept parent**: [[OperatingSystem|Système d'exploitation]]
*   **Fonction essentielle**: [[MemoryManagement|Gestion de la mémoire]]
*   **Menace majeure**: [[Rootkit|Kit de racines]]
*   **Stratégie d'attaque**: [[PrivilegeEscalation|Escalade de Privilèges]]