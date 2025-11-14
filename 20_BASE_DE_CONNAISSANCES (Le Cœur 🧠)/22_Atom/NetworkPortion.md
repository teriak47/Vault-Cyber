---
tags:
  - network-portion
  - subnet-mask-usage
  - ip-address-partition
  - NetworkSegmentation
  - VirtualLocalAreaNetwork
  - DHCPServer
aliases:
  - Partie réseau
  - Network Portion
source:
  - null
cssclasses:
  - max
---

# Partie Réseau

## 📥 Définition en une phrase
> La partie [[Network|réseau]] d'une [[InternetProtocolAddress|adresse IP]] est la section de l'[[InternetProtocolAddress|adresse]] qui identifie le [[Network|réseau]] spécifique auquel un [[Host|hôte]] est connecté, et elle est déterminée par l'application du [[SubnetMask|masque de sous-réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   **Identification du [[Network|réseau]]**: Elle permet aux [[Router|routeurs]] de diriger les [[Packet|paquets]] de [[DataTransmission|données]] vers le [[Network|réseau]] de destination correct.
*   **Détermination par le [[SubnetMask|masque de sous-réseau]]**: Le [[SubnetMask|masque de sous-réseau]] est un nombre binaire qui "masque" la partie [[HostPortion|hôte]] de l'[[InternetProtocolAddress|adresse IP]], laissant apparaître la partie [[NetworkPortion|réseau]].
*   **Contraste avec la [[HostPortion|partie hôte]]**: Alors que la partie [[NetworkPortion|réseau]] désigne le [[Network|réseau]], la [[HostPortion|partie hôte]] identifie un [[Host|hôte]] unique au sein de ce [[Network|réseau]] spécifique.
*   **Fondement de l'[[IPAddressing|adressage IP]]**: Elle est essentielle pour l'[[IPAddressing|adressage IP]] et le [[RoutingTable|routage]] efficace des [[Packet|paquets]] à travers les [[InterconnectedNetworks|réseaux interconnectés]].

## 🛡️ Risques / Menaces Associés
*   [[UnauthorizedAccess|Accès Non Autorisé]]: Une [[NetworkConfiguration|configuration réseau]] ou une [[NetworkSegmentation|segmentation réseau]] incorrecte de la partie [[NetworkPortion|réseau]] peut involontairement exposer des [[System|systèmes]] ou des [[Data|données]] sensibles à des [[UnauthorizedAccess|accès non autorisés]].
*   [[SpoofingAttack|Usurpation d'adresse IP]]: Des [[ThreatActor|acteurs de menace]] peuvent tenter d'usurper des [[InternetProtocolAddress|adresses IP]] légitimes appartenant à une partie [[NetworkPortion|réseau]] spécifique pour contourner les [[SecurityControl|contrôles de sécurité]] ou masquer leur [[Identification|identité]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation Réseau]]: Utiliser la partie [[NetworkPortion|réseau]] pour implémenter une [[NetworkSegmentation|segmentation réseau]] stricte via des [[VirtualLocalAreaNetwork|VLAN]] et des [[Firewall|pare-feu]], ce qui aide à isoler les [[Network|réseaux]] et à contenir les [[Attack|attaques]].
*   [[NetworkConfiguration|Configuration]] et [[IPAddressing|Adressage IP]] Sécurisés: Assurer une [[StaticConfiguration|configuration statique]] ou [[DynamicHostConfigurationProtocol|DHCP]] sécurisée pour toutes les [[InternetProtocolAddress|adresses IP]] et [[SubnetMask|masques de sous-réseau]], en particulier en protégeant les [[DHCPServer|serveurs DHCP]] contre les [[RogueDHCPServer|serveurs DHCP malveillants]].
*   [[AccessControl|Contrôle d'accès]] granulaire: Mettre en œuvre des [[AccessControl|contrôles d'accès]] basés sur la partie [[NetworkPortion|réseau]] (par exemple, à l'aide de listes de contrôle d'accès sur les [[Router|routeurs]] et les [[NetworkSwitch|commutateurs]]) pour restreindre l'accès à des sous-réseaux spécifiques.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[IPAddressing|Adressage IP]]
*   [[HostPortion|Partie Hôte]]
*   [[NetworkSegmentation|Segmentation Réseau]]