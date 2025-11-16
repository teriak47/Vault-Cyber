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
> L'[[InternetControlMessageProtocol|ICMP]] est un [[Protocol|protocole]] de la [[NetworkLayer|couche réseau]] (couche 3 du [[OpenSystemsInterconnectionModel|modèle OSI]] et du [[InternetProtocolSuite|modèle TCP/IP]]) utilisé par les [[NetworkDevice|périphériques réseau]] (comme les [[Router|routeurs]]) pour envoyer des messages d'erreur et des informations opérationnelles, notamment à des fins de [[NetworkMonitoring|diagnostic]].

## ⚙️ Fonctionnement
L'[[InternetControlMessageProtocol|ICMP]] fait partie intégrante de la [[InternetProtocolSuite|suite de protocoles IP]]. Il ne transporte pas de [[Data|données]] utilisateur comme [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]], mais des messages de contrôle essentiels au bon fonctionnement du [[Network|réseau]].

1.  **Structure des messages**: Les messages [[InternetControlMessageProtocol|ICMP]] sont identifiés par un **Type** et un **Code**, spécifiant la nature du message (erreur, requête, réponse).
2.  **Requêtes et Réponses Echo**:
    *   **Type 8 (Echo Request)**: Envoyé pour déterminer si un [[Host|hôte]] de destination est atteignable. C'est la base de l'outil [[Ping]].
    *   **Type 0 (Echo Reply)**: Réponse à une requête Echo, confirmant la joignabilité de l'hôte.
3.  **Messages d'erreur**:
    *   **Type 3 (Destination Unreachable)**: Informe l'expéditeur qu'une [[DestinationInternetProtocolVersion4Address|destination]] (hôte, [[Network|réseau]] ou [[PortNumber|port]]) est inaccessible. Essentiel pour la [[PathMTUDiscovery|découverte du PMTU]].
    *   **Type 11 (Time Exceeded)**: Indique que le champ [[Time-to-Live|Time-to-Live (TTL)]] d'un [[Packet|paquet]] a atteint zéro, provoquant sa suppression. Ce [[Message|message]] est fondamental pour l'outil [[Traceroute]].
* **Ports par défaut**: L'[[InternetControlMessageProtocol|ICMP]] opère directement sur [[InternetProtocol|IP]] et n'utilise pas de [[PortNumber|numéros de port]] comme les protocoles de la [[TransportLayer|couche transport]].

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * [[Reconnaissance|Reconnaissance Réseau]]: L'utilisation des requêtes Echo [[InternetControlMessageProtocol|ICMP]] est la base du [[PingSweep|Balayage Ping]], permettant de découvrir les [[Host|hôtes]] actifs sur un [[Network|réseau]] et de cartographier la [[AttackSurface|surface d'attaque]].
  * [[DenialOfService|Attaques par Déni de Service (DoS)]]: L'[[InternetControlMessageProtocol|ICMP]] peut être détourné pour des [[DenialOfService|attaques par déni de service]], comme l'[[PingFlood|Inondation Ping]] (saturation de la [[Bandwidth|bande passante]]) ou l'[[SmurfAttack|Attaque Smurf]] (attaque par amplification).
  * [[DataExfiltration|Exfiltration de Données]] et [[CommandAndControl|Commande et Contrôle (C2)]]: Le [[ICMPTunneling|Tunneling ICMP]] est une [[InfiltrationMethods|méthode]] utilisée par les [[ThreatActor|acteurs de menace]] pour encapsuler d'autres [[Protocol|protocoles]] ou [[Data|données]] au sein de [[Packet|paquets ICMP]], permettant de contourner les [[Firewall|pare-feux]] et d'établir un canal de [[CommandAndControl|C2]] furtif.
* **Mesures de protection**:
  * [[Firewall|Filtrage Pare-feu]]: Configurer des règles strictes sur les [[Firewall|pare-feux]] pour filtrer les types [[InternetControlMessageProtocol|ICMP]]. Il est courant de bloquer les requêtes Echo (Type 8) entrantes depuis l'[[Internet|Internet]] pour limiter la [[Reconnaissance|reconnaissance]], tout en autorisant les réponses Echo (Type 0) sortantes.
  * **Attention au blocage total**: Bloquer tous les types [[InternetControlMessageProtocol|ICMP]] est déconseillé, car cela peut perturber des mécanismes [[Network|réseau]] essentiels, tels que la [[PathMTUDiscovery|découverte du PMTU]] (qui repose sur le Type 3, Code 4 "Fragmentation Needed").
  * [[SecurityMonitoring|Surveillance Réseau]]: Utiliser des [[IntrusionDetectionSystem|systèmes de détection d'intrusion (IDS)]] ou des solutions de [[NetworkDetectionAndResponse|NDR (Network Detection and Response)]] pour détecter les comportements anormaux liés à l'[[InternetControlMessageProtocol|ICMP]] (scans, tunnels, inondations de paquets) et déclencher des [[IncidentResponse|réponses aux incidents]].

## 🔗 Notes Connexes
* [[Ping]]
* [[Traceroute]]
* [[InternetProtocol]]
* [[InternetProtocolVersion6|ICMPv6]]
* [[OpenSystemsInterconnectionModel|Modèle OSI]]
* [[NetworkLayer|Couche Réseau]]
* [[DenialOfService|Déni de Service]]
* [[PingSweep|Balayage Ping]]
* [[SmurfAttack]]
* [[ICMPTunneling|Tunneling ICMP]]
* [[Firewall]]
* [[Wireshark]]