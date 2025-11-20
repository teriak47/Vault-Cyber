---
tags:
aliases:
  - Authentification
  - Authentication
  - Vérification d'identité
  - Login
  - Connexion
  - Sign-in
  - Log-in
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Authentification

## 📥 Définition en une phrase
> Processus de vérification de l'identité déclarée d'un utilisateur, d'un système ou d'une entité, en comparant des preuves fournies à des informations stockées.

## 🧠 Concepts Clés / Piliers
*   **Identification**: L'entité déclare son identité, souvent via un identifiant unique (ex: nom d'utilisateur, adresse IP). C'est la première étape où l'entité prétend être une identité spécifique.
*   **Preuve (Credentials)**: L'entité fournit un ou plusieurs facteurs d'authentification pour étayer son identification. Ces preuves peuvent inclure des mots de passe, des informations biométriques (empreinte digitale, reconnaissance faciale) ou des certificats numériques.
*   **Vérification**: Le système compare les preuves fournies par l'entité aux informations d'identité enregistrées et fiables. Si les preuves correspondent, l'identité est confirmée et l'utilisateur ou le système est authentifié.
*   **Facteurs d'authentification**: Les catégories de preuves utilisées pour vérifier une identité :
    *   **Ce que vous savez (Knowledge Factor)**: Basé sur une connaissance secrète (ex: mot de passe, code PIN, réponses à des questions secrètes).
    *   **Ce que vous avez (Possession Factor)**: Basé sur la possession d'un objet physique ou virtuel (ex: jeton de sécurité, certificat numérique, application d'authentification mobile).
    *   **Ce que vous êtes (Inherence Factor)**: Basé sur une caractéristique biométrique unique (ex: empreinte digitale, reconnaissance faciale ou vocale).
    *   **Où vous êtes (Location Factor)**: Basé sur des informations de localisation (ex: adresse IP source, géolocalisation GPS).
    *   **Ce que vous faites (Action Factor)**: Basé sur un comportement spécifique (ex: schéma de frappe, démarche).

## 💡 Importance en Cybersécurité
L'authentification est une pierre angulaire de la cybersécurité, agissant comme la première ligne de défense contre l'accès non autorisé aux ressources et systèmes. Elle assure que seules les identités légitimes peuvent interagir avec les systèmes d'entreprise ou personnels, protégeant ainsi la confidentialité, l'intégrité et l'disponibilité des données. Sans une authentification robuste, les systèmes sont vulnérables à des attaques telles que le cassage de mots de passe, le bourrage d'identifiants, le hameçonnage et les attaques par rejeu, menant potentiellement à la violation de données ou à la compromission de système. En mettant en œuvre des mécanismes d'authentification forts, tels que l'MFA et des politiques de mots de passe robustes, les organisations peuvent significativement réduire leur surface d'attaque et renforcer leur posture de sécurité.

## 🔗 Notes Connexes
*   Contrôle d'accès
*   Autorisation
*   Authentification biométrique
*   Attaque par force brute
*   Identifiant
*   Bourrage d'identifiants
*   Certificat Numérique
*   Gestion des Identités et des Accès (IAM)
*   Attaque de l'homme du milieu
*   Authentification Multi-Facteurs (MFA)
*   Mot de passe
*   Cassage de mots de passe
*   Hachage et salage des mots de passe
*   Hameçonnage
*   Attaque par rejeu
*   Audit de sécurité
*   Authentification Unique (SSO)
*   Politique de mots de passe forts
*   Authentification à deux facteurs (2FA)
*   Accès Non Autorisé
*   Identité Utilisateur