---
tags:
  - protocoles-de-routage-securisés
  - empoisonnement-arp
  - serveur-dhcp-malveillant
  - routing
  - border-gateway-protocol
  - networksegmentation
aliases:
  - Attaque de Routage
  - Routing Attack
  - Attaque de la Table de Routage
source:
  - null
cssclasses:
  - max
---

# Attaque de Routage

## 📥 Définition en une phrase
> Une attaque de routage est une tentative malveillante de manipuler les informations de [[Routing|routage]] d'un [[Network|réseau]] afin de rediriger le [[NetworkTrafficAnalysis|trafic]], d'interrompre les services ou d'accéder à des [[UnauthorizedAccess|ressources non autorisées]].

## 🧠 Concepts Clés / Fonctionnement
*   **Détournement de BGP (Border Gateway Protocol):** Un [[ThreatActor|attaquant]] falsifie des annonces de [[Routing|routage]] pour détourner le [[NetworkTrafficAnalysis|trafic]] vers un chemin contrôlé, souvent utilisé pour des attaques de [[DenialOfService|déni de service]] ou l'[[DataExfiltration|exfiltration de données]].
*   **Modification des [[RoutingTable|tables de routage]] :** Compromission d'un [[Router|routeur]] pour altérer ses [[RoutingTable|tables de routage]] et rediriger le [[NetworkTrafficAnalysis|trafic]] vers une destination malveillante.
*   **[[AddressResolutionProtocolPoisoning|Empoisonnement du protocole de résolution d'adresses (ARP Poisoning)]] :** Sur les [[LocalAreaNetwork|réseaux locaux (LAN)]], manipulation du [[AddressResolutionProtocol|protocole ARP]] pour associer l'[[InternetProtocolAddress|adresse IP]] d'une victime à l'[[MediaAccessControlAddress|adresse MAC]] de l'[[ThreatActor|attaquant]], permettant des attaques de type [[ManInTheMiddle|Homme du Milieu (MITM)]].
*   **Attaques par [[DynamicHostConfigurationProtocol|DHCP]] malveillant :** Un [[RogueDHCPServer|serveur DHCP malveillant]] distribue des informations de [[NetworkConfiguration|configuration réseau]] erronées, telles que des [[Gateway|passerelles]] par défaut falsifiées, redirigeant le [[NetworkTrafficAnalysis|trafic]].

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[DataExfiltration|Exfiltration de données]]
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu (MITM)]]
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[SystemCompromise|Compromission de système]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémenter des [[SecureRoutingProtocols|protocoles de routage sécurisés]] (ex: BGPsec pour BGP).
*   Mettre en place une [[NetworkSegmentation|segmentation réseau]] rigoureuse.
*   Utiliser des [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et des [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] pour détecter les anomalies de [[Routing|routage]].
*   Surveillance continue du [[NetworkMonitoring|réseau]] et [[NetworkTrafficAnalysis|analyse du trafic réseau]].
*   [[SecurityAudit|Audits de sécurité]] réguliers des configurations des [[NetworkDevice|équipements réseau]].
*   Protéger physiquement les [[Router|routeurs]] et [[NetworkSwitch|commutateurs réseau]].

## 🔗 Notes Connexes
*   [[Routing|Routage]]
*   [[Router|Routeur]]
*   [[RoutingTable|Table de routage]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[SpoofingAttack|Attaque par Usurpation]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]]
*   [[ManInTheMiddle|Man-in-the-Middle]]
*   [[NetworkProtocol|Protocole Réseau]]