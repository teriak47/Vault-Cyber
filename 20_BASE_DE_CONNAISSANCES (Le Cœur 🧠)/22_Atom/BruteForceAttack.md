---
tags:
  - securite/limitation-tentatives
  - securite/captcha
  - cassage-mot-passe
  - cybersécurité/force-brute
  - cybersécurité/attaques-mots-de-passe
  - authentification/multifacteur
aliases:
  - Attaque par force brute
  - Brute-Force Attack
source:
  - null
cssclasses:
  - max
---

# Attaque par Force Brute

## 📥 Définition en une phrase
> L'attaque par force brute est une méthode cybercriminelle qui consiste à essayer systématiquement toutes les combinaisons possibles (mots de passe, clés de chiffrement, PINs) jusqu'à trouver la bonne, permettant l'accès non autorisé à un système ou un compte.

## 🧠 Concepts Clés / Fonctionnement
*   **Essais Exhaustifs**: L'attaquant essaie chaque combinaison de caractères possible, un par un, jusqu'à ce que la bonne information (ex: mot de passe) soit découverte.
*   **Vitesse et Complexité**: La durée de l'attaque est directement proportionnelle à la longueur et à la complexité de la cible (nombre de caractères, types de caractères). Plus la cible est longue et complexe, plus l'attaque est longue et coûteuse en ressources.
*   **Outils et Automatisation**: Des logiciels spécialisés et des botnets sont utilisés pour automatiser et accélérer le processus d'essai des combinaisons, tirant parti de la puissance de calcul.
*   **Variantes**:
    *   [[DictionaryAttack|Attaque par Dictionnaire]]: Utilise une liste de mots de passe courants ou des phrases (mots d'un dictionnaire) plutôt qu'un essai aléatoire complet.
    *   [[CredentialStuffing|Credential Stuffing]]: Utilise des paires identifiant/mot de passe volées lors de fuites de données antérieures et les essaie sur d'autres services.

## 🛡️ Risques / Menaces Associés
*   [[AccountTakeover|Prise de contrôle de compte]]
*   [[UnauthorizedAccess|Accès non autorisé]] à des systèmes ou des données
*   [[DataBreach|Fuite de données]]
*   [[DenialOfService|Déni de service]] (par surcharge des systèmes d'authentification)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[StrongPasswordPolicy|Politiques de mots de passe forts]] (longueur minimale, caractères variés)
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]]
*   [[RateLimiting|Limitation du taux]] de tentatives de connexion (ex: 3 essais maximum avant un délai)
*   [[AccountLockout|Verrouillage de compte]] après un nombre défini de tentatives échouées
*   [[CAPTCHA|CAPTCHA]] pour distinguer les humains des bots
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[SecurityInformationAndEventManagement|SIEM]] pour détecter et alerter sur les schémas d'attaques par force brute.

## 🔗 Notes Connexes
*   [[PasswordCracking|Cassage de Mots de Passe]]
*   [[DictionaryAttack|Attaque par Dictionnaire]]
*   [[RainbowTableAttack|Attaque par Rainbow Table]]
*   [[CredentialStuffing|Credential Stuffing]]