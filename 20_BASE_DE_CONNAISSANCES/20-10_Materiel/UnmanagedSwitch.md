---
tags:
  - materiel
  - commutateur/non-gere
  - reseau
aliases:
  - Commutateur non géré
  - Unmanaged Network Switch
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Commutateur non géré (Unmanaged Switch)

## 🎯 Rôle et Fonction
> Un [[NetworkSwitch|commutateur réseau]] non géré est un [[NetworkDevice|périphérique réseau]] de base qui permet la connexion de plusieurs [[EndDevices|appareils terminaux]] au sein d'un [[LocalAreaNetwork|réseau local]]. Il fonctionne sur le principe du "plug-and-play", sans nécessiter de [[NetworkConfiguration|configuration]] manuelle. Son rôle principal est de transférer les [[EthernetFrame|trames Ethernet]] entre les appareils connectés en utilisant les [[MediaAccessControlAddress|adresses MAC]] pour diriger le trafic de manière efficace à la [[DataLinkLayer|Couche Liaison de Données]] du [[OpenSystemsInterconnectionModel|Modèle OSI]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Généralement compact et simple, il est souvent utilisé dans les [[SmallHomeNetworks|petits réseaux domestiques]] ou les [[SOHONetwork|petits bureaux]].
*   **Connectique**: Dispose de plusieurs [[RJ45Connector|ports RJ45]] pour les [[EthernetPatchCable|câbles Ethernet]] ([[TwistedPairCable|paires torsadées]]).
*   **Performances**: Prise en charge de diverses vitesses ([[MegabitsPerSecond|Mbps]], [[GigabitsPerSecond|Gbps]]) avec auto-négociation (vitesse et duplex).
*   **Normes associées**: Conforme au [[EthernetProtocol|protocole Ethernet]] ([[InstituteOfElectricalAndElectronicsEngineers|IEEE]] [[Ethernet|802.3]]).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Simplicité d'installation et d'utilisation (plug-and-play).
    *   Faible coût d'acquisition.
    *   Maintenance minimale.
*   **Inconvénients**:
    *   Manque de fonctionnalités de [[Security|sécurité]] avancées.
    *   Pas de [[VirtualLocalAreaNetwork|VLAN]] pour la [[NetworkSegmentation|segmentation du réseau]].
    *   Pas de [[QualityOfService|gestion de la qualité de service (QoS)]].
    *   Absence de [[NetworkMonitoring|capacités de surveillance]] ou de [[TrafficManagement|gestion du trafic]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]
*   Contrôles environnementaux (température, humidité)

## 🔗 Notes Connexes
*   **Alternative plus avancée**: [[ManagedSwitch|Commutateur géré]]
*   **Concept de sécurité pertinent**: [[PortSecurity|Sécurité des ports]]
*   **Modèle de référence associé**: [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   **Impact sur la posture de sécurité**: [[AttackSurface|Surface d'attaque]]