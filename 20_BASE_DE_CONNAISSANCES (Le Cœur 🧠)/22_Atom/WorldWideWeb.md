---
tags:
  - communication/hypertexte
  - programmation/langage-web
  - securite/web/politique-contenu
  - internet
  - protocole/http
  - cyberattaque/deni-service
aliases:
  - Web
  - La Toile Mondiale
  - WWW
  - World Wide Web
source:
  - null
cssclasses:
  - max
---

# World Wide Web (WWW)

## 📥 Définition en une phrase
> Le World Wide Web est un système hypertexte public de documents et d'applications distribués et interconnectés via l'[[Internet]], accessible à l'aide d'un [[WebBrowser|navigateur web]].

## 🧠 Concepts Clés / Fonctionnement
*   **[[HypertextTransferProtocol|HTTP]]/[[HypertextTransferProtocolSecure|HTTPS]]** : Le [[Protocols|protocole]] fondamental utilisé pour la communication client-serveur sur le Web. [[HypertextTransferProtocolSecure|HTTPS]] est la version sécurisée, utilisant [[TransportLayerSecurity|TLS]] pour le chiffrement.
*   **[[UniformResourceLocator|URL]]** : Chaque ressource sur le Web est identifiée de manière unique par une adresse, appelée URL.
*   **[[HTML]] (HyperText Markup Language)** : Le langage standard de balisage utilisé pour structurer et présenter le contenu sur le Web, définissant la sémantique des documents.
*   **[[CSS]] (Cascading Style Sheets)** : Un langage de feuille de style utilisé pour décrire la présentation d'un document écrit en [[HTML]], y compris les couleurs, les polices et la disposition.
*   **[[JavaScript]]** : Un langage de script côté client qui permet d'ajouter de l'interactivité et des fonctionnalités dynamiques aux pages web.
*   **Serveurs Web** : Logiciels qui stockent les pages web et les délivrent aux [[WebBrowser|navigateurs web]] en réponse aux requêtes [[HypertextTransferProtocol|HTTP]].

## 🛡️ Risques / Menaces Associés
*   [[CrossSiteScripting|XSS]] (Cross-Site Scripting) : Injection de scripts malveillants côté client.
*   [[SQLInjection|Injection SQL]] : Exploitation de vulnérabilités pour manipuler les bases de données via des requêtes.
*   [[DenialOfService|Attaques par Déni de Service (DoS/DDoS)]] : Surcharge de serveurs web pour rendre les services indisponibles.
*   [[Phishing|Hameçonnage]] : Usurpation d'identité pour collecter des [[SensitiveData|informations sensibles]].
*   [[Malware|Logiciels Malveillants]] : Diffusion via des sites web compromis ou des téléchargements.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utilisation de [[HypertextTransferProtocolSecure|HTTPS]]** : Chiffrement du trafic pour protéger la confidentialité et l'intégrité des données.
*   **[[WebApplicationFirewall|WAF]]** : Protection contre les attaques au niveau de l'application web.
*   **[[SecureCoding|Développement sécurisé]]** : Application de bonnes pratiques de codage pour prévenir les vulnérabilités (ex: validation des entrées, échappement des sorties).
*   **[[ContentSecurityPolicy|Politique de Sécurité du Contenu (CSP)]]** : Réduction du risque de [[CrossSiteScripting|XSS]] et d'autres attaques par injection.
*   **Mises à jour régulières** : Maintenir les serveurs web, CMS et bibliothèques à jour pour patcher les vulnérabilités connues.

## 🔗 Notes Connexes
*   [[Internet]]
*   [[WebBrowser]]
*   [[DomainNameSystem|DNS]]
*   [[UniformResourceLocator|URL]]
*   [[HypertextTransferProtocol|HTTP]]
*   [[TransportLayerSecurity|TLS]]