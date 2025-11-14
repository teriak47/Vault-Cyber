---
tags:
  - adresse-ip-dynamique
  - snooping-dhcp
  - segmentation-lan
  - MACSpoofing
  - RogueDHCPServer
  - NetworkSegmentation
aliases:
  - Adresse Réseau
  - Network Address
source:
  - null
cssclasses:
  - max
---

# Adresse Réseau

## 📥 Définition en une phrase
> Une adresse réseau est un identifiant unique attribué à chaque dispositif (hôte ou interface réseau) connecté à un [[Network|réseau informatique]] pour permettre sa localisation et sa communication au sein de ce [[Network|réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   **Identification Unique**: Chaque [[NetworkDevice|périphérique réseau]] sur un [[Network|réseau]] possède une [[NetworkAddress|adresse réseau]] qui le distingue des autres.
*   **Types d'Adresses**: Il existe principalement deux types d'[[NetworkAddress|adresses réseau]] utilisées pour la [[NetworkCommunication|communication réseau]]:
    *   Les [[MediaAccessControlAddress|adresses MAC]] (Media Access Control) qui opèrent au niveau de la [[DataLinkLayer|couche liaison de données]] ([[OpenSystemsInterconnectionModel|couche 2 du modèle OSI]]). Elles sont physiques et gravées sur la [[NetworkInterfaceCard|carte d'interface réseau]] ([[Hardware|matériel]]).
    *   Les [[InternetProtocolAddress|adresses IP]] (Internet Protocol) qui opèrent au niveau de la [[NetworkLayer|couche réseau]] ([[OpenSystemsInterconnectionModel|couche 3 du modèle OSI]]). Elles sont logiques et peuvent être configurées de manière [[StaticConfiguration|statique]] ou [[DynamicHostConfigurationProtocol|dynamique]] ([[DynamicHostConfigurationProtocol|DHCP]]).
*   **Routage**: Les [[Router|routeurs]] utilisent les [[InternetProtocolAddress|adresses IP]] pour acheminer les [[Packet|paquets]] de [[Data|données]] entre différents [[Network|réseaux]] ou [[NetworkSegment|segments réseau]].
*   **Communication Locale**: Les [[NetworkSwitch|commutateurs réseau]] utilisent les [[MediaAccessControlAddress|adresses MAC]] pour diriger les [[EthernetFrame|trames Ethernet]] vers le [[EndDevices|dispositif terminal]] approprié au sein d'un même [[LocalAreaNetwork|LAN]].

## 🛡️ Risques / Menaces Associés
*   [[MACSpoofing|Usurpation d'adresse MAC]] : Un [[ThreatActor|attaquant]] peut modifier son [[MediaAccessControlAddress|adresse MAC]] pour se faire passer pour un autre [[NetworkDevice|dispositif]] légitime, potentiellement contourner les [[AccessControl|contrôles d'accès]] comme le [[MacAddressFiltering|filtrage MAC]].
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]] : L'[[ThreatActor|attaquant]] envoie de fausses réponses [[AddressResolutionProtocol|ARP]] pour associer son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocolAddress|adresse IP]] d'une [[Gateway|passerelle]] ou d'un autre [[Host|hôte]], permettant une [[ManInTheMiddle|attaque de l'homme du milieu]].
*   [[RogueDHCPServer|Serveur DHCP malveillant]] : Un [[ThreatActor|serveur DHCP non autorisé]] distribue de fausses [[InternetProtocolAddress|adresses IP]] et informations de [[Gateway|passerelle]], redirigeant le [[NetworkTrafficAnalysis|trafic réseau]] vers des points contrôlés par l'[[ThreatActor|attaquant]].
*   [[UnauthorizedAccess|Accès Non Autorisé]] : Une mauvaise [[NetworkConfiguration|configuration réseau]] ou une vulnérabilité permet à un [[ThreatActor|attaquant]] d'accéder à des [[NetworkSegment|segments réseau]] ou des [[Host|hôtes]] qui devraient être inaccessibles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[PortSecurity|Sécurité des Ports]]**: Utiliser les fonctionnalités de [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] pour limiter le nombre de [[MediaAccessControlAddress|adresses MAC]] autorisées par port ou pour lier des [[MediaAccessControlAddress|adresses MAC]] spécifiques à des ports.
*   **[[DynamicHostConfigurationProtocol|DHCP]] Snooping**: Mettre en œuvre le DHCP Snooping sur les [[NetworkSwitch|commutateurs]] pour valider les messages [[DynamicHostConfigurationProtocol|DHCP]] et empêcher les [[RogueDHCPServer|serveurs DHCP malveillants]].
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Diviser le [[CorporateNetwork|réseau d'entreprise]] en [[VirtualLocalAreaNetwork|VLAN]] pour isoler les différents types de [[Data|données]] et de [[User Account|comptes]], limitant ainsi la portée d'une [[SystemCompromise|compromission]].
*   **[[AccessControl|Contrôle d'Accès]]**: Implémenter des politiques de [[AccessControl|contrôle d'accès]] robustes (ex: [[RoleBasedAccessControl|RBAC]]) pour s'assurer que seuls les [[Account|comptes]] et [[System|systèmes]] autorisés peuvent communiquer avec certaines [[NetworkAddress|adresses réseau]].
*   **[[NetworkMonitoring|Surveillance Réseau]]**: Déployer des outils de [[NetworkMonitoring|surveillance réseau]] pour détecter les activités suspectes, telles que les [[MACSpoofing|tentatives d'usurpation d'adresse MAC]] ou les [[AddressResolutionProtocolPoisoning|attaques ARP]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[SpoofingAttack|Attaque d'Usurpation]]