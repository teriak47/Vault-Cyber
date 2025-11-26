---
aliases:
  - Serveur Web
  - Web Server
  - HTTP Server
  - HTTPS Server
cssclasses:
  - max
archetype: logiciel
tags:
  - logiciel
  - serveur/web
  - securite
  - securite/logiciel
  - hardening
  - protocole/http
  - protocole/https
  - certificat/ssl-tls
  - protocole/ssl-tls
  - confidentialite
  - integrite
  - authentification
  - vulnerabilite
  - cve
  - vulnerabilite/mauvaise-configuration
  - attaque
  - attaque/deni-de-service
  - vulnerabilite/injection-sql
  - vulnerabilite/xss
  - ddos
  - checklist
  - principe/moindre-privilege
  - waf
  - systeme/configuration
  - log/gestion
  - securite/web
  - cybersecurite/defensif
---

# Web Server

> [!summary] À quoi ça sert ?
> Un **serveur web** est un programme informatique qui stocke les fichiers d'un site web (comme les documents HTML, les feuilles de style CSS, les fichiers JavaScript, les images, etc.) et les délivre aux navigateurs web des utilisateurs à la demande. Il utilise le protocole *Hypertext Transfer Protocol* (HTTP) ou *Hypertext Transfer Protocol Secure* (HTTPS) pour communiquer avec les clients. Son rôle principal est de répondre aux requêtes HTTP/HTTPS en envoyant le contenu approprié, permettant ainsi l'affichage des sites web sur internet ou un réseau local.

## ⚙️ Configuration Clé
*   **Fichier de conf (Exemples)** :
    *   Apache: `/etc/apache2/apache2.conf` ou `/etc/httpd/conf/httpd.conf`
    *   Nginx: `/etc/nginx/nginx.conf`
*   **Port par défaut** : 80 (HTTP), 443 (HTTPS)
*   **Logs (Exemples)** :
    *   Apache: `/var/log/apache2/access.log` et `/var/log/apache2/error.log`
    *   Nginx: `/var/log/nginx/access.log` et `/var/log/nginx/error.log`

## 🌐 Mécanismes de Fonctionnement (HTTP/HTTPS)

### HTTP (Hypertext Transfer Protocol)
HTTP est le protocole fondamental utilisé pour transférer des informations sur le World Wide Web. Il fonctionne sur un [[ClientServerModel|modèle client-serveur]], où le navigateur web (client) envoie des requêtes au serveur web, qui répond en renvoyant les ressources demandées (pages web, images, vidéos, etc.). HTTP est un protocole sans état, ce qui signifie que chaque requête est traitée indépendamment des précédentes. Par défaut, HTTP utilise le port 80.

### HTTPS (Hypertext Transfer Protocol Secure)
HTTPS est l'extension sécurisée de HTTP. Il utilise le protocole *Transport Layer Security* (TLS) (ou son prédécesseur SSL) pour chiffrer la communication entre le client et le serveur. Cela garantit la **confidentialité**, l'**intégrité** et l'**authenticité** des données échangées. Pour établir une connexion HTTPS, le serveur web doit posséder un certificat SSL/TLS valide, émis par une autorité de certification de confiance. HTTPS utilise le port 443 par défaut.

## 🔒 Guide de Durcissement (Hardening)
> [!check] Checklist Sécurité
> - [ ] **Mettre à jour régulièrement** le serveur web et le système d'exploitation sous-jacent pour corriger les vulnérabilités connues.
> - [ ] **Désactiver les modules et fonctionnalités inutiles** du serveur web pour réduire la surface d'attaque.
> - [ ] **Implémenter le principe du moindre privilège** en exécutant le serveur web avec un utilisateur dédié et non-root, disposant des permissions minimales nécessaires.
> - [ ] **Configurer des en-têtes de sécurité HTTP** tels que `Strict-Transport-Security` (HSTS), `Content-Security-Policy` (CSP), `X-Frame-Options` et `X-Content-Type-Options`.
> - [ ] **Activer et configurer des logs verbeux** pour surveiller les activités du serveur et détecter les tentatives d'intrusion ou les erreurs.
> - [ ] **Utiliser HTTPS avec des certificats SSL/TLS** forts et à jour pour chiffrer toutes les communications.
> - [ ] **Restreindre l'accès aux répertoires sensibles** et aux fichiers de configuration.
> - [ ] **Mettre en place un pare-feu applicatif web (WAF)**** pour filtrer le trafic malveillant.
> - [ ] **Réaliser des audits de sécurité** et des tests d'intrusion réguliers.

## ⚠️ Surfaces d'Attaque Communes
*   **Mauvaise configuration du serveur** : Des configurations laxistes peuvent exposer des répertoires sensibles, activer des fonctionnalités dangereuses ou permettre des listages de répertoires.
*   **Vulnérabilités logicielles (CVEs)** : Les serveurs web eux-mêmes (Apache, Nginx, IIS) ou les composants qu'ils utilisent (modules, bibliothèques) peuvent contenir des failles de sécurité exploitables. Exemples de CVEs fréquentes incluent des vulnérabilités de buffer overflow, de déni de service (DoS) ou d'exécution de code à distance.
*   **Attaques par injection** : SQL Injection, Cross-Site Scripting (XSS), Command Injection, où l'attaquant injecte du code malveillant via les entrées utilisateur pour manipuler le serveur ou les données.
*   **Attaques par déni de service (DoS/DDoS)** : Submerger le serveur de requêtes pour le rendre indisponible aux utilisateurs légitimes.
*   **Traversal de répertoire (Directory Traversal)** : Tenter d'accéder à des fichiers et répertoires en dehors de la racine web définie.
*   **Fichiers et répertoires non sécurisés** : Mauvaises permissions ou exposition de fichiers sensibles (sauvegardes, logs, fichiers de configuration).
*   **Vulnérabilités SSL/TLS** : Utilisation de versions obsolètes ou de configurations faibles de SSL/TLS (ex: faible chiffrement, défauts dans les implémentations).
