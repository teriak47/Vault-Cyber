---
tags:
  - cyberattaque/prise-de-controle-compte
  - securite/reutilisation-mot-de-passe
  - cybersécurité/bourrage-identifiants
  - cybersécurité/attaques-mots-de-passe
aliases:
  - Bourrage d'identifiants
  - Credential stuffing
source:
  - 
cssclasses:
  - max
---

# Credential Stuffing (Bourrage d'identifiants)

## 📥 Définition en une phrase
> Une cyberattaque automatisée où des identifiants (combinaisons nom d'utilisateur/mot de passe) volés lors d'une précédente fuite de données sont utilisés pour tenter d'accéder à d'autres services en ligne, exploitant la tendance des utilisateurs à réutiliser leurs mots de passe.

## 🧠 Concepts Clés / Fonctionnement
*   **Réutilisation d'identifiants :** L'attaque repose sur la pratique courante des utilisateurs de réutiliser le même nom d'utilisateur et mot de passe sur de multiples sites web ou services.
*   **Automatisation :** Des outils et des scripts automatisés (bots) sont utilisés pour tenter des milliers, voire des millions, de combinaisons d'identifiants sur diverses plateformes cibles.
*   **Fuites de données (Data Breaches) :** Les listes d'identifiants compromis sont souvent obtenues via des fuites de données antérieures sur d'autres sites, ou via des attaques de [[Phishing|Hameçonnage]].
*   **Ciblage :** Les attaquants ciblent souvent des plateformes à forte valeur (bancaires, e-commerce, réseaux sociaux) ou celles où le succès d'une connexion peut mener à d'autres compromissions.

## 🛡️ Risques / Menaces Associés
*   [[AccountTakeover|Prise de contrôle de compte]] : L'objectif principal est de gagner un accès non autorisé aux comptes des utilisateurs.
*   [[DataBreach|Fuite de données]] : Si un compte est compromis, les données personnelles ou sensibles qui y sont stockées peuvent être volées.
*   [[FinancialFraud|Fraude financière]] : Les comptes bancaires ou de commerce électronique compromis peuvent être utilisés pour des transactions frauduleuses.
*   [[ReputationDamage|Dommage à la réputation]] : Pour les entreprises dont les comptes clients sont compromis, cela peut entraîner une perte de confiance.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] : La mesure la plus efficace, car même avec des identifiants valides, l'accès est bloqué sans le deuxième facteur.
*   [[StrongPasswordPolicy|Politique de mots de passe forts]] : Encourager les utilisateurs à créer des mots de passe complexes et uniques pour chaque service.
*   [[PasswordManager|Gestionnaire de mots de passe]] : Promouvoir l'utilisation de gestionnaires de mots de passe pour générer et stocker des mots de passe uniques.
*   [[RateLimiting|Limitation de débit]] : Mettre en œuvre des systèmes de détection et de blocage des tentatives de connexion excessives à partir d'une même adresse IP ou d'un même utilisateur.
*   [[Captcha|CAPTCHA]] : Utiliser des CAPTCHA pour distinguer les utilisateurs humains des bots lors des tentatives de connexion.
*   Surveillance des logs : Analyser les journaux d'authentification pour détecter des motifs d'attaque de bourrage d'identifiants.

## 🔗 Notes Connexes
*   [[PasswordReuse|Réutilisation de mot de passe]]
*   [[Phishing|Hameçonnage]]
*   [[DataBreach|Fuite de données]]
*   [[BruteForceAttack|Attaque par force brute]]