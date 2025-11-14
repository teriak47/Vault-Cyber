---
tags:
  - mot-de-passe-fort
  - complexite-mot-de-passe
  - unicité-mot-de-passe
  - Password
  - PasswordCracking
  - MultiFactorAuthentication
aliases:
  - Mot de passe fort
  - Mot de passe robuste
  - Strong Password
source:
  - null
cssclasses:
  - max
---

# Mot de passe fort

## 📥 Définition en une phrase
> Un mot de passe fort est une combinaison de caractères difficile à deviner ou à craquer, conçue pour protéger les [[Account|comptes]] et les [[Data|données]] contre les accès non autorisés, en maximisant sa longueur, sa complexité et son caractère unique.

## 🧠 Concepts Clés / Fonctionnement
*   **Longueur minimale** : Généralement recommandé d'avoir au moins 12 à 16 caractères pour augmenter la résistance aux [[PasswordCracking|attaques par cassage de mot de passe]].
*   **Complexité** : Inclut une combinaison de lettres majuscules et minuscules, de chiffres et de symboles.
*   **Unicité** : Chaque mot de passe doit être unique pour chaque [[OnlineServices|service en ligne]] ou compte, évitant ainsi le risque de [[CredentialStuffing|bourrage d'identifiants]] si un mot de passe est compromis.
*   **Absence de données personnelles** : Évite d'utiliser des informations facilement accessibles telles que noms, dates de naissance, ou mots courants trouvés dans les [[DictionaryAttack|dictionnaires]].
*   **Aléatoire** : Un mot de passe généré de manière aléatoire est intrinsèquement plus fort car il n'a pas de schéma prévisible.

## 🛡️ Risques / Menaces Associés
*   [[BruteForceAttack|Attaques par force brute]] : Les mots de passe faibles sont rapidement identifiés par des tentatives systématiques.
*   [[DictionaryAttack|Attaques par dictionnaire]] : Les mots de passe basés sur des mots courants sont vulnérables à cette méthode.
*   [[CredentialStuffing|Bourrage d'identifiants]] : Si un mot de passe est réutilisé sur plusieurs sites et qu'une [[DataBreach|fuite de données]] se produit.
*   [[PasswordSpraying|Diffusion de Mot de Passe]] : Attaque qui utilise un petit nombre de mots de passe courants contre un grand nombre de comptes.
*   [[RainbowTableAttack|Attaques par table arc-en-ciel]] : Permettent de retrouver des mots de passe hachés si ces derniers sont faibles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utilisation de [[MultiFactorAuthentication|MFA]] pour ajouter une couche de [[Security|sécurité]] supplémentaire, même si le mot de passe est compromis.
*   Implémentation de [[PasswordManager|gestionnaires de mots de passe]] pour générer, stocker et gérer des mots de passe complexes et uniques.
*   Mise en œuvre de politiques de [[AccountLockout|verrouillage de compte]] après un nombre défini de tentatives de connexion infructueuses.
*   Sensibilisation des utilisateurs aux bonnes pratiques de création et de gestion des mots de passe via la [[SecurityAwareness|sensibilisation à la sécurité]].
*   Côté serveur, l'utilisation du [[Hashing|hachage]] et du [[Salting|salage]] des mots de passe avant leur stockage.

## 🔗 Notes Connexes
*   [[Password|Mot de passe]]
*   [[Authentication|Authentification]]
*   [[SecurityControl|Contrôle de Sécurité]]
*   [[PasswordAttacks|Attaques de mots de passe]]