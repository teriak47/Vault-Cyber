---
tags:
  - client-dhcp
  - processus-dora
  - dhcp-snooping
  - DHCPServer
  - NetworkConfiguration
  - AccessControl
aliases:
  - Client DHCP
  - DHCP Client
  - Dynamic Host Configuration Protocol Client
source:
  - null
cssclasses:
  - max
---

# Client DHCP

## 📥 Définition en une phrase
> Un [[DynamicHostConfigurationProtocolClient|client DHCP]] est un dispositif réseau (un [[Host|hôte]]) qui est configuré pour demander et recevoir automatiquement des informations de [[NetworkConfiguration|configuration réseau]] (comme une [[InternetProtocolAddress|adresse IP]]) d'un [[DHCPServer|serveur DHCP]].

## 🧠 Concepts Clés / Fonctionnement
*   **Requête Automatique**: Lorsqu'un [[Computer|ordinateur]] ou un autre [[NetworkDevice|périphérique réseau]] est configuré comme client DHCP, il envoie un message de découverte (DHCP Discover) lors de sa connexion au [[Network|réseau]].
*   **Processus DORA**: Le client initie la communication en quatre étapes clés pour obtenir une configuration IP :
    1.  **Discover**: Le client envoie une diffusion pour localiser les serveurs DHCP disponibles.
    2.  **Offer**: Les serveurs DHCP répondent avec des offres de configuration.
    3.  **Request**: Le client sélectionne une offre et envoie une requête pour l'accepter.
    4.  **Acknowledge**: Le serveur DHCP envoie un accusé de réception confirmant l'attribution de l'adresse IP et des autres paramètres.
*   **Informations Obtenues**: Le client reçoit une [[InternetProtocolAddress|adresse IP]], un [[SubnetMask|masque de sous-réseau]], l'[[DefaultGateway|adresse de la passerelle par défaut]], et les adresses des [[DomainNameSystem|serveurs DNS]].
*   **Renouvellement de Bail**: Les adresses IP sont louées pour une période définie. Le client DHCP tente de renouveler son bail avant son expiration pour conserver la même adresse IP.

## 🛡️ Risques / Menaces Associés
*   **[[RogueDHCPServer|Serveur DHCP malveillant]]**: Un serveur DHCP non autorisé peut fournir des informations de [[NetworkConfiguration|configuration réseau]] incorrectes ou malveillantes, redirigeant le trafic vers des [[ThreatActor|attaquants]] ou interrompant la [[NetworkCommunication|communication réseau]].
*   **[[DenialOfService|Déni de Service]] (DoS)**: Un [[ThreatActor|attaquant]] peut épuiser le pool d'[[InternetProtocolAddress|adresses IP]] du [[DHCPServer|serveur DHCP]], empêchant les nouveaux clients légitimes d'obtenir une configuration.
*   **[[ManInTheMiddle|Attaques Man-in-the-Middle]]**: En manipulant la [[NetworkConfiguration|configuration réseau]] via un [[RogueDHCPServer|serveur DHCP malveillant]], un attaquant peut intercepter et modifier le trafic du client.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSecurity|Sécurité Réseau]]** : Implémenter des fonctionnalités de [[Security|sécurité]] sur les [[NetworkSwitch|commutateurs réseau]], comme le DHCP Snooping, pour valider les messages DHCP et empêcher les [[RogueDHCPServer|serveurs DHCP malveillants]].
*   **[[AccessControl|Contrôle d'accès]]**: Restreindre l'accès physique au [[NetworkInfrastructure|réseau]] pour empêcher l'introduction de [[RogueDHCPServer|serveurs DHCP non autorisés]].
*   **[[SecurityPolicy|Politiques de sécurité]]**: Définir et appliquer des [[SecurityPolicy|politiques de sécurité]] strictes concernant la [[NetworkConfiguration|configuration réseau]] et la gestion des [[DHCPServer|serveurs DHCP]].
*   **Vérification des Logs**: Surveiller les [[Log|journaux]] du [[DHCPServer|serveur DHCP]] pour détecter toute activité suspecte ou des tentatives d'usurpation.

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[DHCPServer|Serveur DHCP]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkConfiguration|Configuration réseau]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]