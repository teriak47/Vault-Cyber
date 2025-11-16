---
tags:
  - concept/general
  - reseau
  - reseau/virtuel
  - reseau/segmentation
aliases:
  - Réseau Local Virtuel
  - VLAN
  - Virtual Local Area Network
  - Réseaux Locaux Virtuels
  - Virtual LAN
archetype: concept-general
source:
cssclasses:
  - max
---

# Réseau Local Virtuel (VLAN)

## 📥 Définition en une phrase
> Un [[VirtualLocalAreaNetwork|VLAN]] est une méthode de [[NetworkSegmentation|segmentation réseau]] logique qui permet de diviser un [[LocalAreaNetwork|LAN]] physique en plusieurs réseaux virtuels distincts, isolant le trafic entre eux.

## 🧠 Concepts Clés / Piliers
*   **[[NetworkSegmentation|Segmentation Logique]]**: Un [[VirtualLocalAreaNetwork|VLAN]] opère au niveau de la [[DataLinkLayer|couche liaison de données]] (couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]), permettant de regrouper des [[Host|hôtes]] sans tenir compte de leur localisation physique sur un [[NetworkSwitch|commutateur réseau]]. Cela crée des [[NetworkSegment|segments réseau]] logiques distincts.
*   **[[Isolation|Isolation de Trafic]]**: Chaque [[VirtualLocalAreaNetwork|VLAN]] est un [[BroadcastDomain|domaine de diffusion]] indépendant. Le trafic au sein d'un [[VirtualLocalAreaNetwork|VLAN]] n'est pas vu par les autres [[VirtualLocalAreaNetwork|VLANs]]. Pour que deux [[VirtualLocalAreaNetwork|VLANs]] puissent communiquer, le trafic doit être acheminé via un [[Router|routeur]] ou un [[Layer3Switch|commutateur de couche 3]].
*   **Flexibilité et Gestion**: Les [[VirtualLocalAreaNetwork|VLANs]] offrent une grande flexibilité en matière de [[NetworkConfiguration|configuration réseau]]. Ils permettent de déplacer facilement des [[User|utilisateurs]] ou des [[Resource|ressources]] d'un [[NetworkSegment|segment réseau]] à un autre sans nécessiter de recâblage physique, simplifiant ainsi l'[[NetworkManagement|gestion réseau]].
*   **[[PortSecurity|Sécurité des Ports]]**: Les [[NetworkSwitch|commutateurs réseau]] peuvent être configurés pour assigner des [[EthernetPorts|ports Ethernet]] spécifiques à des [[VirtualLocalAreaNetwork|VLANs]] donnés, empêchant ainsi l'[[UnauthorizedAccess|accès non autorisé]] à certains segments réseau, même si l'appareil est physiquement connecté.

## 💡 Importance en Cybersécurité
> Les [[VirtualLocalAreaNetwork|VLANs]] sont un composant essentiel de la [[NetworkSecurity|sécurité réseau]] moderne. Ils permettent de contenir la portée d'une [[Attack|attaque]] en isolant les [[System|systèmes]] critiques ou sensibles dans des segments distincts, ce qui réduit considérablement la [[AttackSurface|surface d'attaque]] et limite le [[LateralMovement|mouvement latéral]] des [[ThreatActor|attaquants]]. En séparant les [[Data|données]] et les [[Application|applications]] par fonction, département ou niveau de [[Security|sécurité]], les [[VirtualLocalAreaNetwork|VLANs]] facilitent l'implémentation du [[PrincipleOfLeastPrivilege|principe du moindre privilège]] et des [[AccessControl|contrôles d'accès]] granulaires. Ils jouent un rôle clé dans une stratégie de [[DefenseInDepth|défense en profondeur]], en ajoutant une couche d'[[Isolation|isolation]] logique qui complète les [[PhysicalSecurity|mesures de sécurité physique]].

## 🔗 Notes Connexes
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[SecurityPolicy|Politique de Sécurité]]
*   [[Ethernet|Ethernet]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La note pourrait bénéficier d'exemples concrets de scénarios d'utilisation des [[VirtualLocalAreaNetwork|VLANs]] pour des cas spécifiques de [[Security|sécurité]] (ex: [[GuestAccess|réseau invité]], [[IoTSecurity|IoT]], serveurs critiques).
*   Des détails techniques supplémentaires sur les modes de [[VirtualLocalAreaNetwork|VLAN]] (port-based, MAC-based, protocol-based) et le [[VirtualLocalAreaNetwork|VLAN tagging]] (ex: [[IEEE8021Q|802.1Q]]) pourraient enrichir la compréhension.
*   Aborder les [[SecurityVulnerabilities|vulnérabilités de sécurité]] spécifiques aux [[VirtualLocalAreaNetwork|VLANs]] (ex: [[VLAN Hopping]], double tagging) et les contremesures associées.