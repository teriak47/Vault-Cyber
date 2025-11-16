---
tags:
aliases:
  - Sécurité Mémoire
  - Memory Safety
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sécurité Mémoire (Memory Safety)

## 📥 Définition en une phrase
> La **sécurité mémoire** désigne l'ensemble des techniques et pratiques visant à prévenir les erreurs d’accès à la [[Memory|mémoire]] qui peuvent entraîner des [[Vulnerability|vulnérabilités]] comme des [[MemoryCorruption|corruptions mémoire]] ou des [[RemoteCodeExecution|exécutions de code arbitraire]].

## 🧠 Concepts Clés / Piliers
*   **Erreurs Fondamentales**: Identification des types d'erreurs d'accès [[Memory|mémoire]] qui compromettent la [[Security|sécurité]], telles que les [[BufferOverflow|débordements de tampon]], les [[UseAfterFree|utilisations après libération]], et les accès hors limites (out-of-bounds access).
*   **Approches Linguistiques**: Distinction entre les [[SafeProgrammingLanguages|langages de programmation sûrs]] (ex: [[Rust|Rust]], [[GoProgrammingLanguage|Go]], [[JavaProgrammingLanguage|Java]]) qui intègrent des mécanismes de [[MemorySafety|sécurité mémoire]] au niveau du [[Compiler|compilateur]] ou de la [[VirtualMachine|machine virtuelle]], et les langages comme C/C++ nécessitant une gestion explicite des pointeurs.
*   **Mécanismes de Défense**: Présentation des [[SecurityControl|contrôles de sécurité]] d'[[Integrity|intégrité mémoire]] tels que les [[StackCanary|canaris de pile]], la [[AddressSpaceLayoutRandomization|randomisation de l'espace d'adressage]] ([[AddressSpaceLayoutRandomization|ASLR]]), et la [[DataExecutionPrevention|prévention de l'exécution des données]] ([[DataExecutionPrevention|DEP]]), ainsi que les techniques de gestion automatique de la [[Memory|mémoire]] (comme le [[GarbageCollection|garbage collector]]).
*   **Outillage et Bonnes Pratiques**: Importance de l'application de [[SecureCoding|pratiques de codage sécurisé]], de l'[[StaticAnalysis|analyse statique]] et [[DynamicAnalysis|dynamique]] du [[CodeReview|code]], ainsi que du [[Fuzzing|fuzzing]] pour identifier et prévenir les [[SoftwareBugs|erreurs logicielles]] et les [[Vulnerability|vulnérabilités]] liées à la [[Memory|mémoire]].

## 💡 Importance en Cybersécurité
> La [[MemorySafety|sécurité mémoire]] est un pilier fondamental de la [[Cybersecurity|cybersécurité]] car les [[Vulnerability|vulnérabilités]] liées à la [[Memory|mémoire]] (comme la [[MemoryCorruption|corruption mémoire]]) sont des [[AttackVector|vecteurs d'attaque]] parmi les plus couramment [[Exploitation|exploités]] par les [[ThreatActor|acteurs de menace]]. Elles permettent souvent des [[RemoteCodeExecution|exécutions de code à distance]] ([[RemoteCodeExecution|RCE]]), des [[PrivilegeEscalation|escalades de privilèges]], ou d'autres formes de [[SystemCompromise|compromission de système]], impactant directement l'[[Integrity|intégrité]], la [[Confidentiality|confidentialité]] et l'[[Availability|disponibilité]] des [[System|systèmes]]. Prévenir ces erreurs est donc essentiel pour construire des [[Software|logiciels]] robustes et sécurisés.

## 🔗 Notes Connexes
*   [[BufferOverflow|Débordement de tampon]]
*   [[UseAfterFree|Usage après libération]]
*   [[MemoryCorruption|Corruption mémoire]]
*   [[RemoteCodeExecution|Exécution de code à distance]]
*   [[PrivilegeEscalation|Escalade de privilèges]]
*   [[Exploit|Exploit]]
*   [[StackCanary|Stack Canary]]
*   [[AddressSpaceLayoutRandomization|ASLR]]
*   [[DataExecutionPrevention|DEP]]
*   [[SecureCoding|Programmation sécurisée]]
*   [[StaticAnalysis|Analyse statique]]
*   [[DynamicAnalysis|Analyse dynamique]]
*   [[Fuzzing|Fuzzing]]
*   [[SafeProgrammingLanguages|Langages de programmation sûrs]]
*   [[Rust|Rust]]
*   [[GoProgrammingLanguage|Go]]
*   [[JavaProgrammingLanguage|Java]]
*   [[Sandbox|Sandboxing]]
*   [[SoftwareVulnerability|Vulnérabilité Logicielle]]