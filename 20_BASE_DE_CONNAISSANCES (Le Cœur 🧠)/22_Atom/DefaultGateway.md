---
tags:
  - securisation-routeur
  - vulnerabilites-logicielles
  - DefaultGateway
  - DHCPServer
  - Firewall
aliases:
  - Default Gateway
  - passerelle par défaut
source:
  - null
cssclasses:
  - max
---

# Passerelle par Défaut

## 📥 Définition en une phrase
> La [[Gateway|passerelle]] par défaut est le [[Router|routeur]] sur un [[LocalAreaNetwork|réseau local]] qui sert de point de sortie pour le [[NetworkTrafficAnalysis|trafic]] destiné à des [[RemoteNetwork|réseaux distants]], tels que l'[[Internet]].

## 🧠 Concepts Clés / Fonctionnement
*   **Point de Sortie :** Chaque [[Host|hôte]] sur un [[LocalAreaNetwork|LAN]] doit connaître l'[[InternetProtocolAddress|adresse IP]] de sa [[Gateway|passerelle]] par défaut pour envoyer des [[Packet|paquets]] en dehors de son [[NetworkSegment|segment réseau]] local.
*   **[[Routing|Routage]] :** Lorsqu'un [[Computer|ordinateur]] doit communiquer avec un appareil qui n'est pas sur son [[LocalAreaNetwork|réseau local]], il envoie les [[Packet|paquets]] à la [[Gateway|passerelle]] par défaut, qui est chargée de les [[Routing|acheminer]] vers le [[Network|réseau]] de destination.
*   **Configuration :** L'[[InternetProtocolAddress|adresse IP]] de la [[Gateway|passerelle]] par défaut est souvent attribuée dynamiquement aux [[EndDevices|appareils terminaux]] par un [[DynamicHostConfigurationProtocol|serveur DHCP]], mais elle peut aussi être configurée statiquement.
*   **[[NetworkLayer|Couche Réseau]] :** La [[Gateway|passerelle]] par défaut opère principalement à la [[NetworkLayer|couche réseau]] du [[OpenSystemsInterconnectionModel|modèle OSI]] (ou [[InternetLayer|couche Internet]] du [[TcpIpModel|modèle TCP/IP]]), prenant des décisions de [[Routing|routage]] basées sur les [[InternetProtocolAddress|adresses IP]].

## 🛡️ Risques / Menaces Associés
*   **[[DenialOfService|Déni de Service]] :** Une [[Attack|attaque]] visant la [[Gateway|passerelle]] par défaut peut empêcher les [[Client|clients]] du [[LocalAreaNetwork|LAN]] d'accéder aux ressources externes, provoquant une [[ServiceDisruption|interruption de service]].
*   **[[ManInTheMiddle|Attaques Man-in-the-Middle]] (MITM) :** Un [[ThreatActor|attaquant]] peut tenter d'usurper l'[[InternetProtocolAddress|adresse IP]] de la [[Gateway|passerelle]] par défaut pour intercepter ou modifier le [[NetworkCommunication|trafic réseau]].
*   **[[RogueDHCPServer|Serveur DHCP malveillant]] :** Un [[ThreatActor|acteur de menace]] peut configurer un [[RogueDHCPServer|serveur DHCP malveillant]] pour distribuer une fausse [[Gateway|passerelle]] par défaut, détournant ainsi le [[NetworkTrafficAnalysis|trafic]].
*   **[[SecurityVulnerabilities|Vulnérabilités de sécurité]] :** Les [[Router|routeurs]] agissant comme [[Gateway|passerelles]] par défaut peuvent avoir des [[SoftwareVulnerability|vulnérabilités logicielles]] ou des configurations faibles qui peuvent être [[Exploit|exploitées]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Security|Sécurisation]] du [[Router|Routeur]] :** Changer les [[Password|mots de passe]] par défaut, désactiver les services inutiles, et maintenir le [[Firmware|micrologiciel]] à jour pour la [[Gateway|passerelle]] physique.
*   **[[NetworkMonitoring|Surveillance Réseau]] :** Implémenter une [[NetworkMonitoring|surveillance continue]] pour détecter les activités suspectes ou les changements non autorisés de [[Gateway|passerelle]].
*   **[[NetworkSegmentation|Segmentation Réseau]] :** Utiliser des [[VirtualLocalAreaNetwork|VLAN]] pour isoler le [[NetworkTrafficAnalysis|trafic]] et limiter l'[[AttackSurface|surface d'attaque]] d'une [[Gateway|passerelle]] compromise.
*   **[[Firewall|Pare-feu]] :** Configurer un [[Firewall|pare-feu]] sur la [[Gateway|passerelle]] pour filtrer le [[NetworkTrafficAnalysis|trafic]] entrant et sortant.
*   **[[DynamicHostConfigurationProtocol|DHCP]] Snooping :** Utiliser des fonctionnalités de [[Security|sécurité]] de [[NetworkSwitch|commutateur]] comme le DHCP snooping pour empêcher les [[RogueDHCPServer|serveurs DHCP malveillants]] d'opérer.

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[Routing|Routage]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[WideAreaNetwork|Réseau Étendu (WAN)]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[LogicalNetwork|Réseau Logique]]