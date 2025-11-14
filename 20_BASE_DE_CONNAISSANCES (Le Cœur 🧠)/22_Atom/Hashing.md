---
tags:
  - cryptographie/fonction-hachage
  - cryptographie/derivation-cle
  - resistance/collision
  - hachage-mot-de-passe
  - cryptographie/salage
  - attaque/table-arc-en-ciel
aliases:
  - Hachage
  - Fonction de Hachage
source:
  - null
cssclasses:
  - max
---

# Hachage (Hashing)

## 📥 Définition en une phrase
> Le hachage est un processus cryptographique qui transforme des données de taille arbitraire en une chaîne de caractères de taille fixe, appelée valeur de hachage, condensat ou empreinte numérique, de manière irréversible.

## 🧠 Concepts Clés / Fonctionnement
*   **Fonction à sens unique :** Le processus de hachage est conçu pour être irréversible ; il est extrêmement difficile de retrouver les données originales à partir de la valeur de hachage seule.
*   **Output de taille fixe :** Quelle que soit la taille de l'entrée (un seul caractère ou un fichier entier), la sortie (la valeur de hachage) aura toujours une longueur prédéterminée.
*   **Déterministe :** La même entrée produira toujours la même valeur de hachage. Une modification, même minime, de l'entrée entraînera une valeur de hachage complètement différente (effet avalanche).
*   **Résistance aux collisions :** Une bonne fonction de hachage doit rendre extrêmement difficile la découverte de deux entrées différentes qui produisent la même valeur de hachage (collision).
*   **Algorithmes courants :** On trouve des algorithmes comme [[MessageDigest5|MD5]] (obsolète pour la sécurité), [[SecureHashAlgorithm|SHA-1]] (obsolète), [[SecureHashAlgorithm2|SHA-256]] et [[SecureHashAlgorithm3|SHA-3]] (actuellement robustes).

## 🛡️ Risques / Menaces Associés
*   [[CollisionAttack|Attaque par collision]] : Pour les algorithmes faibles (ex: MD5, SHA-1), il est possible de trouver deux entrées différentes produisant le même hash, compromettant l'intégrité.
*   [[RainbowTable|Tables arc-en-ciel]] : Base de données précalculées de hachages, utilisées pour retrouver des mots de passe à partir de leurs hachages.
*   [[BruteForceAttack|Attaques par force brute]] : Si le hachage est utilisé pour des mots de passe sans mécanismes de renforcement (comme le [[Salt|salage]] ou le [[KeyDerivationFunction|KDF]]), il peut être vulnérable à la recherche exhaustive.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utiliser des algorithmes robustes :** Privilégier des fonctions de hachage cryptographiques modernes et éprouvées comme SHA-256, SHA-3, Argon2, bcrypt ou scrypt pour le stockage des mots de passe.
*   **[[Salt|Salage]] des mots de passe :** Ajouter une chaîne aléatoire unique ("sel") à chaque mot de passe avant de le hacher, ce qui rend les attaques par tables arc-en-ciel inefficaces.
*   **[[KeyDerivationFunction|Fonctions de dérivation de clé (KDF)]] :** Utiliser des KDFs qui sont intentionnellement lentes et consomment beaucoup de ressources (ex: Argon2, bcrypt, scrypt) pour rendre les attaques par force brute ou dictionnaire plus coûteuses.
*   **Vérification d'intégrité :** Utiliser le hachage pour vérifier l'intégrité des fichiers téléchargés ou des données stockées, en comparant la valeur de hachage calculée à une valeur de référence.

## 🔗 Notes Connexes
*   [[Cryptography|Cryptographie]]
*   [[DigitalSignature|Signature Numérique]]
*   [[PasswordSecurity|Sécurité des Mots de Passe]]
*   [[Checksum|Checksum]]