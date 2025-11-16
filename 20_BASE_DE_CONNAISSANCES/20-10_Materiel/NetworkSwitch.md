---
tags:
  - materiel
  - reseau
  - commutateur/gere
  - commutateur/non-gere
  - couche/liaison/donnees
  - modele/osi
  - adresse-mac
  - configuration-reseau
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
> Un [[NetworkSwitch|commutateur réseau]] (ou switch) est un [[NetworkDevice|équipement réseau]] essentiel, opérant principalement au niveau de la [[DataLinkLayer|couche liaison de données]] (niveau 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]). 
> Son rôle principal est de connecter plusieurs [[EndDevices|appareils]] au sein d'un [[LocalAreaNetwork|réseau local (LAN)]]. 
> Il transfère le trafic de manière intelligente en utilisant les [[MediaAccessControlAddress|adresses MAC]] pour diriger les [[Frame|trames]] vers leur destination spécifique, améliorant ainsi l'efficacité et la [[NetworkPerformance|performance réseau]].

## 🛠️ Caractéristiques Techniques

*   **Type / Catégories**:
    *   [[ManagedSwitch|Commutateur géré]] : Offre des fonctionnalités avancées de [[NetworkConfiguration|configuration]], de [[NetworkMonitoring|surveillance]] et de gestion du trafic.
    *   [[UnmanagedSwitch|Commutateur non géré]] : Fonctionne en mode plug-and-play, sans options de configuration avancées, idéal pour les petits réseaux.
*   **Connectique**:
    *   Généralement équipé de plusieurs [[EthernetPorts|ports Ethernet]] compatibles [[RJ45Connector|RJ45]] pour les [[EthernetPatchCable|câbles Ethernet]].
    *   Peut inclure des [[FiberOpticCable|ports fibre optique]] (par ex. SFP, SFP+) pour des liaisons à haute [[DigitalBandwidth|bande passante]] ou sur de longues distances.
*   **Performances**:
    *   Offre une [[NetworkSegmentation|micro-segmentation]], créant un [[CollisionDomain|domaine de collision]] dédié par port, ce qui réduit les [[Collision|collisions]] et augmente le [[Throughput|débit]].
    *   Permet une [[FullDuplexCommunication|communication full-duplex]], autorisant l'envoi et la réception de données simultanément sur chaque port.
    *   Gère une [[MacAddressTable|table d'adresses MAC]] pour des décisions de [[PacketSwitching|transfert de paquets]] ciblées et efficaces.
*   **Normes associées**:
    *   [[EthernetProtocol|IEEE 802.3]] (standard pour l'[[Ethernet|Ethernet]]).
    *   [[VirtualLocalAreaNetwork|IEEE 802.1Q]] (pour la prise en charge des [[VirtualLocalAreaNetwork|VLANs]]).
    *   [[IEEE8021x|IEEE 802.1X]] (pour l'[[AccessControl|authentification]] et le contrôle d'accès au réseau).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Amélioration significative de la [[NetworkPerformance|performance réseau]] par rapport aux [[Hub|concentrateurs]] grâce au transfert ciblé des trames.
    *   Réduction des [[Collision|collisions]] et augmentation du [[Throughput|débit]] grâce à la [[NetworkSegmentation|micro-segmentation]].
    *   Offre des fonctionnalités de [[NetworkMonitoring|surveillance]] et de [[NetworkConfiguration|configuration]] avancées (pour les modèles gérés) telles que les [[VirtualLocalAreaNetwork|VLANs]] et la [[QualityOfService|QoS]].
*   **Inconvénients**:
    *   Coût plus élevé et complexité de [[NetworkConfiguration|configuration]] pour les commutateurs gérés.
    *   Les commutateurs non gérés n'offrent pas de capacités de sécurité ou de gestion.
    *   Potentielles [[SecurityVulnerabilities|vulnérabilités de sécurité]] s'ils ne sont pas correctement configurés (par exemple, des ports ouverts).

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] via des mesures de sécurité physique (verrouillage des armoires, emplacement sécurisé).
*   Contrôles environnementaux (température, humidité) pour assurer le bon fonctionnement du matériel et prévenir les pannes.

## 🔗 Notes Connexes
*   **Modèle de référence**: [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   **Dispositif similaire mais obsolète**: [[Hub|Hub]]
*   **Dispositif de couche 3 complémentaire**: [[Router|Routeur]]
*   **Concept lié à l'optimisation**: [[NetworkSegmentation|Segmentation Réseau]]
*   **Domaine de sécurité**: [[NetworkSecurity|Sécurité Réseau]]