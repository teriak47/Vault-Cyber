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
> Les [[HttpCookies|Cookies HTTP]] sont de petits fichiers de données qu'un [[WebServer|serveur web]] envoie à un [[WebBrowsers|navigateur web]]. Ils sont stockés localement par le navigateur et renvoyés au même serveur lors des requêtes ultérieures, permettant ainsi de maintenir l'état, de mémoriser des informations ou de suivre l'[[User|utilisateur]] sur le [[WorldWideWeb|Web]]. Ils opèrent au niveau de la [[ApplicationLayer|couche Application]] du [[InternetProtocolSuite|modèle TCP/IP]], spécifiquement pour le [[HypertextTransferProtocol|protocole HTTP]].

## ⚙️ Fonctionnement
1.  **Envoi initial par le serveur**: Lorsqu'un [[WebBrowsers|navigateur]] fait une [[Request|requête]] à un [[WebServer|serveur web]], le serveur peut inclure un ou plusieurs cookies dans l'[[Header|en-tête]] `Set-Cookie` de sa [[Message|réponse HTTP]].
2.  **Stockage par le navigateur**: Le [[WebBrowsers|navigateur]] reçoit les cookies et les stocke sur l'[[Computer|appareil]] de l'[[User|utilisateur]].
3.  **Renvoi automatique**: Pour toutes les [[Request|requêtes]] subséquentes vers le même [[DomainNameSystem|domaine]], le [[WebBrowsers|navigateur]] inclut automatiquement ces cookies dans l'[[Header|en-tête]] `Cookie` de la [[Message|requête HTTP]].
4.  **Objectifs principaux**:
    *   **[[SessionManagement|Gestion de session]]**: Maintien de l'état de l'[[User|utilisateur]] entre différentes [[Request|requêtes]] (ex: statut de [[Login|connexion]], contenu d'un [[ShoppingCart|panier d'achat]]).
    *   **[[Personalization|Personnalisation]]**: Mémorisation des préférences de l'[[User|utilisateur]] (ex: langue, thème).
    *   **[[UserTracking|Suivi et analyse]]**: Collecte d'informations sur le comportement de navigation pour des analyses ou de la [[TargetedAdvertising|publicité ciblée]].
*   **Attributs Clés des Cookies**:
    *   `Expires`/`Max-Age`: Définit la durée de vie du cookie (cookie de session ou [[PersistentCookie|persistant]]).
    *   `Domain`/`Path`: Contrôle les [[DomainNameSystem|domaines]] et [[URLPath|chemins]] pour lesquels le cookie est envoyé.
    *   `Secure`: Indique que le cookie ne doit être envoyé qu'à travers une connexion [[HypertextTransferProtocolSecure|HTTPS]].
    *   `HttpOnly`: Empêche l'accès au cookie via [[JavaScript|JavaScript]] côté [[Client|client]], réduisant les risques de [[CrossSiteScripting|XSS]].
    *   `SameSite`: Permet de spécifier si les cookies doivent être envoyés avec des [[CrossSiteRequest|requêtes "cross-site"]], aidant à prévenir les attaques [[CrossSiteRequestForgery|CSRF]].
*   **Ports par défaut**: Les [[HttpCookies|Cookies HTTP]] utilisent les ports standards du [[HypertextTransferProtocol|HTTP]] (TCP/80) ou [[HypertextTransferProtocolSecure|HTTPS]] (TCP/443).

## 🛡️ Sécurité du Protocole
*   **[[Vulnerability|Vulnérabilités]] connues**:
    *   [[SessionHijacking|Détournement de session]] : Si les cookies de session sont volés, un [[ThreatActor|attaquant]] peut usurper l'[[UserIdentity|identité de l'utilisateur]].
    *   [[CrossSiteRequestForgery|CSRF]] : Un [[ThreatActor|attaquant]] peut forcer le [[WebBrowsers|navigateur]] d'un [[User|utilisateur]] [[Authentication|authentifié]] à envoyer des [[MaliciousRequest|requêtes malveillantes]] au [[WebServer|serveur]].
    *   [[PrivacyInvasion|Violation de la vie privée]] : Utilisation abusive des cookies pour le [[UserTracking|suivi non consenti]] et le [[UserProfiling|profilage des utilisateurs]].
    *   [[InformationDisclosure|Divulgation d'informations]] : Stockage de [[SensitiveData|données sensibles]] non [[DataEncryption|chiffrées]] dans les cookies, les rendant vulnérables à l'[[Eavesdropping|interception]] ou la consultation.
    *   [[CrossSiteScripting|XSS]] : Un [[MaliciousScript|script malveillant]] injecté peut accéder aux cookies non `HttpOnly`.
*   **Mesures de protection et bonnes pratiques**:
    *   **Utiliser `Secure` avec [[HypertextTransferProtocolSecure|HTTPS]] systématiquement** : Assure que les cookies sont envoyés uniquement sur des connexions [[DataEncryption|chiffrées]], protégeant contre l'[[Eavesdropping|interception]].
    *   **Implémenter `HttpOnly`** : Prévient l'accès des [[JavaScript|scripts]] côté [[Client|client]] aux cookies, réduisant le risque de vol de cookies via [[CrossSiteScripting|XSS]].
    *   **Appliquer l'attribut `SameSite`** : Aide à se défendre contre les attaques [[CrossSiteRequestForgery|CSRF]] en limitant l'envoi de cookies dans des [[CrossSiteRequest|requêtes "cross-site"]].
    *   **Minimiser les [[SensitiveData|données sensibles]]** : Ne pas stocker d'[[PersonalData|informations personnelles]] ou [[SensitiveData|sensibles]] non nécessaires. Si des [[SensitiveData|données sensibles]] sont absolument requises, [[DataEncryption|les chiffrer]].
    *   **Définir des durées de vie courtes** : Surtout pour les cookies de session et d'[[Authentication|authentification]], afin de limiter la fenêtre d'opportunité en cas de vol.
    *   **Valider et nettoyer les entrées** : S'assurer que les données lues des cookies sont toujours validées et nettoyées pour prévenir les [[InjectionAttack|attaques par injection]].
    *   **Obtenir le [[ConsentManagement|consentement de l'utilisateur]]** : Se conformer aux [[GeneralDataProtectionRegulation|réglementations sur la protection des données]] (ex: RGPD, CCPA) concernant l'utilisation des cookies, en particulier ceux à des fins de [[UserTracking|suivi]].

## 🔗 Notes Connexes
*   [[HypertextTransferProtocol|HTTP]]
*   [[SessionManagement|Gestion de session]]
*   [[WebBrowsers|Navigateurs Web]]
*   [[DataProtection|Protection des Données]]
*   [[WebApplicationSecurity|Sécurité des applications web]]