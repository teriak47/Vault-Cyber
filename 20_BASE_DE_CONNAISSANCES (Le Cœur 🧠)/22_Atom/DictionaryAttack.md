---
tags:
  - attaque/dictionnaire
  - listes-mots-passe
  - cybersécurité/attaques-mots-de-passe
  - gestion-des-mots-de-passe
aliases:
  - Attaque par dictionnaire
  - Dictionary Attack
source:
  - 
cssclasses:
  - max
---

# Attaque par Dictionnaire

## 📥 Définition en une phrase
> Une attaque par dictionnaire est une méthode de [[PasswordCracking|cassage de mot de passe]] qui tente de deviner les mots de passe en utilisant une liste prédéfinie de mots ou de phrases couramment utilisés, souvent des mots de dictionnaire.

## 🧠 Concepts Clés / Fonctionnement
*   **Listes de Mots:** Les attaquants utilisent des fichiers contenant des milliers, voire des millions, de mots, phrases ou combinaisons de caractères tirés de dictionnaires, de mots de passe divulgués ou de listes de mots de passe par défaut.
*   **Automatisation:** Un logiciel d'attaque automatisé tente chaque mot de la liste contre un compte utilisateur ou un système cible jusqu'à ce qu'une correspondance soit trouvée.
*   **Efficacité:** Plus efficace contre les utilisateurs qui choisissent des mots de passe simples, faciles à deviner ou basés sur des mots courants.
*   **Variantes:** Peut inclure des variations (ajout de chiffres, symboles, capitalisation) pour augmenter le taux de succès.

## 🛡️ Risques / Menaces Associés
*   [[CredentialStuffing|Vol d'identifiants]]
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[WeakPassword|Mots de passe faibles]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[StrongPasswordPolicy|Politiques de mots de passe forts]] (complexité, longueur minimale).
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]].
*   [[AccountLockout|Verrouillage de compte]] après un nombre défini de tentatives échouées.
*   [[RateLimiting|Limitation du taux]] de tentatives de connexion.
*   Utilisation de [[PasswordManager|gestionnaires de mots de passe]] pour générer des mots de passe complexes et uniques.
*   Sensibilisation des utilisateurs aux risques des mots de passe faibles.

## 🔗 Notes Connexes
*   [[BruteForceAttack|Attaque par force brute]]
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[CredentialStuffing|Credential Stuffing]]
*   [[RainbowTableAttack|Attaque par Rainbow Table]]