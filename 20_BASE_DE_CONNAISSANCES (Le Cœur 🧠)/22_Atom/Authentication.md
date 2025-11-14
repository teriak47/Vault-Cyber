---
tags:
  - authentification-unique
  - authentification/facteur-possession
  - authentification/basée-comportement
  - authentification
  - authentification/facteurs
  - authentification/multifacteur
aliases:
  - Authentification
  - Authentication
cssclasses:
  - max
---

# Authentification

## 📥 Définition en une phrase
> Processus de vérification de l'identité déclarée d'un utilisateur, d'un système ou d'une entité, en comparant des preuves fournies à des informations stockées.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification**: L'entité déclare son identité, souvent via un identifiant unique (ex: nom d'utilisateur, adresse IP).
*   **Preuve (Credentials)**: L'entité fournit un ou plusieurs facteurs de preuve pour étayer son identification (ex: mot de passe, empreinte digitale, certificat numérique, jeton matériel).
*   **Vérification**: Le système valide les preuves fournies contre les informations d'identité enregistrées. Si les preuves correspondent, l'identité est confirmée.
*   **Facteurs d'authentification**:
    *   **Ce que vous savez**: (Knowledge factor) Mots de passe, codes PIN, réponses à des questions secrètes.
    *   **Ce que vous avez**: (Possession factor) Cartes à puce, jetons de sécurité (hard/soft tokens), applications d'authentification.
    *   **Ce que vous êtes**: (Inherence factor) Biométrie (empreinte digitale, reconnaissance faciale, scan rétinien).
    *   **Où vous êtes**: (Location factor) Basée sur la géolocalisation ou l'adresse IP.
    *   **Ce que vous faites**: (Action factor) Basée sur le comportement (frappe, démarche).

## 🛡️ Risques / Menaces Associés
*   [[BruteForceAttack|Attaque par force brute]]
*   [[CredentialStuffing|Bourrage d'identifiants]]
*   [[Phishing|Hameçonnage]]
*   [[ManInTheMiddle|Attaque de l'homme du milieu]]
*   [[ReplayAttack|Attaque par rejeu]]
*   [[PasswordCracking|Cassage de mots de passe]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[StrongPasswordPolicy|Politiques de mots de passe robustes]]
*   [[PasswordHashing|Hachage et salage des mots de passe]]
*   [[SecurityAudit|Audits de sécurité réguliers]] des systèmes d'authentification.
*   [[SingleSignOn|Authentification Unique (SSO)]] (pour centraliser et simplifier la gestion des identités).
*   [[BiometricAuthentication|Authentification biométrique]]
*   [[TwoFactorAuthentication|Authentification à Deux Facteurs (2FA)]]

## 🔗 Notes Connexes
*   [[Authorization|Autorisation]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[SingleSignOn|Authentification Unique (SSO)]]
*   [[Password|Mot de passe]]
