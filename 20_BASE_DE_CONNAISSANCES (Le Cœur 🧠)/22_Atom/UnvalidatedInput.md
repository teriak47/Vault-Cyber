---
tags:
  - assainissement-donnees
  - securite-application/entree-non-validee
  - cybersécurité/attaque-injection
  - validation-entree
  - programmation/requetes-parametrees
  - cybersécurité/exploitation-vulnerabilite
aliases:
  - Entrée Non Validée
  - Unvalidated Input
source:
  - OWASP Top 10
cssclasses:
  - max
---

# Entrée Non Validée

## 📥 Définition en une phrase
> Une entrée non validée fait référence aux données reçues par une application qui n'ont pas été correctement vérifiées, nettoyées ou transformées avant d'être traitées ou stockées, ouvrant la porte à diverses vulnérabilités de sécurité.

## 🧠 Concepts Clés / Fonctionnement
*   **Absence de [[InputValidation|Validation d'Entrée]]** : L'application omet d'appliquer des règles de vérification rigoureuses sur les données provenant de sources externes (utilisateurs, API, fichiers, etc.).
*   **Confiance Implicite** : L'application fait confiance aux données reçues, supposant qu'elles sont toujours dans le format et le contenu attendus et qu'elles sont inoffensives.
*   **Types de non-validation** : Cela peut inclure l'absence de vérification du type de données, du format, de la longueur, de la plage de valeurs, ou la présence de caractères spéciaux malveillants.
*   **Contexte d'Exploitation** : Ces failles sont critiques lorsque l'entrée est utilisée pour construire des requêtes de base de données, générer du contenu web dynamique, accéder à des fichiers système ou exécuter des commandes sur le serveur.

## 🛡️ Risques / Menaces Associés
*   [[InjectionAttack|Attaques par injection]] (ex: [[SQLInjection|Injection SQL]], [[CommandInjection|Injection de commandes]], [[LDAPInjection|Injection LDAP]])
*   [[CrossSiteScripting|Cross-Site Scripting (XSS)]]
*   [[PathTraversal|Path Traversal]] (Traversée de chemin)
*   [[DenialOfService|Déni de Service (DoS)]] par manipulation de la charge utile d'entrée.
*   [[RemoteCodeExecution|Exécution de code à distance]] (RCE)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[InputValidation|Validation d'entrée]] : Toujours valider les entrées côté serveur (en plus de la validation côté client pour l'expérience utilisateur) en vérifiant le type, la longueur, le format et la plage des données.
*   [[DataSanitization|Assainissement des données]] : Nettoyer ou encoder les entrées pour neutraliser les caractères spéciaux avant de les afficher ou de les stocker.
*   [[Whitelisting|Validation par liste blanche]] : Autoriser uniquement les caractères, formats ou valeurs connus comme sûrs, plutôt que de tenter de bloquer les entrées malveillantes (liste noire).
*   [[ParameterizedQueries|Requêtes paramétrées]] : Utiliser des requêtes préparées ou des ORM pour interagir avec les bases de données afin de prévenir les injections SQL.
*   [[OutputEncoding|Encodage de sortie]] : Encoder toutes les données générées par l'utilisateur avant de les afficher dans une page web pour prévenir les attaques XSS.

## 🔗 Notes Connexes
*   [[OWASPTopTen|OWASP Top 10]]
*   [[InjectionAttack|Attaque par injection]]
*   [[CrossSiteScripting|Cross-Site Scripting]]
*   [[SecurityByDesign|Sécurité dès la Conception]]