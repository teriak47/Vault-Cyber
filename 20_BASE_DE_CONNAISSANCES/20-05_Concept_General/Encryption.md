---
tags:
aliases:
  - Chiffrement
  - Cryptography
  - Encryption
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Chiffrement

## 📥 Définition en une phrase
> Le chiffrement est le processus de transformation d'informations lisibles (texte en clair) en un format illisible (texte chiffré) à l'aide d'un algorithme et d'une clé cryptographique, afin d'assurer la protection des données et leur confidentialité.

## 🧠 Concepts Clés / Piliers
*   **Algorithmes de Chiffrement**: Des fonctions mathématiques complexes utilisées pour chiffrer et déchiffrer les données. Ils définissent la logique sous-jacente du processus.
*   **Clés Cryptographiques**: Des informations secrètes (chaînes de caractères) indispensables, utilisées par l'algorithme pour verrouiller et déverrouiller les données. La sécurité du chiffrement dépend directement de la robustesse de la clé.
*   **Chiffrement Symétrique**: Méthode utilisant la même clé pour l'chiffrement et le déchiffrement (ex: AES). Il est rapide et efficace pour les transferts de gros volumes de données.
*   **Chiffrement Asymétrique** (ou à clé publique): Emploie une paire de clés différentes (une clé publique et une clé privée) pour l'chiffrement et le déchiffrement (ex: RSA). Cette approche permet un échange sécurisé de clés symétriques et la signature numérique.
*   **Vecteur d'Initialisation (IV)**: Un bloc de données aléatoire utilisé conjointement avec la clé pour garantir l'unicité de chaque message chiffré, même si le texte en clair est identique, renforçant ainsi la sécurité.

## 💡 Importance en Cybersécurité
> Le chiffrement est une mesure de sécurité fondamentale pour garantir la confidentialité des données sensibles et prévenir l'accès non autorisé. Il protège les informations à la fois en transit (transmission) et au repos (stockage sécurisé), contribuant ainsi à la préservation de l'intégrité et au respect de la vie privée. En rendant les données illisibles sans la clé appropriée, il limite considérablement l'impact d'une violation de données et soutient la conformité légale avec des réglementations comme le RGPD.

## 🔗 Notes Connexes
*   Protection des Données
*   Confidentialité
*   Intégrité
*   Signature numérique
*   Hachage
*   Cryptographie
*   TLS
*   SSH
*   Gestion des Clés
*   Attaque par force brute
*   Vulnérabilité