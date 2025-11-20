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

> Un header est une section de métadonnées attachée au début d'un bloc de données (comme un paquet réseau, un message HTTP ou un fichier) qui fournit des informations essentielles sur le contenu, la source, la destination et les instructions de traitement.

## ⚙️ Fonctionnement et Concepts Clés

1.  **Structure**: Généralement constitué de paires clé-valeur (par exemple, `Content-Type: application/json` dans HTTP) qui définissent divers attributs du message ou de la ressource.
2.  **Fonctionnalité**: Permet aux protocoles de communication de fonctionner en indiquant des informations telles que l'expéditeur, le destinataire, le type de données, la taille, l'encodage, les instructions de cache, et des informations de sécurité.
3.  **Variété**: Présent dans de nombreux contextes, incluant les protocoles réseau (ex: IP, TCP, UDP), les protocoles applicatifs (ex: HTTP, SMTP) et les formats de fichiers.
4.  **Traitement**: Les systèmes interprètent les informations des headers pour router les données, appliquer des règles de sécurité, ou afficher le contenu correctement.

## ⚠️ Risques et Vulnérabilités

- Divulgation d'informations : Les headers peuvent involontairement révéler des détails sensibles sur l'infrastructure (versions de serveurs, technologies utilisées), facilitant les attaques ciblées.
- Manipulation d'en-têtes : Des acteurs malveillants peuvent modifier ou injecter des headers pour contourner des contrôles de sécurité, effectuer de l'usurpation de session, du XSS (via le header `Referer` ou `X-Forwarded-For`), ou des attaques par injection SQL.
- Attaques par déni de service (DoS) : Des headers malformés ou trop volumineux peuvent être utilisés pour provoquer des pannes ou des ralentissements, menant à une interruption de service.
- CSRF : Des vulnérabilités liées aux headers (notamment l'absence de vérification des headers `Origin` ou `Referer`) peuvent permettre ces attaques.

## 💎 Mesures de Protection et Bonnes Pratiques

- **Validation et Filtrage**: Implémenter une validation stricte et un filtrage des headers côté serveur pour rejeter les requêtes malformées ou contenant des valeurs suspectes.
- **Suppression des Headers Inutiles**: Éliminer les headers non essentiels qui pourraient révéler des informations d'infrastructure (ex: `X-Powered-By`, `Server`, `X-AspNet-Version`).
- **Implémentation de Headers de Sécurité**: Utiliser des headers HTTP spécifiques pour renforcer la sécurité web, tels que :
  - Content-Security-Policy (CSP) pour prévenir le XSS.
  - Strict-Transport-Security (HSTS) pour forcer l'utilisation de HTTPS.
  - X-Content-Type-Options: nosniff pour empêcher le reniflage de type MIME.
  - X-Frame-Options: DENYou`SAMEORIGIN` pour prévenir le clickjacking.
- **WAF**: Déployer un WAF pour inspecter et filtrer le trafic HTTP, y compris les headers, afin de bloquer les attaques courantes.
- **Journalisation**: Enregistrer les headers des requêtes et réponses pour l'analyse forensique et la détection d'activités suspectes.

## 🔗 Notes Connexes

- Protocole Réseau
- HTTP
- TCP
- IP
- Divulgation d'informations
- Pare-feu applicatif web
