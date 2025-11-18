---
tags:
  - cryptographie/symetrique
  - norme
  - algorithme
  - chiffrement
  - cryptographie
  - securite/donnees
  - confidentialite
aliases:
  - AES
  - Advanced Encryption Standard
  - Standard de Chiffrement Avancé
archetype: norme
source:
cssclasses:
  - max
---

# Advanced Encryption Standard (AES)

## 🎯 Objectif et Périmètre
L'[[AdvancedEncryptionStandard|Advanced Encryption Standard]] (AES) est un [[Algorithm|algorithme]] de [[Encryption|chiffrement]] symétrique par blocs, adopté comme norme de [[DataEncryption|chiffrement des données]] par le gouvernement des États-Unis et reconnu internationalement. Son objectif principal est d'assurer la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]] en les transformant en un format illisible (texte chiffré) qui ne peut être décrypté qu'avec une [[PrivateKey|clé]] secrète correspondante. L'AES est conçu pour être à la fois sécurisé et efficace sur une large gamme de matériels et de plateformes.

## 🔑 Principes Clés
L'AES est un chiffrement par blocs, ce qui signifie qu'il opère sur des blocs de [[Data|données]] de taille fixe (128 bits) et utilise la même [[PrivateKey|clé]] pour le [[Encryption|chiffrement]] et le [[Decryption|déchiffrement]]. Il est basé sur une structure appelée "réseau de substitution-permutation".
*   **Taille des Clés**: L'AES supporte des clés de 128, 192 ou 256 bits, déterminant le nombre de rondes de chiffrement et influençant la robustesse de la sécurité.
*   **Opérations**: Chaque ronde de chiffrement implique une série de transformations mathématiques sur le bloc de données, notamment des substitutions (SubBytes), des décalages de lignes (ShiftRows), des mélanges de colonnes (MixColumns) et l'ajout de la clé de ronde (AddRoundKey).
*   **Modes d'Opération**: Pour chiffrer des données plus grandes qu'un bloc ou pour adapter l'algorithme à des besoins spécifiques, l'AES est utilisé avec divers modes d'opération (par exemple, CBC, GCM, CTR) qui définissent comment l'algorithme de bloc est appliqué de manière répétée.

## 💪 Avantages et Cas d'Usage
L'AES est largement privilégié pour sa robustesse cryptographique et ses performances.
*   **Sécurité Éprouvée**: Malgré des années d'analyses intensives, l'AES reste résistant aux attaques connues lorsqu'il est correctement mis en œuvre. Sa sécurité est une pierre angulaire de la [[Cryptography|cyptographie]] moderne.
*   **Efficacité**: Sa conception permet une implémentation efficace en [[Software|logiciel]] et en [[Hardware|matériel]], ce qui en fait un choix idéal pour les applications nécessitant un traitement rapide du [[DataEncryption|chiffrement des données]].
*   **Ubiquité**: L'AES est omniprésent dans le [[DigitalEnvironment|monde numérique]]. On le retrouve dans :
    *   Les [[VirtualPrivateNetwork|VPN]] et le [[TransportLayerSecurity|TLS]] (anciennement [[SecureSocketLayer|SSL]]) pour sécuriser les communications.
    *   Le [[SecureStorage|stockage sécurisé]] de fichiers et de disques (ex: BitLocker, VeraCrypt).
    *   Les protocoles de [[WirelessSecurity|sécurité sans fil]] (ex: [[WirelessProtectedAccessTwo|WPA2]], [[WirelessProtectedAccessThree|WPA3]]).
    *   Les bases de données et les systèmes de [[Cloud|cloud computing]].

## 📜 Adoption et Standardisation
L'AES a été sélectionné par le [[NIST|National Institute of Standards and Technology]] (NIST) en 2001, succédant au [[DataEncryptionStandard|Data Encryption Standard]] (DES) jugé obsolète. Il est spécifié dans la publication FIPS PUB 197 du NIST et est également un standard ISO/IEC (ISO/IEC 18033-3). Cette [[Standard|standardisation]] a favorisé son adoption mondiale et sa confiance en tant qu'algorithme de chiffrement de référence.

## 🔗 Notes Connexes
*   **Type de chiffrement**: [[SymmetricEncryption|Chiffrement Symétrique]]
*   **Prédécesseur**: [[DataEncryptionStandard|Data Encryption Standard (DES)]]
*   **Gestion associée**: [[KeyManagement|Gestion des clés]]
*   **Domaine de sécurité**: [[DataProtection|Protection des données]]
*   **Framework d'application**: [[NISTSP80053|NIST SP 800-53]]