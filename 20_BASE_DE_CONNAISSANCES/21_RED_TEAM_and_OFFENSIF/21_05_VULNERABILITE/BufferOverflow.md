---
aliases:
  - Dépassement de tampon
  - Débordement de mémoire
  - Buffer Overflow
  - Buffer Overflow Attack
  - BOF
  - Stack Buffer Overflow
  - Heap Buffer Overflow
archetype: vulnerabilite
cve: CVE-2023-0000 (Exemple Générique)
cvss_score: 9.8
cssclasses:
  - max
tags:
  - cve
  - vulnerabilite/buffer-overflow
  - cvss
  - exploitation
  - attaque/deni-de-service
  - memoire
  - vulnerabilite/buffer-overflow/stack-based
  - vulnerabilite/buffer-overflow/heap-based
  - shellcode
  - poc
  - gestion-risques/contre-mesures
  - maintenance/mise-a-jour
  - validation-entrees
  - aslr
  - dep-nx
  - stack-canaries
  - principe/moindre-privilege
  - cybersecurite/detection
  - analyse/code/statique
  - sast
  - analyse/code/dynamique
  - dast
  - fuzzing
  - logiciel
  - langage/c
---

# CVE-2023-0000 : Buffer Overflow (Dépassement de Tampon)

> [!danger] Score CVSS : 9.8 (Critique)
> **Vecteur** : `AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H`
> *L'impact est **Critique** car elle permet l'exécution de code arbitraire à distance (RCE) ou le déni de service (DoS) en manipulant la mémoire du programme.*

## 📥 Description Technique
Un **Buffer Overflow** (dépassement de tampon) est une vulnérabilité de sécurité qui se produit lorsqu'un programme tente d'écrire plus de données dans un *bloc de mémoire* (tampon ou "buffer") qu'il ne peut en contenir. Cela entraîne l'écrasement des données adjacentes en mémoire, ce qui peut corrompre d'autres variables, des pointeurs de fonction, ou des informations de contrôle d'exécution.

Il existe deux types principaux :
*   **Stack-based Buffer Overflow** : Se produit lorsque le dépassement a lieu sur la pile d'exécution d'un programme. Cela peut corrompre les adresses de retour de fonction, permettant à un attaquant de détourner le *flux d'exécution* du programme vers du code malveillant.
*   **Heap-based Buffer Overflow** : Se produit lorsque le dépassement a lieu sur le tas (heap), une zone de mémoire allouée dynamiquement. L'exploitation est souvent plus complexe et vise à manipuler des *structures de données* ou des pointeurs d'allocation du tas.

Le mécanisme d'exploitation repose souvent sur la capacité à injecter des instructions (appelées "shellcode") dans la mémoire du programme et à ensuite forcer le programme à exécuter ce *shellcode* en manipulant des adresses de retour ou des pointeurs.

## 💥 Exploitabilité
*   **POC Public** : Souvent oui (pour les vulnérabilités découvertes)
*   **Facilité d'exploitation** : Moyenne à Difficile (dépend des protections activées et du contexte)
*   **Prérequis** : Dépend du vecteur. Peut être un accès réseau (pour les services exposés) ou un accès local (pour les applications locales), voire aucune authentification si le service est public et vulnérable.

```c
// Snippet de code vulnérable (exemple simplifié en C)
#include <stdio.h>
#include <string.h>

void vulnerable_function(char *input) {
    char buffer[16]; // Tampon de 16 octets
    strcpy(buffer, input); // Pas de vérification de taille
    printf("Buffer content: %s\n", buffer);
}

int main(int argc, char *argv[]) {
    if (argc < 2) {
        printf("Usage: %s <string>\n", argv[0]);
        return 1;
    }
    vulnerable_function(argv[1]);
    return 0;
}
```
Dans l'exemple ci-dessus, si `argv[1]` contient une chaîne de plus de 15 caractères (plus le caractère nul de fin de chaîne), la fonction `strcpy` écrira au-delà des limites du `buffer`, provoquant un dépassement.

## 🛡️ Patch & Mitigation

### Correctif Officiel
> [!success] Version Corrigée
> Mettre à jour vers la version **la plus récente et corrigée** du logiciel ou de la bibliothèque affectée dès qu'elle est disponible. Appliquer les correctifs de sécurité fournis par les éditeurs.

### Contournement (Workaround)
Si le patch n'est pas possible, des mesures de *mitigation* peuvent réduire le risque :
*   **Validation des entrées** : Mettre en place une *validation stricte* de toutes les entrées utilisateur pour s'assurer qu'elles respectent les tailles et formats attendus.
*   **Utilisation de fonctions sûres** : Remplacer les fonctions C/C++ dangereuses (comme `strcpy`, `sprintf`, `gets`) par des équivalents plus sûrs qui effectuent des *vérifications de bornes* (ex: `strncpy`, `snprintf`, `fgets`).
*   **ASLR (Address Space Layout Randomization)** : Activer l'ASLR rend la prédiction des adresses mémoire plus difficile pour un attaquant, compliquant l'exécution de code injecté.
*   **DEP/NX (Data Execution Prevention/No-Execute)** : Empêche l'exécution de code à partir de zones mémoire désignées comme contenant uniquement des données, rendant l'exécution de *shellcode* plus difficile.
*   **Canary Values (Stack Canaries)** : Des valeurs aléatoires sont placées sur la pile avant le *pointeur d'instruction de retour*. Si ces valeurs sont modifiées, le programme détecte une tentative de dépassement et termine l'exécution.
*   **Compilation avec des protections modernes** : Utiliser des compilateurs (comme GCC, Clang) avec des options de sécurité activées (ex: `-fstack-protector-all`, `-Wformat-security`).
*   **Segmentation des privilèges** : Exécuter les applications avec le *principe du moindre privilège* afin de limiter l'impact en cas d'exploitation réussie.

## 🔍 Détection
Comment savoir si on est vulnérable ?
```bash
# Vérification de version
[commande pour vérifier la version du logiciel/service]

# Analyse statique de code
# Utiliser des outils SAST (Static Application Security Testing) comme
# Coverity, SonarQube, Fortify, ou des linters spécifiques au langage
# pour identifier les fonctions potentiellement dangereuses ou les
# motifs de code vulnérables (ex: strcpy sans taille).

# Analyse dynamique de code
# Utiliser des outils DAST (Dynamic Application Security Testing)
# ou des fuzzers (ex: AFL, libFuzzer) pour envoyer des entrées malformées
# et observer les crashes ou comportements anormaux du programme.
```

## 🔗 Références
*   [OWASP - Buffer Overflow](https://owasp.org/www-community/attacks/Buffer_overflow_attack)
*   [MITRE ATT&CK - T1191 : Exploitation for Buffer Overflow](https://attack.mitre.org/techniques/T1191/)
*   [CWE-119 : Improper Restriction of Operations within the Bounds of a Memory Buffer](https://cwe.mitre.org/data/definitions/119.html)