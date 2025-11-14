---
tags:
  - cybersecurite/detournement-session
  - gestion/session
  - communication/gestion-dialogue
  - modele/osi
  - couche/session
  - authentification/multifacteur
aliases:
  - Couche de Session
  - Session Layer
source:
  - OSI Model
cssclasses:
  - max
---

# Couche de Session

## 📥 Définition en une phrase
> La couche de session (couche 5 du [[OpenSystemsInterconnectionModel|modèle OSI]]) est responsable de l'établissement, de la gestion et de la terminaison des sessions de communication entre les applications sur différents hôtes.

## 🧠 Concepts Clés / Fonctionnement
*   **Gestion des Dialogues**: Elle orchestre les communications en déterminant quel processus peut envoyer des données à quel moment (full-duplex ou half-duplex).
*   **Synchronisation**: Elle insère des points de synchronisation (checkpoints) dans le flux de données pour permettre la récupération en cas de défaillance, évitant ainsi de devoir reprendre la transmission depuis le début.
*   **Établissement et Libération de Session**: Gère l'authentification et l'autorisation initiales pour une session, puis la termine proprement une fois la communication achevée.
*   **Délimitation**: Sépare les flux de données de différentes applications, assurant qu'elles ne s'interfèrent pas.

## 🛡️ Risques / Menaces Associés
*   [[SessionHijacking|Détournement de session]] : Un attaquant prend le contrôle d'une session authentifiée.
*   [[DenialOfService|Déni de service]] (DoS) : Surcharge des ressources de gestion de session, empêchant l'établissement de nouvelles sessions.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[SecureSessionManagement|Gestion sécurisée des sessions]] : Utiliser des identifiants de session complexes, des délais d'expiration appropriés et des mécanismes de renouvellement.
*   [[Encryption|Chiffrement]] de bout en bout : Protéger les données de session contre l'interception.
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs]] (MFA) : Renforcer la vérification de l'identité avant l'établissement de la session.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[PresentationLayer|Couche de Présentation]]
*   [[TransportLayer|Couche de Transport]]