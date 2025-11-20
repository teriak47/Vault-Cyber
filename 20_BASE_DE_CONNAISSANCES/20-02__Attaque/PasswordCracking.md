---
tags:
  - attaque
aliases:
  - Cassage de mot de passe
  - Password Cracking
  - Attaques de mots de passe
  - Attaque de mot de passe
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Cassage de Mot de Passe

## 📥 Définition
> Le cassage de mot de passe est le processus de récupération de mots de passe (souvent stockés sous forme hachée ou chiffrée) d'un système informatique, d'un fichier ou d'une connexion réseau, généralement dans le but d'obtenir un accès non autorisé.

## 🎯 Vecteurs d'Attaque
*   **Attaque par Force Brute** : Tentative systématique de toutes les combinaisons possibles de caractères jusqu'à trouver le mot de passe.
*   **Attaque par Dictionnaire** : Utilisation d'une liste prédéfinie de mots de passe courants, de phrases ou de noms.
*   **Attaque par Table Arc-en-Ciel** : Utilisation de tables précalculées pour inverser les fonctions de hachage de mots de passe, permettant de trouver rapidement les mots de passe correspondant aux hachages.
*   **Attaque Hybride** : Combinaison d'attaques par dictionnaire et par force brute, souvent en ajoutant des chiffres ou des symboles aux mots du dictionnaire.
*   **Credential Stuffing** : Réutilisation de paires identifiant/mot de passe compromises lors d'une fuite de données antérieure sur d'autres services.

## 💥 Impacts Potentiels
*   Accès Non Autorisé à des comptes ou systèmes.
*   Fuite de Données sensibles.
*   Vol d'Identité.
*   Élévation de privilèges au sein d'un système.
*   Perte financière et dommage à la réputation.

## 📝 Exemple concret
> Un attaquant obtient une liste de hachages de mots de passe volés suite à une fuite de données d'un service en ligne. Il utilise un logiciel de cassage de mot de passe tel que John the Ripper ou Hashcat pour tenter de déchiffrer ces mots de passe. En commençant par une attaque par dictionnaire et en progressant vers une attaque par force brute ciblée, l'objectif est d'accéder aux comptes des utilisateurs et potentiellement à d'autres systèmes où les mêmes mots de passe sont réutilisés.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Mettre en place une Politique de Mots de Passe Forts exigeant des mots de passe forts, longs, complexes et uniques.
    *   Implémenter l'Authentification Multi-Facteurs (MFA) pour ajouter une couche de vérification supplémentaire.
    *   Utiliser des fonctions de hachage cryptographiques robustes et le salage pour stocker les mots de passe.
    *   Mettre en œuvre des politiques de verrouillage de compte après un nombre défini d'échecs de connexion.
    *   Encourager l'utilisation de Gestionnaires de Mots de Passe pour générer et stocker des mots de passe forts et uniques.
    *   Mener des programmes de sensibilisation des utilisateurs aux risques liés aux mots de passe faibles et à la ingénierie sociale.
*   **Détection** :
    *   Déployer des Systèmes de détection d'intrusion (IDS) et des SIEM pour surveiller les tentatives de cassage de mot de passe.
    *   Implémenter la surveillance de sécurité pour détecter les activités de connexion suspectes ou les schémas d'attaque.
    *   Utiliser la limitation de débit sur les tentatives de connexion pour ralentir les attaques par force brute.
*   **Réponse** :
    *   Mettre en place un Plan de réponse à incident pour réagir rapidement en cas de compromission de système ou de fuite de données.

## 🔗 Notes Connexes
*   Vulnérabilité
*   Acteur de menace
*   Authentification
*   Hachage
*   Salage
*   Gestion des Mots de Passe
*   Mots de Passe Faibles
*   Mauvais Hachage de Mots de Passe
*   Ingénierie Sociale
---