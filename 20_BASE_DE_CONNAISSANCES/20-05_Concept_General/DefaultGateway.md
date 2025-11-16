---
tags:
  - concept
aliases:
  - Default Gateway
  - passerelle par défaut
  - default gateway
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Passerelle par Défaut

## 📥 Définition en une phrase
> La [[DefaultGateway|passerelle par défaut]] est le [[Router|routeur]] sur un [[LocalAreaNetwork|réseau local]] qui sert de point de sortie pour le [[NetworkTrafficAnalysis|trafic]] destiné à des [[RemoteNetwork|réseaux distants]], tels que l'[[Internet]].

## 🧠 Concepts Clés / Piliers
*   **Point de Sortie**: Chaque [[Host|hôte]] sur un [[LocalAreaNetwork|LAN]] doit connaître l'[[InternetProtocol|adresse IP]] de sa [[DefaultGateway|passerelle par défaut]] pour envoyer des [[Packet|paquets]] en dehors de son [[NetworkSegment|segment réseau]] local.
*   **[[Routing|Routage]]**: Lorsqu'un [[Computer|ordinateur]] doit communiquer avec un appareil qui n'est pas sur son [[LocalAreaNetwork|réseau local]], il envoie les [[Packet|paquets]] à la [[DefaultGateway|passerelle par défaut]], qui est chargée de les [[Routing|acheminer]] vers le [[Network|réseau]] de destination.
*   **Configuration**: L'[[InternetProtocol|adresse IP]] de la [[DefaultGateway|passerelle par défaut]] est souvent attribuée dynamiquement aux [[EndDevices|appareils terminaux]] par un [[DHCPServer|serveur DHCP]], mais elle peut aussi être configurée statiquement.
*   **[[NetworkLayer|Couche Réseau]]**: La [[DefaultGateway|passerelle par défaut]] opère principalement à la [[NetworkLayer|couche réseau]] du [[OpenSystemsInterconnectionModel|modèle OSI]] (ou [[InternetLayer|couche Internet]] du [[InternetProtocolSuite|modèle TCP/IP]]), prenant des décisions de [[Routing|routage]] basées sur les [[InternetProtocol|adresses IP]].

## 💡 Importance en Cybersécurité
> La [[DefaultGateway|passerelle par défaut]] est un composant critique de la [[NetworkSecurity|sécurité réseau]], car elle représente un point de contrôle et de vulnérabilité majeur. Une [[Attack|attaque]] réussie contre la [[DefaultGateway|passerelle par défaut]] peut entraîner une [[DenialOfService|interruption de service]] généralisée, compromettre la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]] via des [[ManInTheMiddle|attaques de l'Homme du Milieu]], ou permettre l'[[UnauthorizedAccess|accès non autorisé]] à un [[InternalNetwork|réseau interne]]. Sa [[Security|sécurité]] est donc essentielle pour maintenir la [[Availability|disponibilité]] et la [[DataProtection|protection des données]] des [[System|systèmes]] et des [[User|utilisateurs]]. La mise en œuvre de [[SecurityControl|contrôles de sécurité]] robustes sur la [[DefaultGateway|passerelle]] est une composante fondamentale de la [[RiskManagement|gestion des risques]] en [[Cybersecurity|cybersécurité]].

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[DHCPServer|Serveur DHCP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocol|Adresse IP]]
*   [[Routing|Routage]]
*   [[LocalAreaNetwork|LAN]]
*   [[WideAreaNetwork|WAN]]
*   [[NetworkInterfaceCard|NIC]]
*   [[LogicalNetwork|Réseau Logique]]
*   [[RogueDHCPServer|Serveur DHCP malveillant]]
*   [[SecurityVulnerabilities|Vulnérabilités de sécurité]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[NetworkMonitoring|Surveillance réseau]]
*   [[NetworkSegmentation|Segmentation réseau]]