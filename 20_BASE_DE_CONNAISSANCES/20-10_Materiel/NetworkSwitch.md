---
tags:
  - materiel
aliases:
  - Commutateur réseau
  - Switch
  - Network Switch
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Commutateur Réseau (Switch)

## 🎯 Rôle et Fonction
> Un [[NetworkSwitch|commutateur réseau]] (ou [[NetworkSwitch|switch]]) est un [[NetworkDevice|équipement réseau]] de [[DataLinkLayer|couche liaison de données]] (niveau 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]) dont le rôle principal est de connecter plusieurs [[EndDevices|appareils]] au sein d'un [[LocalAreaNetwork|réseau local (LAN)]]. Il transfère le [[NetworkTrafficAnalysis|trafic]] de manière intelligente en utilisant les [[MediaAccessControlAddress|adresses MAC]] pour diriger les [[Frame|trames]] vers leur destination spécifique, améliorant ainsi l'efficacité et la [[NetworkPerformance|performance réseau]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   [[ManagedSwitch|Commutateur géré]] (offrant des fonctionnalités avancées de [[NetworkConfiguration|configuration]] et de [[NetworkMonitoring|surveillance]]).
    *   [[UnmanagedSwitch|Commutateur non géré]] (plug-and-play, sans options de configuration).
    *   Opère au niveau de la [[DataLinkLayer|couche liaison de données]] (niveau 2 [[OpenSystemsInterconnectionModel|OSI]]).
*   **Connectique**:
    *   Généralement équipé de plusieurs [[EthernetPorts|ports Ethernet]] compatibles [[RJ45Connector|RJ45]] pour les [[EthernetPatchCable|câbles Ethernet]].
    *   Peut inclure des [[FiberOpticCable|ports fibre optique]] (par ex. SFP, SFP+) pour des liaisons à haute [[DigitalBandwidth|bande passante]] ou sur de longues distances.
*   **Performances**:
    *   Offre une [[Microsegmentation|micro-segmentation]], créant un [[CollisionDomain|domaine de collision]] dédié par port, ce qui réduit les [[Collision|collisions]] et augmente la [[NetworkThroughput|débit]].
    *   Permet une [[FullDuplexCommunication|communication full-duplex]], autorisant l'envoi et la réception de [[Data|données]] simultanément sur chaque port.
    *   Gère une [[MacAddressTable|table d'adresses MAC]] pour des décisions de [[PacketSwitching|transfert de paquets]] ciblées et efficaces.
*   **Normes associées**:
    *   [[EthernetProtocol|IEEE 802.3]] (standard pour [[Ethernet|Ethernet]]).
    *   [[VirtualLocalAreaNetwork|IEEE 802.1Q]] (pour la prise en charge des [[VirtualLocalAreaNetwork|VLANs]]).
    *   [[IEEE8021x|IEEE 802.1X]] (pour l'[[AccessControl|authentification]] et le [[AccessControl|contrôle d'accès]] au réseau).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   [[NetworkPerformance|Amélioration significative des performances réseau]] par rapport aux [[Hub|concentrateurs]] grâce à la [[Microsegmentation|micro-segmentation]] et au [[FullDuplexCommunication|full-duplex]].
    *   [[NetworkSegmentation|Segmentation flexible du réseau]] via les [[VirtualLocalAreaNetwork|VLANs]], permettant d'isoler le [[NetworkTrafficAnalysis|trafic]] et d'appliquer des [[SecurityPolicy|politiques de sécurité]] spécifiques.
    *   [[TrafficManagement|Gestion intelligente et ciblée du trafic]], réduisant la charge sur les autres [[NetworkDevice|périphériques]].
    *   [[Scalability|Évolutivité]] pour accueillir un grand nombre de [[EndDevices|périphériques]] avec une dégradation minimale des [[NetworkPerformance|performances]].
*   **Inconvénients**:
    *   Coût généralement plus élevé que les [[Hub|concentrateurs]].
    *   Nécessite une [[NetworkConfiguration|configuration]] appropriée pour tirer parti des fonctionnalités avancées ([[VirtualLocalAreaNetwork|VLANs]], [[PortSecurity|sécurité des ports]]).
    *   Vulnérable à certaines [[Attack.md|attaques]] de [[DataLinkLayer|couche 2]] comme le [[MACFlooding|MAC flooding]] ou l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] pour empêcher la manipulation des [[NetworkConfiguration|configurations]] ou l'interception de [[Data|données]].
*   [[EnvironmentalControls|Contrôles environnementaux]] (température, humidité) pour assurer la fiabilité et la longévité du [[Hardware|matériel]].

## 🔗 Notes Connexes
*   [[DataLinkLayer|Couche Liaison de Données]] (Modèle [[OpenSystemsInterconnectionModel|OSI]])
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[Hub|Concentrateur (Hub)]]
*   [[Router|Routeur]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel (VLAN)]]
*   [[SpanningTreeProtocol|Protocole Spanning Tree (STP)]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[PortSecurity|Sécurité des Ports]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresse (ARP)]]