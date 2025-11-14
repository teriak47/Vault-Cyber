---
tags:
  - cybersécurité/bourrage-identifiants
  - securite/politique-mot-de-passe
  - cybersécurité/attaques-mots-de-passe
  - gestion-des-mots-de-passe
aliases:
  - Attaques de mots de passe
  - Password Attacks
cssclasses:
  - max
---

# Attaques de Mots de Passe

## 📥 Définition en une phrase
> Les attaques de mots de passe désignent un ensemble de techniques utilisées par les acteurs malveillants pour découvrir, deviner ou contourner les mots de passe afin d'obtenir un [[UnauthorizedAccess|accès non autorisé]] à des systèmes, des comptes ou des données.

## 🧠 Concepts Clés / Fonctionnement
*   **[[BruteForceAttack|Attaque par force brute]]**: Tentative systématique et automatisée de toutes les combinaisons possibles de caractères jusqu'à ce que le mot de passe correct soit trouvé.
*   **[[DictionaryAttack|Attaque par dictionnaire]]**: Utilisation d'une liste prédéfinie de mots, de phrases et de mots de passe couramment utilisés pour tenter de deviner le mot de passe.
*   **[[CredentialStuffing|Credential stuffing]]**: Réutilisation de paires nom d'utilisateur/mot de passe obtenues lors de [[DataBreach|fuites de données]] antérieures sur d'autres services, en pariant que les utilisateurs réutilisent leurs mots de passe.
*   **[[RainbowTableAttack|Attaque par table arc-en-ciel]] (Rainbow Table Attack)**: Utilisation de tables de hachage précalculées pour inverser rapidement les hachages de mots de passe et retrouver le mot de passe original.
*   **Devinettes / Social Engineering ([[SocialEngineering|Ingénierie Sociale]])**: Tentatives de deviner des mots de passe basées sur des informations personnelles accessibles publiquement ou par le biais de techniques comme le [[Phishing|hameçonnage]] pour inciter les utilisateurs à révéler leurs identifiants.

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès non autorisé]] aux systèmes et aux données.
*   [[DataBreach|Fuite de données]] et exposition d'[[SensitiveData|informations sensibles]].
*   [[IdentityTheft|Usurpation d'identité]].
*   Perte de réputation et de confiance pour les organisations.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour ajouter une couche de sécurité supplémentaire.
*   Mise en œuvre d'une [[StrongPasswordPolicy|Politique de mots de passe forts]] (longueur, complexité, renouvellement régulier).
*   Utilisation de [[PasswordManager|gestionnaires de mots de passe]] pour générer et stocker des mots de passe uniques et complexes.
*   Implémentation de mécanismes de [[AccountLockout|verrouillage de compte]] après un nombre défini de tentatives infructueuses.
*   Application de techniques de [[PasswordHashing|hachage de mots de passe]] robustes avec salage côté serveur.
*   [[SecurityAwareness|Sensibilisation à la sécurité]] des utilisateurs contre les attaques de [[SocialEngineering|Ingénierie Sociale]] et le partage de mots de passe.

## 🔗 Notes Connexes
*   [[Phishing|Hameçonnage]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[CryptographicHashFunction|Fonction de hachage cryptographique]]
*   [[AccessControl|Contrôle d'accès]]