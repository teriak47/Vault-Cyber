---
tags:
aliases:
  - Système d'exploitation
  - OS
  - Operating System
  - OS (informatique)
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Système d'exploitation (OS)

## 📥 Définition en une phrase
> Un [[OperatingSystem|système d'exploitation]] ([[OperatingSystem|OS]]) est un [[Software|logiciel]] [[System|système]] fondamental qui gère les [[Hardware|ressources matérielles]] et [[Software|logicielles]] d'un [[Computer|ordinateur]], fournissant des [[OperatingSystem|services]] communs pour les [[SoftwareApplication|programmes informatiques]] et l'[[UserInterface|interface utilisateur]].

## 🧠 Concepts Clés / Piliers
*   **[[ResourceManagement|Gestion des ressources]]**: L'[[OperatingSystem|OS]] alloue et désalloue les [[CentralProcessingUnit|ressources CPU]], la [[RandomAccessMemory|mémoire vive]], le [[SecureStorage|stockage]] et les [[PeripheralDevice|périphériques]] aux [[SoftwareApplication|applications]] et aux [[Process|processus]].
*   **[[ProcessManagement|Gestion des processus]]**: Il ordonnance l'exécution des [[SoftwareApplication|programmes]], gère leur état (en cours, en attente, terminé) et assure l'[[Isolation|isolation]] entre eux.
*   **[[MemoryManagement|Gestion de la mémoire]]**: L'[[OperatingSystem|OS]] gère l'allocation de la [[RandomAccessMemory|mémoire vive]] aux [[SoftwareApplication|applications]], utilise la [[VirtualMemory|mémoire virtuelle]] pour étendre l'espace d'adressage et protège les zones de [[MemorySafety|mémoire]].
*   **[[FileManager|Gestion des fichiers]]**: Il organise les [[Data|données]] sur les [[StorageDevice|périphériques de stockage]] (comme les [[HardDiskDrive|disques durs]] et les [[SolidStateDrive|SSD]]) en [[FileSystem|systèmes de fichiers]], contrôlant l'[[AccessControl|accès]], la lecture et l'écriture.
*   **[[DeviceManagement|Gestion des périphériques]]**: Il interagit avec les [[Hardware|composants matériels]] (tels que les [[Keyboard|claviers]], [[ComputerMouse|souris]], [[Monitor|écrans]], [[NetworkPrinter|imprimantes réseau]] et [[NetworkInterfaceCard|cartes réseau]]) via des [[Driver|pilotes]].
*   **[[UserInterface|Interface utilisateur]]**: Fournit une [[GraphicalUserInterface|interface graphique (GUI)]] ou une [[CommandLineInterface|interface en ligne de commande (CLI)]] permettant aux [[User|utilisateurs]] d'interagir avec l'[[Computer|ordinateur]].
*   **[[SystemCall|Appels système]]**: [[SystemCall|Interface programmatique]] par laquelle les [[SoftwareApplication|applications]] demandent des [[OperatingSystem|services]] au [[Kernel|noyau]] de l'[[OperatingSystem|OS]].

## 💡 Importance en Cybersécurité
> L'[[OperatingSystem|OS]] est la fondation logicielle de tout [[System|système informatique]]. Sa [[Security|sécurité]] est primordiale pour protéger l'[[Integrity|intégrité]], la [[Confidentiality|confidentialité]] et l'[[Availability|disponibilité]] des [[Data|données]] et des [[SoftwareApplication|applications]]. Les [[Vulnerability|vulnérabilités]] au sein de l'[[OperatingSystem|OS]] représentent un [[AttackVector|vecteur d'attaque]] majeur, exploité par les [[Malware|logiciels malveillants]] et les [[ThreatActor|acteurs de menace]] via des [[ZeroDay|vulnérabilités zero-day]] ou des [[UnpatchedVulnerability|failles non corrigées]]. Une [[SystemCompromise|compromission du système]] d'exploitation peut mener à des [[PrivilegeEscalation|escalades de privilèges]], des [[DenialOfService|attaques par déni de service]] ou des [[DataExfiltration|exfiltrations de données]]. Une [[PatchManagement|gestion proactive des correctifs]] et l'application de [[SecurityControl|contrôles de sécurité]] robustes (comme le [[SystemHardening|durcissement du système]], l'[[AccessControl|accès contrôlé]], les [[Firewall|pare-feu]] et les [[EndpointSecurity|solutions de sécurité des terminaux]]) sont essentielles pour maintenir un niveau de [[Cybersecurity|cybersécurité]] élevé.

## 🔗 Notes Connexes
*   [[Kernel|Noyau]]
*   [[FileSystem|Système de Fichiers]]
*   [[Virtualization|Virtualisation]]
*   [[Containerization|Conteneurisation]]
*   [[Cloud|Cloud Computing]]
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[EndpointSecurity|Sécurité des endpoints]]
*   [[PatchManagement|Gestion des Patchs]]
*   [[PrivilegeEscalation|Escalade de Privilèges]]
*   [[Malware|Logiciel Malveillant]]