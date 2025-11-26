---
aliases:
  - Modèle Client-Serveur
  - Client Server Model
archetype: modele
cssclasses:
  - max
tags:
  - modele/client-serveur
  - client
  - serveur
  - reseau
  - architecture/reseau
  - protocole
  - protocole/http
  - protocole/dns
  - protocole/ftp
  - gestion/donnees
  - securite
  - systeme/scalabilite
  - gestion/ressources/partage
  - systeme/fiabilite/defaillance-unique
  - reseau/dependance
  - serveur/surcharge
  - infrastructure/cout
  - developpement/complexite
---

# Modèle : Client-Server Model

> [!abstract] Principe Fondamental
> Le *modèle client-serveur* est une architecture distribuée où les tâches et les charges de travail sont réparties entre les *fournisseurs* de services (serveurs) et les *demandeurs* de services (clients) via un réseau informatique.

## 📐 Structure du Modèle
Dans cette architecture, les **clients** initient les demandes, et les **serveurs** y répondent. Le serveur écoute activement les requêtes entrantes des clients, les traite, puis renvoie une réponse appropriée.

```mermaid
graph TD
    Client["Client"] -->|1. Envoie Requête (HTTP, DNS, FTP, etc.)| Server["Serveur"]
    Server -->|2. Traite la Requête| Server
    Server -->|3. Renvoie Réponse (Données, Statut, Ressource)| Client
```

## 🧠 Concepts Clés
*   **Client** : Un programme informatique ou un appareil qui initie une connexion à un serveur pour demander des services ou des ressources. Les clients peuvent être des navigateurs web, des applications mobiles, des applications de messagerie, ou d'autres systèmes nécessitant un accès à des informations ou des fonctionnalités hébergées ailleurs.
*   **Serveur** : Un programme ou un appareil qui écoute les requêtes des clients, les traite et leur fournit des services ou des ressources. Les serveurs sont conçus pour gérer un grand nombre de requêtes simultanées et peuvent être spécialisés (serveur web, serveur de base de données, serveur de fichiers, etc.).
*   **Requête (Request)** : Un message envoyé par un client à un serveur pour demander une action spécifique ou une ressource. Une requête typique inclut l'identité du client, le type d'action souhaitée et les données nécessaires à l'exécution de l'action.
*   **Réponse (Response)** : Un message renvoyé par un serveur au client en réponse à une requête. Elle contient généralement les données ou la ressource demandée, ainsi qu'un code de statut indiquant le succès ou l'échec de la requête.
*   **Réseau** : Le support de communication qui permet aux clients et aux serveurs d'échanger des données. Il peut s'agir d'un réseau local (LAN) ou d'un réseau étendu (WAN) comme Internet.

## ✅ Avantages vs Inconvénients
| Avantages | Inconvénients |
|---|---|
| **Centralisation des données** : Facilite la gestion, la sauvegarde et la sécurité des données sur un seul emplacement. | **Point de défaillance unique** : La panne du serveur peut rendre l'ensemble du système inaccessible aux clients. |
| **Sécurité améliorée** : Les données et les ressources sont gérées par un serveur sécurisé, permettant un contrôle d'accès fin. | **Dépendance du réseau** : Une connexion réseau fiable est indispensable pour que les clients puissent accéder aux services. |
| **Évolutivité (Scalability)** : Il est plus facile d'ajouter de nouveaux clients ou de mettre à niveau le serveur pour gérer une charge accrue. | **Surcharge du serveur** : Un grand nombre de requêtes simultanées peut submerger le serveur et ralentir les performances. |
| **Maintenance facilitée** : Les mises à jour logicielles et la maintenance peuvent être effectuées côté serveur sans affecter chaque client individuellement. | **Coût initial élevé** : L'infrastructure serveur peut être coûteuse à mettre en place et à maintenir. |
| **Partage de ressources** : Plusieurs clients peuvent partager les mêmes ressources et services fournis par le serveur. | **Complexité de développement** : La conception d'applications client-serveur peut être plus complexe que celle de systèmes autonomes. |