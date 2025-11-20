---
tags:
  - protocole
aliases:
  - HTTP
  - Hypertext Transfer Protocol
  - Protocole de Transfert Hypertexte
  - HTTP Protocol
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocole de Transfert Hypertexte (HTTP)

## 🎯 Rôle et Couche OSI
> Le Protocole de Transfert Hypertexte (HTTP) est un protocole de la couche application essentiel pour les systèmes d'information distribués, collaboratifs et hypermédias. Il constitue la base de la communication de données sur le World Wide Web.

## ⚙️ Fonctionnement
1.  **Modèle Client-Serveur**: HTTP opère selon un modèle où un client (généralement un navigateur web) initie des requêtes vers un serveur web, qui lui retourne les ressources demandées.
2.  **Protocole sans état**: Chaque requête HTTP est traitée indépendamment des précédentes. Pour gérer des états (comme une session utilisateur), des mécanismes additionnels tels que les cookies HTTP sont employés.
3.  **Méthodes HTTP (Verbs)**: Des verbes spécifiques (GET, POST, PUT, DELETE, HEAD, OPTIONS, PATCH) définissent l'action à réaliser sur la ressource cible. Par exemple, `GET` récupère une ressource, et `POST` soumet des données.
4.  **En-têtes HTTP**: Les en-têtes HTTP véhiculent des méta-informations concernant la requête ou la réponse, comme le type de contenu, l'agent utilisateur ou les paramètres de cache.
*   **Ports par défaut**: TCP/80
*   **Versions**: HTTP a évolué à travers plusieurs versions majeures, notamment HTTP/1.0, HTTP/1.1 (très répandue), HTTP/2 (qui améliore les performances), et HTTP/3 (basé sur le protocole QUIC).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Attaques de l'homme du milieu lorsque la communication est en clair (sans chiffrement).
    *   Fuite de données par transmission non chiffrée d'informations sensibles (par exemple, identifiants, données personnelles).
    *   Détournement de session si les cookies de session ne sont pas correctement sécurisés.
    *   Attaques par injection (comme le XSS ou l'injection SQL) résultant d'entrées utilisateur non validées dans les requêtes HTTP.
*   **Versions sécurisées**:
    *   HTTPS (pour HTTP) qui utilise TLS pour le chiffrement des communications.

## 🔗 Notes Connexes
*   HTTPS
*   TCP
*   TLS
*   DNS
*   Uniform Resource Locator (URL)
*   Application Web
*   Outil d'analyse de protocole (Wireshark)
*   Pare-feu d'application web (WAF)
*   En-têtes de sécurité
*   Validation des entrées
*   Pratiques de développement sécurisé