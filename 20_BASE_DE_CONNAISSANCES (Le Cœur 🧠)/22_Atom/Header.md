---
tags:
  - cybersecurite/manipulation-entetes
  - securite/politiques-entetes-http
  - journalisation/securite/entetes
  - communication/metadonnees
  - securite/en-tetes-http
  - securite/validation-entrees
aliases:
  - En-tête
  - En-tête de protocole
  - HTTP Header
  - Network Header
source:
  - null
cssclasses:
  - max
---

# Header (En-tête)

## 📥 Définition en une phrase
> Un header est une section de métadonnées attachée au début d'un bloc de données (comme un paquet réseau, un message HTTP ou un fichier) qui fournit des informations essentielles sur le contenu, la source, la destination et les instructions de traitement.

## 🧠 Concepts Clés / Fonctionnement
*   **Structure**: Généralement constitué de paires clé-valeur (par exemple, `Content-Type: application/json` dans [[HTTP|HTTP]]) qui définissent divers attributs du message ou de la ressource.
*   **Fonctionnalité**: Permet aux protocoles de communication de fonctionner en indiquant des informations telles que l'expéditeur, le destinataire, le type de données, la taille, l'encodage, les instructions de cache, et des informations de sécurité.
*   **Variété**: Présent dans de nombreux contextes, incluant les [[NetworkProtocol|protocoles réseau]] (ex: [[InternetProtocol|IP]], [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]), les protocoles applicatifs (ex: [[HTTP|HTTP]], [[SimpleMailTransferProtocol|SMTP]]) et les formats de fichiers.
*   **Traitement**: Les systèmes interprètent les informations des headers pour router les données, appliquer des règles de sécurité, ou afficher le contenu correctement.

## 🛡️ Risques / Menaces Associés
*   [[InformationDisclosure|Divulgation d'informations]] : Les headers peuvent involontairement révéler des détails sensibles sur l'infrastructure (versions de serveurs, technologies utilisées), facilitant les attaques ciblées.
*   [[HeaderManipulation|Manipulation d'en-têtes]] : Des acteurs malveillants peuvent modifier ou injecter des headers pour contourner des contrôles de sécurité, effectuer de l'[[SessionHijacking|usurpation de session]], du [[CrossSiteScripting|XSS]] (via le header `Referer` ou `X-Forwarded-For`), ou des attaques par [[SQLInjection|injection SQL]].
*   [[DenialOfService|Attaques par déni de service]] (DoS) : Des headers malformés ou trop volumineux peuvent être utilisés pour provoquer des pannes ou des ralentissements.
*   [[CrossSiteRequestForgery|CSRF]] : Des vulnérabilités liées aux headers (notamment l'absence de vérification des headers `Origin` ou `Referer`) peuvent permettre ces attaques.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Validation et Filtrage**: Implémenter une validation stricte et un filtrage des headers côté serveur pour rejeter les requêtes malformées ou contenant des valeurs suspectes.
*   **Suppression des Headers Inutiles**: Éliminer les headers non essentiels qui pourraient révéler des informations d'infrastructure (ex: `X-Powered-By`, `Server`, `X-AspNet-Version`).
*   **Implémentation de Headers de Sécurité**: Utiliser des headers HTTP spécifiques pour renforcer la sécurité web, tels que :
    *   `Content-Security-Policy` ([[ContentSecurityPolicy|CSP]]) pour prévenir le [[CrossSiteScripting|XSS]].
    *   `Strict-Transport-Security` ([[HTTPStrictTransportSecurity|HSTS]]) pour forcer l'utilisation de [[TransportLayerSecurity|HTTPS]].
    *   `X-Content-Type-Options: nosniff` pour empêcher le reniflage de type MIME.
    *   `X-Frame-Options: DENY` ou `SAMEORIGIN` pour prévenir le [[Clickjacking|clickjacking]].
*   **[[WebApplicationFirewall|WAF]]**: Déployer un WAF pour inspecter et filtrer le trafic HTTP, y compris les headers, afin de bloquer les attaques courantes.
*   **Journalisation**: Enregistrer les headers des requêtes et réponses pour l'[[IncidentResponse|analyse forensique]] et la détection d'activités suspectes.

## 🔗 Notes Connexes
*   [[NetworkProtocol|Protocole Réseau]]
*   [[HTTP|HTTP]]
*   [[TransmissionControlProtocol|TCP]]
*   [[InternetProtocol|IP]]
*   [[InformationDisclosure|Divulgation d'informations]]
*   [[WebApplicationFirewall|Pare-feu applicatif web]]