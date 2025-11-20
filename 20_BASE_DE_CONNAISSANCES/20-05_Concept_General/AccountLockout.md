---
aliases:
  - Verrouillage de compte
  - Account Lockout
  - Verrouillage de compte utilisateur
  - User Account Lockout
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Verrouillage de Compte (Account Lockout)

## 📥 Définition en une phrase
> Le verrouillage de compte est une mesure de sécurité qui désactive temporairement ou définitivement l'accès à un compte utilisateur après un nombre spécifié de tentatives de connexion infructueuses.

## 🧠 Concepts Clés / Piliers
*   **Mécanisme de Défense**: Une mesure de sécurité fondamentale pour contrer les attaques de mots de passe automatisées, telles que les attaques par force brute et les tentatives répétées de cassage de mot de passe sur les comptes utilisateurs.
*   **Seuil de Tentatives Échouées**: Un nombre prédéfini de tentatives de connexion incorrectes (ex: 3, 5, 10) qui, une fois atteint, déclenche le verrouillage du compte. Ce seuil doit être finement réglé pour équilibrer sécurité et convivialité.
*   **Durée du Verrouillage**: La période pendant laquelle un compte reste verrouillé. Elle peut être temporaire (ex: 30 minutes) avec déverrouillage automatique, ou permanente nécessitant une intervention administrative.
*   **Réinitialisation du Compteur**: Le processus par lequel le décompte des tentatives de connexion échouées est remis à zéro, soit après un laps de temps prédéfini sans activité, soit après une connexion réussie.
*   **Risque de Déni de Service**: Une mauvaise configuration des politiques de verrouillage de compte peut être exploitée par un acteur de menace pour provoquer un déni de service en verrouillant intentionnellement de nombreux comptes légitimes, empêchant les utilisateurs légitimes d'accéder aux ressources.

## 💡 Importance en Cybersécurité
> Le verrouillage de compte est une composante critique de la stratégie d'authentification et de la sécurité des systèmes. Sa mise en œuvre protège directement contre les attaques de mots de passe automatisées en rendant inefficaces les tactiques comme le force brute et, dans une moindre mesure, le bourrage d'identifiants. En imposant un délai ou une intervention pour déverrouiller un compte, il augmente considérablement le coût et le temps nécessaires pour un attaquant cherchant un accès non autorisé ou une prise de contrôle de compte. Cependant, il doit être associé à d'autres contrôles de sécurité tels que la MFA et une politique de mots de passe forts pour une protection complète, et sa configuration doit être gérée avec attention pour éviter les vecteurs de déni de service.

## 🔗 Notes Connexes
*   Authentification
*   Attaque par force brute
*   Politique de mots de passe forts
*   Authentification Multi-Facteurs (MFA)
*   Gestion des Identités et des Accès (IAM)
*   Déni de Service
*   Prise de contrôle de compte
*   Bourrage d'identifiants
*   Mot de passe
*   Contrôle de Sécurité
*   Connexion
*   Gestion de la Configuration
*   Acteur de menace
*   Accès Non Autorisé