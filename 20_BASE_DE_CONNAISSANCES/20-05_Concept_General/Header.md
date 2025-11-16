---
tags:
  - reseau
  - securite/web
aliases:
  - En-tête
  - En-tête de protocole
  - HTTP Header
  - Network Header
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Header (En-tête)

## 🎯 Rôle
> Un header est une section de métadonnées attachée au début d'un bloc de [[Data|données]] (comme un [[Packet|paquet]] [[Network|réseau]], un [[Message|message]] [[HypertextTransferProtocol|HTTP]] ou un fichier) qui fournit des informations essentielles sur le [[Payload|contenu]], la [[SourceInternetProtocolVersion4Address|source]], la [[DestinationInternetProtocolVersion4Address|destination]] et les instructions de traitement.

## ⚙️ Fonctionnement et Concepts Clés
1.  **Structure**: Généralement constitué de paires clé-valeur (par exemple, `Content-Type: application/json` dans [[HypertextTransferProtocol|HTTP]]) qui définissent divers attributs du [[Message|message]] ou de la [[Resource|ressource]].
2.  **Fonctionnalité**: Permet aux [[NetworkProtocol|protocoles de communication]] de fonctionner en indiquant des informations telles que l'expéditeur, le destinataire, le type de [[Data|données]], la [[MessageSize|taille]], l'[[Encoding|encodage]], les instructions de cache, et des informations de [[Security|sécurité]].
3.  **Variété**: Présent dans de nombreux contextes, incluant les [[NetworkProtocol|protocoles réseau]] (ex: [[InternetProtocol|IP]], [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]), les [[SoftwareApplication|protocoles applicatifs]] (ex: [[HypertextTransferProtocol|HTTP]], [[SimpleMailTransferProtocol|SMTP]]) et les formats de fichiers.
4.  **Traitement**: Les [[System|systèmes]] interprètent les informations des headers pour [[Routing|router]] les [[Data|données]], appliquer des règles de [[Security|sécurité]], ou afficher le [[Payload|contenu]] correctement.

## ⚠️ Risques et Vulnérabilités
*   [[InformationDisclosure|Divulgation d'informations]] : Les headers peuvent involontairement révéler des détails sensibles sur l'[[NetworkInfrastructure|infrastructure]] (versions de [[Server|serveurs]], [[WirelessTechnology|technologies]] utilisées), facilitant les [[DigitalAttack|attaques ciblées]].
*   [[HeaderManipulation|Manipulation d'en-têtes]] : Des [[ThreatActor|acteurs malveillants]] peuvent modifier ou injecter des headers pour contourner des [[AccessControl|contrôles de sécurité]], effectuer de l'[[SessionHijacking|usurpation de session]], du [[CrossSiteScripting|XSS]] (via le header `Referer` ou `X-Forwarded-For`), ou des [[SqlInjection|attaques par injection SQL]].
*   [[DenialOfService|Attaques par déni de service]] ([[DenialOfService|DoS]]) : Des headers malformés ou trop volumineux peuvent être utilisés pour provoquer des pannes ou des ralentissements, menant à une [[ServiceDisruption|interruption de service]].
*   [[CrossSiteRequestForgery|CSRF]] : Des [[Vulnerability|vulnérabilités]] liées aux headers (notamment l'absence de vérification des headers `Origin` ou `Referer`) peuvent permettre ces [[DigitalAttack|attaques]].

## 💎 Mesures de Protection et Bonnes Pratiques
*   **Validation et Filtrage**: Implémenter une validation stricte et un filtrage des headers côté [[Server|serveur]] pour rejeter les [[Request|requêtes]] malformées ou contenant des valeurs suspectes.
*   **Suppression des Headers Inutiles**: Éliminer les headers non essentiels qui pourraient révéler des informations d'[[NetworkInfrastructure|infrastructure]] (ex: `X-Powered-By`, `Server`, `X-AspNet-Version`).
*   **Implémentation de [[SecurityHeader|Headers de Sécurité]]**: Utiliser des headers [[HypertextTransferProtocol|HTTP]] spécifiques pour renforcer la [[Security|sécurité]] [[WorldWideWeb|web]], tels que :
    *   `[[ContentSecurityPolicy|Content-Security-Policy]]` ([[ContentSecurityPolicy|CSP]]) pour prévenir le [[CrossSiteScripting|XSS]].
    *   `[[HTTPStrictTransportSecurity|Strict-Transport-Security]]` ([[HTTPStrictTransportSecurity|HSTS]]) pour forcer l'utilisation de [[TransportLayerSecurity|HTTPS]].
    *   `[[XContentTypeOptions|X-Content-Type-Options: nosniff]]` pour empêcher le reniflage de type MIME.
    *   `[[XFrameOptions|X-Frame-Options: DENY]]` ou `SAMEORIGIN` pour prévenir le [[Clickjacking|clickjacking]].
*   **[[WebApplicationFirewall|WAF]]**: Déployer un [[WebApplicationFirewall|WAF]] pour inspecter et filtrer le [[NetworkTrafficAnalysis|trafic HTTP]], y compris les headers, afin de bloquer les [[DigitalAttack|attaques]] courantes.
*   **[[Log|Journalisation]]**: Enregistrer les headers des [[Request|requêtes]] et [[Response|réponses]] pour l'[[IncidentResponse|analyse forensique]] et la [[AnomalyDetection|détection d'activités suspectes]].

## 🔗 Notes Connexes
*   [[NetworkProtocol|Protocole Réseau]]
*   [[HypertextTransferProtocol|HTTP]]
*   [[TransmissionControlProtocol|TCP]]
*   [[InternetProtocol|IP]]
*   [[InformationDisclosure|Divulgation d'informations]]
*   [[WebApplicationFirewall|Pare-feu applicatif web]]