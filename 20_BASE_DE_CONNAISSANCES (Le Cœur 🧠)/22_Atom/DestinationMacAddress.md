---
tags:
  - adressage/mac-destination
  - protocole/arp
  - materiel/commutateur-couche-2
  - reseau/adressage-mac
  - couche/liaison-donnees
  - securite/controle-acces-reseau
aliases:
  - Adresse MAC de Destination
  - Destination Media Access Control Address
  - Destination MAC address
source:
  - null
cssclasses:
  - max
---

# Adresse MAC de Destination

## 📥 Définition en une phrase
> L'adresse MAC de destination est un identifiant unique de 48 bits, spécifié dans l'en-tête d'une [[EthernetFrame|trame Ethernet]], qui désigne le destinataire physique de cette trame sur un segment de réseau local.

## 🧠 Concepts Clés / Fonctionnement
*   C'est un champ essentiel dans l'en-tête de la [[EthernetFrame|trame Ethernet]], utilisée par la [[DataLinkLayer|couche liaison de données]] (Couche 2 du modèle [[OpenSystemsInterconnectionModel|OSI]]) pour diriger les données vers le bon hôte sur un réseau local.
*   Chaque [[NetworkInterfaceController|carte d'interface réseau (NIC)]] possède une [[MediaAccessControlAddress|adresse MAC]] unique mondialement, gravée par le fabricant.
*   Avant l'envoi d'une trame, si l'adresse [[InternetProtocolAddress|IP]] du destinataire est connue mais pas son [[MediaAccessControlAddress|adresse MAC]], le protocole [[AddressResolutionProtocol|ARP]] est utilisé pour résoudre l'[[InternetProtocolAddress|adresse IP]] en [[MediaAccessControlAddress|adresse MAC]] correspondante.
*   Les [[NetworkSwitch|commutateurs réseau]] utilisent l'[[DestinationMacAddress|adresse MAC de destination]] pour faire transiter les trames vers le port approprié, après consultation de leur [[MACAddressTable|table CAM]].

## 🛡️ Risques / Menaces Associés
*   [[MACSpoofing|Usurpation d'adresse MAC]] : Un attaquant peut modifier son [[MediaAccessControlAddress|adresse MAC]] pour se faire passer pour un autre appareil ou contourner les contrôles d'accès.
*   [[ARPPoisoning|Empoisonnement ARP]] : L'attaquant envoie de fausses réponses [[AddressResolutionProtocol|ARP]] pour lier son [[MediaAccessControlAddress|adresse MAC]] à l'[[InternetProtocolAddress|adresse IP]] d'une [[Gateway|passerelle]] ou d'un autre hôte, redirigeant le trafic vers lui.
*   [[MACFlooding|Inondation MAC]] : Une attaque qui vise à saturer la [[MACAddressTable|table CAM]] d'un [[NetworkSwitch|commutateur]] avec de fausses [[MediaAccessControlAddress|adresses MAC]], forçant le commutateur à agir comme un hub et à diffuser le trafic à tous les ports.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] : Configurer les [[NetworkSwitch|commutateurs]] pour limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] apprises par port ou pour autoriser uniquement des [[MediaAccessControlAddress|adresses MAC]] spécifiques.
*   Détection d'[[ARPPoisoning|empoisonnement ARP]] : Utiliser des outils de surveillance réseau ou des fonctionnalités de sécurité des [[NetworkSwitch|commutateurs]] qui peuvent détecter et bloquer les réponses [[AddressResolutionProtocol|ARP]] malveillantes.
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]] : Implémenter des solutions comme [[IEEE8021X|802.1X]] pour authentifier les périphériques avant qu'ils ne puissent communiquer sur le réseau.
*   Filtrage [[MediaAccessControlAddress|MAC]] statique : Configurer manuellement les [[MediaAccessControlAddress|adresses MAC]] autorisées sur des ports spécifiques pour les appareils critiques.

## 🔗 Notes Connexes
*   [[SourceMacAddress|Adresse MAC Source]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[EthernetFrame|Trame Ethernet]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[NetworkInterfaceController|Carte d'Interface Réseau (NIC)]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkSwitch|Commutateur Réseau]]