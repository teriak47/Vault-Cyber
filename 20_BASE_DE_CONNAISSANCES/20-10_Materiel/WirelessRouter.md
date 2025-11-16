---
tags:
  - materiel
  - materiel/routeur-sans-fil
aliases:
  - Routeur sans fil
  - Wireless Router
  - Routeur Wi-Fi
  - Wireless Fidelity Router
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Routeur Sans Fil

## 🎯 Rôle et Fonction
> Un [[WirelessRouter|routeur sans fil]] est un [[NetworkDevice|appareil réseau]] qui agit comme une passerelle centrale, combinant les fonctions d'un [[Router|routeur]], d'un [[AccessPoint|point d'accès sans fil]] et souvent d'un [[NetworkSwitch|commutateur]] et d'un [[DHCPServer|serveur DHCP]]. Il permet à plusieurs [[EndDevices|appareils terminaux]] de se connecter à un [[LocalAreaNetwork|réseau local]] et à [[Internet|Internet]], facilitant la [[NetworkCommunication|communication réseau]] filaire et [[WirelessTransmission|sans fil]]. Il dirige le [[NetworkTrafficAnalysis|trafic]] entre les différents [[NetworkSegment|segments réseau]] (LAN, WAN, WLAN).

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Appareil [[NetworkInfrastructure|d'infrastructure réseau]] hybride, combinant les fonctions de [[Routing|routage]], de [[PacketSwitching|commutation]] et de [[WirelessTechnology|point d'accès sans fil]]. Souvent utilisé dans les [[SmallHomeNetworks|petits réseaux domestiques]] et les [[SOHONetwork|réseaux SOHO]].
*   **Connectique**: Généralement équipé de plusieurs [[EthernetPorts|ports Ethernet]] (un port WAN pour la connexion [[Internet|Internet]] et plusieurs ports LAN pour les connexions filaires), ainsi que d'une ou plusieurs [[WirelessAntenna|antennes]] pour la diffusion des [[WirelessSignals|signaux sans fil]].
*   **Performances**: Les [[NetworkPerformance|performances]] sont déterminées par les standards [[IEEE80211|IEEE 802.11]] pris en charge (ex: 802.11ac, 802.11ax/[[WirelessFidelity|Wi-Fi 6]]), le [[Throughput|débit]] maximal, la [[Bandwidth|bande passante]] disponible et la puissance des [[WirelessSignals|signaux sans fil]].
*   **Normes associées**:
    *   **Sans fil**: [[IEEE80211|IEEE 802.11]] (a/b/g/n/ac/ax - [[WirelessFidelity|Wi-Fi 6]])
    *   **Filaire**: [[EthernetProtocol|IEEE 802.3]] ([[Ethernet]])
    *   **Protocoles réseau**: [[InternetProtocol|IP]], [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]], [[DynamicHostConfigurationProtocol|DHCP]], [[NetworkAddressTranslation|NAT]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Connectivité polyvalente**: Offre des options de connexion [[NetworkCommunication|réseau]] à la fois filaires et [[WirelessTransmission|sans fil]].
    *   **Partage de connexion**: Permet à de multiples [[EndDevices|appareils terminaux]] de partager une seule [[Internet|connexion Internet]].
    *   **Facilité d'utilisation**: Généralement simple à configurer et à gérer pour les [[HomeNetwork|utilisateurs domestiques]] et les petites entreprises.
    *   **Fonctionnalités intégrées**: Intègre des fonctions essentielles comme le [[DHCPServer|serveur DHCP]], la [[NetworkAddressTranslation|NAT]] et un [[Firewall|pare-feu]] de base pour la [[NetworkSecurity|sécurité du réseau]].
*   **Inconvénients**:
    *   **Portée et performance limitées**: La portée des [[WirelessSignals|signaux sans fil]] et le [[Throughput|débit]] peuvent être affectés par les obstacles physiques et les [[ElectromagneticInterference|interférences électromagnétiques]].
    *   **Vulnérabilités de sécurité**: Peut présenter des [[SecurityVulnerabilities|vulnérabilités]] si le [[Firmware|micrologiciel]] n'est pas mis à jour, si des [[StrongPasswords|mots de passe faibles]] sont utilisés, ou si la [[WirelessSecurity|configuration de sécurité sans fil]] est inadéquate ([[WirelessProtectedAccessTwo|WPA2]] ou [[WirelessProtectedAccessThree|WPA3]] est fortement recommandé).
    *   **Point de défaillance unique**: Une panne du [[WirelessRouter|routeur sans fil]] peut entraîner une [[ServiceDisruption|interruption de service]] complète pour l'ensemble du [[LocalAreaNetwork|réseau]].
    *   **Congestion réseau**: Peut être sujet à la [[NetworkCongestion|congestion]] si un grand nombre d'[[WirelessDevices|appareils sans fil]] sont connectés ou si le [[NetworkTrafficAnalysis|trafic]] est intense.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] au [[Hardware|matériel]] (placement dans un endroit sécurisé).
*   [[EnvironmentalControls|Contrôles environnementaux]] (température, humidité) pour garantir un fonctionnement fiable.
*   Sécurisation de l'[[WirelessRouterConfiguration|accès administratif]] avec des [[StrongPasswords|mots de passe forts]] et l'[[AccessControl|accès limité]] au réseau de gestion.

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[AccessPoint|Point d'Accès Sans Fil]]
*   [[DHCPServer|Serveur DHCP]]
*   [[Firewall|Pare-feu]]
*   [[NetworkAddressTranslation|Network Address Translation (NAT)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[IEEE80211|IEEE 802.11]]
*   [[Ethernet|Ethernet]]
*   [[SOHONetwork|Réseau SOHO]]
*   [[WirelessRouterConfiguration|Configuration de Routeur Sans Fil]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]] (Fonctionne principalement aux couches 1, 2 et 3)