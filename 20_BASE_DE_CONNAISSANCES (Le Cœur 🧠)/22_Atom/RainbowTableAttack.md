---
tags:
  - attaque/table-arc-en-ciel
  - cryptographie/compromis-temps-memoire
  - cybersécurité/attaques-mots-de-passe
  - hachage-mot-de-passe
aliases:
  - Attaque par table arc-en-ciel
  - Rainbow Table Attack
source:
  - 
cssclasses:
  - max
---

# Attaque par Table Arc-en-ciel

## 📥 Définition en une phrase
> L'attaque par table arc-en-ciel est une méthode de [[PasswordCracking|cassage de mot de passe]] qui utilise des tables précalculées (tables arc-en-ciel) pour inverser rapidement des fonctions de hachage et retrouver les mots de passe originaux, capitalisant sur un compromis temps-mémoire.

## 🧠 Concepts Clés / Fonctionnement
*   **Précalcul des Hashes**: Des tables géantes sont construites à l'avance, contenant des millions de hachages de mots de passe possibles, liés à leurs mots de passe en clair correspondants.
*   **Chaînes de Réduction**: Les tables arc-en-ciel sont des ensembles de "chaînes" (sequences) où chaque élément est un mot de passe en clair suivi de son hachage, puis ce hachage est transformé en un nouveau mot de passe en clair via une fonction de réduction, et ainsi de suite.
*   **Compromis Temps-Mémoire**: Plutôt que de calculer les hachages à la volée (comme dans une [[BruteForceAttack|attaque par force brute]] classique), l'attaquant stocke un grand volume de données (les tables) pour réduire considérablement le temps nécessaire au craquage.
*   **Efficacité**: Particulièrement efficace contre les fonctions de hachage simples ou non salées, où un même mot de passe produira toujours le même hachage.

## 🛡️ Risques / Menaces Associés
*   [[CredentialCompromise|Compromission d'identifiants]]
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[DataBreach|Fuite de données]] (si les mots de passe hachés sont exposés)

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Salage des Mots de Passe**: L'ajout d'une chaîne aléatoire unique (sel) à chaque mot de passe avant le hachage rend les tables arc-en-ciel inefficaces. Chaque mot de passe, même identique, produira un hachage unique grâce au sel. Voir [[PasswordHashing|Hachage de mot de passe]].
*   **Utilisation de Fonctions de Hachage Robustes**: Privilégier des algorithmes de hachage lents et résistants à la force brute, comme [[Bcrypt]], [[Scrypt]], [[Argon2]] ou [[PBKDF2]], qui augmentent le temps de calcul nécessaire pour le hachage et le craquage.
*   **Politiques de Mots de Passe Forts**: Exiger des mots de passe longs, complexes et uniques pour rendre le précalcul de toutes les combinaisons possibles impraticable.
*   [[MultiFactorAuthentication|MFA]]: Ajoute une couche de sécurité supplémentaire, protégeant même si un mot de passe est compromis via une table arc-en-ciel.

## 🔗 Notes Connexes
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[PasswordHashing|Hachage de mot de passe]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[DictionaryAttack|Attaque par dictionnaire]]
*   [[Bcrypt|Bcrypt]]
*   [[Argon2|Argon2]]