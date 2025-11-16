---
tags:
  - materiel
aliases:
  - Ports Ethernet
  - Ethernet Ports
  - Port Ethernet
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Ports Ethernet

## 🎯 Rôle et Fonction
> Un port Ethernet est une interface physique présente sur un [[NetworkDevice|appareil réseau]] ou un [[Computer|ordinateur]], conçue pour permettre une connexion filaire à un [[LocalAreaNetwork|réseau local]] (LAN) via un [[EthernetCable|câble Ethernet]]. Il sert de point d'entrée/sortie pour le [[DataTransmission|transfert de données]] sur un [[PhysicalNetwork|réseau physique]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Interface physique standardisée pour la connectivité filaire.
*   **Connectique**: Connecteur [[RJ45Connector|RJ-45]] pour les câbles [[UnshieldedTwistedPair|UTP]] ou [[TwistedPair|câbles à paires torsadées]].
*   **Performances**:
    *   Supporte des vitesses de [[Bandwidth|débit]] variées : 10/100 [[MegabitsPerSecond|Mbps]], 1 [[GigabitsPerSecond|Gbps]], 10 [[GigabitsPerSecond|Gbps]] et plus (selon la norme et le matériel).
    *   Opère généralement en mode [[FullDuplex|full-duplex]], permettant l'envoi et la réception de [[Data|données]] simultanément, améliorant le [[Throughput|débit]] et réduisant les [[Collision|collisions]].
*   **Normes associées**: Régis par les normes de la famille [[EthernetProtocol|IEEE 802.3]], définissant les spécifications des [[PhysicalLayer|couches physique]] et [[DataLinkLayer|liaison de données]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Fiabilité et Stabilité**: Offre une connexion plus stable et moins sujette aux [[ElectromagneticInterference|interférences électromagnétiques]] que le [[WirelessNetwork|sans fil]].
    *   **Hautes Performances**: Capacité à supporter des [[DigitalBandwidth|bandes passantes numériques]] élevées et de faibles [[Latency|latences]], idéales pour les applications exigeantes.
    *   **Sécurité Relative**: Moins vulnérable aux [[Eavesdropping|écoutes clandestines]] passives à distance par rapport aux [[WirelessSignals|signaux sans fil]], nécessitant un [[PhysicalAccess|accès physique]] pour l'interception.
*   **Inconvénients**:
    *   **Dépendance Physique**: Nécessite un [[EthernetCable|câble physique]], limitant la [[Mobility|mobilité]] des appareils et ajoutant à la complexité de l'[[NetworkInfrastructure|infrastructure]].
    *   **Gestion des Câbles**: Peut entraîner un encombrement et une gestion complexe des câbles, en particulier dans les grands [[CorporateNetwork|réseaux d'entreprise]].
    *   **Coût d'Installation**: L'installation ou l'extension d'un [[PhysicalNetwork|réseau filaire]] peut être plus coûteuse et chronophage.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: Les ports Ethernet non sécurisés peuvent être des [[AttackVector|vecteurs d'attaque]] permettant à un [[ThreatActor|acteur de menace]] d'accéder directement au [[Network|réseau]]. Des mesures comme le [[PortSecurity|filtrage d'adresses MAC]] ou la [[NetworkAccessControl|sécurité des ports]] sont essentielles.
*   [[EnvironmentalControls|Contrôles environnementaux (température, humidité)]]: Bien que directement liés au [[Hardware|matériel]] en général, la protection des [[NetworkDevice|périphériques réseau]] hôtes des ports contre les conditions environnementales extrêmes est cruciale pour leur bon fonctionnement et leur durabilité.
*   [[DésactivationPortsInutilisés|Désactivation des ports inutilisés]]: Une bonne pratique consiste à désactiver les ports physiques des [[NetworkSwitch|commutateurs]] qui ne sont pas connectés ou en service pour réduire la [[AttackSurface|surface d'attaque]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Couche Physique]]
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[LocalAreaNetwork|Réseau local (LAN)]]
*   [[NetworkInterfaceCard|Carte d'interface réseau (NIC)]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[Router|Routeur]]
*   [[RJ45Connector|Connecteur RJ-45]]
*   [[EthernetCable|Câble Ethernet]]
*   [[FullDuplex|Full-Duplex]]
*   [[RogueDevice|Appareil malveillant]]