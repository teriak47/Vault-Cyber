---
tags:
  - cryptographie/salage
  - hachage-mot-de-passe
  - gestion-des-mots-de-passe
  - securite/authentification
aliases:
  - Salage
  - Password Salting
source:
  - 
cssclasses:
  - max
---

# Salage (Salting)

## 📥 Définition en une phrase
> Le salage est une technique de sécurité qui consiste à ajouter une chaîne de caractères aléatoire et unique (le "sel") à un mot de passe avant de le hacher, afin d'augmenter la résistance aux attaques par dictionnaire et par tables arc-en-ciel.

## 🧠 Concepts Clés / Fonctionnement
*   **Renforcement du hachage** : Le sel est concaténé au mot de passe clair avant d'être passé à une [[HashingAlgorithm|fonction de hachage]] (par exemple, SHA-256, bcrypt, PBKDF2).
*   **Unicité** : Un sel différent est généré pour *chaque* mot de passe, même si plusieurs utilisateurs ont le même mot de passe. Cela signifie que deux utilisateurs ayant le même mot de passe auront des hachages complètement différents.
*   **Stockage du sel** : Le sel n'est pas secret et est généralement stocké en clair avec le hachage du mot de passe dans la base de données. Sa valeur aléatoire rend la tâche de l'attaquant plus difficile, même s'il connaît le sel.
*   **Protection contre les [[RainbowTable|Tables Arc-en-ciel]]** : Parce que chaque mot de passe a un sel unique, il n'est plus possible d'utiliser des tables précalculées pour trouver rapidement les mots de passe correspondants. Chaque hachage doit être craqué individuellement.
*   **Complexification des [[BruteForceAttack|Attaques par Force Brute]] et [[DictionaryAttack|Attaques par Dictionnaire]]** : Sans salage, un attaquant peut calculer le hachage d'un mot de passe courant une seule fois et le comparer à tous les hachages de la base de données. Avec le salage, l'attaquant doit calculer le hachage pour chaque mot de passe potentiel et pour *chaque* sel unique, multipliant considérablement le temps et les ressources nécessaires.

## 🛡️ Risques / Menaces Associés
*   [[RainbowTable|Attaques par Tables Arc-en-ciel]] (si le salage n'est pas utilisé ou mal implémenté)
*   [[BruteForceAttack|Attaques par Force Brute]] et [[DictionaryAttack|Attaques par Dictionnaire]] (moins efficaces, mais restent une menace sans autres [[SecurityControl|contrôles de sécurité]])
*   Fuite des mots de passe hachés (le salage réduit l'impact, mais ne l'élimine pas)

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utiliser le salage systématiquement** : Toujours combiner le [[PasswordHashing|hachage de mot de passe]] avec un salage.
*   **Sels uniques et aléatoires** : Chaque sel doit être généré de manière cryptographiquement sûre et être unique pour chaque mot de passe.
*   **Algorithmes robustes** : Combiner le salage avec des [[KeyDerivationFunction|fonctions de dérivation de clé (KDF)]] robustes et lentes comme [[PBKDF2|PBKDF2]], [[Bcrypt|Bcrypt]], [[Scrypt|Scrypt]] ou [[Argon2|Argon2]], qui sont conçues pour résister aux attaques par force brute modernes.
*   **Longueur du sel** : Un sel d'au moins 16 octets (128 bits) est généralement recommandé.

## 🔗 Notes Connexes
*   [[PasswordHashing|Hachage de Mot de Passe]]
*   [[HashingAlgorithm|Algorithme de Hachage]]
*   [[KeyDerivationFunction|Fonction de Dérivation de Clé (KDF)]]
*   [[RainbowTable|Tables Arc-en-ciel]]
*   [[BruteForceAttack|Attaque par Force Brute]]
*   [[DictionaryAttack|Attaque par Dictionnaire]]