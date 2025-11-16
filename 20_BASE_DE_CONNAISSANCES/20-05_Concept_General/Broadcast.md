---
tags:
  - reseau
  - communication
aliases:
  - Diffusion
  - Broadcast (réseau)
  - Broadcasting
  - Diffusion réseau
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Diffusion (Broadcast)

## 📥 Définition en une phrase
> La [[Broadcast|diffusion]] est une méthode de [[NetworkCommunication|communication réseau]] où un unique [[Message|message]] est envoyé à tous les [[Host|hôtes]] ou [[NetworkDevice|périphériques réseau]] situés au sein d'un même [[BroadcastDomain|domaine de diffusion]].

## 🧠 Concepts Clés / Piliers
*   **Mécanisme de Transmission**: Un [[Packet|paquet]] est expédié avec une [[DestinationMacAddress|adresse MAC de destination]] spéciale (généralement `FF:FF:FF:FF:FF:FF`) ou une [[BroadcastAddress|adresse IP de diffusion]], assurant que chaque [[Host|hôte]] du [[BroadcastDomain|domaine de diffusion]] le reçoive.
*   **Portée et Limites**: Le [[Broadcast|trafic de diffusion]] est intrinsèquement limité à son [[BroadcastDomain|domaine de diffusion]]. Les [[Router|routeurs]] agissent comme des frontières par défaut, empêchant la propagation des diffusions entre différents [[Network|réseaux]], tandis que les [[NetworkSwitch|commutateurs réseau]] transmettent le [[Broadcast|trafic de diffusion]] au sein du [[LocalAreaNetwork|LAN]] ou du [[VirtualLocalAreaNetwork|VLAN]] auquel ils appartiennent.
*   **Utilisation Typique**: Essentielle pour des [[NetworkProtocol|protocoles réseau]] fondamentaux tels que l'[[AddressResolutionProtocol|ARP]] (résolution d'[[InternetProtocol|adresses IP]] en [[MediaAccessControlAddress|adresses MAC]]) et le [[DynamicHostConfigurationProtocol|DHCP]] (attribution dynamique d'[[InternetProtocol|adresses IP]]).
*   **Contraste avec d'autres Communications**: La [[Broadcast|diffusion]] se distingue de l'[[Unicast|unidiffusion]] (communication un-à-un) et de la [[Multicast|multidiffusion]] (communication un-à-un-groupe).

## 💡 Importance en Cybersécurité
> La [[Broadcast|diffusion]] est un pilier fondamental du fonctionnement des [[LocalAreaNetwork|réseaux locaux]], facilitant la découverte et l'allocation des [[NetworkResource|ressources]]. Cependant, sa nature "à tous" la rend intrinsèquement vulnérable. Un excès de [[Broadcast|trafic de diffusion]] peut entraîner une [[NetworkCongestion|congestion réseau]] (potentiellement une [[BroadcastStorm|tempête de diffusion]]) et des [[ServiceDisruption|interruptions de service]]. De plus, l'interception des paquets de [[Broadcast|diffusion]] est triviale pour un [[ThreatActor|attaquant]] au sein du même [[NetworkSegment|segment réseau]], posant des risques d'[[Eavesdropping|écoute clandestine]] et d'[[Spoofing|attaques d'usurpation]] (comme l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]]), particulièrement dans des [[FlatNetwork|réseaux plats]]. Une [[NetworkSegmentation|segmentation réseau]] adéquate, la [[PortSecurity|sécurité des ports]] et des mécanismes de [[StormControl|contrôle des tempêtes]] sont cruciaux pour atténuer ces risques.

## 🔗 Notes Connexes
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[NetworkCommunication|Communication réseau]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[Multicast|Multidiffusion]]
*   [[Unicast|Unidiffusion]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel (VLAN)]]
*   [[BroadcastStorm|Tempête de Diffusion]]
*   [[StormControl|Contrôle des Tempêtes]]