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
> Le hachage est un processus cryptographique qui transforme des données de taille arbitraire en une chaîne de caractères de taille fixe, appelée valeur de hachage, condensat ou empreinte numérique, de manière irréversible.

## 🧠 Concepts Clés / Piliers
*   **Fonction à sens unique (Irréversibilité)**: Le hachage est conçu pour être un processus à sens unique ; il est extrêmement difficile, voire impossible, de retrouver les données originales à partir de la valeur de hachage seule.
*   **Output de taille fixe**: Quelle que soit la taille de l'entrée (un seul octet ou un fichier entier), la sortie (la valeur de hachage) aura toujours une longueur prédéterminée.
*   **Déterminisme**: La même entrée produira toujours la même valeur de hachage. Une modification, même minime, de l'entrée entraînera une valeur de hachage complètement différente (effet avalanche).
*   **Résistance aux collisions**: Une bonne fonction de hachage cryptographique doit rendre extrêmement difficile la découverte de deux entrées différentes qui produisent la même valeur de hachage, ce qui protège contre les attaques par collision.
*   **Algorithmes courants**: Des algorithmes comme MD5 et SHA-1 sont considérés comme obsolètes pour la sécurité en raison de vulnérabilités connues, tandis que SHA-256 et SHA-3 sont actuellement considérés comme robustes.
*   **Renforcement pour les mots de passe**: Pour le stockage sécurisé des mots de passe, le hachage doit être combiné avec des techniques comme le salage (ajout d'une valeur aléatoire unique) et l'utilisation de fonctions de dérivation de clé (KDF) telles qu'Argon2, bcrypt ou scrypt, qui sont conçues pour être coûteuses en calcul.

## 💡 Importance en Cybersécurité
> Le hachage est fondamental en cybersécurité pour garantir l'intégrité des données et la sécurité des authentifications. Il permet de vérifier qu'un fichier ou un message n'a pas été altéré (altération de données) en comparant son hachage avec une référence connue. Dans le cadre de la gestion des mots de passe, le hachage protège les identifiants des utilisateurs en stockant des représentations irréversibles plutôt que les mots de passe en texte clair, réduisant ainsi l'impact d'une fuite de données. Cependant, une implémentation faible ou l'utilisation d'algorithmes obsolètes expose les systèmes à des menaces comme les attaques par table arc-en-ciel ou les attaques par force brute, d'où l'importance cruciale de techniques de renforcement et de l'utilisation de fonctions de hachage robustes.

## 🔗 Notes Connexes
*   Cryptographie
*   Signature numérique
*   Sécurité des mots de passe
*   Somme de contrôle
*   Intégrité des données
*   Vulnérabilité