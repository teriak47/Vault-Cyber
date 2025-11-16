---
tags:
  - materiel
aliases:
  - Port LAN
  - Local Area Network Port
  - LAN Port
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Port LAN

## 🎯 Rôle et Fonction
> Un [[LANPort|port LAN]] est un connecteur physique que l'on trouve sur des [[NetworkDevice|périphériques réseau]] comme les [[Router|routeurs]] ou les [[NetworkSwitch|commutateurs]]. Son rôle principal est de permettre la connexion de [[EndDevices|dispositifs terminaux]] (ordinateurs, [[NetworkPrinter|imprimantes réseau]]) ou d'autres [[NetworkDevice|équipements réseau]] au sein d'un [[LocalAreaNetwork|réseau local]], facilitant ainsi la [[NetworkCommunication|communication réseau]] et le [[FileTransfer|partage de ressources]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Généralement un [[EthernetPorts|port Ethernet]], il peut être présent sur des [[Router|routeurs]], des [[NetworkSwitch|commutateurs réseau]] ou des [[Firewall|pare-feu]].
*   **Connectique**: Utilise le [[RJ45Connector|connecteur RJ45]] pour les [[EthernetPatchCable|câbles Ethernet]], typiquement des [[TwistedPair|câbles à paires torsadées]] [[UnshieldedTwistedPair|UTP]].
*   **Performances**: Supporte diverses [[DigitalBandwidth|bandes passantes numériques]] selon la norme [[EthernetProtocol|Ethernet]] implémentée (ex: 10 Mbps, 100 Mbps, 1 Gbps, 10 Gbps). La [[Throughput|performance de débit]] dépendra du [[NetworkMedia|support réseau]] et de la carte [[NetworkInterfaceCard|NIC]] connectée.
*   **Normes associées**: Principalement défini par la famille de normes [[EthernetProtocol|IEEE 802.3]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Offre une [[NetworkCommunication|connectivité réseau]] filaire stable et généralement plus rapide que le [[WirelessFidelity|Wi-Fi]].
    *   Fiabilité et faible [[Latency|latence]] pour les applications sensibles (voix, vidéo, jeux).
    *   Simplicité d'intégration des [[EndDevices|terminaux]] dans le [[LocalAreaNetwork|réseau local]].
*   **Inconvénients**:
    *   Nécessite une [[PhysicalSecurity|sécurité physique]] pour éviter l'[[UnauthorizedAccess|accès non autorisé]] direct.
    *   Contraintes de câblage et de [[NetworkCableManagement|gestion des câbles]].
    *   Peut devenir une [[Vulnerability|vulnérabilité]] si non configuré avec la [[PortSecurity|sécurité des ports]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] aux [[LANPort|ports LAN]] via des contrôles d'accès physiques aux [[NetworkDevice|équipements réseau]].
*   Utilisation de [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] pour lier les ports à des [[MediaAccessControlAddress|adresses MAC]] spécifiques et désactiver les ports inutilisés.
*   Mise en place de [[NetworkSegmentation|segmentation réseau]] (ex: [[VirtualLocalAreaNetwork|VLAN]]) pour isoler différents groupes d'appareils et limiter la portée d'une compromission.
*   [[EnvironmentalControls|Contrôles environnementaux]] pour protéger les [[NetworkDevice|périphériques réseau]] et leurs ports contre les dommages physiques.

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche Physique]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[RJ45Connector|Connecteur RJ45]]
*   [[TwistedPair|Câble à paires torsadées]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[Router|Routeur]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau]]
*   [[PortSecurity|Sécurité des Ports]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[NetworkConfiguration|Configuration réseau]]
*   [[StaticIPAddressing|Adressage IP Statique]]
*   [[DynamicHostConfigurationProtocol|DHCP]]