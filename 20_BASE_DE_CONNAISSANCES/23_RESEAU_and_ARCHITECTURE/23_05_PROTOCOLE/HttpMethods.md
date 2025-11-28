---
aliases:
  - Méthodes HTTP
  - HTTP Methods
  - Verbes HTTP
  - HTTP Verbs
archetype: protocole
port_defaut: 80, 443
couche_osi:
  - "Couche 7 - Application"
rfc:
  - RFC 9110
tags:
  - protocole/http
  - protocole/http/methodes
  - modele-osi/couche-7
  - port/80
  - port/443
  - protocole/tcp
  - securite/web
  - vulnerabilite
  - bonnes-pratiques
  - outil/wireshark
  - web/uri
  - protocole/ssl-tls
  - reseau/proxy
  - vulnerabilite/csrf
  - vulnerabilite/cross-site-tracing
  - vulnerabilite/mauvaise-configuration
  - confidentialite/donnee
---

# HTTP Methods

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 7 - Application
> * **Port par défaut** : `TCP/80` (HTTP), `TCP/443` (HTTPS)
> * **Transport** : TCP

## ⚙️ Principes des Méthodes HTTP
Les **méthodes HTTP**, aussi appelées verbes HTTP, définissent l'action à effectuer sur la ressource identifiée par l'URI (Uniform Resource Identifier). Elles constituent un élément fondamental de la **sémantique des requêtes HTTP**.

Chaque méthode possède des caractéristiques importantes :

*   **Idempotence** : Une opération est *idempotente* si elle peut être exécutée plusieurs fois sans changer le résultat initial au-delà de la première exécution réussie. Par exemple, supprimer une ressource plusieurs fois a le même résultat que de la supprimer une seule fois (la ressource n'existe plus).
*   **Sûreté (Safety)** : Une opération est considérée comme *sûre* si elle ne modifie pas l'état du serveur. Les méthodes sûres sont généralement utilisées pour la lecture de données.

## 📖 Liste et Description des Méthodes

Les méthodes HTTP courantes sont décrites ci-dessous.

| Méthode | Description | Idempotente | Sûre | Corps de Requête | Corps de Réponse |
|---|---|---|---|---|---|
| **GET** | Récupère une représentation de la ressource spécifiée. | Oui | Oui | Non | Oui |
| **HEAD** | Identique à GET, mais ne retourne que les en-têtes de la réponse, sans le corps. | Oui | Oui | Non | Non |
| **POST** | Soumet des données à la ressource spécifiée, souvent pour créer une nouvelle ressource. | Non | Non | Oui | Oui |
| **PUT** | Remplace toutes les représentations actuelles de la ressource cible avec le contenu du corps de la requête. | Oui | Non | Oui | Oui |
| **DELETE** | Supprime la ressource spécifiée. | Oui | Non | Non | Oui |
| **CONNECT** | Établit un tunnel vers le serveur identifié par la ressource cible. Utilisé pour les proxys SSL/TLS. | Non | Non | Non | Oui |
| **OPTIONS** | Décrit les options de communication disponibles pour la ressource cible. | Oui | Oui | Non | Oui |
| **TRACE** | Effectue une boucle de message de test le long du chemin vers la ressource cible. | Oui | Oui | Non | Oui |
| **PATCH** | Applique des modifications *partielles* à une ressource. | Non | Non | Oui | Oui |

### Exemples d'Utilisation

*   **GET** : `GET /products/123` pour récupérer les détails du produit 123.
*   **POST** : `POST /users` avec un corps JSON pour créer un nouvel utilisateur.
*   **PUT** : `PUT /products/123` avec un corps JSON pour mettre à jour *complètement* le produit 123.
*   **DELETE** : `DELETE /users/456` pour supprimer l'utilisateur 456.
*   **PATCH** : `PATCH /users/456` avec un corps JSON `{"email": "new@example.com"}` pour modifier uniquement l'adresse e-mail de l'utilisateur.

## 🦈 Analyse Wireshark
Les méthodes HTTP apparaissent au début de la ligne de requête dans la section "Hypertext Transfer Protocol" d'une trame Wireshark.

> [!tip] Filtres Utiles
> ```
> # Filtrer par méthode GET
> http.request.method == "GET"
>
> # Filtrer par méthode POST
> http.request.method == "POST"
>
> # Filtrer toutes les requêtes (non-réponses)
> http.request
> ```

## 🛡️ Sécurité et Bonnes Pratiques
> [!danger] Vulnérabilités et Mauvaises Pratiques
> *   **Mauvaise utilisation des méthodes sûres/idempotentes** : Utiliser `GET` pour déclencher des actions qui modifient l'état du serveur (ex: `GET /deleteUser?id=123`). Cela peut entraîner des vulnérabilités CSRF ou des actions non intentionnelles par des robots d'exploration.
> *   **Exposition d'informations sensibles** : Les informations passées dans l'URL avec `GET` sont souvent logguées et peuvent être visibles dans l'historique du navigateur ou les logs du serveur/proxy. Préférer `POST` pour les données sensibles.
> *   **Verbes non autorisés** : Certains serveurs ou applications peuvent ne pas restreindre correctement les méthodes HTTP autorisées pour certaines ressources, permettant à un attaquant d'utiliser `PUT` ou `DELETE` sur des ressources non protégées.
> *   **Méthodes TRACE/OPTIONS/CONNECT** :
    *   `TRACE` peut être utilisé dans des attaques de *Cross-Site Tracing (XST)* si les en-têtes HTTP de l'attaquant sont renvoyés dans la réponse `TRACE`.
    *   `OPTIONS` peut révéler des informations sur les méthodes HTTP supportées par un serveur/ressource, ce qui pourrait être utilisé pour cartographier la surface d'attaque.
    *   `CONNECT` est principalement utilisé pour les proxys HTTPS. Une mauvaise configuration peut potentiellement permettre l'établissement de tunnels non sécurisés.
>
> Il est crucial de s'assurer que l'application web respecte la sémantique des méthodes HTTP et que les contrôles d'accès sont correctement implémentés pour chaque verbe et chaque ressource.