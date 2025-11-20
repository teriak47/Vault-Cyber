---
aliases:
  - HTTPS
  - Hypertext Transfer Protocol Secure
  - Protocole de Transfert Hypertexte Sécurisé
archetype: protocole
rfc: RFC 2818
cssclasses:
  - max
---

# Hypertext Transfer Protocol Secure (HTTPS)

## 🎯 Rôle et Couche OSI
> L'HTTPS est une extension sécurisée du HTTP. Son rôle principal est de fournir une sécurité accrue aux communications sur l'Internet, notamment en garantissant la confidentialité, l'intégrité et l'authentification des données échangées entre un client (généralement un navigateur Web) et un serveur Web.
>
> Il opère au niveau de la couche Application du modèle TCP/IP et utilise les services de la couche de Transport (principalement TCP), mais encapsule les communications HTTP dans une couche TLS (ou historiquement SSL) qui, elle, opère entre les couches Application et Transport.

## ⚙️ Fonctionnement
L'HTTPS fonctionne en combinant le HTTP avec les protocoles de sécurité de la couche de transport (TLS ou SSL) pour chiffrer la communication.

1.  **Initialisation de la Connexion**: Le client initie une connexion TCP au serveur sur le port par défaut de l'HTTPS.
2.  **TLS Handshake**: Une fois la connexion TCP établie, le client et le serveur exécutent un "handshake TLS". Ce processus implique:
    *   La négociation des suites de chiffrement et des versions de TLS.
    *   L'échange de certificats numériques pour l'authentification du serveur (et potentiellement du client).
    *   La création et l'échange de clés de session pour le chiffrement symétrique.
3.  **Vérification du Certificat**: Le client vérifie la validité du certificat numérique du serveur pour s'assurer qu'il communique avec le bon serveur et que le certificat a été émis par une autorité de certification de confiance.
4.  **Communication Sécurisée**: Une fois le handshake TLS terminé, toutes les données HTTP sont chiffrées et authentifiées en utilisant les clés et les algorithmes négociés. Les données sont ensuite transmises via cette connexion sécurisée.
*   **Ports par défaut**: TCP/443

## 🛡️ Sécurité du Protocole
L'HTTPS est intrinsèquement conçu pour la sécurité, mais il peut être vulnérable si sa mise en œuvre est défaillante.

*   **Vulnérabilités connues**:
    *   **Mauvaise configuration du serveur**: Utilisation de versions obsolètes ou faibles de TLS (ex: SSL 3.0, TLS 1.0, 1.1), suites de chiffrement faibles, ou certificats numériques mal configurés ou expirés.
    *   **Attaques sur la chaîne de confiance des certificats**: Si une autorité de certification est compromise ou émet de manière frauduleuse un certificat pour un domaine qu'elle ne devrait pas, cela peut permettre des attaques de l'homme du milieu.
    *   **Fuites d'informations via les cookies HTTP**: Si des cookies sensibles ne sont pas marqués comme sécurisés, ils peuvent être envoyés en clair sur des connexions non-HTTPS.
    *   **Vulnérabilités du serveur**: Les failles dans le serveur lui-même ou l'application web (ex: injections SQL, XSS) peuvent toujours compromettre les données malgré l'HTTPS.
*   **Renforcement de la Sécurité**:
    *   **Utilisation des dernières versions de TLS**: Privilégier TLS 1.2 et 1.3.
    *   **Algorithmes de chiffrement robustes**: Choisir des suites de chiffrement fortes et à jour.
    *   **Épinglage de certificats**: Pour prévenir la confiance aveugle envers des certificats inattendus.
    *   **HSTS (HTTP Strict Transport Security)**: Force les navigateurs à n'utiliser que des connexions HTTPS pour un domaine donné.

## 🔗 Notes Connexes
*   HTTP
*   TLS
*   SSL
*   Certificat Numérique
*   Chiffrement
*   Cryptographie
*   Navigateurs Web
*   Serveur Web
*   Numéro de Port
*   Couche Application
*   TCP
*   Attaque de l'homme du milieu
*   Modèle OSI
*   Modèle TCP/IP
*   Internet
*   Sécurité
*   Confidentialité
*   Intégrité
*   Authentification
*   Client
*   Serveur
*   Texte clair
*   Cookies HTTP
*   Injection SQL
*   Cross-Site Scripting
*   Autorité de Certification
*   Handshake TLS (nouvelle note suggérée)
*   Cryptographie Forte (nouvelle note suggérée)
*   HSTS (nouvelle note suggérée)
*   Épinglage de Certificats (nouvelle note suggérée)
*   Application Logicielle