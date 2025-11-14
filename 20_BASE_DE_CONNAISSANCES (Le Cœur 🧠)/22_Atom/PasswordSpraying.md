---
tags:
  - cybersécurité/diffusion-mot-passe
  - securite/evitement-verrouillage
  - cybersécurité/attaques-mots-de-passe
  - cybersécurité/force-brute
aliases:
  - Diffusion de Mot de Passe
  - Password Spreading
  - Password Spraying
source:
  - 
cssclasses:
  - max
---

# Password Spraying (Diffusion de Mot de Passe)

## 📥 Définition en une phrase
> Le Password Spraying est une attaque de type force brute où un attaquant tente un petit nombre de mots de passe très courants sur un grand nombre de comptes d'utilisateurs afin d'éviter les verrouillages de compte et de rester indétecté.

## 🧠 Concepts Clés / Fonctionnement
*   **Stratégie d'attaque inversée**: Contrairement à une [[BruteForceAttack|attaque par force brute]] classique qui tente de nombreux mots de passe sur un seul compte, le Password Spraying essaie un ou quelques mots de passe sur de nombreux comptes différents.
*   **Ciblage**: Les attaquants ciblent souvent des annuaires d'entreprise ou des services cloud avec des identifiants d'utilisateurs connus (ex: adresses e-mail ou noms d'utilisateurs courants).
*   **Mots de passe courants**: Utilise des listes de mots de passe faibles, par défaut ou très répandus (ex: "Printemps2023!", "Password123", noms de mois/saisons suivis d'une année).
*   **Évitement des verrous de compte**: En n'essayant chaque mot de passe qu'une seule fois (ou un très petit nombre de fois) par compte, l'attaque cherche à ne pas déclencher les [[AccountLockoutPolicy|politiques de verrouillage de compte]] qui limitent le nombre de tentatives infructueuses.
*   **Objectif**: Obtenir un accès non autorisé à au moins un compte, qui peut ensuite servir de point d'entrée pour une [[LateralMovement|mouvement latéral]] ou une [[PrivilegeEscalation|élévation de privilèges]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[AccountCompromise|Compromission de Compte]]
*   [[CredentialTheft|Vol de Credential]]
*   [[DataBreach|Fuite de Données]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]: La défense la plus efficace, car même si l'attaquant découvre un mot de passe valide, il ne pourra pas se connecter sans le second facteur.
*   [[StrongPasswordPolicy|Politiques de Mots de Passe Forts]]: Exiger des mots de passe longs, complexes et uniques pour rendre le "spraying" moins efficace.
*   [[AccountLockoutPolicy|Politiques de Verrouillage de Compte]]: Bien que l'attaque tente de les contourner, des seuils appropriés restent une protection de base.
*   [[ThreatIntelligence|Surveillance des Logs]] et Détection d'Anomalies: Mettre en place des systèmes pour détecter de multiples tentatives de connexion infructueuses provenant de la même adresse IP sur différents comptes ou depuis des emplacements géographiques inhabituels.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[SecurityInformationAndEventManagement|SIEM]]: Utiliser ces outils pour alerter sur des schémas d'attaque de type password spraying.
*   Formation de sensibilisation: Éduquer les utilisateurs sur l'importance de ne pas réutiliser les mots de passe et d'utiliser des mots de passe forts.

## 🔗 Notes Connexes
*   [[BruteForceAttack|Attaque par Force Brute]]
*   [[CredentialStuffing|Bourrage d'Identifiants]]
*   [[PasswordPolicy|Politique de Mot de Passe]]
*   [[Authentication|Authentification]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès]]