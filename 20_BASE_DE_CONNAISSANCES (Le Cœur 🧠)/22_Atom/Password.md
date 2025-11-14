---
tags:
  - cybersécurité/attaques-mots-de-passe
  - securite/stockage-hache
  - authentification
  - gestion-des-mots-de-passe
aliases:
  - Mot de passe
  - Password
cssclasses:
  - max
---

# Mot de passe

## 📥 Définition en une phrase
> Une chaîne de caractères secrète utilisée pour vérifier l'identité d'un utilisateur ou autoriser l'accès à un système, un service ou une ressource.

## 🧠 Concepts Clés / Fonctionnement
*   **Authentification**: Les mots de passe sont le mécanisme le plus courant pour prouver qu'un utilisateur est bien celui qu'il prétend être.
*   **Stockage sécurisé**: Pour des raisons de sécurité, les mots de passe ne doivent jamais être stockés en clair. Ils sont généralement hachés (transformés en une valeur unique et irréversible) et souvent salés (ajout d'une valeur aléatoire unique avant le hachage).
*   **Complexité**: Un mot de passe fort doit être long, contenir une combinaison de lettres majuscules et minuscules, de chiffres et de symboles spéciaux pour résister aux attaques.
*   **Unicité**: L'utilisation du même mot de passe pour plusieurs comptes (réutilisation) est une pratique dangereuse qui peut mener à des compromissions en cascade.

## 🛡️ Risques / Menaces Associés
*   [[BruteForceAttack|Attaque par force brute]]: Tentative systématique de deviner un mot de passe.
*   [[DictionaryAttack|Attaque par dictionnaire]]: Utilisation d'une liste de mots courants ou de mots de passe précédemment compromis.
*   [[CredentialStuffing|Credential Stuffing]]: Utilisation de paires nom d'utilisateur/mot de passe volées sur un site pour tenter d'accéder à d'autres comptes.
*   [[Phishing|Hameçonnage]]: Ingénierie sociale pour inciter les utilisateurs à révéler leurs mots de passe.
*   [[Keylogger|Keylogger]]: Logiciel malveillant enregistrant les frappes clavier pour capturer les mots de passe.
*   [[PasswordCracking|Cassage de mot de passe]]: Utilisation de techniques et d'outils pour déchiffrer des mots de passe hachés.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]: Ajout d'une couche de sécurité supplémentaire au-delà du simple mot de passe.
*   [[PasswordPolicy|Politique de mots de passe]]: Établir des règles strictes sur la longueur, la complexité, l'expiration et la réutilisation des mots de passe.
*   [[PasswordManager|Gestionnaire de mots de passe]]: Utiliser un outil pour générer et stocker des mots de passe forts et uniques pour chaque service.
*   [[Hashing|Hashing]] et [[Salting|Salage]]: Méthodes de stockage sécurisé des mots de passe dans les bases de données.
*   Éducation des utilisateurs: Sensibiliser aux risques et aux meilleures pratiques pour la création et la gestion des mots de passe.
*   Changement régulier des mots de passe: Bien que controversé, le changement périodique peut être bénéfique si les mots de passe ne sont pas simplement modifiés de manière incrémentale.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[Authorization|Autorisation]]
*   [[Hashing|Hashing]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]