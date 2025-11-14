---
tags:
  - securite/verrouillage-compte
  - politique/historique-mot-passe
  - complexite-mot-passe
  - securite/politique-mot-de-passe
  - hachage-mot-de-passe
  - cybersécurité/force-brute
aliases:
  - Politique de mots de passe forts
  - Strong Password Policy
source:
  - null
cssclasses:
  - max
---

# Politique de Mots de Passe Forts

## 📥 Définition en une phrase
> Un ensemble de règles et de pratiques conçues pour imposer la création et le maintien de mots de passe robustes et uniques pour les comptes utilisateurs, réduisant ainsi le risque d'accès non autorisé et de compromission des systèmes.

## 🧠 Concepts Clés / Fonctionnement
*   **Longueur Minimale:** Exiger un nombre minimum de caractères pour un mot de passe (souvent 12-16 caractères ou plus pour une sécurité accrue).
*   **Complexité:** Imposer l'inclusion de différents types de caractères : majuscules, minuscules, chiffres et caractères spéciaux.
*   **Interdiction des Mots de Passe Courants:** Utiliser des listes noires pour empêcher l'utilisation de mots de passe fréquemment compromis, de dictionnaires ou de séquences facilement devinables.
*   **Historique des Mots de Passe:** Empêcher la réutilisation immédiate ou trop fréquente des anciens mots de passe par un utilisateur.
*   **Verrouillage de Compte:** Bloquer temporairement un compte après un nombre excessif de tentatives de connexion infructueuses, afin de contrecarrer les [[BruteForceAttack|attaques par force brute]].
*   **Rotation Régulière (avec prudence):** Bien que traditionnellement recommandée, la rotation forcée et fréquente des mots de passe est de plus en plus déconseillée par les experts en sécurité si elle n'est pas accompagnée d'autres mesures comme la [[MultiFactorAuthentication|MFA]], car elle peut conduire à des mots de passe plus faibles et plus prévisibles.

## 🛡️ Risques / Menaces Associés
*   [[BruteForceAttack|Attaques par force brute]]
*   [[CredentialStuffing|Credential Stuffing]] (Bourrage d'identifiants)
*   [[PasswordCracking|Cassage de mot de passe]]
*   [[SocialEngineering|Ingénierie sociale]] (pour l'obtention de mots de passe faibles ou divulgués)
*   [[WeakAuthentication|Authentification faible]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] (complément essentiel)
*   Encourager l'utilisation de [[PasswordManager|gestionnaires de mots de passe]].
*   Mettre en œuvre des politiques de [[SecurityAwarenessTraining|sensibilisation à la sécurité]] pour éduquer les utilisateurs sur les bonnes pratiques.
*   Utiliser des techniques de [[PasswordHashing|hachage et de salage de mot de passe]] robustes pour le stockage côté serveur.
*   Déployer des systèmes de détection des intrusions et des tentatives de connexion suspectes.

## 🔗 Notes Connexes
*   [[Authentication|Authentification]]
*   [[AccessControl|Contrôle d'accès]]
*   [[InformationSecurity|Sécurité de l'information]]
*   [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]