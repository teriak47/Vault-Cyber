---
tags:
  - materiel
  - materiel/routeur
  - reseau/lan
  - reseau/internet
  - reseau/nat
  - protocole/ip
  - protocole/osi
aliases:
  - Routeur
  - Network Router
archetype: materiel
source:
  -
cssclasses:
  - max
---

# Routeur

## 🎯 Rôle et Fonction
> Un [[Router|routeur]] est un [[NetworkDevice|équipement réseau]] crucial qui opère à la [[NetworkLayer|couche réseau]] (Couche 3) du [[OpenSystemsInterconnectionModel|Modèle OSI]]. Son rôle principal est de transmettre les [[Packet|paquets de données]] entre différents [[Network|réseaux informatiques]], comme un [[LocalAreaNetwork|LAN]] et l'[[Internet|Internet]], en déterminant le chemin le plus efficace pour atteindre leur destination. Il utilise les [[InternetProtocol|adresses IP]] pour faciliter ce [[Routing|routage]] intelligent.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: [[NetworkDevice|Dispositif réseau]] d'[[InterconnectedNetworks|interconnexion de réseaux]], peut être physique ou virtuel (logiciel).
*   **Connectique**: Généralement plusieurs [[EthernetPorts|ports Ethernet]] (ex: [[RJ45Connector|RJ45]]), et parfois des interfaces [[WirelessFidelity|Wi-Fi]] ou pour [[FiberOpticCable|fibre optique]].
*   **Performances**: Débit de traitement des [[Packet|paquets]] (en [[MegabitsPerSecond|Mbps]] ou [[GigabitsPerSecond|Gbps]]), nombre de routes gérées, capacité de [[NetworkAddressTranslation|NAT]].
*   **Normes associées**:
    *   [[InternetProtocolSuite|Suite de protocoles TCP/IP]] (incluant [[InternetProtocol|IP]], [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]).
    *   [[InstituteOfElectricalAndElectronicsEngineers|IEEE]] (pour les interfaces [[Ethernet|Ethernet]] ou [[WirelessFidelity|Wi-Fi]]).
    *   [[InternetEngineeringTaskForce|IETF]] (pour les [[Protocol|protocoles]] de [[Routing|routage]]).
*   **Fonctionnalités Clés**:
    *   Maintien de [[RoutingTable|tables de routage]] pour stocker les informations de chemin.
    *   Supporte les [[RoutingProtocol|protocoles de routage]] dynamiques (tels qu'OSPF, BGP) et le [[StaticConfiguration|routage statique]].
    *   Effectue souvent la [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]].
    *   Peut servir de [[DefaultGateway|passerelle par défaut]] pour un [[LocalAreaNetwork|réseau local]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Interconnexion et Segmentation**: Permet la connexion de multiples [[NetworkSegment|segments de réseau]] et leur [[NetworkSegmentation|segmentation]], améliorant la [[NetworkPerformance|performance]] et la [[NetworkSecurity|sécurité]].
    *   **Optimisation du Trafic**: Sélectionne le meilleur chemin pour les [[Packet|paquets]], réduisant la [[Latency|latence]] et améliorant l'[[Throughput|efficacité du réseau]].
    *   **[[NetworkAddressTranslation|NAT]] et Sécurité**: Offre des fonctions de [[NetworkAddressTranslation|NAT]] pour économiser les [[PublicIPAddress|adresses IP publiques]] et masquer la structure du [[InternalNetwork|réseau interne]], agissant comme une première ligne de [[NetworkSecurity|défense]].
    *   **[[Scalability|Évolutivité]]**: Facilite l'expansion du [[Network|réseau]] en ajoutant de nouveaux [[Subnet|sous-réseaux]].
*   **Inconvénients**:
    *   **Coût**: Peut être coûteux, surtout pour les modèles haute performance d'[[Enterprise|entreprise]].
    *   **Complexité de Configuration**: Nécessite une expertise pour une [[NetworkConfiguration|configuration]] et une [[Security|sécurité]] optimales.
    *   **Point de Défaillance Unique**: Une panne peut interrompre la [[NetworkCommunication|communication]] entre [[Network|réseaux]].
    *   **[[AttackSurface|Surface d'attaque]]**: Cible potentielle pour les [[DigitalAttack|attaques]] s'il n'est pas correctement sécurisé.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] via des verrous ou des zones sécurisées.
*   [[EnvironmentalControls|Contrôles environnementaux]] pour prévenir la surchauffe, l'humidité excessive ou d'autres risques physiques.
*   Mise à jour régulière du [[Firmware|micrologiciel]] pour corriger les [[SoftwareVulnerability|vulnérabilités]] connues.
*   Implémentation de [[AccessControl|contrôles d'accès]] administratifs robustes.

## 🔗 Notes Connexes
*   [[NetworkLayer|Couche Réseau]] : Le [[Router|routeur]] opère principalement à cette [[OpenSystemsInterconnectionModel|couche OSI]].
*   [[InternetProtocol|Protocole Internet (IP)]] : Le [[Router|routeur]] utilise les [[InternetProtocol|adresses IP]] pour le [[Routing|routage]].
*   [[RoutingTable|Table de Routage]] : Une base de données essentielle maintenue par le [[Router|routeur]].
*   [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]] : Une fonction courante des [[Router|routeurs]].
*   [[DefaultGateway|Passerelle par défaut]] : Le point de sortie par défaut pour le trafic réseau sortant d'un [[Subnet|sous-réseau]].
*   [[NetworkSwitch|Commutateur réseau]] : Un autre [[NetworkDevice|dispositif réseau]] souvent utilisé en conjonction avec un [[Router|routeur]] pour la [[NetworkSegmentation|segmentation]] au niveau 2.
*   [[WirelessRouter|Routeur sans fil]] : Une variante intégrant des fonctionnalités [[WirelessFidelity|Wi-Fi]] pour l'accès sans fil.
*   [[RoutingProtocol|Protocoles de Routage]] : Mécanismes utilisés pour échanger des informations de [[Routing|routage]] entre [[Router|routeurs]].