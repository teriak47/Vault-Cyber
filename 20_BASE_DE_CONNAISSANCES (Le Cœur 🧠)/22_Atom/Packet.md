---
tags:
  - reseau/encapsulation
  - securite/filtrage-paquets
  - reseau
aliases:
  - Paquet
  - Datagram
source:
  - 
cssclasses:
  - max
---

# Paquet

## 📥 Définition en une phrase
> Une unité fondamentale de données encapsulée et transmise sur un réseau, conçue pour un acheminement efficace et structuré.

## 🧠 Concepts Clés / Fonctionnement
*   **Encapsulation**: Un paquet est composé d'un en-tête (headers) qui contient les informations d'adresse (source, destination, ports), des informations de contrôle et le corps du message (payload) qui est la donnée utile.
*   **Structure**: Généralement, un paquet comprend un en-tête (header), la charge utile (payload) et parfois un pied de page (trailer) pour le contrôle d'erreur (checksum).
*   **Routage**: Les routeurs et les commutateurs analysent les informations de l'en-tête (notamment les adresses IP et MAC) pour déterminer le chemin optimal pour acheminer le paquet vers sa destination.
*   **Protocoles**: La structure et le comportement d'un paquet sont définis par les protocoles réseau sous-jacents, tels que [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]] ou [[InternetProtocol|IP]].
*   **Fragmentatio**: Les paquets peuvent être fragmentés en unités plus petites pour traverser des réseaux avec des unités de transmission maximale (MTU) différentes, puis réassemblés à destination.

## 🛡️ Risques / Menaces Associés
*   [[PacketSniffing|Analyse de paquets]] (interception et lecture des données)
*   [[ManInTheMiddle|Attaque de l'homme du milieu]] (interception et modification des paquets)
*   [[DenialOfService|Attaques par déni de service]] (inondation ou malformation de paquets pour épuiser les ressources)
*   [[IPSpoofing|Usurpation d'IP]] (falsification de l'adresse IP source dans l'en-tête du paquet)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] (pour protéger la charge utile du paquet, ex: [[TransportLayerSecurity|TLS]], [[VirtualPrivateNetwork|VPN]])
*   [[Firewall|Pare-feu]] (pour filtrer les paquets en fonction de leurs en-têtes)
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) et [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion]] (IPS) (pour analyser les paquets à la recherche de signatures d'attaques)
*   [[SecureProtocol|Utilisation de protocoles sécurisés]] (ex: HTTPS au lieu de HTTP)
*   [[NetworkSegmentation|Segmentation réseau]] (pour limiter la portée des paquets malveillants)

## 🔗 Notes Connexes
*   [[Frame|Trame]]
*   [[Datagram|Datagramme]]
*   [[NetworkTraffic|Trafic réseau]]
*   [[ProtocolStack|Pile de protocoles]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetProtocol|IP]]
