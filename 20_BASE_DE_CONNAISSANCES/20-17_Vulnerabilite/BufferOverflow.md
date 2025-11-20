---
tags:
  - vulnerabilite
  - memoire/buffer-overflow
aliases:
  - Dépassement de Tampon
  - Buffer Overflow
archetype: vulnerabilite
cve: N/A
cvss_score: 0.0
cssclasses:
  - max
---

# Buffer Overflow

> [!danger] Score CVSS : Non applicable (Type de vulnérabilité)
> *Un [[BufferOverflow|dépassement de tampon]] est un type de [[Vulnerability|vulnérabilité]] qui peut potentiellement mener à l'[[RemoteCodeExecution|exécution de code à distance]], des [[DenialOfService|dénis de service]] ou des escalades de privilèges.*

## 📥 Description Technique
Un [[BufferOverflow|dépassement de tampon]] se produit lorsqu'un programme tente d'écrire plus de [[Data|données]] dans un [[Buffer|tampon]] (une zone de [[MemoryManagement|mémoire]] allouée pour stocker des [[Data|données]]) qu'il ne peut en contenir. Cela entraîne l'écrasement des [[Data|données]] adjacentes dans la [[MemoryManagement|mémoire]], ce qui peut corrompre d'autres variables, des pointeurs ou même du [[Process|code]] exécutable.

Cette [[Vulnerability|vulnérabilité]] est souvent exploitée en injectant du [[Malware|code malveillant]] dans la [[MemoryManagement|mémoire]] qui peut ensuite être exécuté par le [[Process|processus]] du programme [[Vulnerability|vulnérable]], conduisant à des [[Exploitation|exploitations]] sérieuses telles que l'[[RemoteCodeExecution|exécution de code à distance]] ou la [[PrivilegeEscalation|montée en privilèges]].

## 💥 Exploitabilité
*   **POC Public** : Oui (nombreux exemples historiques)
*   **Facilité d'exploitation** : Moyenne à Difficile (dépend de l'architecture, de la présence de protections comme [[AddressSpaceLayoutRandomization|ASLR]] ou [[DataExecutionPrevention|DEP]])
*   **Prérequis** : Dépend de la nature spécifique de la [[Vulnerability|vulnérabilité]] et du [[Process|processus]] impacté. Souvent un [[InputDevices|input]] contrôlé par l'[[Client|attaquant]].

```c
// Exemple de code C vulnérable à un Buffer Overflow
#include <string.h>
#include <stdio.h>

void vulnerable_function(char *input) {
    char buffer[10]; // Tampon de taille fixe
    strcpy(buffer, input); // Pas de vérification de taille, cause un dépassement
    printf("Copied: %s\n", buffer);
}

int main(int argc, char **argv) {
    if (argc < 2) {
        printf("Usage: %s <string>\n", argv[0]);
        return 1;
    }
    vulnerable_function(argv[1]);
    return 0;
}
```

## 🛡️ Patch & Mitigation

### Correctif Officiel
> [!success] Éviter les fonctions non sécurisées
> Les développeurs doivent remplacer les fonctions de manipulation de chaînes de [[Process|caractères]] non sécurisées (comme `strcpy`, `strcat`, `sprintf`) par leurs équivalents sécurisés qui vérifient la taille du [[Buffer|tampon]] (comme `strncpy`, `strncat`, `snprintf`, `strlcpy`, `strlcat`).

### Contournement (Workaround)
Si un patch n'est pas possible :
*   Implémenter des contrôles d'[[InputDevices|entrée]] rigoureux et des validations de longueur pour toutes les [[InputDevices|données]] fournies par l'[[Client|utilisateur]].
*   Utiliser des compilateurs modernes avec des protections intégrées comme la détection de [[BufferOverflow|dépassement de tampon]] (ex: `stack canaries`).
*   Activer les mécanismes de sécurité du système d'[[OperatingSystem|exploitation]] tels que [[DataExecutionPrevention|DEP]] (Data Execution Prevention) et [[AddressSpaceLayoutRandomization|ASLR]] (Address Space Layout Randomization).

## 🔍 Détection
Comment savoir si on est [[Vulnerability|vulnérable]] ?
*   [[CodeReview|Revue de code]] pour identifier les fonctions non sécurisées ou les allocations de [[Buffer|tampons]] fixes sans vérification de taille.
*   [[Fuzzing|Fuzzing]] des [[InputDevices|entrées]] de programme pour provoquer des plantages ou des comportements inattendus.
*   Utilisation d'outils d'analyse statique et dynamique de [[CodeReview|code]] qui peuvent identifier les vulnérabilités potentielles de [[BufferOverflow|dépassement de tampon]].

## 🔗 Références
*   [[MemorySafety|Sécurité Mémoire]]
*   [[Exploitation|Exploitation (cybersécurité)]]
*   [[ReturnOrientedProgramming|Programmation Orientée Retour (ROP)]]
*   [OWASP Buffer Overflow](https://owasp.org/www-community/attacks/Buffer_overflow_attack)