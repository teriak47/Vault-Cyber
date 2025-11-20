---
tags:
  - attaque
  - attaque/reverse-shell
aliases:
  - Reverse Shell
  - Shell inversé
  - Coque inversée
  - Reverse Shell Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Reverse Shell (Coque Inversée)

## 📥 Définition
> Une Reverse Shell est une technique d'exploitation où un ordinateur cible est contraint d'établir une connexion réseau *sortante* vers un acteur de menace qui est en écoute. L'objectif principal est de contourner les pare-feu qui bloquent les connexions entrantes mais autorisent les connexions sortantes, permettant ainsi à l'attaquant d'obtenir un shell interactif sur le système cible et d'en prendre le contrôle.

## 🎯 Vecteurs d'Attaque
*   **Exécution de Code à Distance (RCE)**: L'attaquant exploite une vulnérabilité logicielle pour exécuter un script ou une commande sur le système cible qui initie la connexion inverse.
*   **Phishing / Ingénierie Sociale**: Un utilisateur est trompé pour télécharger et exécuter un logiciel malveillant (souvent un Cheval de Troie) qui contient le code du reverse shell.
*   **Distribution de Malware**: Un ver ou autre logiciel malveillant déjà présent sur le réseau peut installer une porte dérobée avec une fonctionnalité de reverse shell.

## 💥 Impacts Potentiels
*   Accès non autorisé complet au système compromis.
*   Vol de données et exfiltration de données sensibles.
*   Élévation de privilèges sur le système compromis.
*   Persistance sur le système pour maintenir l'accès non autorisé.
*   Utilisation du système compromis comme point de pivot pour attaquer d'autres ressources internes.

## 💡 Exemple concret
> Un acteur de menace identifie une vulnérabilité logicielle sur un serveur web qui permet l'exécution de code à distance. Il envoie une attaque via une requête HTTP malveillante, forçant le serveur à exécuter une commande qui lance un script Python. Ce script établit ensuite une connexion TCP sortante vers l'adresse IP de l'attaquant sur un port spécifique où l'attaquant écoute avec un outil comme Netcat. Une fois la connexion établie, l'attaquant obtient un shell interactif sur le serveur, lui permettant d'exécuter des commandes comme s'il était directement connecté.

## 🛡️ Mesures de Mitigation
*   **Prévention** : 
    *   Application rigoureuse du patch management pour corriger les vulnérabilités logicielles.
    *   Configuration stricte des pare-feu pour limiter les connexions sortantes aux seuls services autorisés.
    *   Revue de code régulière pour identifier et corriger les failles menant à des RCE.
    *   Mise en œuvre du principe du moindre privilège pour les processus et utilisateurs.
    *   Sécurité dès la conception dans le développement logiciel.
*   **Détection** :
    *   Utilisation de systèmes de détection d'intrusion (IDS) et IPS pour surveiller le trafic réseau et les activités système inhabituelles (connexions sortantes inattendues, shells interactifs).
    *   SIEM pour l'analyse des logs à la recherche de schémas d'attaque ou de comportements anormaux.
    *   Surveillance réseau active pour identifier les connexions TCP suspectes.
    *   EDR et EPP pour la surveillance des endpoints.
*   **Réponse** :
    *   Mise en place d'un plan de réponse à incident pour réagir rapidement aux compromissions.
    *   Analyse forensique des systèmes compromis pour comprendre le mode opératoire et les impacts.

## 🔗 Notes Connexes
*   Shellcode
*   Exploitation
*   Commande et Contrôle (C2)
*   Persistance
*   Pare-feu
*   Shell
*   Exécution de Code à Distance
*   Vulnérabilité
*   Acteur de menace