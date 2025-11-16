---
tags:
  - cryptographie
  - controle/securite
  - authentification
  - integrite
  - non-repudiation
aliases:
  - Signature numérique
  - Digital Signature
  - Signature électronique
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Signature Numérique

## 📥 Définition en une phrase
> Une [[DigitalSignature|signature numérique]] est un mécanisme [[Cryptography|cryptographique]] qui permet de vérifier l'[[Authentication|authenticité]] et l'[[Integrity|intégrité]] de données ou de documents électroniques, assurant qu'ils proviennent d'une source connue et n'ont pas été altérés.

## 🧠 Concepts Clés / Piliers
*   **Cryptographie Asymétrique**: Les [[DigitalSignature|signatures numériques]] reposent sur la [[AsymmetricEncryption|cryptographie asymétrique]], utilisant une paire de [[PublicKey|clés publique]] et [[PrivateKey|privée]] pour signer et vérifier.
*   **Processus de Signature**: L'expéditeur calcule un [[Hashing|hachage cryptographique]] (empreinte numérique) des données, puis [[Encryption|chiffre]] ce [[Hashing|hachage]] avec sa [[PrivateKey|clé privée]] pour créer la [[DigitalSignature|signature numérique]].
*   **Vérification et Garanties**: Le destinataire utilise la [[PublicKey|clé publique]] de l'expéditeur (souvent via un [[DigitalCertificate|certificat numérique]]) pour déchiffrer la [[DigitalSignature|signature]], puis compare le [[Hashing|hachage]] obtenu avec celui qu'il calcule indépendamment des données reçues. Cette correspondance garantit la [[NonRepudiation|non-répudiation]], l'[[Integrity|intégrité]] des données et l'[[Authentication|authenticité]] de l'origine.

## 💡 Importance en Cybersécurité
> La [[DigitalSignature|signature numérique]] est un pilier fondamental de la [[Cybersecurity|cybersécurité]] car elle établit la confiance dans les échanges de données et documents électroniques. Elle prévient la [[Tampering|falsification]] et l'[[Spoofing|usurpation d'identité]], essentielles pour les transactions légales, financières et les communications sensibles. Elle permet de s'assurer que les informations n'ont pas été modifiées depuis leur envoi et qu'elles proviennent bien de la source prétendue, un aspect vital pour l'[[InformationSecurity|intégrité de l'information]] et la [[DataProtection|protection des données]].

## 🔗 Notes Connexes
*   [[Cryptography|Cryptographie]]
*   [[AsymmetricEncryption|Cryptographie Asymétrique]]
*   [[Hashing|Fonction de Hachage]]
*   [[PublicKeyInfrastructure|Infrastructure à Clé Publique (PKI)]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[NonRepudiation|Non-répudiation]]
*   [[Integrity|Intégrité]]
*   [[Authentication|Authentification]]
*   [[PrivateKey|Clé Privée]]
*   [[PublicKey|Clé Publique]]
*   [[Encryption|Chiffrement]]
*   [[PrivateKeyCompromise|Compromission de Clé Privée]]
*   [[CertificateRevocation|Révocation de Certificat]]
*   [[HashCollision|Collision de Hachage]]
*   [[HardwareSecurityModule|Module de Sécurité Matériel (HSM)]]