---
tags:
aliases:
  - Domaine de Diffusion
  - Broadcast Domain
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Domaine de Diffusion (Broadcast Domain)

## 📥 Définition en une phrase
> Un [[BroadcastDomain|domaine de diffusion]] est une section logique d'un [[Network|réseau informatique]] dans laquelle toutes les [[Host|stations de travail]] peuvent atteindre les autres par [[Broadcast|diffusion]] au niveau de la [[DataLinkLayer|couche liaison de données]].

## 🧠 Concepts Clés / Piliers
*   **Propagation de Diffusion**: Lorsqu'un [[NetworkDevice|appareil]] envoie un [[Message|message]] de [[Broadcast|diffusion]], tous les autres [[EndDevices|appareils]] au sein du même [[BroadcastDomain|domaine de diffusion]] le reçoivent, y compris les [[Server|serveurs]], [[Client|clients]] et [[NetworkPrinter|imprimantes réseau]].
*   **Limites du Domaine**: Les [[Router|routeurs]] agissent comme des frontières et ne transmettent pas les messages de [[Broadcast|diffusion]] entre différents [[BroadcastDomain|domaines de diffusion]]. En revanche, les [[NetworkSwitch|commutateurs]], par défaut, transmettent les diffusions à tous leurs [[EthernetPorts|ports]] au sein du même domaine.
*   **Impact de la Taille**: Un [[BroadcastDomain|grand domaine de diffusion]] peut générer un volume élevé de [[Broadcast|trafic de diffusion]], entraînant une [[NetworkCongestion|congestion réseau]], une dégradation de la [[NetworkPerformance|performance]] et augmentant les [[SecurityVulnerabilities|vulnérabilités de sécurité]].
*   **Segmentation Logique**: Les [[VirtualLocalAreaNetwork|VLANs]] sont une technique couramment utilisée pour segmenter un [[NetworkSwitch|commutateur]] en plusieurs [[LogicalNetwork|domaines de diffusion logiques]], permettant ainsi de mieux gérer le [[NetworkTrafficAnalysis|trafic]] et d'améliorer la [[NetworkSecurity|sécurité]].

## 💡 Importance en Cybersécurité
> Le contrôle et la [[NetworkSegmentation|segmentation des domaines de diffusion]] sont fondamentaux pour la [[Cybersecurity|cybersécurité]] et la [[NetworkPerformance|performance réseau]]. Des domaines trop étendus augmentent l'[[AttackSurface|surface d'attaque]], rendant le [[Network|réseau]] vulnérable aux [[DenialOfService|attaques par déni de service]] via des [[BroadcastStorm|tempêtes de diffusion]] et facilitant l'[[Eavesdropping|écoute clandestine]], ce qui peut exposer des [[SensitiveData|données sensibles]]. Une gestion adéquate des [[BroadcastDomain|domaines de diffusion]] est essentielle pour limiter la portée des [[Attack|attaques]] et optimiser le [[NetworkTrafficAnalysis|trafic réseau]].

## 🔗 Notes Connexes
*   [[CollisionDomain|Domaine de Collision]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur]]
*   [[AddressResolutionProtocol|ARP]]
*   [[NeighborDiscoveryProtocol|NDP]]
*   [[DenialOfService|Déni de Service]]
*   [[Eavesdropping|Écoute clandestine]]
*   [[NetworkPerformance|Performance réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[AttackSurface|Surface d'attaque]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[BroadcastStorm|Tempête de Diffusion]]