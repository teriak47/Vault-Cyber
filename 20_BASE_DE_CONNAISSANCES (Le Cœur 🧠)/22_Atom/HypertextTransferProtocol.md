---
tags:
  - methode-http
  - protocole/sans-etat
  - securite/en-tetes-http
  - protocole/http
  - reseau/couche-application
  - modele/client-serveur
aliases:
  - HTTP
  - Hypertext Transfer Protocol
  - Protocole de Transfert Hypertexte
source:
  - null
cssclasses:
  - max
---

# Protocole de Transfert Hypertexte (HTTP)

## 📥 Définition en une phrase
> Le Protocole de Transfert Hypertexte (HTTP) est un protocole de la [[ApplicationLayer|couche application]] pour les systèmes d'information distribués, collaboratifs et hypermédias, servant de base à la communication de données sur le World Wide Web.

## 🧠 Concepts Clés / Fonctionnement
*   **Modèle Client-Serveur:** HTTP fonctionne sur un modèle [[ClientServerArchitecture|client-serveur]] où le client (généralement un navigateur web) envoie des requêtes au serveur web, qui répond avec les ressources demandées.
*   **Sans État (Stateless):** Chaque requête HTTP est traitée indépendamment des requêtes précédentes. Pour maintenir un état (comme une session utilisateur), des mécanismes supplémentaires comme les [[HttpCookies|cookies]] sont utilisés.
*   **Méthodes HTTP (Verbs):** Les verbes HTTP (GET, POST, PUT, DELETE, HEAD, OPTIONS, PATCH) définissent l'action à effectuer sur la ressource identifiée. Par exemple, `GET` récupère une ressource, et `POST` soumet des données pour traitement.
*   **En-têtes HTTP (Headers):** Les en-têtes HTTP transportent des méta-informations sur la requête ou la réponse, telles que le type de contenu, l'agent utilisateur, les paramètres de cache, etc.
*   **Ports Standard:** Par défaut, HTTP utilise le port [[TransmissionControlProtocol|TCP]] 80.
*   **Versions:** Plusieurs versions existent, notamment HTTP/1.0, HTTP/1.1 (la plus répandue pendant longtemps), HTTP/2 (améliorant la performance) et HTTP/3 (basé sur [[QuickUdpInternetConnections|QUIC]]).

## 🛡️ Risques / Menaces Associés
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] (lorsque la communication n'est pas chiffrée via [[HypertextTransferProtocolSecure|HTTPS]]).
*   [[DataLeakage|Fuite de données]] par transmission en clair d'[[SensitiveData|informations sensibles]] (identifiants, données personnelles).
*   [[SessionHijacking|Détournement de session]] si les cookies de session ne sont pas sécurisés.
*   [[InjectionAttack|Attaques par injection]] (comme le [[CrossSiteScripting|XSS]] ou l'[[SqlInjection|injection SQL]]) via des entrées utilisateur mal validées dans les requêtes HTTP.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[HypertextTransferProtocolSecure|Utiliser HTTPS]]: Toujours privilégier et imposer l'utilisation de [[HypertextTransferProtocolSecure|HTTPS]] pour chiffrer les communications via [[TransportLayerSecurity|TLS/SSL]].
*   [[WebApplicationFirewall|Mettre en œuvre un WAF]]: Déployer un [[WebApplicationFirewall|pare-feu d'application web]] pour filtrer et bloquer les requêtes malveillantes.
*   [[SecurityHeaders|Implémenter des en-têtes de sécurité]]: Utiliser des en-têtes comme `Content-Security-Policy` (CSP) et `HTTP Strict Transport Security` (HSTS) pour renforcer la sécurité du navigateur.
*   [[InputValidation|Valider et assainir les entrées]]: Effectuer une [[InputValidation|validation rigoureuse des entrées]] côté serveur pour prévenir les attaques par injection.
*   [[SecureCodingPractices|Pratiques de développement sécurisé]]: Suivre les principes de [[SecureCodingPractices|développement sécurisé]] pour éviter les vulnérabilités courantes.

## 🔗 Notes Connexes
*   [[HypertextTransferProtocolSecure|HTTPS]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UniformResourceLocator|URL]]
*   [[TransportLayerSecurity|TLS]]
*   [[DomainNameSystem|DNS]]
*   [[WebApplication|Application Web]]