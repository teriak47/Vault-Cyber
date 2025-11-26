---
aliases:
  - Encodage des Données
  - Data Encoding
archetype: definition
cssclasses:
  - max
tags:
  - encoding
  - codage/donnees
  - informatique
  - cybersecurite
  - definition
  - character-set
  - transmission-donnees
  - stockage/donnees
  - integrite
  - interoperabilite
  - protocole
  - encoding/ascii
  - encoding/utf-8
  - encoding/base64
  - encoding/url-encoding
  - encoding/html-entities
---

# Data Encoding

> [!question] C'est quoi ?
> L'**encodage des données** est le processus de conversion des données d'un format à un autre, généralement pour faciliter la transmission, le stockage, la compression ou la protection de leur intégrité, en les rendant interprétables par différents systèmes ou applications.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le concept d'encodage des données est intrinsèquement lié à l'émergence de l'informatique numérique. L'un des premiers et plus fondamentaux systèmes d'encodage, le code *Morse*, est apparu dès 1837 pour la transmission télégraphique. Dans le domaine informatique, l'**American Standard Code for Information Interchange (ASCII)**, normalisé pour la première fois en 1963, a été un jalon majeur en définissant une représentation numérique standard pour les caractères alphanumériques et de contrôle, permettant l'interopérabilité entre différents équipements.

## 💡 Principes de l'Encodage
L'encodage repose sur la définition d'un **jeu de caractères** ou d'un ensemble de symboles, et d'une **méthode de mappage** qui attribue une représentation numérique (souvent binaire) unique à chaque élément de cet ensemble. Les principes clés incluent :
*   **Représentation universelle** : Permettre à des systèmes hétérogènes de comprendre et de traiter la même information.
*   **Efficacité** : Optimiser l'espace de stockage ou la bande passante nécessaire à la transmission.
*   **Intégrité** : Assurer que les données restent intactes et non corrompues lors de leur transit ou de leur stockage.
*   **Lisibilité** : Dans certains cas, rendre les données compréhensibles pour l'œil humain ou plus facilement débuggables.

## ⚙️ Types d'Encodage Courants et Finalités

L'encodage des données prend diverses formes, chacune adaptée à des besoins spécifiques :

*   **ASCII (American Standard Code for Information Interchange)** :
    *   **Finalité** : Représentation de base des caractères textuels en anglais. Il utilise 7 bits pour encoder 128 caractères, incluant les lettres majuscules et minuscules, les chiffres, les symboles de ponctuation et certains caractères de contrôle.
    *   **Utilisation** : Fondement de nombreux formats de fichiers texte, protocoles de communication et systèmes d'exploitation.

*   **UTF-8 (Unicode Transformation Format - 8-bit)** :
    *   **Finalité** : Encodage de caractères *Unicode* à longueur variable, permettant de représenter pratiquement tous les caractères et symboles de toutes les langues du monde. Il est rétrocompatible avec ASCII, car les premiers 128 caractères UTF-8 sont identiques à ASCII.
    *   **Utilisation** : Encodage dominant sur le web (plus de 98% des sites web), dans les systèmes d'exploitation modernes, les bases de données et les applications internationales.

*   **Base64** :
    *   **Finalité** : Convertir des données binaires (comme des images, des fichiers audio, des certificats) en une représentation textuelle ASCII, rendant ainsi les données binaires "sûres" pour la transmission via des protocoles qui ne gèrent que le texte (ex: e-mail, URL). Il encode 3 octets de données binaires en 4 caractères ASCII.
    *   **Utilisation** : Pièces jointes d'e-mails (MIME), intégration d'images dans des fichiers HTML ou CSS (data URIs), transmission de jetons d'authentification (JWT), et pour l'obfuscation légère de données.

*   **URL Encoding (Percent-Encoding)** :
    *   **Finalité** : Rendre les caractères non alphanumériques ou ayant une signification spéciale (comme les espaces, `/`, `?`, `&`) dans une URL conformes aux spécifications URI. Ces caractères sont remplacés par un `%` suivi de leur valeur hexadécimale.
    *   **Utilisation** : Dans les paramètres d'URL pour les requêtes HTTP (GET), les formulaires web, et les chemins de fichiers pour s'assurer que l'URL est correctement interprétée par les navigateurs et les serveurs.

*   **HTML Entities (Entités HTML)** :
    *   **Finalité** : Représenter des caractères spéciaux (ex: `<`, `>`, `&`, `"`) ou des caractères non présents sur un clavier standard (ex: `©`, `é`) de manière à ce qu'ils soient affichés correctement dans un document HTML sans être interprétés comme du code HTML.
    *   **Utilisation** : Affichage de texte sur les pages web, notamment pour les caractères réservés (comme `&lt;` pour `<`) ou pour des symboles spéciaux (`&euro;` pour `€`).

## 🛡️ Rôle en Informatique et Cybersécurité

L'encodage joue un rôle fondamental tant dans le fonctionnement quotidien des systèmes informatiques que dans la posture de sécurité.

### En Informatique :
*   **Interopérabilité** : Il permet à des systèmes différents (ordinateurs, serveurs, applications) développés par des entités diverses de communiquer et d'échanger des données de manière cohérente et compréhensible.
*   **Stockage et Transmission** : L'encodage assure que les données sont stockées et transmises dans un format approprié au support ou au canal, qu'il s'agisse de fichiers sur un disque, de paquets réseau ou de requêtes API.
*   **Intégration de Données** : Il facilite la fusion et le traitement de données provenant de sources variées en standardisant leur représentation.

### En Cybersécurité :
*   **Intégrité et Conformité** : Certains encodages, comme Base64, sont utilisés pour assurer l'intégrité des données binaires lors de leur passage à travers des systèmes qui pourraient les altérer si elles n'étaient pas représentées textuellement. L'encodage correct est crucial pour la conformité des protocoles.
*   **Obfuscation Légère** : Bien que ce ne soit pas un mécanisme de sécurité robuste, des encodages comme Base64 peuvent rendre les données moins immédiatement lisibles par un œil humain, masquant un contenu potentiellement sensible (ex: identifiants encodés dans des URL) ou simplement des données binaires rendues textuelles. Ce n'est pas de la cryptographie, mais une forme de dissimulation.
*   **Prévention des Attaques (indirectement)** : Une mauvaise gestion de l'encodage est une source fréquente de vulnérabilités. Par exemple, une application web qui ne décode pas correctement les entrées utilisateur avant de les traiter peut être sujette à des attaques par *injection* (telles que le *Cross-Site Scripting (XSS)* ou l'*injection SQL*) si des caractères malveillants sont encodés et contournent les filtres. De même, l'*URL encoding* est essentiel pour prévenir l'interprétation erronée de caractères spéciaux dans les requêtes HTTP, qui pourrait ouvrir des brèches de sécurité.
*   **Standardisation des Données** : En cybersécurité, l'encodage permet de normaliser les journaux d'événements (logs) ou les données de menaces, rendant leur analyse plus facile et plus uniforme pour les systèmes de détection d'intrusion (IDS/IPS) ou les SIEM (Security Information and Event Management).