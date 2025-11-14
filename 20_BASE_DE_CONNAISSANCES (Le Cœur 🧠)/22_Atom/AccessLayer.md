---
tags:
  - architecture/couches/acces
  - reseau/conception-hierarchique
  - gestion/dispositifs-terminaux
  - architecture/reference-reseau
  - securite/securite-port
  - reseau/segmentation-vlan
aliases:
  - Couche d'Accès
  - Access Layer
source:
  - null
cssclasses:
  - max
---

# Couche d'Accès

## 📥 Définition en une phrase
> La couche d'accès est le niveau le plus bas dans une architecture de réseau hiérarchique, chargée de connecter les utilisateurs finaux et les appareils au reste du réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Point de connexion initial** : Sert de point d'entrée pour les utilisateurs, les ordinateurs, les imprimantes, les téléphones [[VoiceOverIP|VoIP]] et les autres dispositifs finaux.
*   **Concentration du trafic** : Agrège le trafic des utilisateurs finaux et le transmet vers la [[DistributionLayer|couche de distribution]].
*   **Implémentation de fonctionnalités périphériques** : Souvent responsable de fonctions telles que les [[VirtualLocalAreaNetwork|VLANs]], la [[QualityOfService|QoS]], la [[PowerOverEthernet|PoE]] pour les téléphones IP et les [[WirelessAccessPoint|points d'accès sans fil]], et la [[PortSecurity|sécurité des ports]].
*   **Haute densité de ports** : Les commutateurs de la couche d'accès sont généralement caractérisés par un grand nombre de ports Ethernet.
*   **Segmentation logique** : Permet de segmenter le réseau en domaines de broadcast plus petits via les [[VirtualLocalAreaNetwork|VLANs]] pour améliorer les performances et la sécurité.

## 🛡️ Risques / Menaces Associés
*   [[PhysicalSecurity|Accès physique]] non autorisé aux commutateurs ou ports non sécurisés.
*   [[DenialOfService|Attaques par déni de service]] (DoS) via inondation de MAC ou de paquets.
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] (MITM) comme le [[AddressResolutionProtocol|ARP]] spoofing ou le [[DynamicHostConfigurationProtocol|DHCP]] spoofing.
*   Connexion de dispositifs non autorisés ou malveillants au réseau.
*   [[UnsecuredWirelessNetwork|Points d'accès sans fil non sécurisés]] permettant un accès non authentifié.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[PortSecurity|Sécurité des ports]]** : Limiter le nombre de [[MediaAccessControlAddress|MAC addresses]] apprises par port, ou autoriser uniquement des [[MediaAccessControlAddress|MAC addresses]] spécifiques.
*   **[[8021X|Authentification 802.1X]]** : Exiger une authentification des dispositifs avant d'accorder l'accès au réseau.
*   **[[DynamicHostConfigurationProtocol|DHCP Snooping]]** : Prévenir les serveurs [[DynamicHostConfigurationProtocol|DHCP]] non autorisés et les attaques par inondation [[DynamicHostConfigurationProtocol|DHCP]].
*   **[[AccessControlList|ACLs]]** : Filtrer le trafic au niveau du port ou du [[VirtualLocalAreaNetwork|VLAN]].
*   **[[Segmentation|Segmentation réseau]]** : Utiliser des [[VirtualLocalAreaNetwork|VLANs]] pour isoler différents groupes d'utilisateurs ou types de trafic.
*   **[[PhysicalSecurity|Sécurité physique]]** : Protéger les commutateurs d'accès contre tout accès physique non autorisé.
*   **[[StormControl|Contrôle des tempêtes]]** : Limiter le trafic de broadcast, multicast et unicast inconnu pour prévenir les interruptions de service.

## 🔗 Notes Connexes
*   [[DistributionLayer|Couche de Distribution]]
*   [[CoreLayer|Couche Cœur]]
*   [[HierarchicalNetworkDesign|Conception de Réseaux Hiérarchiques]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkSwitch|Commutateur Réseau]]