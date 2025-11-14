---
tags:
  - reseau/tempete-diffusion
  - reseau/frontiere-domaine
  - securite/protection-tempete
  - reseau/domaine-broadcast
  - reseau/segmentation-vlan
  - cyberattaque/deni-service
aliases:
  - Domaine de Diffusion
  - Broadcast Domain
source:
  - null
cssclasses:
  - max
---

# Domaine de Diffusion

## 📥 Définition en une phrase
> Un domaine de diffusion est une section logique d'un réseau informatique dans laquelle toutes les stations de travail peuvent atteindre les autres par diffusion au niveau de la couche liaison de données.

## 🧠 Concepts Clés / Fonctionnement
*   **Propagation des messages** : Lorsqu'un appareil envoie un message de diffusion (broadcast), tous les autres appareils au sein du même [[BroadcastDomain|domaine de diffusion]] le reçoivent.
*   **Limites du domaine** : Les [[Router|routeurs]] agissent comme des frontières et ne transmettent pas les messages de diffusion entre les différents domaines, contrairement aux [[NetworkSwitch|commutateurs]] qui, par défaut, transmettent les diffusions à tous leurs ports au sein du même domaine.
*   **Taille du domaine** : Un grand domaine de diffusion peut entraîner une congestion du réseau due au volume élevé de trafic de diffusion, réduisant les performances et augmentant les risques de sécurité.
*   **Segmentation** : Les [[VirtualLocalAreaNetwork|VLANs]] sont couramment utilisés pour segmenter un [[NetworkSwitch|commutateur]] en plusieurs domaines de diffusion logiques, améliorant ainsi la performance et la sécurité.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service]] (DoS) via des tempêtes de diffusion (broadcast storms) qui peuvent paralyser le réseau.
*   [[Sniffing|Écoute clandestine]] facile, car tous les hôtes du même domaine reçoivent les messages de diffusion, pouvant exposer des [[SensitiveData|informations sensibles]].
*   Performances réseau dégradées en raison d'un trafic de diffusion excessif.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémenter la [[NetworkSegmentation|segmentation réseau]] à l'aide de [[VirtualLocalAreaNetwork|VLANs]] pour diviser un grand [[BroadcastDomain|domaine de diffusion]] en plusieurs petits, réduisant ainsi le trafic de diffusion.
*   Utiliser des [[Router|routeurs]] pour interconnecter des domaines de diffusion différents, car ils ne transmettent pas les diffusions par défaut, limitant leur portée.
*   Configurer la protection contre les tempêtes de diffusion sur les [[NetworkSwitch|commutateurs]] pour prévenir les incidents de [[DenialOfService|DoS]].
*   Adopter le [[InternetProtocolVersionSix|IPv6]] avec son [[NeighborDiscoveryProtocol|NDP]] qui est plus efficace que [[AddressResolutionProtocol|ARP]] pour les diffusions.

## 🔗 Notes Connexes
*   [[CollisionDomain|Domaine de Collision]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur]]
*   [[AddressResolutionProtocol|ARP]]
*   [[NeighborDiscoveryProtocol|NDP]]