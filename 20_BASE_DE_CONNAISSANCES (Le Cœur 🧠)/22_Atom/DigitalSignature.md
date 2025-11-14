---
tags:
  - securite/non-repudiation
  - securite/certificat-numerique
  - risque/cle-privee-compromise
  - signature-numerique
  - cryptographie/asymetrique
  - cryptographie/fonction-hachage
aliases:
  - Signature numérique
  - Digital Signature
source:
  - null
cssclasses:
  - max
---

# Signature Numérique

## 📥 Définition en une phrase
> Une signature numérique est un mécanisme cryptographique qui permet de vérifier l'authenticité et l'intégrité de données ou de documents électroniques, assurant qu'ils proviennent d'une source connue et n'ont pas été altérés.

## 🧠 Concepts Clés / Fonctionnement
*   Utilise la [[AsymmetricEncryption|cryptographie asymétrique]] (paire de [[PublicKey|clé publique]] / [[PrivateKey|clé privée]]).
*   L'expéditeur calcule un [[HashFunction|hachage cryptographique]] (empreinte numérique) des données à signer, puis chiffre ce hachage avec sa [[PrivateKey|clé privée]]. C'est la signature numérique.
*   Le destinataire vérifie la signature en déchiffrant le hachage signé avec la [[PublicKey|clé publique]] de l'expéditeur, puis calcule indépendamment le hachage des données reçues. Si les deux hachages correspondent, la signature est valide.
*   Garantit la [[NonRepudiation|non-répudiation]] (l'expéditeur ne peut pas nier avoir signé), l'[[Integrity|intégrité]] des données (pas d'altération en transit) et l'[[Authenticity|authentification]] de l'origine.
*   Souvent adossée à une [[PublicKeyInfrastructure|infrastructure à clé publique (PKI)]] pour la gestion et la validation des [[DigitalCertificate|certificats numériques]] qui lient les clés publiques à leurs propriétaires.

## 🛡️ Risques / Menaces Associés
*   [[PrivateKeyCompromise|Compromission de la clé privée]] : Un attaquant ayant accès à la clé privée peut forger des signatures valides.
*   [[CertificateRevocation|Problèmes de révocation de certificat]] : Si un certificat compromis n'est pas révoqué à temps ou si la liste de révocation n'est pas consultée.
*   [[HashCollision|Collisions de hachage]] : L'utilisation d'un algorithme de hachage faible peut permettre à un attaquant de créer deux documents avec le même hachage.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Protéger rigoureusement la [[PrivateKey|clé privée]] avec des dispositifs comme les [[HardwareSecurityModule|HSM]], des mots de passe forts et une gestion d'accès stricte.
*   Utiliser des [[HashFunction|algorithmes de hachage]] et de chiffrement reconnus comme robustes (ex: SHA-256, RSA avec des longueurs de clés suffisantes).
*   Vérifier systématiquement la chaîne de confiance et l'état de révocation des [[DigitalCertificate|certificats numériques]] lors de la validation d'une signature.
*   Mettre en œuvre une politique de gestion du cycle de vie des clés et des certificats, incluant la [[CertificateRevocation|révocation]] et le renouvellement.

## 🔗 Notes Connexes
*   [[Cryptography|Cryptographie]]
*   [[AsymmetricEncryption|Chiffrement Asymétrique]]
*   [[HashFunction|Fonction de Hachage]]
*   [[PublicKeyInfrastructure|PKI (Infrastructure à Clé Publique)]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[NonRepudiation|Non-répudiation]]
*   [[Integrity|Intégrité]]
*   [[Authenticity|Authenticité]]