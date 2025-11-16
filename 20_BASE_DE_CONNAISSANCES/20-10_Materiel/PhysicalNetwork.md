---
tags:
  - materiel
  - reseau
  - infrastructure
aliases:
  - Réseau Physique
  - Physical Network
  - Réseau matériel
  - Infrastructure Physique
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Réseau Physique

## 🎯 Rôle et Fonction
> Le réseau physique représente l'ensemble des [[Hardware|équipements]] et des [[NetworkMedia|supports de transmission]] tangibles (câbles, ondes radio, etc.) qui interconnectent les [[NetworkDevice|dispositifs réseau]] et les [[EndDevices|terminaux]] afin de permettre la [[DataTransmission|transmission de données]]. Il constitue la [[PhysicalLayer|couche fondamentale]] sur laquelle toutes les [[NetworkCommunication|communications réseau]] reposent.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: L'ensemble des [[Hardware|équipements]] (ex: [[Hub|concentrateurs]], [[NetworkSwitch|commutateurs]], [[Router|routeurs]], [[AccessPoint|points d'accès sans fil]]) et des [[NetworkMedia|supports de transmission]] (ex: [[CopperWire|câbles en cuivre]] comme les [[TwistedPair|paires torsadées]] et les [[CoaxialCable|câbles coaxiaux]], [[FiberOpticCable|câbles à fibre optique]], et [[WirelessMedia|supports sans fil]] utilisant des [[RadioWaves|ondes radio]], des [[Microwaves|micro-ondes]] ou des [[InfraredWaves|ondes infrarouges]]).
*   **Connectique**: Dépend des [[NetworkDevice|équipements]] et [[NetworkMedia|supports]], inclut typiquement les connecteurs [[RJ45Connector|RJ45]] pour les [[Ethernet|réseaux filaires]] et les antennes pour les [[WirelessNetwork|réseaux sans fil]].
*   **Performances**: Les capacités de [[Bandwidth|bande passante]], le [[Throughput|débit]] et la [[Latency|latence]] sont directement influencées par la qualité du [[NetworkMedia|support]], la [[NetworkTopology|topologie physique]] et les [[NetworkDevice|dispositifs d'interconnexion]].
*   **Normes associées**: Principalement [[EthernetProtocol|IEEE 802.3]] pour les [[LocalAreaNetwork|réseaux locaux]] filaires et [[IEEE80211|IEEE 802.11]] ([[WirelessFidelity|Wi-Fi]]) pour les [[WirelessNetwork|réseaux sans fil]]. Il opère principalement au niveau de la [[PhysicalLayer|couche physique]] (Couche 1) du [[OpenSystemsInterconnectionModel|modèle OSI]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Fournit la [[PhysicalLayer|fondation tangible]] indispensable à toute [[NetworkCommunication|communication réseau]], garantissant l'interconnexion des [[Computer|ordinateurs]] et [[NetworkDevice|dispositifs]].
    *   Permet un contrôle direct sur la [[PhysicalSecurity|sécurité physique]] et l'[[AccessControl|accès]] aux [[NetworkDevice|équipements]], offrant une ligne de défense initiale.
    *   La [[Redundancy|redondance]] au niveau physique peut améliorer la [[HighAvailability|haute disponibilité]] et la [[Reliability|fiabilité]] du [[Network|réseau]].
*   **Inconvénients**:
    *   Vulnérable aux [[HardwareFailure|défaillances matérielles]], aux [[EnvironmentalControls|conditions environnementales défavorables]] et aux [[UnauthorizedAccess|accès physiques non autorisés]], pouvant entraîner une [[ServiceDisruption|interruption de service]] ou un [[DataTheft|vol de données]].
    *   Coûts initiaux d'installation et de maintenance potentiellement élevés, surtout pour le déploiement de [[FiberOpticCable|fibres optiques]] ou de grandes infrastructures câblées.
    *   Moins flexible que les [[LogicalNetwork|réseaux logiques]] pour les reconfigurations, les ajouts ou les suppressions de [[NetworkSegment|segments]].
    *   Sensible aux [[ElectromagneticInterference|interférences électromagnétiques]] et autres [[ElectricalInterference|interférences électriques]] qui peuvent dégrader la qualité des [[SignalTransmission|transmissions de signaux]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] via des contrôles d'accès (verrous, caméras, systèmes d'alarme) et une surveillance régulière des zones où se trouvent les [[NetworkDevice|équipements réseau]].
*   [[EnvironmentalControls|Contrôles environnementaux]] (température, humidité, alimentation électrique stable) pour protéger les [[Hardware|équipements]] des pannes et prolonger leur durée de vie.
*   [[NetworkSegmentation|Segmentation Réseau]] pour isoler les services et les utilisateurs, limitant la portée des [[Attack|attaques]] physiques ou des compromissions.
*   [[WirelessNetworkSecurity|Sécurité des Réseaux Sans Fil]] robuste (ex: [[WirelessProtectedAccessThree|WPA3]], [[MACAddressFiltering|filtrage MAC]], désactivation du [[ServiceSetIdentifier|SSID]]) pour empêcher les [[UnauthorizedAccess|accès non autorisés]] via les ondes.

## 🔗 Notes Connexes
*   [[LogicalNetwork|Réseau Logique]]
*   [[PhysicalLayer|Couche Physique]] ([[OpenSystemsInterconnectionModel|Modèle OSI]])
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[NetworkMedia|Supports de Transmission Réseau]]
*   [[NetworkDevice|Périphérique Réseau]]
*   [[Cybersecurity|Cybersécurité]]
*   [[DataTransmission|Transmission de Données]]