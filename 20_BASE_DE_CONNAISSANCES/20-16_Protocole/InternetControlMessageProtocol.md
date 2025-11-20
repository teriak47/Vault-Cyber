---
tags:
  - protocole
aliases:
  - Protocole de message de contrôle Internet
  - ICMP
  - Internet Control Message Protocol
archetype: protocole
rfc:
  - RFC 792 (IPv4)
  - RFC 4443 (IPv6)
cssclasses:
  - max
---

# Protocole de Message de Contrôle Internet (ICMP)

## 🎯 Rôle et Couche OSI
> L'ICMP est un protocole de la couche réseau (couche 3 du modèle OSI et du modèle TCP/IP) utilisé par les périphériques réseau (comme les routeurs) pour envoyer des messages d'erreur et des informations opérationnelles, notamment à des fins de diagnostic.

## ⚙️ Fonctionnement
L'ICMP fait partie intégrante de la suite de protocoles IP. Il ne transporte pas de données utilisateur comme TCP ou UDP, mais des messages de contrôle essentiels au bon fonctionnement du réseau.

1.  **Structure des messages**: Les messages ICMP sont identifiés par un **Type** et un **Code**, spécifiant la nature du message (erreur, requête, réponse).
2.  **Requêtes et Réponses Echo**:
    *   **Type 8 (Echo Request)**: Envoyé pour déterminer si un hôte de destination est atteignable. C'est la base de l'outil Ping.
    *   **Type 0 (Echo Reply)**: Réponse à une requête Echo, confirmant la joignabilité de l'hôte.
3.  **Messages d'erreur**:
    *   **Type 3 (Destination Unreachable)**: Informe l'expéditeur qu'une destination (hôte, réseau ou port) est inaccessible. Essentiel pour la découverte du PMTU.
    *   **Type 11 (Time Exceeded)**: Indique que le champ Time-to-Live (TTL) d'un paquet a atteint zéro, provoquant sa suppression. Ce message est fondamental pour l'outil Traceroute.
* **Ports par défaut**: L'ICMP opère directement sur IP et n'utilise pas de numéros de port comme les protocoles de la couche transport.

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * Reconnaissance Réseau: L'utilisation des requêtes Echo ICMP est la base du Balayage Ping, permettant de découvrir les hôtes actifs sur un réseau et de cartographier la surface d'attaque.
  * Attaques par Déni de Service (DoS): L'ICMP peut être détourné pour des attaques par déni de service, comme l'Inondation Ping (saturation de la bande passante) ou l'Attaque Smurf (attaque par amplification).
  * Exfiltration de Données et Commande et Contrôle (C2): Le Tunneling ICMP est une méthode utilisée par les acteurs de menace pour encapsuler d'autres protocoles ou données au sein de paquets ICMP, permettant de contourner les pare-feux et d'établir un canal de C2 furtif.
* **Mesures de protection**:
  * Filtrage Pare-feu: Configurer des règles strictes sur les pare-feux pour filtrer les types ICMP. Il est courant de bloquer les requêtes Echo (Type 8) entrantes depuis l'Internet pour limiter la reconnaissance, tout en autorisant les réponses Echo (Type 0) sortantes.
  * **Attention au blocage total**: Bloquer tous les types ICMP est déconseillé, car cela peut perturber des mécanismes réseau essentiels, tels que la découverte du PMTU (qui repose sur le Type 3, Code 4 "Fragmentation Needed").
  * Surveillance Réseau: Utiliser des systèmes de détection d'intrusion (IDS) ou des solutions de NDR (Network Detection and Response) pour détecter les comportements anormaux liés à l'ICMP (scans, tunnels, inondations de paquets) et déclencher des réponses aux incidents.

## 🔗 Notes Connexes
* Ping
* Traceroute
* InternetProtocol
* ICMPv6
* Modèle OSI
* Couche Réseau
* Déni de Service
* Balayage Ping
* SmurfAttack
* Tunneling ICMP
* Firewall
* Wireshark