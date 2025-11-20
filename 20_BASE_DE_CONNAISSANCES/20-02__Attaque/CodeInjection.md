---
tags:
  - attaque
  - attaque/injection-de-code
  - vulnerabilite
  - securite/logiciel
  - developpement-securise
  - validation-entree
aliases:
  - Injection de Code
  - Code Injection
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Injection de Code

## 📥 Définition
> L'injection de code est une attaque où des données malveillantes sont insérées ou "injectées" dans une application ou un programme en cours d'exécution. Cela permet à un attaquant d'exécuter son propre code ou d'altérer le comportement d'un programme, souvent en exploitant des vulnérabilités logicielles liées à la validation des entrées.

## 🎯 Vecteurs d'Attaque
*   **Entrées utilisateur non validées** : Données fournies par l'utilisateur via des formulaires web, des paramètres d'URL, des requêtes API ou d'autres périphériques d'entrée qui ne sont pas correctement filtrées ou échappées.
*   **Désérialisation non sécurisée** : Exploitation de vulnérabilités dans la manière dont une application traite des objets sérialisés, permettant l'injection de code malveillant lors de leur reconstruction.
*   **Appels système non sécurisés** : Utilisation de fonctions ou de bibliothèques qui exécutent des commandes externes sans valider les entrées, telles que `system()` ou `exec()`.

## 💥 Impacts Potentiels
*   Exécution de code à distance (RCE)
*   Vol de données
*   Élévation de privilèges
*   Compromission de système
*   Déni de service (DoS)
*   Défiguration de site web

## 📝 Exemple Concret
> L'injection SQL est une forme courante d'injection de code. Un attaquant peut insérer des extraits de code SQL malveillants dans un champ de saisie d'un site web (par exemple, un champ de connexion ou de recherche). Si l'application ne valide pas correctement cette entrée, le code SQL de l'attaquant est exécuté par la base de données, pouvant entraîner la révélation, la modification ou la suppression de données. Par exemple, en entrant `' OR '1'='1` comme mot de passe, l'attaquant peut contourner l'authentification.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Validation rigoureuse des entrées : S'assurer que toutes les entrées utilisateur sont validées, filtrées et nettoyées côté client et surtout côté serveur.
    *   Utilisation de requêtes paramétrées ou d'algorithmes ORM (Object-Relational Mapping) pour l'interaction avec les bases de données afin de prévenir l'injection SQL.
    *   Revue de code régulière pour identifier et corriger les failles logicielles potentielles.
    *   Implémentation du principe de sécurité dès la conception dans le développement logiciel.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) et IPS pour surveiller le trafic réseau et les journaux d'applications à la recherche de signatures d'attaques.
    *   SIEM pour l'analyse centralisée des journaux et la corrélation des événements de sécurité.
*   **Réponse** :
    *   Mise en place d'un plan de réponse aux incidents pour gérer et contenir rapidement les attaques par injection de code.
    *   Application rapide de correctifs de sécurité aux vulnérabilités découvertes.

## 🔗 Notes Connexes
*   **Type d'attaque**: Injection SQL
*   **Type d'attaque**: Scripting Inter-sites (XSS)
*   **Vulnérabilité principale**: Entrée non validée
*   **Conséquence grave**: Exécution de code à distance (RCE)
*   **Mesure préventive clé**: Revue de code