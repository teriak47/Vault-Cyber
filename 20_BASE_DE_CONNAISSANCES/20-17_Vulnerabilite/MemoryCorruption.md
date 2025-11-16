---
tags:
  - vulnerabilite
aliases:
  - Corruption de mémoire
  - Memory Corruption
archetype: vulnerabilite
cve: 
cvss_score: 
cssclasses:
  - max
---

# Vulnérabilité : Corruption de Mémoire (Memory Corruption)

## 📥 Définition et Impact
> La corruption de [[Memory|mémoire]] est une [[Vulnerability|vulnérabilité]] où le contenu d'un emplacement mémoire est modifié de manière non intentionnelle, menant à des comportements imprévisibles d'un [[Software|programme]] ou à l'[[Exploitation|exécution de code malveillant]]. Elle peut entraîner des plantages d'application, un comportement incorrect, des fuites d'[[SensitiveData|informations sensibles]], une [[PrivilegeEscalation|élévation de privilèges]], ou permettre l'[[RemoteCodeExecution|exécution de code à distance]] par un [[ThreatActor|attaquant]].

## 📝 Détails Techniques
*   **Vecteur d'attaque**: Généralement exploitée en fournissant des [[UnvalidatedInput|entrées non validées]] à un [[Software|programme]], déclenchant des erreurs dans la [[MemoryManagement|gestion de la mémoire]]. Les attaquants cherchent à altérer les données ou les pointeurs pour détourner le flux d'exécution normal vers leur [[Shellcode|code malveillant]].
*   **Composant affecté**: Générique, affectant souvent les [[Software|logiciels]] et [[OperatingSystem|systèmes d'exploitation]] développés en langages à gestion de mémoire manuelle (ex: C/C++), où les développeurs sont responsables de l'allocation et de la libération des ressources mémoire.
*   **Type de faille (CWE)**:
    *   [[CommonWeaknessEnumeration|CWE-119]] - Improper Restriction of Operations within the Bounds of a Memory Buffer (Dépassement de tampon)
    *   [[CommonWeaknessEnumeration|CWE-416]] - [[UseAfterFree|Use After Free]] (Utilisation après libération)
    *   [[CommonWeaknessEnumeration|CWE-415]] - Double Free (Double libération)
    *   [[CommonWeaknessEnumeration|CWE-787]] - Out-of-bounds Write (Écriture hors limites)
    *   [[CommonWeaknessEnumeration|CWE-824]] - Access of Uninitialized Pointer (Accès à un pointeur non initialisé)

## 🛡️ Correctifs et Contournements
*   **Versions patchées**: N/A (dépend du [[Software|logiciel]] spécifique et de la [[Vulnerability|vulnérabilité]] exploitée).
*   **Mesures de contournement (Workarounds)**:
    *   **Développement sécurisé**: Adopter des pratiques de [[SecureCodingPractices|codage sécurisé]] et utiliser des langages offrant des garanties de [[MemorySafety|sécurité mémoire]] (ex: Rust, Go).
    *   **[[InputValidation|Validation des entrées]]**: Implémenter des contrôles rigoureux sur toutes les [[InputDevices|entrées]] pour prévenir les [[BufferOverflow|dépassements de tampon]].
    *   **Atténuations d'exploitation**: Déployer des mécanismes au niveau du [[OperatingSystem|système d'exploitation]] et du compilateur tels que [[AddressSpaceLayoutRandomization|ASLR]], [[DataExecutionPrevention|DEP]] (aussi connu sous [[NoExecuteBit|NX Bit]]), et les [[StackCanary|canaries de pile]].
    *   **Analyse et tests**: Effectuer des [[CodeReview|revues de code]], des analyses statiques et dynamiques, et des tests de [[Fuzzing|fuzzing]] pour identifier et corriger les [[SoftwareVulnerability|vulnérabilités logicielles]] avant le [[Installation|déploiement]].

## 🔍 Comment la détecter ?
*   **Signatures réseau/IDS**: Dépend de la [[Attack|nature de l'attaque]] spécifique. Les [[IntrusionDetectionSystem|IDS]] peuvent détecter des schémas d'[[Exploit|exploit]] connus ou des comportements anormaux liés à l'[[Exploitation|exploitation]] (ex: tentatives de modification de [[Process|processus]], sauts d'exécution inattendus).
*   **Commandes de détection locale**:
    ```bash
    # La détection d'une corruption de mémoire générique sur un système en production est complexe.
    # Elle implique souvent la surveillance des plantages d'applications, des erreurs de segmentation (segmentation faults)
    # ou l'utilisation d'outils d'analyse de la mémoire (ex: Valgrind en environnement de développement).
    # Sur un système compromis, l'analyse forensique de la mémoire (memory forensics) peut révéler des preuves de corruption.
    ```

## 🔗 Notes Connexes
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[UseAfterFree|Utilisation Après Libération]]
*   [[Exploitation|Exploitation]]
*   [[MemorySafety|Sécurité Mémoire]]
*   [[Vulnerability|Vulnérabilité]]
*   [[RemoteCodeExecution|Exécution de Code à Distance]]
*   [[DenialOfService|Déni de Service]]
*   [[PrivilegeEscalation|Élévation de Privilèges]]
*   [[InformationDisclosure|Divulgation d'Informations]]
*   [[AddressSpaceLayoutRandomization|Address Space Layout Randomization]]
*   [[DataExecutionPrevention|Data Execution Prevention]]
*   [[StackCanary|Stack Canary]]
*   [[NoExecuteBit|No-Execute Bit]]
*   [[SecureCodingPractices|Pratiques de Codage Sécurisé]]
*   [[InputValidation|Validation des Entrées]]
*   [[CommonWeaknessEnumeration|Common Weakness Enumeration]]
*   [[Fuzzing|Fuzzing]]
*   [[Memory|Mémoire]]