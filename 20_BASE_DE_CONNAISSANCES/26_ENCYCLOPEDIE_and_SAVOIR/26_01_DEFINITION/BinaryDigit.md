---
aliases:
  - Chiffre Binaire
  - Bit
  - Binary Digit
  - Unité Binaire
archetype: definition
cssclasses:
  - max
tags:
  - bit
  - informatique/fondamentaux
  - code-binaire
  - theorie-information
  - unite-information
  - octet
  - cryptographie
  - cybersecurite
  - analyse/forensique
  - malware
  - authentification
  - integrite
---

# Binary Digit (Bit)

> [!question] C'est quoi ?
> Un **bit** (contraction de *binary digit*) est la plus petite unité d'information en informatique et en théorie de l'information, représentant l'un des deux états binaires possibles : `0` (faux, off) ou `1` (vrai, on).

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le terme "bit" a été proposé par Claude Shannon en 1948 dans son article fondateur "A Mathematical Theory of Communication", bien que le concept de code binaire remonte à Gottfried Wilhelm Leibniz au 17ème siècle. Il est devenu la pierre angulaire de toute l'ère numérique.

## ⚙️ Caractéristiques Techniques
*   **Atomicité** : Le bit est l'unité d'information la plus fondamentale et indivisible.
*   **Dualité** : Il ne peut prendre que deux valeurs distinctes, généralement `0` ou `1`, qui peuvent représenter n'importe quel concept binaire (vrai/faux, marche/arrêt, haut/bas tension).
*   **Base de tout** : Tous les types de données numériques (nombres, texte, images, sons, vidéos) sont stockés et traités comme des séquences de bits.
*   **Groupement** : Les bits sont souvent regroupés en unités plus grandes pour former des informations utiles :
    *   Un **octet** (byte) est généralement composé de 8 bits.
    *   Un **mot** (word) est une séquence de bits traitée par le processeur (ex: 16, 32, 64 bits).

## 💡 Importance en Informatique et Cybersécurité
Le concept de bit est central pour comprendre le fonctionnement des systèmes numériques et la sécurité de l'information.

*   **Traitement de l'Information** :
    *   **Représentation des données** : Chaque caractère alphanumérique, pixel d'une image, ou échantillon sonore est codé par une combinaison spécifique de bits.
    *   **Opérations Logiques** : Les processeurs effectuent des calculs et des opérations logiques (AND, OR, XOR, NOT) bit par bit, formant la base de toute l'arithmétique et de la logique computationnelle.
    *   **Compression de données** : Les algorithmes de compression manipulent les patterns de bits pour réduire la taille des fichiers.

*   **Cybersécurité** :
    *   **Cryptographie** : Les algorithmes de chiffrement (AES, RSA) et les fonctions de hachage opèrent intensivement au niveau du bit. La sécurité d'un système cryptographique dépend de la difficulté à deviner ou manipuler les séquences de bits (clés de chiffrement, données chiffrées).
    *   **Analyse Forensique** : L'examen des données brutes sur un disque dur ou en mémoire se fait au niveau binaire pour récupérer des informations effacées ou cachées.
    *   **Malware et Exploits** : Les logiciels malveillants et les exploits fonctionnent souvent en manipulant des bits dans la mémoire ou les registres du processeur pour détourner l'exécution d'un programme.
    *   **Authentification** : Les mécanismes d'authentification (mots de passe, clés SSH) sont comparés bit par bit pour vérifier l'identité d'un utilisateur ou d'un système.
    *   **Contrôle d'Intégrité** : Des sommes de contrôle (checksums) ou des fonctions de hachage calculées sur des séquences de bits permettent de détecter toute altération, même minime, des données.