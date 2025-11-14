---
tags:
  - securite/gestion-session
  - securite/attributs-http
  - web/cookies
  - vie-privee
aliases:
  - Cookies HTTP
  - Témoins de connexion
  - HTTP Cookies
  - cookie
  - cookies
source:
  - 
cssclasses:
  - max
---

# Cookies HTTP

## 📥 Définition en une phrase
> Les cookies HTTP sont de petits fichiers de données qu'un serveur web envoie à un navigateur web, lequel les stocke et les renvoie au même serveur lors des requêtes ultérieures, permettant ainsi de mémoriser l'état ou des informations sur l'utilisateur.

## 🧠 Concepts Clés / Fonctionnement
*   **Stockage côté client :** Les cookies sont stockés localement sur l'appareil de l'utilisateur par le navigateur, et non sur le serveur.
*   **Échange de données :** Le serveur envoie un cookie via l'en-tête `Set-Cookie` dans la réponse HTTP. Le navigateur renvoie ensuite ce cookie via l'en-tête `Cookie` dans les requêtes subséquentes au même domaine.
*   **Objectifs principaux :**
    *   **Gestion de session :** Maintien de l'état de l'utilisateur entre différentes requêtes (ex: statut de connexion, contenu d'un panier d'achat).
    *   **Personnalisation :** Mémorisation des préférences de l'utilisateur (ex: langue, thème).
    *   **Suivi et analyse :** Collecte d'informations sur le comportement de navigation pour des analyses ou de la publicité ciblée.
*   **Attributs clés :**
    *   `Expires`/`Max-Age` : Définit la durée de vie du cookie (session ou persistant).
    *   `Domain`/`Path` : Contrôle les domaines et chemins pour lesquels le cookie est envoyé.
    *   `Secure` : Indique que le cookie ne doit être envoyé qu'à travers une connexion HTTPS.
    *   `HttpOnly` : Empêche l'accès au cookie via JavaScript côté client, réduisant les risques de [[CrossSiteScripting|XSS]].
    *   `SameSite` : Permet de spécifier si les cookies doivent être envoyés avec des requêtes "cross-site", aidant à prévenir les attaques [[CrossSiteRequestForgery|CSRF]].

## 🛡️ Risques / Menaces Associés
*   [[SessionHijacking|Détournement de session]] : Si les cookies de session sont volés, un attaquant peut usurper l'identité de l'utilisateur.
*   [[CrossSiteRequestForgery|CSRF]] : Un attaquant peut forcer le navigateur d'un utilisateur authentifié à envoyer des requêtes malveillantes au serveur.
*   [[PrivacyViolation|Violation de la vie privée]] : Utilisation abusive des cookies pour le suivi non consenti et le profilage des utilisateurs.
*   [[InformationDisclosure|Divulgation d'informations]] : Stockage d'[[SensitiveData|informations sensibles]] non chiffrées dans les cookies, les rendant vulnérables à l'interception ou la consultation.
*   [[CrossSiteScripting|XSS]] : Un script malveillant injecté peut accéder aux cookies non `HttpOnly`.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utiliser HTTPS systématiquement :** Assure que les cookies sont envoyés via une connexion sécurisée, en utilisant l'attribut `Secure`.
*   **Mettre en œuvre `HttpOnly` :** Protège les cookies contre l'accès par [[CrossSiteScripting|XSS]], en particulier pour les cookies de session.
*   **Appliquer l'attribut `SameSite` :** Aide à prévenir les attaques [[CrossSiteRequestForgery|CSRF]] en contrôlant l'envoi de cookies dans des requêtes "cross-site".
*   **Minimiser les [[SensitiveData|informations sensibles]] :** Ne pas stocker de données personnelles ou sensibles non nécessaires dans les cookies. Si des [[SensitiveData|données sensibles]] sont absolument requises, [[DataEncryption|les chiffrer]].
*   **Définir des durées de vie courtes :** Surtout pour les cookies de session ou d'authentification, afin de limiter la fenêtre d'opportunité en cas de vol.
*   **Valider et nettoyer les entrées :** Assurer que les données lues des cookies sont validées et nettoyées pour prévenir les injections.
*   **Obtenir le [[ConsentManagement|consentement]] :** Se conformer aux réglementations sur la [[DataPrivacy|vie privée des données]] (ex: RGPD, CCPA) concernant l'utilisation des cookies.

## 🔗 Notes Connexes
*   [[WebApplicationSecurity|Sécurité des applications web]]
*   [[HypertextTransferProtocol|HTTP]]
*   [[SessionManagement|Gestion de session]]
*   [[DataPrivacy|Vie privée des données]]