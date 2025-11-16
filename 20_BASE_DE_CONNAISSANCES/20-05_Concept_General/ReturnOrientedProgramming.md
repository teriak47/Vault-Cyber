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
> La [[ReturnOrientedProgramming|Programmation Orientée Retour]] (ROP) est une technique d'[[Exploitation|exploitation]] avancée qui permet à un [[ThreatActor|attaquant]] d'exécuter du [[RemoteCodeExecution|code arbitraire]] en chaînant de courtes séquences d'instructions (appelées [[Gadget|gadgets]]) déjà présentes dans la [[MemoryCorruption|mémoire]] d'un [[System|programme]], afin de [[BypassSecurityControl|contourner des protections]] telles que la [[DataExecutionPrevention|Prévention d'Exécution des Données (DEP)]].

## 🧠 Concepts Clés / Piliers
*   **[[Gadget|Gadgets]]**: Ce sont de petites séquences d'instructions [[MachineLanguage|machine]], généralement de quelques octets, qui se terminent par une instruction de retour (`ret`). Ces [[Gadget|gadgets]] sont extraits du [[Software|code exécutable]] existant (par exemple, des [[SoftwareLibrary|bibliothèques logicielles]] ou le [[BinaryDigit|binaire]] principal du [[Process|programme]]).
*   **Chaînes ROP (ROP Chains)**: L'[[ThreatActor|attaquant]] construit une "chaîne" d'adresses de [[Gadget|gadgets]] sur la [[Stack|pile]] d'[[Process|exécution]] du [[System|programme]]. Lorsqu'une [[Vulnerability|vulnérabilité]] de [[MemoryCorruption|corruption de mémoire]] (comme un [[BufferOverflow|dépassement de tampon]]) détourne le flux d'[[Exploitation|exécution]] vers le début de cette chaîne, chaque instruction `ret` à la fin d'un [[Gadget|gadget]] redirige l'[[Exploitation|exécution]] vers le [[Gadget|gadget]] suivant dont l'adresse est sur la [[Stack|pile]].
*   **Contournement de Protections**: La [[ReturnOrientedProgramming|ROP]] est principalement utilisée pour [[BypassSecurityControl|contourner des protections]] d'exécution de [[Software|code]] telles que la [[DataExecutionPrevention|Prévention d'Exécution des Données (DEP)]] (qui empêche l'exécution de [[Software|code]] depuis la [[Stack|pile]] ou le [[Heap|tas]]) et rendre plus difficile l'[[AddressSpaceLayoutRandomization|ASLR]] (qui randomise les adresses mémoire) en n'[[Shellcode|injectant pas de nouveau code]] mais en réutilisant l'existant.

## 💡 Importance en Cybersécurité
> La [[ReturnOrientedProgramming|Programmation Orientée Retour]] est cruciale en [[Cybersecurity|cybersécurité]] car elle représente une technique d'[[Exploitation|exploitation]] sophistiquée capable de [[BypassSecurityControl|contourner des mesures de sécurité]] fondamentales comme la [[DataExecutionPrevention|Prévention d'Exécution des Données (DEP)]] et l'[[AddressSpaceLayoutRandomization|ASLR]]. Sa compréhension est essentielle pour les [[RedTeam|équipes rouges]] qui l'utilisent pour évaluer les [[AttackSurface|surfaces d'attaque]] et pour les [[BlueTeam|équipes bleues]] afin de développer des [[ExploitMitigation|contres-mesures robustes]]. Elle met en lumière la nécessité d'une [[MemorySafety|sécurité mémoire]] rigoureuse et de [[CompilerHardening|renforcements du compilateur]] pour prévenir les [[Vulnerability|vulnérabilités]] de [[MemoryCorruption|corruption de mémoire]] initiales qui rendent les [[ReturnOrientedProgramming|attaques ROP]] possibles.

## 🔗 Notes Connexes
*   [[BufferOverflow|Dépassement de tampon]]
*   [[Exploitation|Exploitation]]
*   [[DataExecutionPrevention|Prévention d'Exécution des Données (DEP)]]
*   [[AddressSpaceLayoutRandomization|Randomisation de l'Espace d'Adressage (ASLR)]]
*   [[StackCanary|Stack Canaries]]
*   [[Shellcode|Shellcode]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   [[DataExfiltration|Exfiltration de données]]
*   [[MemoryCorruption|Corruption de mémoire]]
*   [[Vulnerability|Vulnérabilité]]
*   [[BypassSecurityControl|Contournement de contrôle de sécurité]]
*   [[ExploitMitigation|Atténuation d'exploit]]
*   [[CompilerHardening|Renforcement du compilateur]]
*   [[Gadget|Gadget]]