---
tags:
  - cybersécurité/shellcode
  - code/independant-position
  - cybersécurité/shell-inverse
  - malware/charge-utile
  - cybersécurité/exploitation-vulnerabilite
  - depassement-tampon
aliases:
  - Code d'exploitation
  - Code malveillant
cssclasses:
  - max
---

# Shellcode (Code d'exploitation)

## 📥 Définition en une phrase
> Un shellcode est un petit bloc de code exécutable, souvent écrit en assembleur, utilisé comme charge utile dans l'exploitation d'une vulnérabilité pour prendre le contrôle d'un système, généralement en ouvrant un shell.

## 🧠 Concepts Clés / Fonctionnement
*   **Exécution Arbitraire de Code :** L'objectif principal est d'exécuter des instructions arbitraires sur le système cible après qu'une vulnérabilité ait été exploitée.
*   **Charge Utile (Payload) :** Le shellcode agit comme la partie active d'un [[Exploit|exploit]], délivrant la fonctionnalité malveillante souhaitée une fois l'accès initial obtenu.
*   **Obtention d'un Shell :** Il est le plus souvent conçu pour lancer un shell de commande (local ou distant) afin de permettre à l'attaquant d'interagir avec le système compromis. Un [[ReverseShell|shell inverse]] est courant pour contourner les pare-feux.
*   **Position-Independent Code (PIC) :** Les shellcodes sont souvent écrits pour être du code indépendant de la position, ce qui signifie qu'ils peuvent s'exécuter correctement quel que soit l'endroit où ils sont chargés en mémoire.
*   **Techniques d'Injection :** Il est typiquement injecté après des vulnérabilités comme le [[BufferOverflow|dépassement de tampon]], les injections de commandes ou les failles de format string.

## 🛡️ Risques / Menaces Associés
*   [[CodeExecution|Exécution de Code Arbitraire]]
*   [[PrivilegeEscalation|Élévation de Privilèges]]
*   [[RemoteCodeExecution|Exécution de Code à Distance (RCE)]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[InputValidation|Validation des Entrées]] : Empêcher les dépassements de tampon et autres injections.
*   [[MemoryProtection|Protections de la Mémoire]] : Utilisation de techniques comme la Randomisation de l'Espace d'Adresse (ASLR) et la Prévention de l'Exécution des Données (DEP/NX) pour rendre l'exploitation plus difficile.
*   [[PatchManagement|Gestion des Patchs]] : Maintenir les logiciels à jour pour corriger les vulnérabilités exploitables.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] : Détecter et bloquer les tentatives d'injection et d'exécution de shellcodes.
*   Compilation avec des flags de sécurité : Utiliser des options de compilation (ex: `-fstack-protector`, `-pie`) pour renforcer la sécurité du binaire.

## 🔗 Notes Connexes
*   [[ExploitDevelopment|Développement d'Exploits]]
*   [[BufferOverflow|Dépassement de Tampon]]
*   [[Payload|Charge Utile]]
*   [[Metasploit|Metasploit]]