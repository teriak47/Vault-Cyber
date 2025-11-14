---
tags:
  - reseau/interconnexion
  - cybersécurité/menaces-reseau
  - modele/couche-reseau
  - routage
aliases:
  - Couche Réseau
  - Network Layer
source:
  - 
cssclasses:
  - max
---

# Couche Réseau

## 📥 Définition en une phrase
> La couche réseau est la troisième couche du [[OpenSystemsInterconnectionModel|Modèle OSI]], chargée de l'adressage logique et de l'acheminement des [[Packet|paquets]] de données entre des réseaux différents (inter-réseaux).

## 🧠 Concepts Clés / Fonctionnement
*   **[[InternetProtocol|Protocoles d'Adressage Logique]]**: Utilise des adresses logiques (comme les adresses [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]]) pour identifier de manière unique les hôtes sur un réseau.
*   **[[Routing|Routage]]**: Détermine le meilleur chemin pour les [[Packet|paquets]] de données à travers un inter-réseau en utilisant des [[Router|routeurs]] et des tables de routage.
*   **Encapsulation/Désencapsulation**: Encapsule les segments de la [[TransportLayer|couche transport]] dans des [[Packet|paquets]] à l'émission et les désencapsule à la réception.
*   **Fragmentatio**: Peut diviser les [[Packet|paquets]] en unités plus petites si la taille du paquet dépasse la MTU (Maximum Transmission Unit) d'un lien réseau.
*   **Dispositifs**: Les principaux dispositifs opérant à cette couche sont les [[Router|routeurs]], qui connectent différents réseaux et transmettent les paquets.

## 🛡️ Risques / Menaces Associés
*   [[DDoSAttack|Attaques par déni de service distribué (DDoS)]]: Visent à saturer le réseau pour empêcher le trafic légitime d'atteindre sa destination.
*   [[IPSpoofing|Usurpation d'adresse IP (IP Spoofing)]]: Falsification de l'adresse IP source pour masquer l'identité de l'attaquant ou contourner les contrôles d'accès.
*   [[RoutingTablePoisoning|Empoisonnement des tables de routage]]: Manipulation des informations de routage pour rediriger le trafic vers des destinations malveillantes.
*   [[PacketSniffing|Reniflage de paquets]]: Interception et analyse du trafic réseau pour obtenir des [[SensitiveData|informations sensibles]].
*   [[ManInTheMiddle|Attaque de l'homme du milieu (MITM)]]: L'attaquant intercepte et potentiellement modifie la communication entre deux parties sans qu'elles le sachent.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Pare-feux]]: Mettre en œuvre des pare-feux pour filtrer le trafic basé sur les adresses IP et les ports, bloquant les connexions non autorisées.
*   [[NetworkSegmentation|Segmentation réseau]]: Diviser le réseau en segments plus petits (ex: avec des [[VirtualLAN|VLAN]]) pour limiter la propagation des menaces et isoler les ressources critiques.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion (IPS)]]: Déployer des IDS/IPS pour surveiller le trafic réseau et détecter/bloquer les activités suspectes.
*   [[VirtualPrivateNetwork|Réseaux Privés Virtuels (VPN)]]: Utiliser des VPN pour chiffrer le trafic réseau et garantir la confidentialité et l'intégrité des données lors de la transmission.
*   [[SecureRoutingProtocol|Protocoles de routage sécurisés]]: Mettre en œuvre des [[SecureRoutingProtocols|protocoles de routage sécurisés]] (ex: BGPsec) et authentifier les échanges de routage pour prévenir l'empoisonnement des tables.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocol|Protocole Internet (IP)]]
*   [[Routing|Routage]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[TransportLayer|Couche Transport]]
*   [[Packet|Paquet]]