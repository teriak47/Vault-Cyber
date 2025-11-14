---
tags:
  - attaque/injection-client
  - securite/encodage-sortie
  - politique-securite/contenu
  - cybersécurité
  - validation-entree
  - vulnerabilite/injection-web
aliases:
  - Scripting Inter-sites
  - XSS
  - Cross-Site Scripting
source:
  - null
cssclasses:
  - max
---

# Cross-Site Scripting (XSS)

## 📥 Définition en une phrase
> Le Cross-Site Scripting (XSS) est une vulnérabilité de sécurité des applications web qui permet à un attaquant d'injecter du [[MaliciousCode|code malveillant]] (généralement JavaScript) côté client dans les pages web vues par d'autres utilisateurs.

## 🧠 Concepts Clés / Fonctionnement
*   **Injection de code client**: Contrairement à d'autres attaques d'injection, le XSS cible l'exécution de scripts dans le navigateur de l'utilisateur final plutôt que sur le serveur.
*   **Types de XSS**:
    *   **XSS Persistant (Stored XSS)**: Le code malveillant est stocké de manière permanente sur le serveur (ex: dans une base de données) et délivré aux utilisateurs par l'application web. C'est le type le plus dangereux car il affecte tous les utilisateurs qui accèdent à la page compromise.
    *   **XSS Reflété (Reflected XSS)**: Le code malveillant est réfléchi depuis le serveur web vers le navigateur de l'utilisateur. Il est généralement livré via une URL malveillante dans un e-mail ou un autre site web, et ne se manifeste que lorsque l'utilisateur clique sur le lien.
    *   **XSS Basé sur le DOM (DOM-based XSS)**: La vulnérabilité réside dans le code côté client lui-même, plutôt que dans le code côté serveur. Le script malveillant modifie le Document Object Model (DOM) de la page dans le navigateur de l'utilisateur.
*   **Mécanisme**: L'attaque exploite le fait que l'application web ne valide pas ou n'échappe pas correctement les entrées utilisateur avant de les afficher sur une page web.

## 🛡️ Risques / Menaces Associés
*   [[SessionHijacking|Détournement de session]] via le vol de cookies.
*   [[DataTheft|Vol de données]] sensibles (informations d'identification, données personnelles).
*   [[Defacement|Défiguration]] de sites web.
*   [[Malware|Distribution de logiciels malveillants]] via des redirections.
*   [[Phishing|Attaques de phishing]] ciblant les utilisateurs.
*   [[Vulnerability|Vulnérabilité de validation d'entrée]] (Input Validation Vulnerability).

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[InputValidation|Validation rigoureuse des entrées]] côté serveur et client (filtrage, assainissement).
*   [[OutputEncoding|Encodage contextuel des sorties]] pour neutraliser les caractères spéciaux avant qu'ils ne soient rendus par le navigateur.
*   Utilisation de [[ContentSecurityPolicy|Politiques de Sécurité du Contenu (CSP)]] pour restreindre les sources de scripts et autres ressources.
*   Marquer les cookies comme `HttpOnly` pour empêcher l'accès aux cookies via JavaScript.
*   Utilisation d'un [[WebApplicationFirewall|Pare-feu d'Application Web (WAF)]] pour détecter et bloquer les attaques XSS.

## 🔗 Notes Connexes
*   [[WebApplicationSecurity|Sécurité des applications web]]
*   [[SQLInjection|Injection SQL]]
*   [[CrossSiteRequestForgery|Cross-Site Request Forgery (CSRF)]]
*   [[InputValidation|Validation des entrées]]