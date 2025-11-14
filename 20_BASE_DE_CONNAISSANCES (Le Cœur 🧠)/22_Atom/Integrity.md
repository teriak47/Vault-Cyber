---
tags:
  - gestion-donnees/validation
  - securite/verification-donnees
  - securite/integrite
  - securite/triade-cia
aliases:
  - Intégrité
  - Data Integrity
cssclasses:
  - max
---

# Intégrité

## 📥 Définition en une phrase
> L'intégrité est l'assurance que les données sont exactes, complètes et n'ont pas été modifiées de manière non autorisée ou accidentelle, garantissant leur fiabilité tout au long de leur cycle de vie.

## 🧠 Concepts Clés / Fonctionnement
*   **Non-altération des données** : Garantit que les informations restent dans leur état d'origine, sans modification malveillante ou involontaire.
*   **Exactitude et Complétude** : Assure que les données sont précises et que toutes les informations pertinentes sont présentes, sans lacunes.
*   **Fonctions de hachage** : Utilisées pour créer une empreinte numérique unique des données. Toute modification des données entraîne un hachage différent, signalant une altération.
*   **Signatures numériques** : Combinaison de hachage et de cryptographie asymétrique pour vérifier l'authenticité de l'expéditeur et l'intégrité du message.
*   **Contrôles d'accès** : Limite l'accès et les permissions de modification aux seules personnes ou systèmes autorisés.

## 🛡️ Risques / Menaces Associés
*   [[DataTampering|Altération des données]]
*   [[InsiderThreat|Menace interne]] (modification intentionnelle ou non)
*   [[Malware|Malware]] (virus, ransomware pouvant corrompre des fichiers)
*   [[UnauthorizedAccess|Accès non autorisé]] (conduisant à des modifications non désirées)
*   [[DataCorruption|Corruption de données]] (erreurs système, défaillances matérielles)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Hashing|Utilisation de fonctions de hachage]] (MD5, SHA-256) pour la vérification des fichiers.
*   [[DigitalSignature|Implémentation de signatures numériques]] pour l'authentification et l'intégrité des documents et logiciels.
*   [[AccessControl|Mise en œuvre de contrôles d'accès]] robustes (RBAC, ABAC) avec le principe du moindre privilège.
*   [[BackupAndRecovery|Stratégies de sauvegarde et de récupération]] régulières et testées pour restaurer les données en cas d'altération.
*   [[AuditLogging|Journalisation d'audit]] et monitoring pour détecter les tentatives de modification non autorisées.
*   [[DataValidation|Validation des données]] à l'entrée et en interne pour s'assurer de leur conformité.

## 🔗 Notes Connexes
*   [[Confidentiality|Confidentialité]]
*   [[Availability|Disponibilité]]
*   [[Cryptography|Cryptographie]]
*   [[NonRepudiation|Non-répudiation]]