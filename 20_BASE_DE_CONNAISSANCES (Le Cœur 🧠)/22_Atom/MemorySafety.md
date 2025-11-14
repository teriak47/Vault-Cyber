---
tags:
  - vulnerabilite/utilisation-apres-liberation
  - gestion-memoire/automatique
  - programmation/langages-surs
  - depassement-tampon
  - securite/aslr
  - securite/canaris-pile
aliases:
  - Sécurité Mémoire
  - Memory Safety
source: null
cssclasses:
  - max
---

# Sécurité Mémoire (Memory Safety)  
  
## 📥 Définition en une phrase  
> La **sécurité mémoire** désigne l'ensemble des techniques et pratiques visant à prévenir les erreurs d’accès à la mémoire qui peuvent entraîner des vulnérabilités comme des corruptions mémoire ou des exécutions de code arbitraire.  
  
## 🧠 Concepts Clés / Fonctionnement  
* **Erreurs courantes** : débordements de tampon (buffer overflow), utilisation après libération (use-after-free), accès hors limites (out-of-bounds access), double libération de mémoire.  
* **Types d'erreurs mémoire** : lecture/écriture hors limites, fuites de mémoire, corruption de pointeurs.  
* **Langages sûrs vs non sûrs** : les langages comme Rust ou Java implémentent la sécurité mémoire au niveau du compilateur ou de la machine virtuelle, tandis que C/C++ sont plus sujets aux erreurs mémoire sans protections explicites.  
* **Mécanismes de sécurité** : vérifications à l’exécution, gestion automatique de la mémoire (garbage collector), système de types sécurisé, analyse statique et dynamique du code.  
* **Contrôles d’intégrité mémoire** : canaris de pile (stack canaries), ASLR (Address Space Layout Randomization), DEP (Data Execution Prevention).  
* **Importance dans la sécurité applicative** : la violation de la sécurité mémoire est souvent l’entrée initiale d’exploitations de vulnérabilités (ex: RCE, escalades de privilèges).  
  
## 🛡️ Risques / Menaces Associés  
* [[BufferOverflow|Débordement de tampon]]  
* [[UseAfterFree|Usage après libération]]  
* [[MemoryCorruption|Corruption mémoire]]  
* [[CodeInjection|Injection de code]]  
* [[PrivilegeEscalation|Escalade de privilèges]]  
* [[RemoteCodeExecution|Exécution de code à distance]]  
  
## 💎 Mesures de Protection / Bonnes Pratiques  
* Utilisation de langages avec sécurité mémoire intégrée ([[Rust|Rust]], [[Java|Java]], [[Go|Go]])  
* Application de pratiques de codage sécurisé (contrôle des entrées, vérifications systématiques d’index)  
* Compilation avec options de sécurité activées (stack canaries, ASLR, DEP)  
* Utilisation d’outils d’analyse statique et dynamique pour détecter les erreurs mémoire ([[StaticAnalysis|Analyse statique]], [[DynamicAnalysis|Analyse dynamique]])  
* Adoption de mécanismes d’exécution protégée (sandboxing)  
* Revue et audit réguliers du code critique accès mémoire  
* Tests de fuzzing ciblés sur les entrées mémoire  
  
## 🔗 Notes Connexes  
* [[BufferOverflow|Débordement de tampon]]  
* [[UseAfterFree|Usage après libération]]  
* [[SecureCoding|Programmation sécurisée]]  
* [[MemoryCorruption|Corruption mémoire]]  
* [[Rust|Rust]]  
* [[SafeProgrammingLanguages|Langages de programmation sûrs]]