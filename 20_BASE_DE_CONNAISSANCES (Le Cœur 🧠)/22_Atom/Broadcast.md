---
tags:
  - reseau/domaine-diffusion
  - reseau/controle-tempete
  - reseau/adresse-diffusion
  - reseau/modes-de-diffusion
  - reseau/tempete-diffusion
  - protocole/arp
aliases:
  - Diffusion
  - Broadcast (réseau)
cssclasses:
  - max
---

# Broadcast (Diffusion)

## 📥 Définition en une phrase
> Le [[Broadcast|broadcast]], ou diffusion, est une méthode de [[NetworkCommunication|communication réseau]] où un message est transmis de manière unique à tous les [[Host|hôtes]] connectés au même [[BroadcastDomain|domaine de diffusion]].

## 🧠 Concepts Clés / Fonctionnement
*   **Principe de Transmission**: Un paquet [[Message|message]] est envoyé avec une [[DestinationMacAddress|adresse MAC de destination]] spéciale (généralement FF:FF:FF:FF:FF:FF) ou une [[InternetProtocolAddress|adresse IP]] de diffusion, garantissant que tous les [[Host|hôtes]] du [[BroadcastDomain|domaine de diffusion]] le reçoivent.
*   **Portée**: Le [[Broadcast|trafic de diffusion]] est limité à un [[BroadcastDomain|domaine de diffusion]] spécifique. Les [[Router|routeurs]] agissent généralement comme des frontières, empêchant le trafic de diffusion de se propager entre différents [[Network|réseaux]]. Les [[NetworkSwitch|commutateurs réseau]] transmettent les diffusions au sein du même [[LocalAreaNetwork|LAN]] ou [[VirtualLocalAreaNetwork|VLAN]].
*   **Utilisation Courante**: Indispensable pour des protocoles de [[NetworkProtocol|protocole réseau]] fondamentaux comme le [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]] (pour mapper les [[InternetProtocolAddress|adresses IP]] aux [[MediaAccessControlAddress|adresses MAC]]) et le [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]] (pour l'attribution d'[[InternetProtocolAddress|adresses IP]]).
*   **Types de Communication**: Le [[Broadcast|broadcast]] contraste avec l'[[Unicast|unicast]] (communication un-à-un) et le [[Multicast|multidiffusion]] (communication un-à-un-groupe).

## 🛡️ Risques / Menaces Associés
*   [[ServiceDisruption|Congestion réseau]]: Un excès de [[Broadcast|trafic de diffusion]] peut entraîner un "[[BroadcastStorm|tempête de diffusion]]", submergeant le [[Network|réseau]] et causant des [[ServiceDisruption|interruptions de service]].
*   [[Eavesdropping|Écoute clandestine]]: Comme tous les [[Host|hôtes]] reçoivent les paquets de diffusion, des [[Attack|attaquants]] peuvent facilement intercepter et analyser ce trafic, surtout dans des [[FlatNetwork|réseaux plats]].
*   [[SpoofingAttack|Attaques d'usurpation]]: Les protocoles utilisant le [[Broadcast|broadcast]] sont parfois vulnérables aux [[SpoofingAttack|attaques d'usurpation]], comme l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]], où un attaquant envoie de fausses informations de diffusion.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation Réseau]]: L'utilisation de [[VirtualLocalAreaNetwork|VLANs]] pour créer des [[BroadcastDomain|domaines de diffusion]] plus petits réduit la portée des diffusions et isole le trafic.
*   [[Router|Routage]]: Les [[Router|routeurs]] bloquent les diffusions par défaut, empêchant leur propagation au-delà du [[LocalAreaNetwork|LAN]] d'origine et contenant ainsi leur impact.
*   [[StormControl|Contrôle des tempêtes]]: Configurer les [[NetworkSwitch|commutateurs réseau]] avec des fonctionnalités de [[StormControl|contrôle des tempêtes]] permet de limiter la quantité de trafic [[Broadcast|de diffusion]] pour prévenir la congestion.
*   [[PortSecurity|Sécurité des Ports]]: Sur les [[NetworkSwitch|commutateurs]], la [[PortSecurity|sécurité des ports]] peut être configurée pour limiter les types et volumes de trafic autorisés.

## 🔗 Notes Connexes
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[NetworkCommunication|Communication réseau]]
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses]]
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique]]
*   [[Multicast|Multidiffusion]]
*   [[Unicast|Unicast]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel]]