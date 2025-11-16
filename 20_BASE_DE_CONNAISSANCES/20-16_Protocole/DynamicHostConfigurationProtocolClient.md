---
tags:
  - protocole
aliases:
  - Client DHCP
  - DHCP Client
  - Dynamic Host Configuration Protocol Client
  - Client du Protocole de Configuration d'Hôte Dynamique
archetype: protocole
rfc:
cssclasses:
  - max
---

# Client du Protocole de Configuration d'Hôte Dynamique (Client DHCP)

## 🎯 Rôle et Couche OSI
> Un [[DynamicHostConfigurationProtocolClient|client DHCP]] est un [[NetworkDevice|dispositif réseau]] (un [[Host|hôte]]) configuré pour demander et recevoir automatiquement des informations de [[NetworkConfiguration|configuration réseau]] d'un [[DHCPServer|serveur DHCP]]. Il joue un rôle essentiel dans la gestion dynamique des [[InternetProtocol|adresses IP]] et autres paramètres réseau pour les [[EndDevices|terminaux]], opérant au niveau de l'[[ApplicationLayer|couche Application]] du [[InternetProtocolSuite|modèle TCP/IP]] pour l'échange de messages, mais ayant un impact direct sur la [[NetworkLayer|couche Réseau]] pour la connectivité.

## ⚙️ Fonctionnement
Le [[DynamicHostConfigurationProtocolClient|client DHCP]] initie un processus en quatre étapes, souvent appelé DORA (Discover, Offer, Request, Acknowledge), pour obtenir et gérer sa [[NetworkConfiguration|configuration réseau]]:

1.  **Discover (Découverte)**: Lorsqu'un [[Computer|ordinateur]] ou un autre [[NetworkDevice|périphérique réseau]] est configuré comme client DHCP, il envoie un message de découverte (DHCP Discover) en [[Broadcast|diffusion]] pour localiser les [[DHCPServer|serveurs DHCP]] disponibles sur le [[NetworkSegment|segment réseau]].
2.  **Offer (Offre)**: Les [[DHCPServer|serveurs DHCP]] qui reçoivent la requête répondent avec des messages d'offre (DHCP Offer), proposant une [[InternetProtocol|adresse IP]] et d'autres paramètres de [[NetworkConfiguration|configuration réseau]] au client.
3.  **Request (Requête)**: Le client sélectionne l'une des offres reçues (généralement la première) et envoie un message de requête (DHCP Request) pour accepter l'[[InternetProtocol|adresse IP]] proposée et les autres paramètres. Ce message est également en [[Broadcast|diffusion]] pour informer les autres [[DHCPServer|serveurs DHCP]] de son choix.
4.  **Acknowledge (Accusé de réception)**: Le [[DHCPServer|serveur DHCP]] choisi envoie un message d'accusé de réception (DHCP Acknowledge ou DHCP ACK) confirmant l'attribution de l'[[InternetProtocol|adresse IP]] et des autres paramètres (comme le [[SubnetMask|masque de sous-réseau]], l'[[DefaultGateway|adresse de la passerelle par défaut]], et les adresses des [[DomainNameSystem|serveurs DNS]]).

*   **Informations Obtenues**: Outre l'[[InternetProtocol|adresse IP]], le client reçoit le [[SubnetMask|masque de sous-réseau]], l'[[DefaultGateway|adresse de la passerelle par défaut]], les adresses des [[DomainNameSystem|serveurs DNS]], et la durée du bail (lease time).
*   **Renouvellement de Bail**: Les [[InternetProtocol|adresses IP]] attribuées sont louées pour une période définie (le bail). Le client DHCP tente de renouveler son bail auprès du [[DHCPServer|serveur DHCP]] avant son expiration pour conserver la même [[InternetProtocol|adresse IP]] et assurer une [[BusinessContinuity|continuité]] de la [[NetworkCommunication|communication]].
*   **Ports par défaut**: Le [[DynamicHostConfigurationProtocolClient|client DHCP]] envoie des requêtes depuis le port [[UserDatagramProtocol|UDP]]/68 vers le port [[UserDatagramProtocol|UDP]]/67 du [[DHCPServer|serveur DHCP]] et écoute les réponses sur le port [[UserDatagramProtocol|UDP]]/68.

## 🛡️ Sécurité du Protocole
L'interaction entre un [[DynamicHostConfigurationProtocolClient|client DHCP]] et un [[DHCPServer|serveur DHCP]] peut être la cible de diverses [[Vulnerability|vulnérabilités]] et [[Attack|attaques]]:

*   **[[RogueDHCPServer|Serveur DHCP malveillant]]**: Un [[ThreatActor|attaquant]] peut déployer un [[RogueDHCPServer|serveur DHCP non autorisé]] pour fournir aux clients des informations de [[NetworkConfiguration|configuration réseau]] incorrectes ou malveillantes. Cela peut entraîner une [[ServiceDisruption|interruption de service]], une [[DataExfiltration|exfiltration de données]] ou des [[ManInTheMiddle|attaques de l'homme du milieu]] en redirigeant le trafic vers des serveurs contrôlés par l'attaquant.
*   **[[DenialOfService|Déni de Service]] (DoS)**: Un [[ThreatActor|attaquant]] peut inonder le [[DHCPServer|serveur DHCP]] de requêtes d'[[InternetProtocol|adresses IP]] légitimes ou falsifiées, épuisant ainsi son pool d'[[InternetProtocol|adresses IP]] disponibles. Cela empêche les nouveaux clients légitimes d'obtenir une configuration et de se connecter au [[Network|réseau]].
*   **[[ManInTheMiddle|Attaques Man-in-the-Middle]]**: En manipulant la [[NetworkConfiguration|configuration réseau]] via un [[RogueDHCPServer|serveur DHCP malveillant]], un [[ThreatActor|attaquant]] peut se positionner entre le client et le reste du [[Network|réseau]], interceptant et modifiant le trafic échangé.

**Mesures de Protection:**
*   **[[PortSecurity|Sécurité des Ports]] et DHCP Snooping**: Implémenter des fonctionnalités de [[NetworkSecurity|sécurité réseau]] sur les [[NetworkSwitch|commutateurs réseau]], comme le DHCP Snooping, qui permettent de valider les messages DHCP et d'empêcher les [[RogueDHCPServer|serveurs DHCP malveillants]] d'opérer sur le [[Network|réseau]].
*   **[[AccessControl|Contrôle d'accès]] Physique**: Restreindre l'accès physique à l'[[NetworkInfrastructure|infrastructure réseau]] pour empêcher l'introduction de [[RogueDHCPServer|serveurs DHCP non autorisés]].
*   **[[SecurityPolicy|Politiques de sécurité]] Strictes**: Définir et appliquer des [[SecurityPolicy|politiques de sécurité]] claires concernant la [[NetworkConfiguration|configuration réseau]] et la gestion des [[DHCPServer|serveurs DHCP]].
*   **[[NetworkMonitoring|Surveillance réseau]] et Vérification des [[Log|Logs]]**: Surveiller activement les [[Log|journaux]] du [[DHCPServer|serveur DHCP]] et le [[NetworkTrafficAnalysis|trafic réseau]] pour détecter toute activité suspecte, comme des attributions d'[[InternetProtocol|adresses IP]] inhabituelles ou la présence de [[RogueDHCPServer|serveurs DHCP malveillants]].

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[DHCPServer|Serveur DHCP]]
*   [[InternetProtocol|Adresse IP]]
*   [[NetworkConfiguration|Configuration réseau]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[Wireshark|Wireshark]]