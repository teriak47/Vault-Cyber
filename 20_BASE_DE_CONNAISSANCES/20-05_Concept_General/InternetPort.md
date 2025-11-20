---
tags:
  - reseau
  - protocole
  - securite
aliases:
  - Port Internet
  - Internet Port
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Port Internet

## 📥 Définition en une phrase
> Un port Internet est un point de communication logiciel, identifié par un numéro, qui permet à des applications ou services spécifiques sur un système informatique d'envoyer et de recevoir des données via un réseau.

## 🧠 Concepts Clés / Piliers
*   **Numérotation et Catégories**: Les ports sont numérotés de 0 à 65535 et sont classifiés en trois catégories principales, gérées en partie par l'IANA:
    *   **Ports Bien Connus (0-1023)**: Réservés aux services système courants et normalisés (ex: HTTP sur 80, SSH sur 22, FTP sur 21).
    *   **Ports Enregistrés (1024-49151)**: Utilisés par des applications ou services spécifiques qui se sont enregistrés auprès de l'IANA.
    *   **Ports Dynamiques/Privés (49152-65535)**: Attribués dynamiquement par le système d'exploitation aux clients pour initier des connexions sortantes vers des serveurs.
*   **Association IP et Port (Socket)**: Un port est toujours associé à une adresse IP pour former une "socket". Cette combinaison adresse IP:port identifie de manière unique une application spécifique sur un hôte au sein d'un réseau, permettant un point de communication précis.
*   **Rôle des Protocoles de Transport**: Les ports sont un élément fondamental de la couche de transport du modèle TCP/IP. Ils sont utilisés par des protocoles réseau comme le TCP et l'UDP pour multiplexer (envoyer plusieurs flux de données sur une seule connexion) et démultiplexer (diriger les données reçues vers la bonne application) les données entre différentes applications.
*   **États des Ports**: Un port peut être dans différents états, chacun avec des implications pour la sécurité:
    *   **Ouvert**: Le système accepte les connexions entrantes car un service ou une application écoute activement.
    *   **Fermé**: Le système refuse activement les connexions sur ce port, aucun service n'écoute.
    *   **Filtré**: Le système ne répond pas aux requêtes sur ce port, souvent en raison d'un pare-feu qui bloque le trafic.

## 💡 Importance en Cybersécurité
Les ports Internet sont des cibles primordiales dans le domaine de la cybersécurité car ils représentent des points d'entrée et de sortie essentiels pour le trafic réseau. Leur gestion et leur sécurité sont fondamentales pour prévenir les attaques numériques. Une configuration laxiste ou une surveillance insuffisante des ports peut créer des surfaces d'attaque significatives, permettant aux acteurs de menaces de réaliser des analyses de ports pour découvrir des vulnérabilités potentielles, d'exploiter des services non sécurisés, ou de lancer des attaques par déni de service. La mise en œuvre du principe du moindre privilège en n'ouvrant que les ports strictement nécessaires et une gestion des vulnérabilités rigoureuse sont des pierres angulaires d'une défense en profondeur.

## 🔗 Notes Connexes
*   Adresse IP
*   Protocole de Contrôle de Transmission
*   Protocole de Datagrammes Utilisateur
*   Service Réseau
*   Pare-feu
*   Analyse de ports
*   Sécurité Réseau
*   Couche de Transport
*   Zone Démilitarisée
*   Socket