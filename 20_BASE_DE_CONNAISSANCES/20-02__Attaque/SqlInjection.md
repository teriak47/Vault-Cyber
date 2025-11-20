---
tags:
  - attaque
  - attaque/injection-sql
  - manipulation/donnees
  - base-de-donnees
  - securite/donnees
aliases:
  - Injection SQL
  - SQL Injection
  - SQLi
  - Structured Query Language Injection
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Injection SQL

## 📥 Définition
> L'Injection SQL est une attaque qui exploite des vulnérabilités logicielles dans le code d'une application pour injecter des requêtes SQL (new link) malveillantes dans une base de données, permettant un accès non autorisé ou une manipulation de données.

## 🎯 Vecteurs d'Attaque
*   **Champs de saisie web**: Formulaires (connexion, recherche), paramètres d'URL où les entrées non validées sont utilisées pour construire des requêtes SQL.
*   **Cookies HTTP**: Les données stockées dans les cookies HTTP si elles sont intégrées directement dans les requêtes SQL sans vérification.
*   **En-têtes HTTP**: Certains en-têtes (ex: User-Agent, Referer) peuvent être vulnérables si l'application les utilise dans des requêtes SQL.

## 💥 Impacts Potentiels
*   Accès non autorisé à la base de données et aux systèmes sous-jacents.
*   Exfiltration de données sensibles (informations d'identité des utilisateurs, mots de passe, informations financières, etc.).
*   Altération de données (modification, suppression de registres importants).
*   Contournement de l'authentification, permettant à un attaquant de se connecter sans identifiants valides.
*   Élévation de privilèges au sein de la base de données ou du système d'exploitation.
*   Exécution de code à distance sur le serveur de la base de données (selon la configuration et les privilèges).

##  concret
> Un attaquant trouve un formulaire de recherche sur un site web qui ne valide pas correctement les entrées. Au lieu de taper un terme de recherche normal, il entre `' OR '1'='1' --`. Si l'application construit la requête SQL comme `SELECT * FROM produits WHERE nom LIKE '%` + `entrée_utilisateur` + `%'`, l'injection transformerait la requête en `SELECT * FROM produits WHERE nom LIKE '%' OR '1'='1' --%'`. Le `' OR '1'='1'` est toujours vrai, et `--` commente la fin de la requête originale, permettant à l'attaquant de récupérer toutes les informations de la table sans avoir à se connecter ou à connaître des critères spécifiques.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   **Requêtes préparées et paramétrées**: Utiliser des requêtes préparées avec des paramètres pour toutes les interactions avec la base de données, empêchant l'interprétation des entrées utilisateur comme du code SQL.
    *   **Validation des entrées**: Valider et nettoyer rigoureusement toutes les entrées utilisateur côté client et serveur (filtrage, échappement des caractères spéciaux).
    *   **Principe du moindre privilège**: Configurer les comptes d'accès à la base de données avec les privilèges minimaux nécessaires.
    *   **Revue de code**: Effectuer des revues de code régulières et des tests d'intrusion pour identifier les vulnérabilités.
    *   **Pare-feu applicatif web (WAF)** (new link): Déployer un WAF pour filtrer le trafic malveillant avant qu'il n'atteigne l'application.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) et systèmes de prévention d'intrusion (IPS) pour surveiller les motifs d'attaque.
    *   Surveillance de sécurité et analyse des journaux de la base de données et de l'application web.
*   **Réponse** :
    *   Plan de réponse à incident pour réagir rapidement aux attaques.
    *   Correction immédiate des vulnérabilités découvertes.

## 🔗 Notes Connexes
*   Vulnérabilité
*   Base de données
*   Sécurité des applications web (new link)
*   Cross-Site Scripting (XSS)
*   Exécution de Code à Distance (RCE)
*   Exfiltration de données
*   Entrée Non Validée