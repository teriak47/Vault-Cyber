---
tags:
  - authentification/echec-connexion
  - gestion/deverrouillage-compte
  - controle-acces/reactif
  - securite/verrouillage-compte
  - cybersecurite/force-brute
  - securite/politique-mot-de-passe
aliases:
  - Verrouillage de compte
  - Account Lockout
source:
  - null
cssclasses:
  - max
---

# Verrouillage de Compte (Account Lockout)

## 📥 Définition en une phrase
> Le verrouillage de compte est une mesure de sécurité qui désactive temporairement ou définitivement l'accès à un compte utilisateur après un nombre spécifié de tentatives de connexion infructueuses.

## 🧠 Concepts Clés / Fonctionnement
*   **Seuil de Tentatives :** Un nombre prédéfini de tentatives de connexion échouées (ex: 3, 5, 10) qui, une fois atteintes, déclenchent le verrouillage.
*   **Durée du Verrouillage :** Le temps pendant lequel le compte reste verrouillé, qui peut être temporaire (ex: 30 minutes, 1 heure) ou nécessiter une intervention administrative pour le déverrouiller.
*   **Objectif Primaire :** Empêcher les [[BruteForceAttack|attaques par force brute]] où un attaquant essaie systématiquement de deviner les informations d'identification d'un utilisateur.
*   **Réinitialisation du Compteur :** Le compteur de tentatives échouées est généralement réinitialisé après un certain laps de temps sans activité, ou après une connexion réussie.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service]] (DoS) : Les attaquants peuvent intentionnellement déclencher des verrouillages massifs pour empêcher des utilisateurs légitimes d'accéder à leurs comptes.
*   [[CredentialStuffing|Bourrage d'identifiants]] : Bien qu'il protège contre la force brute, un verrouillage de compte mal configuré peut être contourné ou exploité par le bourrage d'identifiants si le seuil est trop élevé ou la durée trop courte.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Configuration Appropriée :** Définir des seuils de tentatives et des durées de verrouillage qui équilibrent sécurité et convivialité, en tenant compte du risque de DoS.
*   **Alertes et Surveillance :** Mettre en place des alertes pour les événements de verrouillage de compte afin de détecter les tentatives d'attaque ou de DoS.
*   **[[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] :** Compléter le verrouillage de compte par l'[[MultiFactorAuthentication|MFA]] pour renforcer considérablement la sécurité des accès.
*   **[[PasswordPolicy|Politique de Mots de Passe]] Robuste :** Encourager des mots de passe complexes et uniques pour réduire l'efficacité des tentatives de force brute avant même le déclenchement du verrouillage.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[BruteForceAttack|Attaque par force brute]]
*   [[PasswordPolicy|Politique de mots de passe]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]