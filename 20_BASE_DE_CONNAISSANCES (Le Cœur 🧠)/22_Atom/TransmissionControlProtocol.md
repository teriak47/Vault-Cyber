---
tags:
  - reseau/controle-flux
  - etablissement-connexion
  - protocole
  - reseau/couche-transport
aliases:
  - Protocole de Contrôle de Transmission
  - TCP
  - Transmission Control Protocol
source:
  - 
cssclasses:
  - max
---

# Protocole de Contrôle de Transmission (TCP)

## 📥 Définition en une phrase
> Le Protocole de Contrôle de Transmission (TCP) est un [[Protocols|protocole]] fondamental, fiable et orienté connexion de la couche [[TransportLayer|Transport]] du modèle [[TcpIpModel|TCP/IP]], conçu pour garantir une livraison ordonnée et sans erreur des données entre applications sur un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Établissement de Connexion (Three-Way Handshake) :** Avant tout transfert de données, TCP utilise une [[ThreeWayHandshake|poignée de main en trois étapes]] (SYN, SYN-ACK, ACK) pour établir une connexion logique fiable entre deux hôtes.
*   **Fiabilité et Ordre :** Assure la livraison complète et dans le bon ordre des données en attribuant un [[Sequencing|numéro de séquence]] à chaque segment et en nécessitant un [[Acknowledgement|acquittement (ACK)]] pour la réception. Si un acquittement n'est pas reçu, le segment est retransmis.
*   **Contrôle de Flux (Flow Control) :** Empêche un émetteur d'envoyer des données plus rapidement que le récepteur ne peut les traiter en utilisant des [[FlowControl|fenêtres glissantes]], évitant ainsi la saturation du tampon du récepteur.
*   **Contrôle de Congestion (Congestion Control) :** Ajuste dynamiquement le taux de transmission des données pour éviter l'engorgement du réseau, en utilisant des algorithmes tels que [[CongestionControl|Slow Start et Congestion Avoidance]].
*   **Gestion des Segments :** Les données d'application sont divisées en segments TCP, qui sont ensuite encapsulés dans des paquets [[InternetProtocol|IP]] pour le routage.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service (DoS/DDoS)]] : Notamment les [[SYNFlood|attaques SYN Flood]], où l'attaquant envoie un grand nombre de requêtes SYN sans jamais compléter la poignée de main, épuisant les ressources du serveur.
*   [[PortScanning|Scans de Ports]] : Utilisation des paquets TCP pour déterminer quels services sont actifs et quels ports sont ouverts sur un hôte cible.
*   [[SessionHijacking|Détournement de Session]] : Un attaquant prend le contrôle d'une session TCP déjà établie entre deux hôtes légitimes.
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu (MITM)]] : L'attaquant intercepte et potentiellement modifie la communication TCP entre deux parties.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Firewall|Filtrage par Pare-feu]] :** Configurer les [[Firewall|pare-feu]] pour bloquer le trafic TCP non essentiel et les ports inutilisés, ainsi que pour limiter les requêtes SYN.
*   **[[IntrusionDetectionSystem|Systèmes de Détection et Prévention d'Intrusion (IDS/IPS)]] :** Déployer des [[IntrusionPreventionSystem|IPS]] pour détecter et atténuer les attaques basées sur TCP, telles que les SYN Floods.
*   **[[SecureConfiguration|Configuration Sécurisée des Services]] :** Assurer que tous les services utilisant TCP sont configurés avec les paramètres de sécurité appropriés, y compris l'utilisation de protocoles de chiffrement comme [[TransportLayerSecurity|TLS]] au-dessus de TCP.
*   **[[RateLimiting|Limitation de Débit]] :** Implémenter des mécanismes de limitation de débit sur les serveurs pour gérer et atténuer les pics de trafic anormaux.

## 🔗 Notes Connexes
*   [[UserDatagramProtocol|UDP]]
*   [[InternetProtocol|IP]]
*   [[TcpIpModel|Modèle TCP/IP]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[TransportLayerSecurity|TLS]]