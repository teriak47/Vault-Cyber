---
tags:
  - logiciel
  - application
  - logiciel/serveur-web
  - architecture/client-serveur
  - protocole/http
  - protocole/https
  - a-revoir
  - a-completer
aliases:
  - Serveur Web
  - Web Server
  - Webserver
archetype: logiciel
version:
cssclasses:
  - max
source:
---

# Logiciel : Serveur Web

## 🎯 Rôle et Fonction

> Un serveur web est un programme informatique ou un appareil dont la fonction principale est de stocker les fichiers de sites web et de les délivrer aux navigateurs web sur demande. Il utilise majoritairement le protocole HTTP et constitue une composante essentielle de l'architecture client-serveur.
>
> Ses fonctions clés incluent :
*   **Hébergement de Contenu** : Stocke tous les éléments d'un site web (pages HTML, feuilles de style CSS, images, fichiers JavaScript, etc.).
*   **Traitement des Requêtes** : Reçoit et traite les requêtes HTTP émises par les navigateurs web.
*   **Envoi des Réponses** : Après traitement, renvoie la ressource demandée au navigateur via une réponse HTTP.
*   **Intégration Client-Serveur** : Agit comme le "serveur" central qui répond aux sollicitations des "clients".

## ⚙️ Configuration
*   **Fichiers de configuration clés**: La localisation et le nom des fichiers varient selon le logiciel serveur web spécifique (ex: Apache, Nginx, IIS).
    *   Exemple pour Apache: `/etc/httpd/conf/httpd.conf` ou `/etc/apache2/apache2.conf`
    *   Exemple pour Nginx: `/etc/nginx/nginx.conf`
*   **Modules importants**: Ces modules étendent les fonctionnalités du serveur web, comme la gestion de l'authentification, le support du chiffrement (via TLS), ou la réécriture d'URL.
    *   Exemple Apache: `mod_ssl` (pour HTTPS), `mod_rewrite` (pour la réécriture d'URL).
*   **Dépendances**: Un serveur web dépend souvent de plusieurs autres systèmes et logiciels :
    *   Système d'exploitation hôte (ex: Linux, Windows)
    *   Bibliothèques cryptographiques (ex: OpenSSL)
    *   Langages de programmation côté serveur (ex: PHP, Python, Ruby)
    *   Bases de données pour le contenu dynamique (ex: MySQL, PostgreSQL)

## 🔒 Sécurisation (Durcissement / Hardening)
*   **Mises à jour régulières**: Appliquer les patchs de sécurité et les mises à jour logicielles pour corriger les vulnérabilités connues et se protéger contre les attaques Zero-Day.
*   **Principe du moindre privilège**: Exécuter le serveur web avec un compte utilisateur et des permissions minimales requises.
*   **Désactiver les fonctionnalités inutiles**: Supprimer ou désactiver les modules, les services ou les répertoires non nécessaires pour réduire la surface d'attaque.
*   **Configuration des en-têtes de sécurité HTTP**: Mettre en œuvre des en-têtes tels que HSTS, X-Frame-Options, X-XSS-Protection, Content-Security-Policy pour renforcer la sécurité du navigateur.
*   **Contrôle d'accès**: Restreindre l'accès aux fichiers de configuration et aux répertoires sensibles via des politiques de sécurité strictes.
*   **Chiffrement**: Utiliser HTTPS avec des certificats numériques valides pour sécuriser les transmissions de données et garantir la confidentialité.
*   **Protection contre les vulnérabilités courantes**: Mettre en œuvre des mesures de défense contre les injections SQL, XSS, RCE et autres attaques web.

## 🔍 Audit et Surveillance
*   **Logs importants**: Ces journaux sont essentiels pour le monitorage de sécurité et la réponse aux incidents.
    *   Logs d'accès (ex: `/var/log/apache2/access.log` pour Apache, `/var/log/nginx/access.log` pour Nginx) : enregistrent toutes les requêtes HTTP reçues.
    *   Logs d'erreur (ex: `/var/log/apache2/error.log`, `/var/log/nginx/error.log`) : enregistrent les erreurs du serveur.
    *   Logs système : pour détecter les activités anormales au niveau du système d'exploitation hôte.
*   **Commandes d'audit**:
```bash
# Vérifier la syntaxe de la configuration Apache
apachectl configtest

# Vérifier la syntaxe de la configuration Nginx
nginx -t

# Vérifier les ports ouverts sur le serveur (HTTP 80, HTTPS 443)
netstat -tulnp | grep ":80\|:443"

# Examiner les connexions actives au serveur web
ss -tunap | grep ":80\|:443"
```
*   **Surveillance de sécurité**: Intégrer les logs du serveur web à un SIEM ou utiliser des outils de surveillance réseau pour détecter les anomalies et les attaques en temps réel.

## 🔗 Notes Connexes
* Vulnérabilités connues (CVEs)
* Protocoles utilisés (ex: [[HypertextTransferProtocol|HTTP, HTTPS)]]
* Navigateurs Web
* Architecture Client-Serveur
* Application logicielle
* Serveur

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La note actuelle se concentre sur le concept général de "Serveur Web". Pour une application plus concrète, elle mériterait des notes dédiées à des implémentations spécifiques (ex: ApacheWebServer, NginxWebServer, MicrosoftIISWebServer) avec leurs configurations, modules et stratégies de sécurisation détaillées.
*   Les sections "Configuration" et "Audit et Surveillance" sont nécessairement génériques. Elles seraient grandement améliorées par des exemples spécifiques à un ou deux serveurs web populaires.