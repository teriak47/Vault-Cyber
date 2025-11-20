---
tags:
  - attaque
aliases:
  - Attaque par force brute
  - Brute-Force Attack
  - Force brute
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque par Force Brute

## 📥 Définition
> L'attaque par force brute est une méthode cybercriminelle qui implique d'essayer systématiquement toutes les combinaisons possibles de caractères (tels que des mots de passe, clés de chiffrement ou PINs) pour obtenir un accès non autorisé à un système, un compte ou une ressource. Son objectif est de découvrir la bonne combinaison par épuisement.

## 🎯 Vecteurs d'Attaque
*   **Interfaces d'Authentification** : Formulaires de connexion web, services SSH, RDP ou FTP.
*   **Protocoles réseau** : Tentatives de connexion sur des services exposés (bases de données, applications web).
*   **Cryptographie** : Essais pour déchiffrer des données en testant toutes les clés possibles.

## 💥 Impacts Potentiels
*   Prise de contrôle de compte
*   Accès non autorisé à des systèmes ou des données
*   Fuite de données et vol de données
*   Déni de service par surcharge des systèmes d'authentification
*   Compromission de la confidentialité et de l'intégrité des données

## concret
> Un attaquant cible un nom d'utilisateur connu sur une plateforme en ligne. Il utilise un logiciel automatisé qui essaie des milliers de combinaisons de mots de passe par seconde. Chaque tentative est envoyée au serveur d'authentification. Après un certain nombre d'essais (qui peut varier de quelques-uns à des millions), le logiciel trouve le bon mot de passe, accordant à l'attaquant un accès non autorisé au compte de l'utilisateur.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Politiques de mots de passe forts imposant longueur et complexité (caractères variés).
    *   Authentification Multi-Facteurs (MFA) pour ajouter une couche de sécurité.
    *   Limitation de débit sur les tentatives de connexion (ex: 3 essais maximum avant un délai).
    *   Verrouillage de compte après un nombre défini d'échecs d'authentification.
    *   CAPTCHA ou mécanismes similaires pour distinguer les humains des bots.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) et SIEM pour surveiller les journaux d'authentification et détecter les schémas d'attaques par force brute.
    *   Journalisation et surveillance de sécurité des échecs d'authentification.
*   **Réponse** :
    *   Plan de réponse à incident en cas de détection d'une attaque.

## 🔗 Notes Connexes
*   Cassage de Mots de Passe
*   Attaque par Dictionnaire
*   Attaque par Rainbow Table
*   Bourrage d'identifiants
*   Verrouillage de Compte
*   Mot de passe
*   Authentification