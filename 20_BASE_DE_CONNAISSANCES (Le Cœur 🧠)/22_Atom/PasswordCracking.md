---
tags:
  - attaque/hybride
  - cryptographie/salage-hachage
  - politique/exigences-complexite
  - cassage-mot-passe
  - cybersécurité/force-brute
  - authentification/multifacteur
aliases:
  - Cassage de mot de passe
  - Password Cracking
source:
  - null
cssclasses:
  - max
---

# Cassage de Mot de Passe

## 📥 Définition en une phrase
> Le cassage de mot de passe est le processus de récupération de mots de passe (souvent stockés sous forme hachée ou chiffrée) d'un système informatique, d'un fichier ou d'une connexion réseau, généralement dans le but d'obtenir un accès non autorisé.

## 🧠 Concepts Clés / Fonctionnement
*   **Techniques d'Attaque**:
    *   [[BruteForceAttack|Attaque par Force Brute]]: Essai systématique de toutes les combinaisons possibles de caractères jusqu'à trouver le mot de passe.
    *   [[DictionaryAttack|Attaque par Dictionnaire]]: Utilisation d'une liste prédéfinie de mots et de phrases courants comme mots de passe potentiels.
    *   [[RainbowTableAttack|Attaque par Table Arc-en-Ciel]]: Utilisation de tables précalculées pour inverser les fonctions de hachage de mots de passe, ce qui permet de trouver rapidement les mots de passe correspondant aux hachages.
    *   [[HybridAttack|Attaque Hybride]]: Combinaison d'attaques par dictionnaire et par force brute, en ajoutant des chiffres ou des symboles aux mots du dictionnaire.
    *   [[CredentialStuffing|Credential Stuffing]]: Réutilisation de paires identifiant/mot de passe compromises lors d'une [[DataBreach|fuite de données]] antérieure sur d'autres services.
*   **Cibles**: Généralement des [[PasswordHashing|hachages de mots de passe]] ou des mots de passe faibles non chiffrés.
*   **Objectif**: Obtenir un [[UnauthorizedAccess|accès non autorisé]] à des comptes, des systèmes ou des [[SensitiveData|données sensibles]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[DataBreach|Fuite de Données]]
*   [[IdentityTheft|Vol d'Identité]]
*   [[WeakPassword|Mots de Passe Faibles]]
*   [[PoorPasswordHashing|Mauvais Hachage de Mots de Passe]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[StrongPasswordPolicy|Politique de Mots de Passe Forts]]: Exiger des mots de passe longs, complexes et uniques.
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]: Ajout d'une ou plusieurs couches de vérification d'identité en plus du mot de passe.
*   [[PasswordHashing|Hachage et Salage des Mots de Passe]]: Utiliser des algorithmes de hachage robustes et des sels uniques pour chaque mot de passe afin de rendre les attaques par table arc-en-ciel inefficaces.
*   [[AccountLockoutPolicy|Politique de Verrouillage de Compte]]: Verrouiller un compte après un certain nombre d'échecs de connexion pour contrer les attaques par force brute.
*   [[PasswordManager|Gestionnaires de Mots de Passe]]: Encourager l'utilisation de gestionnaires de mots de passe pour générer et stocker des mots de passe forts et uniques.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]]: Surveiller les tentatives de connexion suspectes.

## 🔗 Notes Connexes
*   [[PasswordManagement|Gestion des Mots de Passe]]
*   [[CredentialStuffing|Credential Stuffing]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[Authentication|Authentification]]
*   [[HashFunction|Fonction de Hachage]]