---
tags:
  - reseau
  - ipv4
aliases:
  - Limited Broadcast
  - Diffusion limitée
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Diffusion Limitée (Limited Broadcast)

## 🎯 Rôle et Couche OSI

> La diffusion limitée est un mécanisme de communication spécifique à [[InternetProtocolVersion4|IPv4]] qui permet à un [[Host|hôte]] d'envoyer un [[Packet|paquet]] de données à tous les autres [[Host|hôtes]] présents sur le même [[NetworkSegment|segment réseau]] local. Elle opère principalement au niveau de la [[NetworkLayer|couche Réseau]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement

1.  **Adresse de Destination**: Le [[Packet|paquet]] est adressé à l'[[BroadcastAddress|adresse IP de diffusion]] spécifique à un segment local, qui est [[BroadcastAddress|255.255.255.255]].
2.  **Portée Locale**: Les [[Router|routeurs]] sont configurés par défaut pour ne pas retransmettre les [[Packet|paquets]] envoyés à l'adresse `255.255.255.255`, confinant ainsi la [[Broadcast|diffusion]] au [[BroadcastDomain|domaine de diffusion]] d'origine.
3.  **Réception Universelle Locale**: Tous les [[EndDevices|dispositifs terminaux]] et [[IntermediateDevice|intermédiaires]] connectés au [[NetworkSegment|segment réseau]] local reçoivent et traitent ce [[Packet|paquet]].
4.  **Cas d'Usage**: Elle est couramment utilisée par des [[NetworkProtocol|protocoles]] comme [[DynamicHostConfigurationProtocol|DHCP]] pour la découverte initiale de serveurs ou de services sur un [[LocalAreaNetwork|réseau local]] lorsque l'[[InternetProtocol|adresse IP]] de destination n'est pas encore connue.

- **Ports par défaut**: N/A (ce n'est pas un protocole de transport, mais une méthode d'adressage IP)

## 🛡️ Sécurité du Protocole

- **Vulnérabilités connues**:
  - [[DenialOfService|Déni de Service (DoS)]]: Un volume excessif de [[Broadcast|diffusions]] peut saturer le [[Network|réseau]] local, provoquant une [[NetworkCongestion|congestion réseau]] et potentiellement un [[DenialOfService|déni de service]] pour les [[Host|hôtes]] du segment.
  - [[SmurfAttack|Attaques Smurf]]: Bien que les [[Router|routeurs]] modernes bloquent généralement les [[DirectedBroadcast|diffusions dirigées]] vers des réseaux distants, une configuration laxiste ou une exploitation locale des [[Broadcast|diffusions]] limitées peut toujours contribuer à une [[Attack|attaque]] par surcharge.
  - [[PacketSniffing|Interception de Paquets]]: Étant donné que tous les [[Host|hôtes]] du [[NetworkSegment|segment réseau]] reçoivent le [[Packet|paquet]], il est plus facile pour un [[ThreatActor|acteur de menace]] d'intercepter les données si elles ne sont pas [[DataEncryption|chiffrées]].
- **Versions sécurisées**:
  - Pas de "versions" sécurisées au sens protocolaire, mais des mesures de [[SecurityControl|contrôle de sécurité]] sont cruciales:
    - [[NetworkSegmentation|Segmentation Réseau]]: L'utilisation de [[VirtualLocalAreaNetwork|VLANs]] pour réduire la taille des [[BroadcastDomain|domaines de diffusion]].
    - [[Firewall|Filtrage par Pare-feu]]: Configuration rigoureuse des [[Firewall|pare-feu]] pour bloquer les [[Broadcast|diffusions]] inutiles ou suspectes.
    - [[NetworkMonitoring|Surveillance Réseau]]: Détection d'activités de [[Broadcast|diffusion]] anormales via des outils de [[NetworkTrafficAnalysis|surveillance du trafic réseau]].

## 🔗 Notes Connexes

- [[Broadcast|Diffusion]]
- [[BroadcastAddress|Adresse de Diffusion]]
- [[DirectedBroadcast|Diffusion Dirigée]]
- [[InternetProtocolVersion4|Internet Protocol version 4]] ([[IPv4]])
- [[LocalAreaNetwork|Réseau Local]] ([[LAN]])
- [[NetworkLayer|Couche Réseau]]
- [[NetworkCongestion|Congestion Réseau]]
- [[SmurfAttack|Attaque Smurf]]
- [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique]] ([[DHCP]])
- [[NetworkSegmentation|Segmentation Réseau]]
