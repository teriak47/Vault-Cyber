---
tags:
  - protocole/icmp
  - reseau/diagnostic
  - cybersecurite/tunneling-icmp
  - reseau
  - protocole/signalement-erreurs
  - cyberattaque/deni-service
aliases:
  - Protocole de message de contrôle Internet
  - ICMP
  - Internet Control Message Protocol
source: null
cssclasses:
  - max
---

# Protocole De Message De Contrôle Internet (ICMP)

## 📥 Définition En Une Phrase

> **ICMP** est un [[Protocols|protocole]] de support de la couche réseau (Couche 3 du [[OpenSystemsInterconnectionModel|Modèle OSI]]) utilisé par les périphériques réseau, comme les routeurs, pour envoyer des messages d'erreur et des informations opérationnelles (diagnostics).

## 🧠 Concepts Clés / Fonctionnement

- ICMP fait partie intégrante de la suite [[InternetProtocol|IP]]. Il n'est pas conçu pour transporter des données utilisateur (contrairement à [[TransmissionControlProtocol]] ou [[UDP]]), mais uniquement des messages de contrôle.
- Il fonctionne sur un système de **Types** et de **Codes** pour spécifier la nature du message.
- **Type 8 (Echo Request)** et **Type 0 (Echo Reply)** : C'est le mécanisme utilisé par l'outil [[Ping]] pour tester la joignabilité d'un hôte.
- **Type 3 (Destination Unreachable)** : Informe un hôte qu'une destination (hôte, réseau ou port) n'est pas accessible.
- **Type 11 (Time Exceeded)** : Indique que le champ [[TTL|Time-to-Live (TTL)]] d'un paquet a atteint zéro. Ce message est fondamental pour le fonctionnement de [[Traceroute]].

## 🛡️ Risques / Menaces Associés

- **Reconnaissance Réseau** : L'utilisation d'ICMP (notamment les "Echo Requests") est la base du [[PingSweep|Balayage Ping (Ping Sweep)]] pour découvrir les hôtes actifs sur un réseau.
- **Attaques par Déni de Service (DoS)** : ICMP peut être détourné pour des attaques [[DenialOfService]] telles que l'[[PingFlood|Inondation Ping (Ping Flood)]] (saturation de la bande passante) ou l'[[SmurfAttack|Attaque Smurf]] (attaque par amplification).
- **Exfiltration de Données / C2** : Le [[ICMPTunneling|Tunneling ICMP]] est une technique qui encapsule d'autres protocoles ou données dans des paquets ICMP (souvent Echo) pour contourner les règles de [[Firewall|Pare-feu]] et établir un canal de [[CommandAndControl|Commande et Contrôle (C2)]].
    

## 💎 Mesures De Protection / Bonnes Pratiques

- **Filtrage Pare-feu** : Configurer des règles de [[Firewall|Pare-feu]] strictes pour filtrer les types ICMP. Il est courant de bloquer les "Echo Request" (Type 8) entrants depuis Internet, tout en autorisant les "Echo Reply" (Type 0) sortants.
- **Attention au blocage total** : Bloquer _tous_ les types ICMP est déconseillé, car cela peut "casser" des mécanismes réseau essentiels, notamment la [[PathMTUDiscovery|Découverte du PMTU]] (qui repose sur le Type 3, Code 4 "Fragmentation Needed").
- **Surveillance Réseau** : Utiliser des [[IDS|Systèmes de Détection d'Intrusion (IDS)]] ou [[NDR|NDR (Network Detection and Response)]] pour détecter les comportements anormaux d'ICMP (scans, tunnels, floods).
    

## 🔗 Notes Connexes

- [[Ping]]
- [[Traceroute]]
- [[InternetProtocol|Protocole Internet (IP)]]
- [[OpenSystemsInterconnectionModel|Modèle OSI]]
- [[PingSweep|Ping Sweep]]
- [[SmurfAttack]]
- [[ICMPTunneling|Tunneling ICMP]]
