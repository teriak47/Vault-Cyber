---
tags:
  - architecture/separation-roles
  - communication/requete-reponse
  - serveur/disponibilite
  - modele/client-serveur
  - reseau/protocoles
  - securite/pare-feu
aliases:
  - Architecture Client-Serveur
  - Client-Server Architecture
source:
  - null
cssclasses:
  - max
---

# Architecture Client-Serveur

## 📥 Définition en une phrase
> Modèle d'architecture réseau fondamental où les clients initient des requêtes de services ou de ressources à des serveurs, qui les fournissent en réponse.

## 🧠 Concepts Clés / Fonctionnement
*   **Clients** : Des applications, postes de travail ou appareils qui demandent des services ou des ressources. Ils sont généralement moins puissants et interagissent directement avec l'utilisateur.
*   **Serveurs** : Des ordinateurs ou des programmes dédiés qui fournissent des services, stockent des données ou hébergent des applications en réponse aux requêtes des clients. Ils sont conçus pour être robustes et disponibles.
*   **Communication** : La communication entre clients et serveurs s'effectue généralement via des [[NetworkProtocol|protocoles réseau]] standardisés (ex: HTTP pour le web, FTP pour le transfert de fichiers, SMTP pour l'email).
*   **Requête/Réponse** : Le client envoie une requête au serveur, qui la traite et renvoie une réponse au client.
*   **Séparation des rôles** : Les rôles et les responsabilités sont clairement distincts, ce qui facilite la gestion, la maintenance et l'évolution des systèmes.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS)]] ou [[DistributedDenialOfService|DDoS]] visant les serveurs pour les rendre indisponibles.
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]] pour intercepter les communications entre client et serveur.
*   [[Vulnerability|Vulnérabilités logicielles]] dans les applications clientes ou serveurs pouvant être exploitées.
*   [[DataBreach|Fuites de données]] si les bases de données des serveurs sont compromises.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en place des [[Firewall|pare-feu]] pour contrôler le trafic réseau entrant et sortant des serveurs.
*   Utiliser le [[DataEncryption|chiffrement des données]] (ex: TLS/SSL) pour sécuriser les communications entre clients et serveurs.
*   Appliquer des [[AccessControl|contrôles d'accès]] stricts pour limiter l'accès aux ressources serveur.
*   Mettre en œuvre des systèmes de [[IntrusionDetectionSystem|détection d'intrusion (IDS)]] et de [[IntrusionPreventionSystem|prévention d'intrusion (IPS)]] sur les serveurs.
*   Maintenir à jour les systèmes d'exploitation et les applications logicielles sur les clients et les serveurs.

## 🔗 Notes Connexes
*   [[NetworkProtocol|Protocole Réseau]]
*   [[DistributedSystem|Système Distribué]]
*   [[PeerToPeer|Peer-to-Peer (P2P)]] (architecture alternative)
*   [[WebApplication|Application Web]]