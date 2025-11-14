---
tags:
  - somme-controle
  - securite/verification-integrite
  - cryptographie/resistance-collision
  - algorithme/crc
  - protection/controle-integrite
  - cryptographie/fonction-hachage
aliases:
  - Somme de contrôle
  - Check Sum
source:
  - null
cssclasses:
  - max
---

# Checksum (Somme de contrôle)

## 📥 Définition en une phrase
> Un checksum, ou somme de contrôle, est une petite valeur numérique calculée à partir d'un bloc de données, utilisée principalement pour détecter les erreurs de transmission ou de stockage et vérifier l'intégrité des données.

## 🧠 Concepts Clés / Fonctionnement
*   Le principe consiste à appliquer un algorithme (fonction de hachage) sur des données pour produire une valeur de taille fixe, la somme de contrôle.
*   Cette somme est ensuite stockée ou transmise aux côtés des données originales.
*   Lorsqu'un système reçoit les données, il recalcule la somme de contrôle à partir des données reçues et compare le résultat avec la somme de contrôle originale.
*   Si les deux sommes correspondent, il est probable que les données n'ont pas été altérées ou corrompues. Dans le cas contraire, une erreur est détectée.
*   Les algorithmes varient en complexité et en robustesse, allant des simples sommes arithmétiques aux [[CyclicRedundancyCheck|CRC]] (Cyclic Redundancy Check) et aux [[CryptographicHashFunction|fonctions de hachage cryptographiques]] comme SHA-256.

## 🛡️ Risques / Menaces Associés
*   [[DataCorruption|Corruption de données]] : Le risque principal que le checksum vise à atténuer, mais il ne peut que détecter, pas corriger.
*   [[DataIntegrityAttack|Altération intentionnelle des données]] : Si la fonction de hachage utilisée n'est pas cryptographique, un attaquant peut modifier les données et recalculer un nouveau checksum valide, rendant l'attaque indétectable par ce seul mécanisme.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser des [[CryptographicHashFunction|fonctions de hachage cryptographiques]] (ex: [[SecureHashAlgorithm|SHA-256]], SHA-3) pour la vérification d'intégrité dans des contextes de sécurité, car elles sont conçues pour être résistantes aux collisions et aux préimages.
*   Vérifier systématiquement les checksums des fichiers téléchargés ou des données reçues, surtout pour les logiciels critiques ou les mises à jour.
*   Intégrer la vérification de checksum dans les protocoles de communication pour s'assurer que les paquets de données arrivent intacts.

## 🔗 Notes Connexes
*   [[DataIntegrity|Intégrité des Données]]
*   [[ErrorDetection|Détection d'Erreurs]]
*   [[Hashing|Hachage]]
*   [[DigitalSignature|Signature Numérique]]