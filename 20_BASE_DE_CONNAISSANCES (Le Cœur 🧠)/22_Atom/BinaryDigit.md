---
tags:
  - cybersecurite/attaque/inversion-bit
  - informatique/representation-donnees
  - informatique/systeme-binaire
  - informatique-fondamentale/bit
  - information/unite-base
  - somme-controle
aliases:
  - Chiffre binaire
  - bit
  - Binary digit
source:
  - Connaissance générale
cssclasses:
  - max
---

# Chiffre Binaire (Bit)

## 📥 Définition en une phrase
> Le chiffre binaire, communément appelé bit, est l'unité d'information la plus fondamentale en informatique et en télécommunications, ne pouvant prendre que deux valeurs distinctes, généralement représentées par 0 ou 1.

## 🧠 Concepts Clés / Fonctionnement
*   **Unité Fondamentale**: Représente l'état le plus simple d'une information numérique, servant de base à toute donnée traitée par un ordinateur.
*   **Deux États**: Un bit peut être dans l'un de deux états mutuellement exclusifs, souvent interprétés comme "vrai/faux", "ouvert/fermé", "haut/bas" ou "0/1".
*   **Représentation Numérique**: Les combinaisons de bits permettent de représenter des nombres, des caractères, des images, des sons et des instructions. Par exemple, un groupe de 8 bits forme un [[Byte|octet]].
*   **Système Binaire**: Le bit est l'élément constitutif du système de numération binaire (base 2), essentiel au fonctionnement interne des ordinateurs.

## 🛡️ Risques / Menaces Associés
*   [[DataCorruption|Corruption de Données]]: Des erreurs dans la transmission ou le stockage des bits peuvent altérer l'intégrité des données.
*   [[BitFlippingAttack|Attaque par inversion de bit]]: Tentative malveillante de modifier des bits dans la mémoire ou la transmission de données.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[ErrorDetectionAndCorrection|Détection et Correction d'Erreurs]]: Utilisation de codes comme les codes de Hamming ou les contrôles de parité pour identifier et corriger les altérations de bits.
*   [[Checksum|Somme de Contrôle]]: Calcul et vérification de valeurs pour s'assurer de l'intégrité des blocs de données.
*   [[DataIntegrity|Intégrité des Données]]: Implémentation de mécanismes pour garantir que les bits stockés ou transmis restent inchangés et précis.

## 🔗 Notes Connexes
*   [[Byte|Octet]]
*   [[DataRepresentation|Représentation des Données]]
*   [[BinaryCode|Code Binaire]]