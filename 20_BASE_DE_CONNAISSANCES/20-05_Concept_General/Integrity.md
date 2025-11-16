---
tags:
aliases:
  - Intégrité
  - Data Integrity
  - Integrity
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Intégrité

## 📥 Définition en une phrase
> L'intégrité est l'assurance que les [[Data|données]] sont exactes, complètes et n'ont pas été modifiées de manière non autorisée ou accidentelle, garantissant leur fiabilité tout au long de leur [[DataLifecycle|cycle de vie]].

## 🧠 Concepts Clés / Piliers
*   **Non-altération des données**: Garantit que les [[InformationSecurity|informations]] restent dans leur état d'origine, sans modification malveillante ou involontaire.
*   **Exactitude et Complétude**: Assure que les [[Data|données]] sont précises et que toutes les informations pertinentes sont présentes, sans lacunes, à travers des mécanismes de [[DataValidation|validation des données]].
*   **[[Hashing|Fonctions de hachage]]**: Utilisées pour créer une empreinte numérique unique des [[Data|données]]. Toute modification des [[Data|données]] entraîne un hachage différent, signalant une [[DataCorruption|altération]].
*   **[[DigitalSignature|Signatures numériques]]**: Combinaison de [[Hashing|hachage]] et de [[Cryptography|cryptographie asymétrique]] pour vérifier l'authenticité de l'expéditeur et l'intégrité du [[Message|message]].
*   **[[AccessControl|Contrôles d'accès]]**: Limite l'accès et les permissions de modification aux seules personnes ou [[System|systèmes]] autorisés, en suivant le [[PrincipleOfLeastPrivilege|principe du moindre privilège]].

## 💡 Importance en Cybersécurité
> L'[[Integrity|intégrité]] est un pilier fondamental de la [[CIATriad|triade CIA]] et de la [[InformationSecurity|sécurité de l'information]] en général. Elle garantit la fiabilité et l'exactitude des [[Data|données]], ce qui est crucial pour la [[DecisionMaking|prise de décision]], la [[LegalCompliance|conformité réglementaire]] et la confiance des [[User|utilisateurs]]. Sans [[Integrity|intégrité]], les [[Data|données]] pourraient être altérées (par [[DataTampering|altération de données]], [[DataCorruption|corruption de données]], [[Malware|logiciels malveillants]] ou [[HumanError|erreur humaine]]), menant à des conséquences graves telles que des [[FinancialLoss|pertes financières]], des atteintes à la [[Reputation|réputation]] ou des échecs de [[System|système]]. Elle est également essentielle pour la [[NonRepudiation|non-répudiation]], assurant qu'une partie ne peut nier la création ou la réception d'une [[Data|donnée]].

## 🔗 Notes Connexes
*   [[Confidentiality|Confidentialité]]
*   [[Availability|Disponibilité]]
*   [[CIATriad|Triade CIA]]
*   [[NonRepudiation|Non-répudiation]]
*   [[DataTampering|Altération de données]]
*   [[DataCorruption|Corruption de données]]
*   [[DigitalSignature|Signature numérique]]
*   [[Hashing|Hachage]]
*   [[AccessControl|Contrôle d'accès]]
*   [[BackupAndRecovery|Sauvegarde et Récupération]]
*   [[Malware|Malware]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[Log|Journalisation d'audit]]
*   [[DataValidation|Validation des données]]