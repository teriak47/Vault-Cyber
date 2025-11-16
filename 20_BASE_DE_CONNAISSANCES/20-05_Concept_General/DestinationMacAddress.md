---
tags:
  - reseau
  - couche/liaison
  - mac
aliases:
  - Adresse MAC de Destination
  - Destination Media Access Control Address
  - Destination MAC address
  - Destination MAC
  - MAC de destination
archetype: concept-general
source:
cssclasses:
  - max
---

# Adresse MAC de Destination

## 🎯 Rôle et Contexte Réseau
> L'[[DestinationMacAddress|adresse MAC de destination]] est un [[MediaAccessControlAddress|identifiant unique de 48 bits]], spécifié dans l'[[Header|en-tête]] d'une [[EthernetFrame|trame Ethernet]], qui désigne le [[NetworkDevice|destinataire physique]] de cette [[Frame|trame]] sur un [[NetworkSegment|segment de réseau local]]. Elle est essentielle pour diriger les [[Data|données]] vers le bon [[Host|hôte]] au sein d'un [[LocalAreaNetwork|réseau local]] et opère au niveau de la [[DataLinkLayer|couche liaison de données]] (Couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]). Chaque [[NetworkInterfaceCard|carte d'interface réseau (NIC)]] possède une [[MediaAccessControlAddress|adresse MAC]] unique mondialement, gravée par le fabricant.

## ⚙️ Mécanismes et Fonctions Clés
1.  **Résolution d'Adresse**: Avant l'envoi d'une [[Frame|trame]], si l'[[InternetProtocol|adresse IP]] du destinataire est connue mais pas son [[MediaAccessControlAddress|adresse MAC]], le [[AddressResolutionProtocol|protocole ARP]] est utilisé pour résoudre l'[[InternetProtocol|adresse IP]] en [[MediaAccessControlAddress|adresse MAC]] correspondante.
2.  **Commutation sur Réseau Local**: Les [[NetworkSwitch|commutateurs réseau]] utilisent l'[[DestinationMacAddress|adresse MAC de destination]] pour faire transiter les [[Frame|trames]] vers le port approprié, après consultation de leur [[MacAddressTable|table MAC]].
3.  **Encapsulation**: L'[[MediaAccessControlAddress|adresse MAC de destination]] est encapsulée dans l'[[Header|en-tête]] de la [[EthernetFrame|trame Ethernet]] par la [[DataLinkLayer|couche liaison de données]] du [[Host|système]] émetteur, permettant une [[SignalTransmission|transmission]] efficace sur le [[PhysicalNetwork|réseau physique]].

## 🛡️ Sécurité et Menaces Associées
*   [[MACSpoofing|Usurpation d'adresse MAC]] : Un [[ThreatActor|attaquant]] peut modifier son [[MediaAccessControlAddress|adresse MAC]] pour se faire passer pour un autre [[NetworkDevice|appareil]] ou contourner les [[AccessControl|contrôles d'accès]].
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]] : L'[[ThreatActor|attaquant]] envoie de fausses réponses [[AddressResolutionProtocol|ARP]] pour lier son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocol|adresse IP]] d'une [[Gateway|passerelle]] ou d'un autre [[Host|hôte]], redirigeant le [[NetworkTrafficAnalysis|trafic]] vers lui.
*   [[MACFlooding|Inondation MAC]] : Une [[Attack|attaque]] qui vise à saturer la [[MacAddressTable|table MAC]] d'un [[NetworkSwitch|commutateur]] avec de fausses [[MediaAccessControlAddress|adresses MAC]], forçant le [[NetworkSwitch|commutateur]] à agir comme un [[Hub|concentrateur]] et à diffuser le [[NetworkTrafficAnalysis|trafic]] à tous les ports.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] : Configurer les [[NetworkSwitch|commutateurs]] pour limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] apprises par port ou pour autoriser uniquement des [[MediaAccessControlAddress|adresses MAC]] spécifiques.
*   Détection d'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]] : Utiliser des [[NetworkMonitoring|outils de surveillance réseau]] ou des [[SecurityControl|fonctionnalités de sécurité]] des [[NetworkSwitch|commutateurs]] qui peuvent détecter et bloquer les réponses [[AddressResolutionProtocol|ARP]] malveillantes.
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]] : Implémenter des [[SecurityControl|solutions]] comme [[IEEE8021x|802.1X]] pour [[Authentication|authentifier]] les [[NetworkDevice|périphériques]] avant qu'ils ne puissent communiquer sur le [[Network|réseau]].
*   Filtrage [[MediaAccessControlAddress|MAC]] statique : Configurer manuellement les [[MediaAccessControlAddress|adresses MAC]] autorisées sur des ports spécifiques pour les [[NetworkDevice|appareils]] critiques.

## 🔗 Notes Connexes
*   [[SourceMacAddress|Adresse MAC Source]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[InternetProtocol|Adresse IP]]
*   [[EthernetFrame|Trame Ethernet]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[MACFlooding|Inondation MAC]]
*   [[IEEE8021x|802.1X]]
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]]