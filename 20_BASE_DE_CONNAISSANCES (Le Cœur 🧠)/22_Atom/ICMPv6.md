---
tags:
  - protocole/signalement-erreurs
  - securite/protocole-controle
  - ipv6/decouverte-voisins
  - reseau/protocole
aliases:
  - Internet Control Message Protocol version 6
  - Protocol de Message de Contrôle Internet version 6
source:
  - 
cssclasses:
  - max
---

# Protocole de Message de Contrôle Internet version 6 (ICMPv6)

## 📥 Définition en une phrase
> ICMPv6 est un [[Protocols|protocole]] fondamental dans le stack [[InternetProtocolVersion6]], utilisé pour le signalement d'erreurs, les fonctions de diagnostic et des fonctionnalités essentielles telles que la découverte de voisins et de routeurs.

## 🧠 Concepts Clés / Fonctionnement
*   **Signalement d'erreurs :** Informe les hôtes des problèmes de livraison de paquets, incluant "Destination Unreachable" (destination inaccessible), "Packet Too Big" (paquet trop grand), "Time Exceeded" (temps dépassé) et "Parameter Problem" (problème de paramètre).
*   **Fonctions de diagnostic :** Permet de tester la connectivité entre les hôtes via les messages "Echo Request" et "Echo Reply" (similaire à la commande `ping` d'[[InternetControlMessageProtocol|IPv4]]).
*   **[[NeighborDiscoveryProtocol|Découverte de Voisins (NDP)]] :** Un ensemble de messages ICMPv6 essentiels à la résolution d'adresses, la détection d'adresses en double, et la découverte de routeurs. Il comprend :
    *   [[RouterSolicitation|Router Solicitation (RS)]] : Les hôtes l'envoient pour trouver les routeurs sur le segment.
    *   [[RouterAdvertisement|Router Advertisement (RA)]] : Les routeurs l'envoient en réponse aux RS ou périodiquement pour annoncer leur présence et les préfixes réseau.
    *   [[NeighborSolicitation|Neighbor Solicitation (NS)]] : Utilisé pour la résolution d'adresses MAC et la détection d'adresses en double.
    *   [[NeighborAdvertisement|Neighbor Advertisement (NA)]] : Réponse aux NS, annonçant l'adresse MAC d'un hôte.
    *   [[Redirect|Redirection]] : Les routeurs l'envoient pour indiquer une meilleure route vers une destination spécifique.
*   **[[MulticastListenerDiscovery|Multicast Listener Discovery (MLD)]] :** Gère l'adhésion et le départ des hôtes aux groupes de diffusion multilatérale (multicast).

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service (DoS)]] : Les attaques par inondation de requêtes ICMPv6 peuvent saturer les ressources d'un hôte ou d'un réseau.
*   [[Reconnaissance|Reconnaissance]] : Les requêtes Echo peuvent être utilisées pour identifier les hôtes actifs sur un réseau.
*   [[ManInTheMiddle|Attaques Man-in-the-Middle (MitM)]] : Via le spoofing de messages [[NeighborDiscoveryProtocol|NDP]] (par exemple, de fausses RA ou NA), un attaquant peut rediriger le trafic.
*   [[AddressSpoofing|Usurpation d'adresse]] : Des messages ICMPv6 malveillants peuvent tenter de faire passer une adresse IPv6 pour une autre.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Filtrage]] ICMPv6 : Mettre en œuvre des règles de pare-feu pour limiter les types de messages ICMPv6 autorisés, tout en étant conscient que bloquer totalement ICMPv6 peut perturber le fonctionnement d'[[InternetProtocolVersion6]].
*   [[SecureNeighborDiscovery|Secure Neighbor Discovery (SEND)]] : Protège le [[NeighborDiscoveryProtocol|NDP]] contre le spoofing et les attaques MitM en utilisant la cryptographie.
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]] : Appliquer des politiques d'accès strictes pour les appareils connectés.
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] : Surveiller le trafic ICMPv6 pour détecter des activités suspectes ou des schémas d'attaque.
*   [[RateLimiting|Limitation de débit]] : Implémenter des contrôles de débit pour les messages ICMPv6 afin de prévenir les attaques par inondation.

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6]]
*   [[InternetControlMessageProtocol]]
*   [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol (NDP)]]
*   [[RouterSolicitation|Router Solicitation]]
*   [[RouterAdvertisement|Router Advertisement]]
*   [[NeighborSolicitation|Neighbor Solicitation]]
*   [[NeighborAdvertisement|Neighbor Advertisement]]
*   [[MulticastListenerDiscovery|Multicast Listener Discovery]]