---
tags:
  - cryptographie/proprietes-securite
  - cryptographie/selection-algorithme
  - attaque/canal-auxiliaire
  - cryptographie/asymetrique
  - cryptographie/gestion-cles
  - signature-numerique
aliases:
  - Cryptographie
  - Cryptography
source:
  - null
cssclasses:
  - max
---

# Cryptographie

## 📥 Définition en une phrase
> L'art et la science de sécuriser les communications et les données contre des entités malveillantes, en utilisant des principes mathématiques pour transformer l'information et garantir ses propriétés de sécurité.

## 🧠 Concepts Clés / Fonctionnement
* Les systèmes cryptographiques s'appuient sur des [[Algorithm|algorithmes]] complexes et des [[Key|clés]] secrètes pour chiffrer (rendre illisible) et déchiffrer (restaurer) les données.
* Elle vise à garantir la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]], l'[[Authentication|authentification]] et la [[NonRepudiation|non-répudiation]] des informations.
* Il existe deux catégories principales : la [[SymmetricCryptography|cryptographie symétrique]] (même clé pour chiffrer et déchiffrer) et la [[AsymmetricCryptography|cryptographie asymétrique]] (paire de clés publique/privée).
* Des [[CryptographicHashFunction|fonctions de hachage cryptographiques]] sont utilisées pour l'intégrité des données, générant une empreinte numérique unique.
* Les [[DigitalSignature|signatures numériques]] sont utilisées pour prouver l'authenticité et l'intégrité de l'origine d'un message ou d'un document.

## 🛡️ Risques / Menaces Associés
* [[BruteForceAttack|Attaque par force brute]] (tentative exhaustive de deviner les clés ou mots de passe).
* [[SideChannelAttack|Attaques par canaux auxiliaires]] (exploitation des fuites d'informations physiques comme le temps d'exécution ou la consommation électrique).
* [[KeyCompromise|Compromission de clé]] (perte ou vol de clés cryptographiques, rendant les données vulnérables).
* [[ChosenPlainTextAttack|Attaque à texte clair choisi]] (analyse d'un texte chiffré dont l'attaquant connaît ou a choisi le [[Cleartext|texte clair]] original).

## 💎 Mesures de Protection / Bonnes Pratiques
* [[AlgorithmSelection|Sélection d'algorithmes]] robustes et standardisés (ex: [[AdvancedEncryptionStandard|AES]], [[RivestShamirAdleman|RSA]], [[EllipticCurveCryptography|ECC]]).
* [[KeyManagement|Gestion sécurisée des clés]] (génération forte, stockage protégé, rotation régulière et révocation des clés compromises).
* Utilisation de [[SecureProtocol|protocoles sécurisés]] (ex: [[TransportLayerSecurity|TLS]], [[IPSecurity|IPsec]]) pour protéger les communications réseau.
* [[ImplementationSecurity|Implémentation sécurisée]] des primitives cryptographiques pour éviter les failles logicielles.

## 🔗 Notes Connexes
* [[SymmetricCryptography|Cryptographie Symétrique]]
* [[AsymmetricCryptography|Cryptographie Asymétrique]]
* [[CryptographicHashFunction|Fonction de Hachage Cryptographique]]
* [[DigitalSignature|Signature Numérique]]
* [[KeyManagement|Gestion des Clés]]
* [[QuantumCryptography|Cryptographie Quantique]]
* [[PostQuantumCryptography|Cryptographie Post-Quantique]]