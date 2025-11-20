---
tags:
  - protocole
aliases:
  - Cookies HTTP
  - Témoins de connexion
  - HTTP Cookies
  - cookie
  - cookies
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Cookies HTTP

## 🎯 Rôle et Couche OSI
> Les Cookies HTTP sont de petits fichiers de données qu'un serveur web envoie à un navigateur web. Ils sont stockés localement par le navigateur et renvoyés au même serveur lors des requêtes ultérieures, permettant ainsi de maintenir l'état, de mémoriser des informations ou de suivre l'utilisateur sur le Web. Ils opèrent au niveau de la couche Application du modèle TCP/IP, spécifiquement pour le protocole HTTP.

## ⚙️ Fonctionnement
1.  **Envoi initial par le serveur**: Lorsqu'un navigateur fait une requête à un serveur web, le serveur peut inclure un ou plusieurs cookies dans l'en-tête `Set-Cookie` de sa réponse HTTP.
2.  **Stockage par le navigateur**: Le navigateur reçoit les cookies et les stocke sur l'appareil de l'utilisateur.
3.  **Renvoi automatique**: Pour toutes les requêtes subséquentes vers le même domaine, le navigateur inclut automatiquement ces cookies dans l'en-tête `Cookie` de la requête HTTP.
4.  **Objectifs principaux**:
    *   **Gestion de session**: Maintien de l'état de l'utilisateur entre différentes requêtes (ex: statut de connexion, contenu d'un panier d'achat).
    *   **Personnalisation**: Mémorisation des préférences de l'utilisateur (ex: langue, thème).
    *   **Suivi et analyse**: Collecte d'informations sur le comportement de navigation pour des analyses ou de la publicité ciblée.
*   **Attributs Clés des Cookies**:
    *   `Expires`/`Max-Age`: Définit la durée de vie du cookie (cookie de session ou persistant).
    *   `Domain`/`Path`: Contrôle les domaines et chemins pour lesquels le cookie est envoyé.
    *   `Secure`: Indique que le cookie ne doit être envoyé qu'à travers une connexion HTTPS.
    *   `HttpOnly`: Empêche l'accès au cookie via JavaScript côté client, réduisant les risques de XSS.
    *   `SameSite`: Permet de spécifier si les cookies doivent être envoyés avec des requêtes "cross-site", aidant à prévenir les attaques CSRF.
*   **Ports par défaut**: Les Cookies HTTP utilisent les ports standards du HTTP (TCP/80) ou HTTPS (TCP/443).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Détournement de session : Si les cookies de session sont volés, un attaquant peut usurper l'identité de l'utilisateur.
    *   CSRF : Un attaquant peut forcer le navigateur d'un utilisateur authentifié à envoyer des requêtes malveillantes au serveur.
    *   Violation de la vie privée : Utilisation abusive des cookies pour le suivi non consenti et le profilage des utilisateurs.
    *   Divulgation d'informations : Stockage de données sensibles non chiffrées dans les cookies, les rendant vulnérables à l'interception ou la consultation.
    *   XSS : Un script malveillant injecté peut accéder aux cookies non `HttpOnly`.
*   **Mesures de protection et bonnes pratiques**:
    *   **Utiliser `Secure` avec HTTPS systématiquement** : Assure que les cookies sont envoyés uniquement sur des connexions chiffrées, protégeant contre l'interception.
    *   **Implémenter `HttpOnly`** : Prévient l'accès des scripts côté client aux cookies, réduisant le risque de vol de cookies via XSS.
    *   **Appliquer l'attribut `SameSite`** : Aide à se défendre contre les attaques CSRF en limitant l'envoi de cookies dans des requêtes "cross-site".
    *   **Minimiser les données sensibles** : Ne pas stocker d'informations personnelles ou sensibles non nécessaires. Si des données sensibles sont absolument requises, les chiffrer.
    *   **Définir des durées de vie courtes** : Surtout pour les cookies de session et d'authentification, afin de limiter la fenêtre d'opportunité en cas de vol.
    *   **Valider et nettoyer les entrées** : S'assurer que les données lues des cookies sont toujours validées et nettoyées pour prévenir les attaques par injection.
    *   **Obtenir le consentement de l'utilisateur** : Se conformer aux réglementations sur la protection des données (ex: RGPD, CCPA) concernant l'utilisation des cookies, en particulier ceux à des fins de suivi.

## 🔗 Notes Connexes
*   HTTP
*   Gestion de session
*   Navigateurs Web
*   Protection des Données
*   Sécurité des applications web