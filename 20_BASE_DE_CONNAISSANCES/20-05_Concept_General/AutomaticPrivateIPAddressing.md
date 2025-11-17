---
tags:
aliases:
  - APIPA
  - Automatic Private IP Addressing
  - Adressage IP Privé Automatique
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage IP Privé Automatique (APIPA)

## 📥 Définition en une phrase
> L'[[AutomaticPrivateIPAddressing|APIPA]] est une fonctionnalité des [[OperatingSystem|systèmes d'exploitation]] qui permet à un [[Host|hôte]] de s'auto-attribuer une [[InternetProtocol|adresse IP]] dans une plage spécifique lorsqu'il ne peut pas contacter de [[DynamicHostConfigurationProtocol|serveur DHCP]].

## 🧠 Concepts Clés / Piliers
*   **Plage et [[SubnetMask|Masque]] Standard**: L'[[AutomaticPrivateIPAddressing|APIPA]] attribue aux [[Computer|ordinateurs]] une [[InternetProtocol|adresse IP]] dans la plage **169.254.0.1 à 169.254.255.254**, avec un [[SubnetMask|masque de sous-réseau]] fixe de **255.255.0.0**.
*   **Mécanisme de Déclenchement**: Cette fonctionnalité s'active automatiquement lorsqu'un [[NetworkDevice|périphérique réseau]], configuré pour obtenir son [[InternetProtocol|adresse IP]] via [[DynamicHostConfigurationProtocol|DHCP]], ne parvient pas à recevoir de réponse d'un [[DHCPServer|serveur DHCP]] après plusieurs tentatives.
*   **Vérification des Conflits**: Avant d'utiliser une [[InternetProtocol|adresse IP]] générée, l'[[Host|hôte]] effectue une vérification de sa disponibilité sur le [[LocalAreaNetwork|réseau local]] à l'aide du [[AddressResolutionProtocol|Protocole de Résolution d'Adresse (ARP)]].
*   **Portée de la [[NetworkCommunication|Communication]]**: Les [[Host|hôtes]] utilisant des [[AutomaticPrivateIPAddressing|adresses APIPA]] peuvent communiquer entre eux sur le même [[NetworkSegment|segment]] de [[LocalAreaNetwork|réseau]]. Cependant, ils ne peuvent pas accéder à d'autres [[RemoteNetwork|réseaux]] ou à l'[[Internet|Internet]] sans la présence d'un [[Router|routeur]] ou d'une [[Gateway|passerelle]] configurée avec une [[InternetProtocol|adresse IP]] routable.

## 💡 Importance en Cybersécurité
> Bien que l'[[AutomaticPrivateIPAddressing|APIPA]] soit conçue pour assurer une connectivité de base en l'absence de [[DynamicHostConfigurationProtocol|DHCP]], elle présente des implications significatives en [[Cybersecurity|cybersécurité]]. Elle peut masquer une [[ServiceDisruption|interruption de service]] du [[DHCPServer|serveur DHCP]], rendant l'identification des problèmes de [[NetworkConfiguration|configuration réseau]] plus difficile. Les [[Host|hôtes]] avec des [[AutomaticPrivateIPAddressing|adresses APIPA]] ont une connectivité limitée, ce qui peut entraîner des problèmes de [[NetworkCommunication|communication réseau]] et une [[InadvertentExposure|exposition involontaire]] si des données sont censées être transmises à des [[RemoteNetwork|réseaux]] externes. De plus, un [[ThreatActor|acteur de menace]] pourrait potentiellement exploiter cette dépendance en déployant un [[RogueDHCPServer|serveur DHCP malveillant]] pour attribuer des [[InternetProtocol|adresses IP]] contrôlées, augmentant ainsi la [[AttackSurface|surface d'attaque]]. Pour atténuer ces risques, une [[NetworkMonitoring|surveillance réseau]] rigoureuse du [[DynamicHostConfigurationProtocol|DHCP]], une [[NetworkSegmentation|segmentation réseau]] (par exemple, via des [[VirtualLocalAreaNetwork|VLAN]]) et des [[SecurityAudit|audits de sécurité]] réguliers sont essentiels, complétés par une [[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|sensibilisation des utilisateurs]] et des administrateurs.

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[InternetProtocol|Adresse IP]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkConfiguration|Configuration Réseau]]
*   [[SubnetMask|Masque de Sous-réseau]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresse (ARP)]]
*   [[DHCPServer|Serveur DHCP]]
*   [[RogueDHCPServer|Serveur DHCP malveillant]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[NetworkSegmentation|Segmentation Réseau]]
---