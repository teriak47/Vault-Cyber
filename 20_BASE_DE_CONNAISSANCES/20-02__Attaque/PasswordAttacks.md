---
tags:
  - attaque
aliases:
  - Attaques de mots de passe
  - Password Attacks
  - Attaque de mot de passe
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaques de Mots de Passe

## 📥 Définition
> Les attaques de mots de passe englobent diverses techniques utilisées par les acteurs malveillants pour découvrir, deviner ou contourner les mots de passe, dans le but d'obtenir un accès non autorisé à des systèmes, des comptes ou des données.

## 🎯 Vecteurs d'Attaque
*   **Attaque par force brute**: Tentatives systématiques et automatisées de toutes les combinaisons de caractères possibles jusqu'à la découverte du mot de passe correct.
*   **Attaque par dictionnaire**: Utilisation de listes prédéfinies de mots, de phrases courantes et de mots de passe fréquemment utilisés pour tenter de deviner l'accès.
*   **Credential stuffing**: Réutilisation de paires nom d'utilisateur / mot de passe obtenues lors de fuites de données antérieures, en misant sur la réutilisation de mots de passe par les utilisateurs.
*   **Attaque par table arc-en-ciel**: Utilisation de tables de hachage précalculées pour inverser rapidement les hachages de mots de passe et révéler les mots de passe originaux.
*   **Ingénierie Sociale**: Techniques de manipulation, comme le hameçonnage, visant à inciter les utilisateurs à révéler volontairement leurs identifiants.

## 💥 Impacts Potentiels
*   Vol de données ou exfiltration de données
*   Accès non autorisé et prise de contrôle de compte
*   Usurpation d'identité
*   Dommage à la réputation et perte financière

##  concret
> Un attaquant utilise un logiciel spécialisé qui essaie des millions de combinaisons de caractères (force brute) ou des mots de passe courants (attaque par dictionnaire) pour tenter de se connecter à un compte en ligne. Après plusieurs heures, le logiciel trouve la bonne combinaison, permettant à l'attaquant d'accéder au compte de la victime et potentiellement à ses données personnelles.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Mise en place de l'Authentification Multi-Facteurs (MFA).
    *   Application d'une Politique de mots de passe forts exigeant complexité et longueur.
    *   Utilisation de gestionnaires de mots de passe pour générer et stocker des identifiants uniques.
    *   Implémentation de mécanismes de verrouillage de compte après un nombre défini de tentatives infructueuses.
    *   Stockage des mots de passe sous forme de hachage robuste avec salage.
    *   Sensibilisation des utilisateurs aux risques d'ingénierie sociale et de hameçonnage.
*   **Détection** :
    *   Surveillance des tentatives de connexion suspectes via un SIEM.
    *   Détection d'anomalies dans les journaux d'authentification pour identifier les attaques de mots de passe en cours.
    *   Systèmes de détection d'intrusion (IDS) pour alerter sur des activités inhabituelles.
*   **Réponse** :
    *   Exécution d'un plan de réponse à incident en cas de détection d'une attaque réussie.
    *   Réinitialisation forcée des mots de passe des comptes compromis.

## 🔗 Notes Connexes
*   Hameçonnage
*   Ingénierie Sociale
*   Fonction de hachage
*   Contrôle d'accès
*   Vulnérabilité
*   Acteur de menace
*   Authentification