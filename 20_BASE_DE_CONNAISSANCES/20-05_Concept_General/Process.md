---
aliases:
  - Processus
  - Computer Process
  - OS Process
cssclasses:
  - max
archetype: concept-general
---

# Processus (Process)

## 📥 Définition en une phrase
> Un [[Process|processus]] est une instance en cours d'exécution d'un [[Software|programme]] informatique, gérée par le [[OperatingSystem|système d'exploitation]] et possédant son propre ensemble de [[Resource|ressources]] système.

## 🧠 Concepts Clés / Piliers
*   **Instance d'exécution**: Un [[Process|processus]] représente une [[Software|application]] ou un [[System|service]] en [[Execution|cours d'exécution]]. Il encapsule l'[[ExecutionContext|état d'exécution]] du [[Software|programme]], y compris son [[MemorySpace|espace mémoire]] dédié, ses [[RegisterValues|valeurs de registre]] et les [[Resource|ressources]] qu'il utilise.
*   **Gestion par le [[OperatingSystem|Système d'exploitation]]**: Le [[OperatingSystem|système d'exploitation]] est le gestionnaire central des [[Process|processus]]. Il alloue les [[CentralProcessingUnit|ressources CPU]], la [[MemoryManagement|mémoire]], les fichiers et les périphériques d'[[InputOutput|entrée/sortie]], planifie leur [[Execution|exécution]] et les isole les uns des autres pour assurer la [[Security|stabilité]] et la [[Security|sécurité]] du [[System|système]].
*   **États du Processus**: Un [[Process|processus]] peut transiter par plusieurs états (nouveau, prêt, en cours d'exécution, bloqué/attente, terminé) en fonction de son [[Activity|activité]] et de l'accès aux [[Resource|ressources]] nécessaires.

## 💡 Importance en Cybersécurité
> Les [[Process|processus]] sont des cibles primordiales pour les [[ThreatActor|acteurs de menace]], car la compromission d'un [[Process|processus]] peut mener à une [[SystemCompromise|compromission du système]]. Comprendre comment les [[Process|processus]] fonctionnent et sont gérés est essentiel pour la [[Cybersecurity|cybersécurité]], notamment pour la [[Malware|détection de logiciels malveillants]], l'[[Exploitation|analyse des exploits]], l'[[PrivilegeEscalation|escalade de privilèges]] et la [[SecurityMonitoring|surveillance]] des [[System|systèmes]]. Des techniques comme la [[DataExecutionPrevention|Prévention de l'Exécution des Données (DEP)]] et l'[[AddressSpaceLayoutRandomization|ASLR]] sont spécifiquement conçues pour protéger les [[Process|processus]] contre les [[Attack|attaques]] courantes.

## 🔗 Notes Connexes
*   [[OperatingSystem|Système d'exploitation]]
*   [[MemoryManagement|Gestion de la mémoire]]
*   [[Exploitation|Exploitation]]
*   [[Malware|Logiciel malveillant]]
*   [[PrivilegeEscalation|Escalade de Privilèges]]
*   [[System|Système]]
*   [[Software|Logiciel]]
*   [[AttackVector|Vecteur d'attaque]]
*   [[SecurityMonitoring|Surveillance de sécurité]]
*   [[NoExecuteBit|Bit No-Execute (NX Bit)]]
*   [[AddressSpaceLayoutRandomization|Address Space Layout Randomization (ASLR)]]
*   [[CentralProcessingUnit|Processeur]]
*   [[InputOutput|Entrée/Sortie]]
*   [[ExecutionContext|Contexte d'exécution]]
*   [[Execution|Exécution]]
*   [[Activity|Activité]]
*   [[MemorySpace|Espace mémoire]]
*   [[RegisterValues|Valeurs de registre]]