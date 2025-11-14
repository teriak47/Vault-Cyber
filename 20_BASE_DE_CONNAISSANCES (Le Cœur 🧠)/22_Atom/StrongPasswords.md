---
tags:
  - securite/phrase-de-passe
  - authentification/multifacteur
  - authentification
  - securite/robustesse-mot-de-passe
aliases:
  - Mots de passe forts
  - Strong Passwords
source:
  - 
cssclasses:
  - max
---

# Mots de Passe Forts

## 📥 Définition en une phrase
> Un mot de passe fort est une chaîne de caractères complexe et difficile à deviner ou à casser, conçue pour protéger l'accès à un compte ou un système contre les tentatives d'authentification non autorisées.

## 🧠 Concepts Clés / Fonctionnement
*   **Longueur Minimale :** Idéalement, les mots de passe forts devraient avoir au moins 12 à 16 caractères pour augmenter l'espace de recherche lors d'une attaque par force brute.
*   **Complexité :** Intègrent une combinaison de majuscules, minuscules, chiffres et caractères spéciaux.
*   **Unicité :** Ne doit jamais être réutilisé sur différents comptes afin de limiter l'impact du [[CredentialStuffing|Credential Stuffing]] ou de fuites de données.
*   **Imprévisibilité :** Évitent les informations personnelles (noms, dates de naissance), les mots de dictionnaire et les séquences faciles.
*   **Rotation :** Bien que la rotation fréquente ne soit plus toujours recommandée, l'absence de réutilisation et l'utilisation de phrases de passe sont préférables.

## 🛡️ Risques / Menaces Associés
*   [[BruteForceAttack|Attaque par force brute]]
*   [[DictionaryAttack|Attaque par dictionnaire]]
*   [[CredentialStuffing|Credential Stuffing]]
*   [[Phishing|Hameçonnage]] (qui peut voler des mots de passe)
*   [[PasswordCracking|Cassage de mot de passe]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utilisation de Gestionnaires de Mots de Passe :** Outils comme [[PasswordManager|Bitwarden]] ou [[PasswordManager|LastPass]] génèrent et stockent des mots de passe complexes et uniques.
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] :** Ajoute une couche de sécurité supplémentaire, même si le mot de passe est compromis.
*   **[[PasswordPolicy|Politiques de Mots de Passe Robustes]] :** Implémentation de règles de complexité, de longueur et d'interdiction de mots de passe courants.
*   **Phrases de Passe :** Utilisation de plusieurs mots non liés pour créer une phrase longue et facile à retenir mais difficile à deviner.
*   **Éducation des Utilisateurs :** Sensibilisation à l'importance des mots de passe forts et aux bonnes pratiques.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[Hashing|Hachage]]
*   [[Salting|Salage]]
*   [[PasswordPolicy|Politique de Mots de Passe]]