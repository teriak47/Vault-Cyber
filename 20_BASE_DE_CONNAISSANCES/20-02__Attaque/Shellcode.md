---
tags:
  - attaque
  - attaque/shellcode
aliases:
  - Code d'exploitation
  - Code malveillant
  - Shellcode
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Shellcode (Code d'exploitation)

## 📥 Définition
> Un [[Shellcode|shellcode]] est un petit bloc de code exécutable, souvent écrit en assembleur, qui agit comme la [[Payload|charge utile]] d'une [[Exploit|exploitation de vulnérabilité]]. Son objectif principal est de prendre le contrôle d'un [[System|système]] compromis, généralement en ouvrant un [[Shell|shell]] interactif pour l'[[ThreatActor|attaquant]].

## 🎯 Vecteurs d'Attaque
*   **[[BufferOverflow|Dépassement de Tampon]]**: Injection de [[Shellcode|shellcode]] dans des zones mémoire allouées au-delà des limites prévues, écrasant le code légitime.
*   **[[CommandInjection|Injection de commandes]]**: Intégration du [[Shellcode|shellcode]] via des entrées utilisateur non validées qui sont ensuite exécutées comme des commandes du [[OperatingSystem|système d'exploitation]].
*   **[[FormatStringVulnerability|Failles de format string]]**: Exploitation de vulnérabilités dans des fonctions de formatage de chaînes pour lire ou écrire en [[Memory|mémoire]] arbitrairement et injecter du [[Shellcode|shellcode]].

## 💥 Impacts Potentiels
*   [[SystemCompromise|Compromission de Système]] complète
*   [[UnauthorizedAccess|Accès Non Autorisé]] aux [[Resource|ressources]] système
*   [[PrivilegeEscalation|Élévation de privilèges]] au niveau root ou administrateur
*   [[DataExfiltration|Exfiltration de données]] sensibles
*   [[RemoteCodeExecution|Exécution de Code à Distance]] arbitraire

## 💡 Exemple concret
> Suite à un [[BufferOverflow|dépassement de tampon]] dans une [[SoftwareApplication|application]] mal configurée, un [[ThreatActor|attaquant]] parvient à injecter un [[Shellcode|shellcode]] malveillant. Ce code, conçu pour être indépendant de la [[Memory|position]] en mémoire, est exécuté à la place du code légitime de l'application. Le [[Shellcode|shellcode]] ouvre un [[ReverseShell|shell inversé]] (par exemple, via [[Netcat|nc]]) vers la [[Computer|machine]] de l'attaquant, lui accordant un [[CommandLineInterface|accès en ligne de commande]] direct et persistant au [[System|système]] compromis, souvent avec les privilèges de l'application exploitée.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[SecureCodingPractices|Pratiques de codage sécurisé]] pour éviter les vulnérabilités courantes (ex: [[BufferOverflow|dépassement de tampon]], [[CommandInjection|injection de commandes]]).
    *   Utilisation de mécanismes de [[MemorySafety|sécurité mémoire]] tels que [[DataExecutionPrevention|DEP]] (Prévention de l'exécution des données) et [[AddressSpaceLayoutRandomization|ASLR]] (Randomisation de l'espace d'adressage).
    *   Implémentation de [[StackCanary|Stack Canary]] et du [[NoExecuteBit|bit No-Execute]] pour protéger la [[Stack|pile]] et le [[Heap|tas]].
    *   Réalisation de [[CodeReview|revues de code]] et de [[PenetrationTesting|tests d'intrusion]] réguliers.
    *   [[PatchManagement|Gestion des Patchs]] proactive pour corriger les [[Vulnerability|vulnérabilités]] connues.
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour identifier les [[MessagePattern|motifs de messages]] ou les comportements anormaux liés aux [[Exploit|exploits]] et au [[Shellcode|shellcode]].
    *   [[EndpointDetectionAndResponse|EDR]] et [[EndpointProtectionPlatform|EPP]] pour la surveillance des [[EndDevices|terminaux]].
    *   [[SecurityInformationAndEventManagement|SIEM]] pour l'analyse des [[Log|logs]] et la corrélation d'événements.
*   **Réponse** :
    *   Mise en place d'un [[IncidentResponse|Plan de réponse à incident]] pour contenir, éradiquer et récupérer après une [[Attack|attaque]] impliquant un [[Shellcode|shellcode]].

## 🔗 Notes Connexes
*   [[Exploit|Exploit]]
*   [[Payload|Charge utile]]
*   [[RemoteCodeExecution|Exécution de Code à Distance]]
*   [[BufferOverflow|Buffer Overflow]]
*   [[ReverseShell|Reverse Shell]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Attack|Attaque]]