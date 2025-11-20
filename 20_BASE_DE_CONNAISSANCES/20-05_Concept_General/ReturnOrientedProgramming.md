---
tags:
aliases:
  - Programmation Orientée Retour
  - ROP
  - Return-Oriented Programming
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Programmation Orientée Retour (ROP)

## 📥 Définition en une phrase
> La Programmation Orientée Retour (ROP) est une technique d'exploitation avancée qui permet à un attaquant d'exécuter du code arbitraire en chaînant de courtes séquences d'instructions (appelées gadgets) déjà présentes dans la mémoire d'un programme, afin de contourner des protections telles que la Prévention d'Exécution des Données (DEP).

## 🧠 Concepts Clés / Piliers
*   **Gadgets**: Ce sont de petites séquences d'instructions machine, généralement de quelques octets, qui se terminent par une instruction de retour (`ret`). Ces gadgets sont extraits du code exécutable existant (par exemple, des bibliothèques logicielles ou le binaire principal du programme).
*   **Chaînes ROP (ROP Chains)**: L'attaquant construit une "chaîne" d'adresses de gadgets sur la pile d'exécution du programme. Lorsqu'une vulnérabilité de corruption de mémoire (comme un dépassement de tampon) détourne le flux d'exécution vers le début de cette chaîne, chaque instruction `ret` à la fin d'un gadget redirige l'exécution vers le gadget suivant dont l'adresse est sur la pile.
*   **Contournement de Protections**: La ROP est principalement utilisée pour contourner des protections d'exécution de code telles que la Prévention d'Exécution des Données (DEP) (qui empêche l'exécution de code depuis la pile ou le tas) et rendre plus difficile l'ASLR (qui randomise les adresses mémoire) en n'injectant pas de nouveau code mais en réutilisant l'existant.

## 💡 Importance en Cybersécurité
> La Programmation Orientée Retour est cruciale en cybersécurité car elle représente une technique d'exploitation sophistiquée capable de contourner des mesures de sécurité fondamentales comme la Prévention d'Exécution des Données (DEP) et l'ASLR. Sa compréhension est essentielle pour les équipes rouges qui l'utilisent pour évaluer les surfaces d'attaque et pour les équipes bleues afin de développer des contres-mesures robustes. Elle met en lumière la nécessité d'une sécurité mémoire rigoureuse et de renforcements du compilateur pour prévenir les vulnérabilités de corruption de mémoire initiales qui rendent les attaques ROP possibles.

## 🔗 Notes Connexes
*   Dépassement de tampon
*   Exploitation
*   Prévention d'Exécution des Données (DEP)
*   Randomisation de l'Espace d'Adressage (ASLR)
*   Stack Canaries
*   Shellcode
*   Élévation de privilèges
*   Exfiltration de données
*   Corruption de mémoire
*   Vulnérabilité
*   Contournement de contrôle de sécurité
*   Atténuation d'exploit
*   Renforcement du compilateur
*   Gadget