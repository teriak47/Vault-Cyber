---
tags:
  - attaque/injection-sql-aveugle
  - securite/base-de-donnees
  - securite/pare-feu-web
  - vulnerabilite/injection-web
  - programmation/requetes-parametrees
  - acces/non-autorise
aliases:
  - Injection SQL
  - SQL Injection
source:
  - null
cssclasses:
  - max
---

# Injection SQL

## 📥 Définition en une phrase
> L'Injection SQL est une technique d'attaque qui exploite des vulnérabilités dans le code d'une application pour injecter des requêtes SQL malveillantes dans une base de données, permettant un accès non autorisé ou une manipulation des données.

## 🧠 Concepts Clés / Fonctionnement
*   **Vulnérabilité des Entrées** : L'attaque survient lorsque l'application ne valide pas ou n'échappe pas correctement les entrées utilisateur avant de les inclure dans une requête SQL.
*   **Exécution Arbitraire de Commandes** : Un attaquant insère des portions de code SQL dans les champs de saisie, qui sont ensuite exécutées par la base de données comme faisant partie de la requête légitime.
*   **Types d'Injection** :
    *   **In-band (Classique)** : Les données sont extraites directement via la même connexion que l'injection (ex: Union-based, Error-based).
    *   **Out-of-band** : Les données sont extraites par un canal différent (ex: DNS, HTTP).
    *   **Blind SQL Injection** : L'attaquant ne reçoit pas les données directement, mais déduit les informations en observant le comportement de l'application (ex: Boolean-based, Time-based).
*   **Conséquences** : Peut permettre le contournement de l'authentification, la récupération de [[SensitiveData|données sensibles]], la modification ou la suppression de données, et dans certains cas, l'exécution de commandes système.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de Données]]
*   [[UnauthorizedAccess|Accès Non Autorisé]]
*   [[DataManipulation|Manipulation de Données]]
*   [[DenialOfService|Déni de Service]] (par corruption ou suppression de données)
*   [[RemoteCodeExecution|Exécution de Code à Distance]] (via certaines fonctions de base de données)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[ParameterizedQueries|Requêtes Paramétrées]] : Utiliser des requêtes préparées avec des paramètres pour toutes les interactions avec la base de données. C'est la défense la plus efficace.
*   [[InputValidation|Validation des Entrées]] : Valider et assainir toutes les entrées utilisateur côté serveur.
*   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]] : Configurer les comptes de base de données avec le strict minimum de permissions nécessaires.
*   [[ErrorHandling|Gestion des Erreurs]] : Ne pas afficher d'informations détaillées sur les erreurs de base de données aux utilisateurs finaux.
*   [[WebApplicationFirewall|WAF]] : Déployer un WAF pour filtrer et bloquer les tentatives d'injection connues.
*   **Encodage de Sortie** : Encoder les données lors de leur affichage pour éviter d'autres types d'attaques comme le [[CrossSiteScripting|XSS]].

## 🔗 Notes Connexes
*   [[CrossSiteScripting|Cross-Site Scripting (XSS)]]
*   [[CommandInjection|Injection de Commandes]]
*   [[Vulnerability|Vulnérabilité]]
*   [[DatabaseSecurity|Sécurité des Bases de Données]]