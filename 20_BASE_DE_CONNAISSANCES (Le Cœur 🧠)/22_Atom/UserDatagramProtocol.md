---
tags:
  - protocole/udp
  - reseau/faible-surcharge
  - cyberattaque/amplification
  - reseau/couche-transport
  - protocole/transport
  - cyberattaque/deni-service
aliases:
  - Protocole de Datagrammes Utilisateur
  - UDP
  - User Datagram Protocol
source:
  - null
cssclasses:
  - max
---

# Protocole de Datagrammes Utilisateur (UDP)

## 📥 Définition en une phrase
> L'[[UserDatagramProtocol|UDP]] est un [[Protocols|protocole]] de la [[TransportLayer|couche transport]] du modèle TCP/IP, offrant un service de communication de données sans connexion et non fiable, caractérisé par sa rapidité et sa faible surcharge.

## 🧠 Concepts Clés / Fonctionnement
*   **Sans Connexion (Connectionless)** : Contrairement à [[TransmissionControlProtocol|TCP]], l'[[UserDatagramProtocol|UDP]] n'établit pas de connexion préalable ("handshake") entre l'émetteur et le récepteur avant d'envoyer les données. Chaque paquet ([[Datagram|datagramme]]) est traité indépendamment.
*   **Non Fiable (Unreliable)** : L'[[UserDatagramProtocol|UDP]] n'inclut pas de mécanismes de garantie de livraison, de réordonnancement des paquets, ni de détection des doublons. Il n'y a pas d'accusés de réception.
*   **Faible Surcharge (Low Overhead)** : L'en-tête [[UserDatagramProtocol|UDP]] est très petit (8 octets), ce qui le rend idéal pour les applications où la vitesse est critique et une certaine perte de données est acceptable.
*   **Communication par Datagrammes** : Les données sont envoyées sous forme de datagrammes, qui sont des unités de données indépendantes.
*   **Utilisation des Ports** : L'[[UserDatagramProtocol|UDP]] utilise des numéros de [[Port|port]] pour multiplexer et démultiplexer les flux de données vers les applications spécifiques sur les hôtes.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS)]] : L'[[UserDatagramProtocol|UDP]] est fréquemment utilisé dans les attaques par [[DenialOfService|déni de service]] (notamment les attaques par [[AmplificationAttack|amplification]]) en raison de son absence de connexion et de sa facilité d'usurpation d'adresse [[InternetProtocolAddress|IP]] source.
*   [[Spoofing|Usurpation d'adresse IP]] : Il est facile d'usurper l'adresse [[InternetProtocolAddress|IP]] source d'un paquet [[UserDatagramProtocol|UDP]] car aucune validation de session n'est requise.
*   **Perte de données** : Inhérente à la nature non fiable de l'[[UserDatagramProtocol|UDP]], la perte de paquets peut entraîner des problèmes pour les applications qui ne gèrent pas cette fiabilité au niveau applicatif.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Filtrage par pare-feu]] : Restreindre l'accès aux [[Port|ports UDP]] non essentiels via des [[Firewall|pare-feux]] pour réduire la surface d'attaque.
*   [[RateLimiting|Limitation de débit]] : Implémenter des mécanismes de [[RateLimiting|limitation de débit]] sur les interfaces réseau pour atténuer les attaques par flooding [[UserDatagramProtocol|UDP]].
*   [[IntrusionDetectionSystem|Surveillance IDS/IPS]] : Utiliser des [[IntrusionDetectionSystem|systèmes de détection/prévention d'intrusion]] pour identifier et bloquer les trafics [[UserDatagramProtocol|UDP]] malveillants ou anormaux.
*   **Validation au niveau applicatif** : Pour les applications qui nécessitent une certaine fiabilité, implémenter des mécanismes de contrôle d'erreurs et de réémission au niveau applicatif.

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|TCP]]
*   [[TransportLayer|Couche Transport]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[Port|Port]]
*   [[DenialOfService|Déni de Service]]