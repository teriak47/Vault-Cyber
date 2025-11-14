---
tags:
  - securite/corruption-memoire
  - programmation/securite-memoire
  - securite/attenuation-exploitation
  - depassement-tampon
  - vulnerabilite/utilisation-apres-liberation
  - securite/aslr
aliases:
  - Corruption de mémoire
  - Memory Corruption
source:
  - null
cssclasses:
  - max
---

# Corruption de Mémoire (Memory Corruption)

## 📥 Définition en une phrase
> La corruption de mémoire est un défaut ou une erreur où le contenu d'un emplacement mémoire est modifié de manière non intentionnelle, menant à des comportements imprévisibles d'un programme ou à l'exécution de code malveillant.

## 🧠 Concepts Clés / Fonctionnement
*   **Modification non autorisée:** Fait référence à l'altération des données ou des instructions dans la mémoire vive d'un programme sans l'intention du développeur ou le contrôle approprié du système.
*   **Causes courantes:** Les vulnérabilités typiques incluent les [[BufferOverflow|dépassements de tampon (Buffer Overflow)]], les [[UseAfterFree|utilisations après libération (Use-After-Free)]], les "double-free", les erreurs d'initialisation de pointeurs, et l'utilisation de pointeurs "sauvages".
*   **Impact potentiel:** Peut entraîner divers problèmes, tels que des plantages de l'application, un comportement incorrect ou imprévisible du programme, des fuites d'[[SensitiveData|informations sensibles]], une [[PrivilegeEscalation|élévation de privilèges]], ou permettre l'[[Exploitation|exécution de code arbitraire]] par un attaquant.
*   **Mécanisme d'Exploitation:** Les attaquants exploitent souvent la corruption de mémoire pour détourner le flux d'exécution normal d'un programme vers leur propre code malveillant injecté, prenant ainsi le contrôle de l'application ou du système.

## 🛡️ Risques / Menaces Associés
*   [[RemoteCodeExecution|Exécution de Code à Distance]]
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[PrivilegeEscalation|Élévation de Privilèges]]
*   [[InformationDisclosure|Divulgation d'Informations]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Développement sécurisé:** Utilisation de langages de programmation qui intègrent des mécanismes de [[MemorySafety|sécurité mémoire]] (ex: Rust, Go) ou adoption de pratiques de [[SecureCodingPractices|codage sécurisé]] strictes pour les langages à faible niveau (C/C++).
*   **Validation des entrées:** Implémentation de [[InputValidation|validations des entrées]] rigoureuses et de contrôles de limites pour prévenir les vulnérabilités comme les dépassements de tampon.
*   **Techniques d'atténuation d'exploitation:** Déploiement et configuration d'atténuations au niveau du système d'exploitation et du compilateur, telles que [[AddressSpaceLayoutRandomization|ASLR (Address Space Layout Randomization)]], [[DataExecutionPrevention|DEP (Data Execution Prevention)]], et les "stack canaries".
*   **Analyse et tests:** Réalisation d'audits de code, de tests de fuzzing, et d'analyses statiques et dynamiques pour identifier et corriger les vulnérabilités de corruption de mémoire avant le déploiement.

## 🔗 Notes Connexes
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[UseAfterFree|Utilisation Après Libération]]
*   [[Exploitation|Exploitation]]
*   [[MemorySafety|Sécurité Mémoire]]
*   [[Vulnerability|Vulnérabilité]]