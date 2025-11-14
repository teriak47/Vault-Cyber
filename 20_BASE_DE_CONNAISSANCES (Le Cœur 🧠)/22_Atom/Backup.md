---
tags:
  - types-sauvegarde/differentielle
  - types-sauvegarde/incrementielle
  - sauvegarde/immuable
  - planification/sauvegarde
  - strategie/sauvegarde-3-2-1
  - planification/reprise-sinistre
aliases:
  - Sauvegarde
  - Backup
source:
  - null
cssclasses:
  - max
---

# Sauvegarde

## 📥 Définition en une phrase
> Une sauvegarde est une copie des données informatiques, conservée séparément des données originales, dans le but de pouvoir les restaurer en cas de perte, de corruption ou de destruction des données primaires.

## 🧠 Concepts Clés / Fonctionnement
*   **Types de Sauvegarde** : [[FullBackup|Complète]] (toutes les données), [[IncrementalBackup|Incrémentielle]] (seulement les données modifiées depuis la dernière sauvegarde), [[DifferentialBackup|Différentielle]] (seulement les données modifiées depuis la dernière sauvegarde complète).
*   **Restauration** : Le processus de récupération des données à partir d'une sauvegarde pour les rendre à nouveau disponibles et utilisables.
*   **Règle du 3-2-1** : Avoir au moins **3** copies de données, sur **2** types de médias différents, avec **1** copie conservée hors site.
*   **RTO (Recovery Time Objective)** : Temps maximum admissible pendant lequel un système ou une application peut être hors service.
*   **RPO (Recovery Point Objective)** : Quantité maximale de données que l'on est prêt à perdre, mesurée en temps.

## 🛡️ Risques / Menaces Associés
*   [[DataLoss|Perte de données]] due à des défaillances matérielles, erreurs humaines ou logiciels malveillants.
*   [[Ransomware|Ransomware]] peut chiffrer non seulement les données primaires mais aussi les sauvegardes accessibles.
*   [[PhysicalDamage|Dommages physiques]] aux supports de stockage des sauvegardes.
*   [[CyberAttack|Cyberattaques]] ciblant spécifiquement les systèmes de sauvegarde pour entraver la récupération.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[RegularBackup|Sauvegardes régulières]] et automatisées pour minimiser la perte de données.
*   [[OffsiteStorage|Stockage hors site]] des sauvegardes pour se prémunir contre les sinistres locaux.
*   [[BackupEncryption|Chiffrement des sauvegardes]] pour protéger la confidentialité des données stockées.
*   [[RestoreTesting|Tests réguliers de restauration]] pour vérifier l'intégrité et l'opérabilité des sauvegardes.
*   [[AccessControl|Contrôle d'accès]] strict aux systèmes de sauvegarde pour prévenir les accès non autorisés.
*   Mise en œuvre du principe d'immuabilité (sauvegardes WORM - Write Once, Read Many).

## 🔗 Notes Connexes
*   [[BusinessContinuity|Continuité d'activité]]
*   [[DisasterRecovery|Reprise après sinistre]]
*   [[DataLossPrevention|Prévention de la perte de données]]
*   [[StorageAreaNetwork|SAN]]