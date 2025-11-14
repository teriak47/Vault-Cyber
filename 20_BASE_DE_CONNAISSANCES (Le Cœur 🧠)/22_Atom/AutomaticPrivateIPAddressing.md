---
tags:
  - automatic-private-ip-addressing
  - apipa
  - dhcp-failure-detection
  - DHCPServer
  - NetworkMonitoring
  - NetworkSegmentation
aliases:
  - APIPA
  - Automatic Private IP Addressing
  - Adressage IP Privé Automatique
cssclasses:
  - max
---

# Adressage IP Privé Automatique (APIPA)

## 📥 Définition en une phrase
> L'[[AutomaticPrivateIPAddressing|APIPA]] est une fonctionnalité des [[OperatingSystem|systèmes d'exploitation]] qui permet à un [[Host|hôte]] de s'auto-attribuer une [[InternetProtocolAddress|adresse IP]] dans une plage spécifique lorsqu'il ne peut pas contacter de [[DynamicHostConfigurationProtocol|serveur DHCP]].

## 🧠 Concepts Clés / Fonctionnement
*   **Plage d'[[InternetProtocolAddress|Adresses IP]] :** Les [[Computer|ordinateurs]] utilisant l'[[AutomaticPrivateIPAddressing|APIPA]] s'attribuent une [[InternetProtocolAddress|adresse IP]] dans la plage **169.254.0.1 à 169.254.255.254**.
*   **[[SubnetMask|Masque de sous-réseau]] :** Le [[SubnetMask|masque de sous-réseau]] associé est toujours **255.255.0.0**.
*   **Absence de [[DynamicHostConfigurationProtocol|DHCP]] :** L'[[AutomaticPrivateIPAddressing|APIPA]] est activé automatiquement quand un [[NetworkDevice|périphérique réseau]] configuré pour obtenir une [[InternetProtocolAddress|adresse IP]] via [[DynamicHostConfigurationProtocol|DHCP]] ne reçoit pas de réponse d'un [[DHCPServer|serveur DHCP]].
*   **Vérification de l'[[InternetProtocolAddress|Adresse]] :** Avant d'attribuer une [[InternetProtocolAddress|adresse IP]], l'[[Host|hôte]] utilise le [[AddressResolutionProtocol|Protocole de Résolution d'Adresse (ARP)]] pour s'assurer que l'[[InternetProtocolAddress|adresse]] n'est pas déjà utilisée sur le [[LocalAreaNetwork|réseau local]].
*   **Communication Locale :** Les [[Host|hôtes]] configurés avec des [[AutomaticPrivateIPAddressing|adresses APIPA]] peuvent communiquer entre eux sur un même [[NetworkSegment|segment]] de [[LocalAreaNetwork|réseau]], mais ne peuvent pas accéder à d'autres [[RemoteNetwork|réseaux]] ou à l'[[Internet|Internet]] sans un [[Router|routeur]] ou un [[Gateway|serveur de passerelle]] configuré avec une [[InternetProtocolAddress|adresse IP]] routable.

## 🛡️ Risques / Menaces Associés
*   **[[ServiceDisruption|Interruption de Service]] Masquée :** L'[[AutomaticPrivateIPAddressing|APIPA]] peut masquer un échec du [[DHCPServer|serveur DHCP]], rendant difficile l'identification des problèmes de [[NetworkConfiguration|configuration réseau]] sous-jacents.
*   **Problèmes de Connectivité :** Les [[Host|hôtes]] utilisant des [[AutomaticPrivateIPAddressing|adresses APIPA]] ne peuvent pas communiquer en dehors de leur [[LocalAreaNetwork|LAN]] immédiat, ce qui peut entraîner des problèmes de [[NetworkCommunication|communication réseau]] inattendus.
*   **[[AttackSurface|Surface d'Attaque]] :** Un [[ThreatActor|attaquant]] pourrait potentiellement exploiter la dépendance à l'[[DynamicHostConfigurationProtocol|APIPA]] en déployant un [[RogueDHCPServer|serveur DHCP malveillant]] pour attribuer des [[InternetProtocolAddress|adresses IP]] contrôlées.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Surveillance du [[DynamicHostConfigurationProtocol|DHCP]] :** Mettre en place une [[NetworkMonitoring|surveillance réseau]] rigoureuse pour s'assurer que les [[DHCPServer|serveurs DHCP]] sont toujours opérationnels et répondent correctement.
*   **[[NetworkSegmentation|Segmentation Réseau]] :** Utiliser la [[NetworkSegmentation|segmentation réseau]] (par exemple, des [[VirtualLocalAreaNetwork|VLAN]]) pour limiter la portée des communications des [[AutomaticPrivateIPAddressing|adresses APIPA]] et isoler les problèmes potentiels.
*   **[[SecurityAudit|Audits de Sécurité]] Réguliers :** Effectuer des [[SecurityAudit|audits de sécurité]] pour identifier les [[SecurityVulnerabilities|vulnérabilités de sécurité]] liées à une dépendance excessive ou non gérée à l'[[AutomaticPrivateIPAddressing|APIPA]].
*   **Sensibilisation :** [[UserAwarenessTraining|Sensibiliser les utilisateurs]] et les administrateurs aux implications de l'[[AutomaticPrivateIPAddressing|APIPA]] et à la nécessité d'une [[NetworkConfiguration|configuration réseau]] appropriée.

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkConfiguration|Configuration Réseau]]
*   [[SubnetMask|Masque de Sous-réseau]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresse (ARP)]]
*   [[DHCPServer|Serveur DHCP]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[RogueDHCPServer|Serveur DHCP malveillant]]
---