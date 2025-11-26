---
aliases:
  - Pair à Pair
  - Peer to Peer
  - P2P
archetype: concept-reseau
couche_osi:
  - "Couche 7 - Application"
technologie:
  - BitTorrent
  - Blockchain
  - VoIP
  - DHT
tags:
  - reseau/p2p
  - architecture/reseau/decentralisee
  - nat/traversal
  - mecanisme/encapsulation
  - partage/fichiers
  - cryptomonnaie
  - blockchain
  - application/voip
  - application/jeux-en-ligne
  - securite
  - malware/propagation
  - protocole/tcp
  - protocole/ip
  - reseau/dht
  - calcul/distribue
---

# Peer-to-Peer (P2P)

> [!abstract] Définition
> Un réseau *Peer-to-Peer* (P2P), ou *pair à pair*, est une architecture réseau décentralisée où chaque nœud (ou pair) agit simultanément comme un client et un serveur. Les pairs se connectent et partagent des ressources (fichiers, puissance de calcul, bande passante) directement entre eux, sans l'intervention d'un serveur centralisé. Ce modèle favorise la collaboration directe et la distribution des tâches.

## ⚙️ Mécanisme & Fonctionnement
Dans un réseau P2P, les participants (peers) établissent des connexions directes les uns avec les autres. Chaque pair peut initier des requêtes de service (agir en tant que client) et répondre à des requêtes provenant d'autres pairs (agir en tant que serveur). La communication s'appuie sur les protocoles de la suite TCP/IP pour le transport des données.

Certains réseaux P2P sont *structurés*, utilisant des techniques comme les *Distributed Hash Tables* (DHT) pour organiser les pairs dans une topologie spécifique, facilitant la recherche efficace de ressources. D'autres sont *non structurés*, avec des connexions plus ad-hoc.

Un défi majeur pour les communications P2P est la traversée des *Network Address Translators* (NAT) et des pare-feu, car les pairs peuvent ne pas avoir d'adresses IP publiques directement joignables. Des techniques comme le *Hole Punching* (via STUN ou TURN) sont utilisées pour établir des connexions directes malgré les NATs, en exploitant la façon dont les NATs gèrent les sessions sortantes.

### Encapsulation / Traitement
*   **Entrée** : Une application P2P sur un pair souhaite envoyer ou recevoir des données.
*   **Action** :
    *   L'application P2P initie une connexion ou écoute les connexions entrantes.
    *   Les données de l'application sont formatées et passées aux couches de transport (TCP ou UDP), réseau (IP), liaison et physique du modèle OSI pour l'encapsulation standard et la transmission à travers le réseau.
    *   Pour les connexions directes entre pairs derrière des NAT, des mécanismes de *NAT traversal* peuvent être nécessaires pour "percer" les NATs et permettre le flux de données.
    *   Le pair récepteur décapsule les données à travers les couches inférieures jusqu'à l'application P2P.
*   **Sortie** : Les données sont échangées directement entre les applications P2P des deux pairs, apparaissant comme un flux d'informations direct au niveau de l'application, bien qu'elles transitent par l'infrastructure réseau sous-jacente.

```mermaid
sequenceDiagram
    participant PeerA as Pair A (Client/Serveur)
    participant RendezvousS as Serveur de Rendez-vous (Optionnel)
    participant PeerB as Pair B (Client/Serveur)

    Note over PeerA,PeerB: Identification des pairs
    PeerA->>RendezvousS: Enregistrer son IP publique et port
    PeerB->>RendezvousS: Enregistrer son IP publique et port
    RendezvousS-->>PeerA: Fournir IP publique et port de Peer B
    RendezvousS-->>PeerB: Fournir IP publique et port de Peer A

    Note over PeerA,PeerB: Établissement de la connexion directe (via NAT Traversal si nécessaire)
    PeerA->>PeerB: Tentative de connexion directe
    PeerB->>PeerA: Acceptation de la connexion directe

    Note over PeerA,PeerB: Communication P2P
    PeerA-->>PeerB: Envoi de données
    PeerB-->>PeerA: Réception et envoi de données```

## 💡 Cas d'Usage Typique
Les réseaux P2P sont utilisés pour diverses applications nécessitant une distribution de ressources ou une collaboration décentralisée :
1.  **Partage de fichiers** : Historiquement popularisé par des plateformes comme Napster, Gnutella et BitTorrent, il permet aux utilisateurs de partager et télécharger des fichiers directement les uns des autres, rendant la distribution de contenu plus rapide et plus efficace.
2.  **Cryptomonnaies et Blockchain** : La technologie blockchain, comme celle de Bitcoin, repose sur un réseau P2P où les transactions sont vérifiées et enregistrées par les nœuds du réseau, garantissant la décentralisation, la sécurité et la transparence.
3.  **Voix sur IP (VoIP) et Communication** : Des applications comme Skype (historiquement) et certaines applications de messagerie utilisent des architectures P2P pour les appels vocaux et vidéo, ou la messagerie directe, réduisant la latence et améliorant la confidentialité.
4.  **Jeux en ligne** : Certains jeux utilisent des connexions P2P pour permettre aux joueurs de se connecter directement, réduisant ainsi la latence par rapport aux serveurs centralisés.
5.  **Calcul distribué** : Les réseaux P2P peuvent être utilisés pour distribuer des tâches de calcul complexes sur plusieurs nœuds, exploitant la puissance de traitement inutilisée.

## ⚠️ Limitations & Problèmes
> [!warning] Points d'attention
> *   **Sécurité** : La nature décentralisée des réseaux P2P introduit des défis de sécurité uniques.
    *   **Propagation de logiciels malveillants** : Les fichiers partagés sur les réseaux P2P peuvent facilement contenir et propager des malwares et des virus, infectant rapidement de nombreux appareils.
    *   **Attaques de type *Man-in-the-Middle* (MiTM)** : L'absence de contrôle centralisé rend les communications P2P vulnérables à l'interception et à la manipulation des données par des attaquants.
    *   **Attaques Sybil** : Un attaquant peut créer de multiples identités ou nœuds faux pour gagner une influence disproportionnée sur le réseau.
    *   **Intégrité et authentification des données** : Il peut être difficile de vérifier l'authenticité et l'intégrité des données sans autorité centrale.
    *   **Exposition des adresses IP** : Les pairs révèlent souvent leurs adresses IP pour communiquer directement, ce qui peut les exposer à des attaques ciblées ou à des problèmes de confidentialité.
    *   **Utilisation dans les botnets** : Les architectures P2P sont utilisées par des botnets pour leur résilience et pour coordonner les appareils infectés sans serveur de commande central.
*   **Performance** : La performance peut être variable, dépendante de la disponibilité et de la bande passante des pairs participants. Les *free-riders* (pairs qui consomment des ressources sans en fournir suffisamment) peuvent affecter l'efficacité du réseau.
*   **Problèmes juridiques** : Le partage de contenu non autorisé, notamment pour les fichiers multimédias, a historiquement posé d'importants défis juridiques aux plateformes P2P.
*   **Complexité de NAT Traversal** : Bien que des techniques existent, l'implémentation robuste et sécurisée de la traversée des NAT reste complexe et peut échouer avec certains types de NAT.

## 🔗 Notes Connexes
*   **Protocole lié** : Protocole TCP/IP
*   **Protocole lié** : NAT
*   **Concept lié** : DistributedHashTable