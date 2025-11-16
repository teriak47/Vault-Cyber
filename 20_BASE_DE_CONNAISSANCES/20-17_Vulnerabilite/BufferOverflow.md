---
tags:
  - vulnerabilite
aliases:
  - Dépassement de Tampon
  - Buffer Overflow
archetype: vulnerabilite
cve: CVE-YYYY-NNNNN
cvss_score: 0.0
cssclasses:
  - max
---

# Vulnérabilité : Dépassement de Tampon (Buffer Overflow)

## 📥 Définition et Impact
> Une [[Vulnerability|vulnérabilité]] de [[Security|sécurité]] où un [[Software|programme]] tente d'écrire plus de [[Data|données]] dans un [[Buffer|tampon mémoire]] que ce pour quoi il a été alloué, écrasant ainsi les [[Data|données]] adjacentes. 
> Cela peut mener à une [[MemoryCorruption|corruption de mémoire]], une [[DataCorruption|corruption de données]], un [[DenialOfService|déni de service]], une [[PrivilegeEscalation|élévation de privilèges]] ou, plus gravement, à une [[RemoteCodeExecution|exécution de code à distance]].

## 📝 Détails Techniques
*   **Vecteur d'attaque**: Exploité lorsqu'un [[Software|programme]] ne vérifie pas les limites d'une zone de [[MemoryManagement|mémoire allouée]] (un [[Buffer|tampon]]) avant d'y écrire des [[Data|données]]. L'excès de données déborde du [[Buffer|tampon]] et écrase les informations stockées dans les adresses [[MemoryManagement|mémoire]] contiguës, comme les adresses de retour de [[Process|fonctions]] sur la [[Stack|pile]] ou les pointeurs sur le [[Heap|tas]]. Les [[ThreatActor|attaquants]] peuvent injecter et exécuter du [[Shellcode|code malveillant]].
*   **Composant affecté**: Principalement les [[Software|programmes]] écrits dans des [[Programming|langages de programmation]] de bas niveau (C, C++) qui n'offrent pas de [[MemorySafety|gestion automatique de la sécurité mémoire]]. Les [[OperatingSystem|systèmes d'exploitation]] peuvent également avoir des [[SecurityVulnerabilities|vulnérabilités]] dans leurs composants de gestion de la [[MemoryManagement|mémoire]].
*   **Type de faille (CWE)**: [[CommonWeaknessEnumeration|CWE-119]] - Improper Restriction of Operations within the Bounds of a Memory Buffer

## 🛡️ Correctifs et Contournements
*   **Versions patchées**: N/A (concerne une catégorie de [[Vulnerability|vulnérabilités]] plutôt qu'une faille spécifique à un [[Software|logiciel]] donné).
*   **Mesures de contournement (Workarounds)**:
    *   **Programmation sécurisée**: Utiliser des [[SecureCoding|fonctions de programmation sécurisées]] qui vérifient les limites de [[Buffer|tampon]] (ex: `strncpy_s`, `snprintf`) et éviter les fonctions non sécurisées (ex: `strcpy`, `sprintf`).
    *   **Langages sécurisés**: Préférer des [[Programming|langages de programmation]] modernes avec une [[MemorySafety|gestion automatique de la mémoire]] et des vérifications de limites (ex: Rust, Python, Java).
    *   **Protections de l'[[OperatingSystem|OS]]**: Mettre en œuvre et activer des mécanismes de protection au niveau du [[OperatingSystem|système d'exploitation]] tels que l'[[AddressSpaceLayoutRandomization|ASLR]] (Randomisation de l'Espace d'Adressage), la [[DataExecutionPrevention|DEP]] (Prévention de l'Exécution des Données) ou le [[NoExecuteBit|Bit NX]], et les [[StackCanary|Stack Canaries]].
    *   **[[CodeReview|Revue de Code]]**: Effectuer des examens réguliers et approfondis du [[Software|code source]] pour identifier les vulnérabilités de [[BufferOverflow|dépassement de tampon]].
    *   **[[PenetrationTesting|Tests d'intrusion]]**: Intégrer des [[Fuzzing|tests de fuzzing]] dans le cycle de développement pour découvrir les scénarios de dépassement.

## 🔍 Comment la détecter ?
*   **Signatures réseau/IDS**: Les [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] (IDS) et les [[IntrusionPreventionSystem|systèmes de prévention d'intrusion]] (IPS) peuvent être configurés avec des signatures spécifiques pour détecter des modèles d'[[Attack|attaques]] de [[BufferOverflow|dépassement de tampon]] dans le [[NetworkTrafficAnalysis|trafic réseau]].
*   **Analyse de code**: Des outils d'analyse de code statique (SAST) et dynamique (DAST) peuvent identifier les erreurs de gestion de [[Buffer|tampon]] et les conditions de dépassement potentielles.
*   **[[Fuzzing|Tests de Fuzzing]]**: Envoyer des entrées malformées ou excessives à un [[Software|programme]] pour provoquer des plantages ou des comportements inattendus, révélant des [[BufferOverflow|vulnérabilités]] potentielles.

## 🔗 Notes Connexes
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[MemoryCorruption|Corruption de mémoire]]
*   [[Exploit|Exploit]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Stack|Pile]]
*   [[Heap|Tas]]
*   [[ReturnOrientedProgramming|Programmation Orientée Retour]]
*   [[Shellcode|Shellcode]]