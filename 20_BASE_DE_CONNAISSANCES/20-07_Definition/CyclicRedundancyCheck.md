---
tags:
  - definition
  - vocabulaire
  - erreur
aliases:
  - Vérification de Redondance Cyclique
  - CRC
archetype: definition
cssclasses:
  - max
---

# CyclicRedundancyCheck

> [!question] C'est quoi ?
> La vérification de redondance cyclique (CRC) est une méthode de détection d'erreurs utilisée pour vérifier l'intégrité des données transmises ou stockées, en s'assurant qu'aucune altération accidentelle n'a eu lieu.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le terme vient de l'anglais "Cyclic Redundancy Check". Il s'agit d'un algorithme mathématique de somme de contrôle inventé par W. Wesley Peterson en 1961. Il est devenu un standard pour la détection fiable d'erreurs dans les signaux numériques en raison de sa simplicité de mise en œuvre et de sa capacité à détecter un large éventail d'erreurs.

## 💡 Exemples Concrets
*   **Vérification de trames réseau** : Dans les trames Ethernet, une séquence de vérification de trame (FCS) est calculée à l'aide d'un CRC pour s'assurer que les paquets de données n'ont pas été corrompus pendant la transmission sur un réseau.
*   **Intégrité des fichiers** : De nombreux formats de fichiers compressés, tels que les archives ZIP ou RAR, utilisent des CRC pour vérifier que les fichiers extraits sont identiques aux fichiers originaux et n'ont pas subi de corruption de données.

## Notes Connexes
*   Somme de contrôle
*   Séquence de Vérification de Trame
*   Corruption de Données