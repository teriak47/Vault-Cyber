---
tags:
  - reseau/security
  - attaque
  - defense
  - tool
  - protocole/analyse
aliases:
  - Capture de Paquets
  - Interception de Paquets
  - Packet Sniffing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Capture de Paquets (Packet Sniffing)

## 📥 Définition en une phrase
> La capture de paquets est le processus d'interception et d'analyse du [[NetworkTraffic|trafic réseau]] qui transite sur un [[Network|réseau]], permettant d'examiner les [[Packet|paquets de données]] à des fins de diagnostic, de surveillance ou d'attaque.

## 🧠 Concepts Clés / Piliers
*   **Mécanisme de Capture**: Le [[PacketSniffing|sniffing]] repose souvent sur le [[PromiscuousMode|mode promiscueux]] d'une [[NetworkInterfaceCard|carte réseau]], qui lui permet d'intercepter tous les paquets présents sur un [[NetworkSegment|segment réseau]], et non uniquement ceux qui lui sont directement adressés. Des outils spécialisés appelés [[PacketAnalyzer|analyseurs de paquets]] (comme [[Wireshark|Wireshark]] ou [[Tcpdump|Tcpdump]]) sont utilisés pour acquérir, décoder et analyser ces paquets, en inspectant leurs [[Header|en-têtes]] et [[Payload|charges utiles]].
*   **Dualité des Usages**: La capture de paquets est une technique à double tranchant. Elle est légitimement employée pour le [[NetworkMonitoring|monitorage réseau]], le [[Troubleshooting|dépannage]] des problèmes de [[NetworkCommunication|communication]], l'[[NetworkTrafficAnalysis|analyse des performances]] ou la [[SecurityMonitoring|surveillance de sécurité]]. Cependant, elle est également un [[AttackVector|vecteur d'attaque]] fondamental pour des activités malveillantes comme l'[[Eavesdropping|écoute clandestine]], le [[DataTheft|vol de données]] et la préparation d'[[ManInTheMiddle|attaques de l'homme du milieu]].
*   **Stratégies de Protection**: Pour se prémunir contre la capture de paquets illégitime, le [[Encryption|chiffrement]] du [[CommunicationChannel|canal de communication]] est primordial (ex: [[HypertextTransferProtocolSecure|HTTPS]], [[SecureShell|SSH]], [[TransportLayerSecurity|TLS]], [[VirtualPrivateNetwork|VPN]], [[WirelessProtectedAccessThree|WPA3]]). La [[NetworkSegmentation|segmentation réseau]] limite la portée d'une capture, et l'activation de la [[PortSecurity|sécurité des ports]] sur les [[NetworkSwitch|commutateurs]] empêche l'interception non autorisée. Les [[IntrusionDetectionSystem|systèmes de détection d'intrusion (IDS)]] peuvent alerter sur les comportements suspects liés au sniffing, comme l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]].

## 💡 Importance en Cybersécurité
> La capture de paquets est fondamentale en [[Cybersecurity|cybersécurité]] car elle permet d'obtenir une visibilité directe sur le flux de [[Data|données]] transitant sur un [[Network|réseau]]. Pour les défenseurs (voir [[BlueTeam|Blue Team]]), c'est un outil indispensable pour la [[NetworkTrafficAnalysis|forensique réseau]], la détection d'[[Attack|attaques]] et l'optimisation des performances. Pour les [[ThreatActor|attaquants]] (voir [[RedTeam|Red Team]]), elle constitue une étape initiale critique dans la [[Reconnaissance|reconnaissance]] et l'[[Exploitation|exploitation]] des [[Vulnerability|vulnérabilités]], pouvant mener à la [[DataBreach|fuite de données sensibles]] ou à l'[[UnauthorizedAccess|accès non autorisé]] à des [[System|systèmes]]. Comprendre ses mécanismes est essentiel pour implémenter des [[SecurityControl|mesures de sécurité]] efficaces.

## 🔗 Notes Connexes
*   [[NetworkTrafficAnalysis|Analyse du Trafic Réseau]]
*   [[PromiscuousMode|Mode Promiscueux]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]]
*   [[Wireshark|Wireshark]]
*   [[Encryption|Chiffrement]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion]]
*   [[Eavesdropping|Écoute Clandestine]]
*   [[Tcpdump|Tcpdump]]
*   [[InformationDisclosure|Divulgation d'informations]]
*   [[Troubleshooting|Dépannage]]