---
aliases:
  - "URL"
  - "Uniform Resource Locator"
  - "Localisateur Uniforme de Ressource"
  - "Adresse web"
  - "Web Address"
archetype: concept-reseau
couche_osi:
  - "Couche 7 - Application"
technologie:
  - "HTTP"
  - "HTTPS"
  - "DNS"
  - "Web"
cssclasses:
  - max
tags:
  - web
  - web/url
  - protocole
  - protocole/http
  - protocole/https
  - protocole/ftp
  - protocole/mailto
  - adresse-ip
  - port
  - web/domaine
  - web/chemin
  - web/requete
  - web/fragment
  - web/navigation
  - web/api
  - web/hyperlien
  - identification
  - attaque/phishing
  - securite/web
  - encoding/url-encoding
  - web/limitation-url
---

# Url (Uniform Resource Locator)

> [!abstract] Définition
> Une **URL** (Uniform Resource Locator) est une chaîne de caractères standardisée utilisée pour identifier de manière unique et localiser des ressources sur un réseau informatique, le plus souvent sur le World Wide Web. Elle fournit l'adresse d'une ressource et le mécanisme pour y accéder.

## ⚙️ Mécanisme & Fonctionnement
Une URL est structurée en plusieurs composants qui, une fois analysés, permettent à un client (comme un navigateur web) de localiser et de récupérer une ressource spécifique.

### Structure et Composants
*   **Protocole (Schéma)** : Indique la méthode d'accès à la ressource (ex: *http*, *https*, *ftp*, *mailto*). Ce composant détermine le protocole réseau à utiliser pour la communication.
*   **Hôte (Domaine ou Adresse IP)** : Nom du serveur ou adresse IP où la ressource est hébergée (ex: *www.example.com*, *192.168.1.1*).
*   **Port** : Numéro de port du serveur sur lequel le service est disponible. Il est souvent omis si le port par défaut du protocole est utilisé (ex: *80* pour HTTP, *443* pour HTTPS).
*   **Chemin** : Spécifie l'emplacement exact de la ressource sur le serveur (ex: */chemin/vers/page.html*).
*   **Requête (Paramètres)** : Une chaîne de caractères optionnelle débutant par un point d'interrogation ( *?* ) et contenant des paires clé-valeur séparées par des esperluettes ( *&* ). Elles sont utilisées pour envoyer des données supplémentaires au serveur (ex: *?id=123&categorie=produit*).
*   **Fragment** : Une ancre optionnelle précédée d'un dièse ( *#* ) qui pointe vers une sous-section spécifique au sein de la ressource identifiée. Il n'est pas envoyé au serveur mais est interprété par le client.

Exemple : `https://www.example.com:8080/produits/electronique?id=42&couleur=rouge#details`

*   **Entrée** : Chaîne de caractères représentant l'URL fournie par l'utilisateur ou une application.
*   **Action** : Le client (navigateur, application) analyse l'URL. Il détermine le protocole à utiliser, extrait le nom d'hôte pour effectuer une résolution DNS et obtenir l'adresse IP du serveur, identifie le port, le chemin de la ressource et tous les paramètres de requête. Le fragment est traité localement par le client.
*   **Sortie** : Établissement d'une connexion avec le serveur identifié via le protocole spécifié, envoi de la requête pour la ressource avec les paramètres éventuels, et affichage/traitement de la ressource reçue.

## 💡 Cas d'Usage Typique
Pourquoi l'utilise-t-on ?
1.  **Navigation Web** : Permet aux utilisateurs d'accéder à des pages web, des images, des vidéos et d'autres contenus en ligne en spécifiant leur emplacement unique.
2.  **API et Services Web** : Les API RESTful utilisent des URLs pour identifier des ressources et des actions, permettant aux applications de communiquer entre elles.
3.  **Liaison et Référencement** : Les URLs sont fondamentales pour créer des hyperliens (liens hypertextes) qui connectent différentes ressources sur le web, formant la structure du World Wide Web. Elles sont également cruciales pour l'indexation par les moteurs de recherche.
4.  **Identification de Services** : Au-delà du web, les URLs peuvent identifier des ressources sur d'autres protocoles (ex: `ftp://`, `sftp://`, `smb://`), des adresses e-mail (`mailto:`), ou des fichiers locaux (`file://`).

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Longueur** : Bien qu'il n'y ait pas de limite standard stricte définie par les RFC pour la longueur des URLs, la plupart des navigateurs et serveurs imposent des limites pratiques (souvent autour de 2048 caractères), ce qui peut causer des problèmes avec des URLs très longues, notamment celles contenant de nombreux paramètres de requête.
> *   **Sécurité (Phishing)** : Les URLs peuvent être falsifiées ou déguisées pour tromper les utilisateurs et les diriger vers des sites malveillants (attaques de *phishing*), rendant la vigilance nécessaire lors de la vérification de l'URL dans la barre d'adresse.
> *   **Lisibilité et Complexité** : Des URLs très longues ou avec des caractères spéciaux encodés peuvent être difficiles à lire et à mémoriser pour les utilisateurs, ou sujettes à des erreurs de copier-coller.
> *   **Encodage des Caractères** : Certains caractères spéciaux dans le chemin ou les paramètres de requête doivent être encodés (%xx) pour garantir la conformité et éviter des ambiguïtés, ce qui peut rendre l'URL moins intuitive.