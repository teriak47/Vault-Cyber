---
aliases:
  - Intégrité
  - Data Integrity
  - Information Integrity
archetype: definition
cssclasses:
  - max
tags:
  - definition
  - integrite
  - cybersecurite
  - modele/cia-triade
  - confidentialite
  - disponibilite
  - donnee
  - algorithme-hachage
  - signature-numerique
  - chiffrement/asymetrique
  - authentification
---

# Integrity

> [!question] C'est quoi ?
> L'intégrité, en cybersécurité, est le principe qui garantit que les données sont exactes, complètes et n'ont pas été modifiées de manière non autorisée, assurant ainsi leur fiabilité tout au long de leur cycle de vie et constituant l'un des piliers de la *triade CIA*.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le concept d'intégrité est fondamental à la sécurité de l'information. Sa formalisation comme composante essentielle de la *triade CIA* (Confidentialité, Intégrité, Disponibilité) a été popularisée à partir des années 1970 avec des modèles de sécurité comme le modèle Biba, spécifiquement conçu pour préserver l'intégrité des données en contrôlant l'accès en écriture. Il vise à protéger l'information contre toute altération, qu'elle soit intentionnelle ou accidentelle.

## 💡 Exemples Concrets
*   **Hachage (Hashing)** : L'utilisation de fonctions de hachage cryptographique (comme SHA-256 ou MD5) pour générer une empreinte numérique unique d'un ensemble de données. Si ne serait-ce qu'un seul bit de la donnée originale est modifié, l'empreinte générée sera complètement différente, révélant ainsi une altération de l'intégrité.
*   **Signatures Numériques (Digital Signatures)** : Basées sur la cryptographie asymétrique, les signatures numériques permettent de garantir l'authenticité de l'expéditeur et l'intégrité du contenu d'un message ou d'un document. Un récepteur peut vérifier que les données n'ont pas été modifiées après avoir été signées par l'émetteur légitime.