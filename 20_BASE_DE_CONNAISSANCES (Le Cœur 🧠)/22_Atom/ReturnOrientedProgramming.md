---
tags:
  - exploitation/programmation-orientee-retour
  - gadget-rop
  - securite/prevention-execution-donnees
  - cybersécurité/exploitation-vulnerabilite
  - depassement-tampon
  - securite/aslr
aliases:
  - Programmation Orientée Retour
  - ROP
  - Return-Oriented Programming
source:
  - null
cssclasses:
  - max
---

# Programmation Orientée Retour (ROP)

## 📥 Définition en une phrase
> La Programmation Orientée Retour (ROP) est une technique d'exploitation avancée qui permet à un attaquant d'exécuter du code arbitraire en chaînant des séquences d'instructions courtes (gadgets) déjà présentes dans la mémoire d'un programme, contournant ainsi des protections comme la [[DataExecutionPrevention|Prévention d'Exécution des Données (DEP)]].

## 🧠 Concepts Clés / Fonctionnement
*   **Contournement de Protections :** ROP est principalement utilisée pour contourner les protections d'exécution de code telles que [[DataExecutionPrevention|DEP]] et rendre plus difficile l'[[AddressSpaceLayoutRandomization|ASLR]] en n'injectant pas de nouveau code.
*   **Gadgets :** Ce sont de petites séquences d'instructions machine, généralement de quelques octets, se terminant par une instruction de retour (`ret`). Ces gadgets sont extraits du code exécutable existant (bibliothèques partagées, binaire principal).
*   **Chaînes ROP (ROP Chains) :** L'attaquant construit une "chaîne" d'adresses de gadgets sur la pile de l'exécution du programme. Lorsqu'un [[BufferOverflow|dépassement de tampon]] ou une autre [[Vulnerability|vulnérabilité]] de corruption de mémoire détourne le flux d'exécution vers le début de cette chaîne, chaque instruction `ret` à la fin d'un gadget redirige l'exécution vers le gadget suivant sur la pile.
*   **Fonctionnalité Arbitraire :** En orchestrant l'ordre des gadgets, un attaquant peut effectuer des opérations complexes, comme appeler des fonctions de bibliothèque, manipuler des registres ou des arguments, et finalement exécuter des commandes arbitrares.
*   **Diversité des Gadgets :** La richesse des jeux d'instructions modernes et la taille des bibliothèques logicielles garantissent généralement un nombre suffisant de gadgets pour construire des charges utiles variées.

## 🛡️ Risques / Menaces Associés
*   [[CodeExecution|Exécution de code arbitraire]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[DataExfiltration|Exfiltration de données]]
*   [[BypassSecurityControl|Contournement de contrôles de sécurité]] comme DEP et ASLR.
*   [[MemoryCorruption|Corruption de mémoire]] (généralement la cause initiale qui permet la ROP).

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[DataExecutionPrevention|DEP]] :** Rendre la pile et le tas non exécutables pour empêcher l'exécution directe de code injecté (ROP contourne cela, mais reste une première ligne de défense).
*   **[[AddressSpaceLayoutRandomization|ASLR]] :** Randomiser les adresses mémoire des bibliothèques et du code exécutable pour rendre la localisation des gadgets plus difficile.
*   **[[StackCanary|Stack Canaries]] :** Insérer des valeurs aléatoires sur la pile avant les adresses de retour pour détecter les [[BufferOverflow|dépassements de tampon]] avant qu'ils ne puissent détourner le contrôle.
*   **Compiler Hardening :** Utiliser des options de compilation qui renforcent la sécurité, comme la protection contre le débordement de pile (`-fstack-protector`).
*   **[[ExploitMitigation|Mesures d'atténuation des exploits]] :** Utiliser des systèmes de prévention d'intrusion (IPS) ou des modules de sécurité du noyau qui peuvent détecter et bloquer les chaînes ROP ou les comportements anormaux.
*   **Programmation Sécurisée :** Éliminer les [[Vulnerability|vulnérabilités]] de [[MemorySafety|sécurité de la mémoire]] telles que les dépassements de tampon et les erreurs de format string qui sont souvent les vecteurs initiaux pour les attaques ROP.

## 🔗 Notes Connexes
*   [[BufferOverflow|Dépassement de tampon]]
*   [[Exploitation|Exploitation]]
*   [[DataExecutionPrevention|Prévention d'Exécution des Données (DEP)]]
*   [[AddressSpaceLayoutRandomization|Randomisation de l'Espace d'Adresse (ASLR)]]
*   [[StackCanary|Stack Canaries]]
*   [[Shellcode|Shellcode]]