---
tags:
aliases:
  - Table d'adresses MAC
  - MAC Address Table
  - MAC table
  - CAM table
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Table d'Adresses MAC

## 📥 Définition en une phrase
> Une table d'adresses MAC est une base de données maintenue par les [[NetworkSwitch|commutateurs réseau]] qui stocke les associations entre les [[MediaAccessControlAddress|adresses MAC]] des [[EndDevices|appareils connectés]] et les [[LANPort|ports physiques]] du [[NetworkSwitch|commutateur]].

## 🧠 Concepts Clés / Piliers
*   **[[Learning|Apprentissage]]**: Le [[NetworkSwitch|commutateur]] examine les [[Frame|trames]] entrantes pour enregistrer l'[[SourceMacAddress|adresse MAC source]] et son [[LANPort|port]] d'arrivée dans la table. Cela lui permet de savoir quel appareil se trouve sur quel port.
*   **[[Forwarding|Commutation]]**: Lorsque le [[NetworkSwitch|commutateur]] reçoit une [[Frame|trame]], il consulte la table pour transmettre le trafic uniquement vers le [[LANPort|port]] associé à l'[[DestinationMacAddress|adresse MAC de destination]], évitant ainsi le [[Flooding|l'inondation]] inutile sur d'autres ports.
*   **[[Flooding|Inondation]]**: Si l'[[DestinationMacAddress|adresse MAC de destination]] d'une [[Frame|trame]] est inconnue dans la table, le [[NetworkSwitch|commutateur]] envoie cette [[Frame|trame]] sur tous les [[LANPort|ports]] (sauf celui d'entrée), se comportant temporairement comme un [[NetworkHub|concentrateur]]. Il apprendra ensuite la position de la destination lors de sa réponse.
*   **[[Aging|Vieillissement]]**: Les entrées de la table ont une [[Timing|durée de vie]] limitée. Si une [[MediaAccessControlAddress|adresse MAC]] n'est pas vue pendant une période définie, son entrée est supprimée, garantissant l'actualisation et l'exactitude de la table.
*   **[[CollisionDomain|Domaine de Collision]]**: Chaque [[LANPort|port]] d'un [[NetworkSwitch|commutateur]] opère dans son propre [[CollisionDomain|domaine de collision]], ce qui réduit considérablement les [[Collision|collisions]] et améliore la [[NetworkPerformance|performance réseau]] par rapport aux [[NetworkHub|concentrateurs]].

## 💡 Importance en Cybersécurité
> La [[MacAddressTable|table d'adresses MAC]] est fondamentale pour l'efficacité et la [[Security|sécurité]] des [[LocalAreaNetwork|LAN]] modernes. Elle permet aux [[NetworkSwitch|commutateurs]] de diriger le [[NetworkTrafficAnalysis|trafic réseau]] de manière intelligente, réduisant l'[[InadvertentExposure|exposition]] des données aux [[EndDevices|appareils]] non concernés. Cependant, une mauvaise [[NetworkConfiguration|configuration]] ou une exploitation de ses mécanismes peut entraîner des [[SecurityVulnerabilities|vulnérabilités]] majeures.

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[Ethernet|Ethernet]]
*   [[Switching|Commutation (réseau)]]
*   [[MACFlooding|MAC Flooding]]
*   [[PortSecurity|Sécurité des Ports]]
*   [[DHCPSnooping|DHCP Snooping]]
*   [[AddressResolutionProtocolPoisoning|ARP Spoofing]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]