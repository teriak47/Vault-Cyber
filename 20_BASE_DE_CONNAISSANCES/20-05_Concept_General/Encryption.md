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
> Le [[Encryption|chiffrement]] est le [[Process|processus]] de transformation d'[[Cleartext|informations lisibles]] (texte en clair) en un [[Cleartext|format illisible]] (texte chiffré) à l'aide d'un [[Algorithm|algorithme]] et d'une [[CryptographicKey|clé cryptographique]], afin d'assurer la [[DataProtection|protection des données]] et leur [[Confidentiality|confidentialité]].

## 🧠 Concepts Clés / Piliers
*   **[[Algorithm|Algorithmes de Chiffrement]]**: Des fonctions mathématiques complexes utilisées pour [[Encryption|chiffrer]] et [[Decryption|déchiffrer]] les [[Data|données]]. Ils définissent la logique sous-jacente du processus.
*   **[[CryptographicKey|Clés Cryptographiques]]**: Des informations secrètes (chaînes de caractères) indispensables, utilisées par l'[[Algorithm|algorithme]] pour [[Encryption|verrouiller]] et [[Decryption|déverrouiller]] les [[Data|données]]. La [[Security|sécurité]] du [[Encryption|chiffrement]] dépend directement de la [[KeyStrength|robustesse de la clé]].
*   **[[SymmetricEncryption|Chiffrement Symétrique]]**: Méthode utilisant la même [[CryptographicKey|clé]] pour l'[[Encryption|chiffrement]] et le [[Decryption|déchiffrement]] (ex: [[AdvancedEncryptionStandard|AES]]). Il est rapide et efficace pour les [[DataTransfer|transferts de gros volumes de données]].
*   **[[AsymmetricEncryption|Chiffrement Asymétrique]]** (ou à [[PublicKeyCryptography|clé publique]]): Emploie une paire de [[CryptographicKey|clés]] différentes (une [[PublicKey|clé publique]] et une [[PrivateKey|clé privée]]) pour l'[[Encryption|chiffrement]] et le [[Decryption|déchiffrement]] (ex: [[RivestShamirAdleman|RSA]]). Cette approche permet un [[SecureKeyExchange|échange sécurisé de clés symétriques]] et la [[DigitalSignature|signature numérique]].
*   **[[InitializationVector|Vecteur d'Initialisation (IV)]]**: Un bloc de [[Data|données]] [[RandomData|aléatoire]] utilisé conjointement avec la [[CryptographicKey|clé]] pour garantir l'unicité de chaque [[Message|message chiffré]], même si le [[Cleartext|texte en clair]] est identique, renforçant ainsi la [[Security|sécurité]].

## 💡 Importance en Cybersécurité
> Le [[Encryption|chiffrement]] est une [[SecurityControl|mesure de sécurité]] fondamentale pour garantir la [[Confidentiality|confidentialité]] des [[SensitiveData|données sensibles]] et prévenir l'[[UnauthorizedAccess|accès non autorisé]]. Il protège les [[Data|informations]] à la fois en transit ([[DataTransmission|transmission]]) et au repos ([[SecureStorage|stockage sécurisé]]), contribuant ainsi à la [[DataIntegrity|préservation de l'intégrité]] et au respect de la [[Privacy|vie privée]]. En rendant les [[Data|données]] illisibles sans la [[CryptographicKey|clé appropriée]], il limite considérablement l'[[ImpactOfBreach|impact d'une violation de données]] et soutient la [[LegalCompliance|conformité légale]] avec des réglementations comme le [[GeneralDataProtectionRegulation|RGPD]].

## 🔗 Notes Connexes
*   [[DataProtection|Protection des Données]]
*   [[Confidentiality|Confidentialité]]
*   [[Integrity|Intégrité]]
*   [[DigitalSignature|Signature numérique]]
*   [[Hashing|Hachage]]
*   [[Cryptography|Cryptographie]]
*   [[TransportLayerSecurity|TLS]]
*   [[SecureShell|SSH]]
*   [[KeyManagement|Gestion des Clés]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[Vulnerability|Vulnérabilité]]