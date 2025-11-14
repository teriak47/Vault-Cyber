---
tags:
  - serveur-web
  - protocole-http
  - architecture-client-serveur
  - pare-feu
  - cyberattaque/deni-service
  - attaque/injection-sql-aveugle
aliases:
  - Serveur Web
  - Web Server
source:
  - null
cssclasses:
  - max
---

# Serveur Web

## 📥 Définition en une phrase
> Un [[WebServer|serveur web]] est un programme informatique ou un appareil qui stocke des fichiers de [[Website|sites web]] et les délivre aux [[Client|navigateurs web]] sur demande, utilisant principalement le [[HypertextTransferProtocol|protocole HTTP]].

## 🧠 Concepts Clés / Fonctionnement
*   **Hébergement de Contenu** : Il stocke les composants d'un site web, tels que les pages [[HypertextMarkupLanguage|HTML]], les feuilles de style [[CascadingStyleSheets|CSS]], les images, les fichiers [[JavaScript|script]] et d'autres médias.
*   **Traitement des Requêtes** : Lorsqu'un [[Client|navigateur web]] envoie une [[HypertextTransferProtocol|requête HTTP]] (par exemple, pour afficher une page), le [[WebServer|serveur web]] la reçoit et la traite.
*   **Envoi des Réponses** : Après avoir traité la requête, le [[WebServer|serveur web]] renvoie la ressource demandée au [[Client|navigateur]] via une [[HypertextTransferProtocol|réponse HTTP]].
*   **Partie de l'Architecture Client-Serveur** : Le [[WebServer|serveur web]] est une composante essentielle de l'[[ClientServerArchitecture|architecture client-serveur]], agissant comme le "serveur" qui répond aux requêtes des "clients".

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service]] ([[DistributedDenialOfService|DDoS]]) visant à rendre le [[WebServer|serveur]] indisponible.
*   [[SqlInjection|Injections SQL]] lorsque le [[WebServer|serveur]] interagit avec une [[Database|base de données]] vulnérable.
*   [[CrossSiteScripting|Cross-Site Scripting (XSS)]] et d'autres [[SoftwareVulnerability|vulnérabilités logicielles]] dans l'application web hébergée.
*   [[RemoteCodeExecution|Exécution de Code à Distance]] (RCE) via des [[Exploit|exploits]] ciblant des failles du [[WebServer|serveur]] ou de ses applications.
*   [[DataBreach|Fuites de données]] sensibles stockées sur le [[WebServer|serveur]] en cas d'accès non autorisé.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en place un [[Firewall|pare-feu]] pour filtrer le trafic entrant et sortant.
*   Appliquer régulièrement le [[PatchManagement|patch management]] et les mises à jour de sécurité pour le [[OperatingSystem|système d'exploitation]] et le [[WebServer|logiciel serveur]].
*   Implémenter des [[AccessControl|contrôles d'accès]] stricts et le principe du moindre privilège pour les utilisateurs et les processus du [[WebServer|serveur]].
*   Réaliser des [[SecurityAudit|audits de sécurité]] réguliers, des tests de pénétration et des analyses de vulnérabilités.
*   Utiliser le [[DataEncryption|chiffrement]] (ex: [[TransportLayerSecurity|TLS]]) pour sécuriser les communications entre le [[Client|navigateur]] et le [[WebServer|serveur]].
*   Protéger le [[WebServer|serveur]] contre les attaques par force brute avec la [[RateLimiting|limitation de débit]] et le [[AccountLockout|verrouillage de compte]].

## 🔗 Notes Connexes
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[HypertextTransferProtocol|HTTP]]
*   [[Server|Serveur]]
*   [[Internet|Internet]]
*   [[WebBrowser|Navigateur Web]]
*   [[TransportLayerSecurity|TLS]]