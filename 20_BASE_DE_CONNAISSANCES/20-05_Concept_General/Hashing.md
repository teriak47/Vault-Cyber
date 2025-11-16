---
tags:
aliases:
  - Hachage
  - Fonction de Hachage
  - Hashing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Hachage (Hashing)

## 📥 Définition en une phrase
> Le hachage est un processus [[Cryptography|cryptographique]] qui transforme des [[Data|données]] de taille arbitraire en une chaîne de caractères de taille fixe, appelée valeur de hachage, condensat ou empreinte numérique, de manière irréversible.

## 🧠 Concepts Clés / Piliers
*   **Fonction à sens unique (Irréversibilité)**: Le hachage est conçu pour être un processus [[OneWayFunction|à sens unique]] ; il est extrêmement difficile, voire impossible, de retrouver les [[Data|données]] originales à partir de la valeur de hachage seule.
*   **Output de taille fixe**: Quelle que soit la taille de l'entrée (un seul [[Byte|octet]] ou un [[File|fichier]] entier), la [[Output|sortie]] (la valeur de hachage) aura toujours une longueur prédéterminée.
*   **Déterminisme**: La même entrée produira toujours la même valeur de hachage. Une modification, même minime, de l'entrée entraînera une valeur de hachage complètement différente (effet [[AvalancheEffect|avalanche]]).
*   **Résistance aux [[Collision|collisions]]**: Une bonne [[CryptographicHashFunction|fonction de hachage cryptographique]] doit rendre extrêmement difficile la découverte de deux entrées différentes qui produisent la même valeur de hachage, ce qui protège contre les [[CollisionAttack|attaques par collision]].
*   **Algorithmes courants**: Des algorithmes comme [[MessageDigest5|MD5]] et [[SecureHashAlgorithm|SHA-1]] sont considérés comme obsolètes pour la [[Security|sécurité]] en raison de [[Vulnerability|vulnérabilités]] connues, tandis que [[SecureHashAlgorithm2|SHA-256]] et [[SecureHashAlgorithm3|SHA-3]] sont actuellement considérés comme robustes.
*   **Renforcement pour les mots de passe**: Pour le stockage sécurisé des [[Password|mots de passe]], le hachage doit être combiné avec des techniques comme le [[Salting|salage]] (ajout d'une valeur aléatoire unique) et l'utilisation de [[KeyDerivationFunction|fonctions de dérivation de clé (KDF)]] telles qu'Argon2, bcrypt ou scrypt, qui sont conçues pour être coûteuses en calcul.

## 💡 Importance en Cybersécurité
> Le hachage est fondamental en [[Cybersecurity|cybersécurité]] pour garantir l'[[Integrity|intégrité]] des [[Data|données]] et la [[Security|sécurité]] des [[Authentication|authentifications]]. Il permet de vérifier qu'un [[File|fichier]] ou un message n'a pas été altéré ([[Tampering|altération de données]]) en comparant son hachage avec une référence connue. Dans le cadre de la [[Password|gestion des mots de passe]], le hachage protège les [[Credential|identifiants]] des [[User|utilisateurs]] en stockant des représentations irréversibles plutôt que les mots de passe en [[Cleartext|texte clair]], réduisant ainsi l'impact d'une [[DataBreach|fuite de données]]. Cependant, une implémentation faible ou l'utilisation d'algorithmes obsolètes expose les [[System|systèmes]] à des [[Threat|menaces]] comme les [[RainbowTableAttack|attaques par table arc-en-ciel]] ou les [[BruteForceAttack|attaques par force brute]], d'où l'importance cruciale de techniques de renforcement et de l'utilisation de [[RobustHashingAlgorithm|fonctions de hachage robustes]].

## 🔗 Notes Connexes
*   [[Cryptography|Cryptographie]]
*   [[DigitalSignature|Signature numérique]]
*   [[PasswordSecurity|Sécurité des mots de passe]]
*   [[Checksum|Somme de contrôle]]
*   [[DataIntegrity|Intégrité des données]]
*   [[Vulnerability|Vulnérabilité]]