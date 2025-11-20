---
tags:
  - attaque
aliases:
  - Attaque par dictionnaire
  - Dictionary Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque par Dictionnaire

## 📥 Définition
> L'attaque par dictionnaire est une méthode de cassage de mot de passe automatisée qui consiste à tenter de deviner les mots de passe d'un compte ou d'un système en utilisant une liste prédéfinie de mots ou de phrases couramment utilisés.

## 🎯 Vecteurs d'Attaque
*   **Tentatives de connexion automatisées**: Utilisation de scripts ou de logiciels spécialisés pour soumettre des milliers de crédentiels potentiels tirés d'une liste de mots à un formulaire de connexion ou à une procédure d'authentification.
*   **Ciblage de mots de passe faibles**: Exploitation du fait que de nombreux utilisateurs choisissent des mots de passe simples, basés sur des mots courants ou des informations personnelles facilement devinables.

## 💥 Impacts Potentiels
*   Accès non autorisé au système ou au compte de l'utilisateur.
*   Vol de données personnelles ou sensibles.
*   Prise de contrôle de compte.
*   Pertes financières (pour l'organisation ou l'utilisateur).

## 💡 Exemple concret
> Un attaquant télécharge une liste de mots de passe couramment utilisés et se procure une liste de noms d'utilisateur d'une entreprise. Il utilise ensuite un outil (par exemple, un crackeur de mots de passe) pour tester chaque mot de la liste contre chaque nom d'utilisateur. Si l'un des mots de passe correspond, l'attaquant obtient un accès non autorisé au compte de l'utilisateur.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Mise en place de politiques de mots de passe forts imposant complexité, longueur minimale et interdiction de réutiliser des mots de passe.
    *   Sensibilisation des utilisateurs aux risques liés aux mots de passe faibles et à la réutilisation de mots de passe.
    *   Utilisation de gestionnaires de mots de passe pour générer et stocker des mots de passe forts et uniques.
*   **Détection** :
    *   Implémentation du verrouillage de compte après un nombre défini de tentatives de connexion échouées.
    *   Configuration de la limitation de débit pour les tentatives de connexion.
    *   SIEM et surveillance de sécurité pour détecter les activités de force brute ou de dictionnaire.
*   **Réponse** :
    *   Activation de la MFA pour ajouter une couche de sécurité supplémentaire.
    *   Mise en œuvre d'un plan de réponse à incident pour réagir rapidement en cas de détection d'attaque.

## 🔗 Notes Connexes
*   Attaque par force brute
*   Bourrage d'identifiants
*   Attaque par table arc-en-ciel
*   Cassage de mot de passe
*   Politique de mots de passe forts
*   Authentification Multi-Facteurs