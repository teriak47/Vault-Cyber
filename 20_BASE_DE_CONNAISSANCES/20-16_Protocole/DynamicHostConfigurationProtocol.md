---
tags:
  - protocole
aliases:
  - Protocole de Configuration d'Hôte Dynamique
  - DHCP
  - Dynamic Host Configuration Protocol
archetype: protocole
rfc: RFC 2131
cssclasses:
  - max
---

# Protocole de Configuration d'Hôte Dynamique (DHCP)

## 🎯 Rôle et Couche OSI
> Le [[DynamicHostConfigurationProtocol|DHCP]] est un [[NetworkProtocol|protocole réseau]] qui permet à un [[DHCPServer|serveur DHCP]] de distribuer automatiquement des [[InternetProtocol|adresses IP]] et d'autres paramètres de [[NetworkConfiguration|configuration réseau]] (comme le [[SubnetMask|masque de sous-réseau]], la [[DefaultGateway|passerelle par défaut]] et les [[DomainNameSystem|serveurs DNS]]) aux [[DynamicHostConfigurationProtocolClient|clients DHCP]] sur un [[Network|réseau]] [[InternetProtocol|IP]]. Il opère principalement à la [[ApplicationLayer|couche Application]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
Le [[DynamicHostConfigurationProtocol|DHCP]] utilise un processus en quatre étapes, souvent désigné par l'acronyme DORA :
1.  **Découverte (Discovery)** : Un [[DynamicHostConfigurationProtocolClient|client DHCP]] non configuré envoie un paquet de [[Broadcast|diffusion]] (`DHCPDISCOVER`) sur le [[NetworkSegment|segment réseau]] local pour localiser les [[DHCPServer|serveurs DHCP]] disponibles. Ce paquet utilise l'[[UserDatagramProtocol|UDP]] sur le port 68.
2.  **Offre (Offer)** : Un ou plusieurs [[DHCPServer|serveurs DHCP]] reçoivent le message de découverte et répondent avec un paquet d'offre (`DHCPOFFER`), contenant une [[InternetProtocol|adresse IP]] proposée, un [[Lease|bail]], un [[SubnetMask|masque de sous-réseau]], et l'[[DefaultGateway|adresse de la passerelle par défaut]]. Ce paquet est envoyé en [[Unicast|unidiffusion]] ou [[Broadcast|diffusion]] sur le port 67.
3.  **Requête (Request)** : Le [[DynamicHostConfigurationProtocolClient|client DHCP]] reçoit les offres et sélectionne généralement la première offre reçue. Il envoie ensuite un paquet de requête (`DHCPREQUEST`) en [[Broadcast|diffusion]] pour accepter l'offre spécifique et informer les autres [[DHCPServer|serveurs DHCP]] que leur offre n'a pas été retenue.
4.  **Accusé de Réception (Acknowledgement)** : Le [[DHCPServer|serveur DHCP]] sélectionné confirme l'attribution de l'[[InternetProtocol|adresse IP]] et des paramètres via un paquet d'[[Acknowledgement|accusé de réception]] (`DHCPACK`). Ce message est envoyé en [[Unicast|unidiffusion]] ou [[Broadcast|diffusion]] et marque la fin du processus d'attribution.

*   **Ports par défaut**: Le [[DynamicHostConfigurationProtocol|DHCP]] utilise les ports [[UserDatagramProtocol|UDP]] :
    *   **UDP/67** pour les [[DHCPServer|serveurs DHCP]].
    *   **UDP/68** pour les [[DynamicHostConfigurationProtocolClient|clients DHCP]].
*   **Concepts clés**:
    *   **[[Lease|Bail]]** : Durée pendant laquelle une [[InternetProtocol|adresse IP]] est attribuée à un [[DynamicHostConfigurationProtocolClient|client]]. Le client doit renouveler son bail avant son expiration.
    *   **Pool d'adresses** : Plage d'[[InternetProtocol|adresses IP]] configurée sur le [[DHCPServer|serveur DHCP]] et disponible pour la distribution.
    *   **Options DHCP** : Paramètres [[NetworkConfiguration|réseau]] supplémentaires qui peuvent être distribués, tels que les [[DomainNameSystem|serveurs DNS]], les serveurs WINS, le nom de [[DomainNameSystem|domaine]], etc.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[DhcpStarvation|DHCP starvation]] : Une [[ThreatActor|acteur de menace]] envoie un grand nombre de requêtes [[DynamicHostConfigurationProtocol|DHCP]] pour épuiser le pool d'[[InternetProtocol|adresses IP]] disponibles, empêchant les [[DynamicHostConfigurationProtocolClient|clients légitimes]] d'obtenir une adresse et provoquant un [[DenialOfService|déni de service]].
    *   [[DhcpSpoofing|DHCP spoofing]] : Une [[ThreatActor|acteur de menace]] déploie un [[RogueDHCPServer|serveur DHCP malveillant]] sur le [[Network|réseau]]. Ce [[RogueDHCPServer|serveur]] distribue de fausses [[NetworkConfiguration|configurations IP]] (par exemple, une [[DefaultGateway|passerelle par défaut]] ou des [[DomainNameSystem|serveurs DNS]] frauduleux), redirigeant le [[NetworkTrafficAnalysis|trafic client]] vers l'[[ManInTheMiddle|attaquant]] pour l'[[Eavesdropping|interception]] ou l'[[DataTheft|exfiltration de données]].
    *   Divulgation d'informations : Un [[DHCPServer|serveur DHCP]] mal configuré peut involontairement révéler des informations sensibles sur la [[NetworkConfiguration|structure du réseau]] aux [[ThreatActor|attaquants]] lors de la [[Reconnaissance|phase de reconnaissance]].
*   **Mesures de protection**:
    *   [[DhcpSnooping|DHCP Snooping]] : Une [[SecurityControl|fonctionnalité de sécurité]] implémentée sur les [[NetworkSwitch|commutateurs réseau]] qui valide les messages [[DynamicHostConfigurationProtocol|DHCP]] et bloque ceux provenant de [[RogueDHCPServer|serveurs DHCP malveillants]]. Elle aide à prévenir les attaques de [[DhcpSpoofing|DHCP spoofing]] et [[DhcpStarvation|starvation]].
    *   [[NetworkSegmentation|Segmentation réseau]] : L'utilisation de [[VirtualLocalAreaNetwork|VLAN]] pour isoler différents segments du [[Network|réseau]] peut limiter la portée et l'impact des [[Attack|attaques DHCP]].
    *   [[PhysicalSecurity|Sécurité physique]] : Protéger l'accès physique aux [[DHCPServer|serveurs DHCP]] et aux [[NetworkDevice|équipements réseau]] pour empêcher l'installation de [[RogueDHCPServer|serveurs DHCP malveillants]].
    *   [[AccessControl|Contrôle d'accès]] basé sur les ports (ex: [[IEEE8021x|IEEE 802.1X]]) : Authentifie les [[EndDevices|terminaux]] avant de leur accorder l'accès au [[Network|réseau]], rendant plus difficile pour les [[ThreatActor|attaquants]] d'introduire des [[RogueDHCPServer|serveurs DHCP malveillants]].
    *   [[StaticConfiguration|Configuration statique]] pour les [[Server|serveurs]] critiques : Attribuer manuellement des [[StaticIPAddressing|adresses IP statiques]] aux [[Server|serveurs]] critiques et aux [[NetworkDevice|équipements réseau]] plutôt que de dépendre de [[DynamicHostConfigurationProtocol|DHCP]].

## 🔗 Notes Connexes
*   [[IPAddressing|Adressage IP]]
*   [[NetworkProtocol|Protocoles Réseau]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[DHCPServer|Serveur DHCP]]
*   [[DynamicHostConfigurationProtocolClient|Client DHCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[Broadcast|Diffusion]]
*   [[StaticIPAddressing|Adressage IP Statique]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[SecurityVulnerabilities|Vulnérabilités de sécurité]]