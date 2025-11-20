---
tags:
aliases:
  - MFA
  - Multi-Factor Authentication
  - Authentification Multi-Facteurs
  - Authentification Multi-Facteur
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Authentification Multi-Facteurs (MFA)

## 📥 Définition en une phrase
> L'Authentification Multi-Facteurs (MFA) est une méthode de vérification d'identité qui exige qu'un utilisateur fournisse deux ou plusieurs facteurs de vérification distincts pour accéder à un compte, un système ou une application.

## 🧠 Concepts Clés / Piliers
*   **Facteurs d'Authentification**: La MFA combine au moins deux des trois catégories de facteurs pour prouver l'identité de l'utilisateur :
    *   **Ce que vous savez** (Mot de passe, code PIN, réponse à une question secrète).
    *   **Ce que vous avez** (Smartphone pour OTP temporel (TOTP), clé de sécurité FIDO2, carte à puce, jeton logiciel).
    *   **Ce que vous êtes** (Caractéristique biométrique unique comme une empreinte digitale ou la reconnaissance faciale).
*   **Sécurité Renforcée**: En exigeant plusieurs types de preuves provenant de catégories distinctes, la MFA réduit considérablement le risque d'accès non autorisé. Si un facteur est compromis (ex: vol de mot de passe), l'attaquant ne pourra pas se connecter sans les autres facteurs.
*   **Diversité des Méthodes**: Les implémentations courantes incluent les OTP (générés par applications ou envoyés par SMS - bien que moins sécurisés), les clés de sécurité physiques (FIDO2 ou U2F) résistantes au hameçonnage, et les méthodes biométriques intégrées aux appareils mobiles. La MFA adaptative peut ajuster les exigences en fonction du contexte (localisation, appareil, heure).

## 💡 Importance en Cybersécurité
> La MFA est fondamentale en cybersécurité car elle offre une couche de sécurité essentielle au-delà du simple mot de passe. Elle résout le problème de la facilité avec laquelle les informations d'identification uniques peuvent être volées, devinées ou cassées. En rendant beaucoup plus difficile pour un attaquant d'accéder à un compte, même après avoir obtenu un premier facteur, elle protège la confidentialité des données et prévient les prises de contrôle de compte, les violations de données et les pertes financières. C'est un pilier clé de la gestion des identités et des accès modernes.

## 🔗 Notes Connexes
*   Authentification
*   Gestion des Identités et des Accès (IAM)
*   Confiance Zéro
*   Mot de passe fort