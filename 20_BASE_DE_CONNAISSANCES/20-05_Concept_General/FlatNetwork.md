---
tags:
aliases:
  - Réseau Plat
  - Single Local Network Segment
  - Réseau sans segmentation
  - Flat Network
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Réseau Plat

## 📥 Définition en une phrase
> Une [[FlatNetwork|topologie de réseau plat]] est une architecture où tous les [[Host|hôtes]] se trouvent sur un seul [[BroadcastDomain|domaine de diffusion]] et partagent le même [[NetworkSegment|segment de réseau local]], ce qui simplifie la [[NetworkCommunication|communication directe]] mais peut entraîner des défis de [[NetworkPerformance|performance]] et de [[NetworkSecurity|sécurité]].

## 🧠 Concepts Clés / Piliers
*   **Simplicité Structurelle**: Tous les [[Host|hôtes]] sont sur un unique [[LocalAreaNetwork|LAN]] et un seul [[BroadcastDomain|domaine de diffusion]], ce qui simplifie la [[NetworkConfiguration|configuration]] initiale et peut réduire les [[NetworkInfrastructure|coûts d'infrastructure]].
*   **Communication Directe**: Les [[Host|hôtes]] utilisent le [[AddressResolutionProtocol|protocole ARP]] pour se découvrir mutuellement et [[NetworkCommunication|communiquer directement]], sans nécessiter de [[Router|routeur]] intermédiaire pour les communications au sein du [[NetworkSegment|segment]].
*   **Visibilité Élevée**: Tous les [[NetworkDevice|équipements]] connectés sur le [[NetworkSegment|segment]] sont mutuellement visibles, facilitant les interactions au sein du groupe mais augmentant également la surface d'exposition.

## 💡 Importance en Cybersécurité
> Bien que les [[FlatNetwork|réseaux plats]] soient faciles à mettre en place pour les [[SmallHomeNetworks|petits réseaux domestiques]] ou les [[SOHONetwork|petits bureaux]], ils présentent des [[SecurityVulnerabilities|vulnérabilités de sécurité]] significatives. L'absence de [[NetworkSegmentation|segmentation réseau]] signifie qu'une seule [[Vulnerability|vulnérabilité]] sur un [[Host|hôte]] peut potentiellement exposer l'ensemble du [[Network|réseau]] à des [[Threat|menaces]], favorisant la [[MalwareDistribution|propagation de malwares]] et facilitant les [[ManInTheMiddle|attaques de l'homme du milieu]]. La gestion de la [[QualityOfService|qualité de service (QoS)]] et la [[NetworkMonitoring|surveillance réseau]] sont également plus complexes, rendant la [[IncidentResponse|réponse aux incidents]] plus ardue. Comprendre cette topologie est crucial pour évaluer et atténuer l'[[AttackSurface|étendue de l'attaque]] dans un tel environnement.

## 🔗 Notes Connexes
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[AddressResolutionProtocol|ARP]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[QualityOfService|Qualité de Service (QoS)]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Router|Routeur]]
*   [[AttackSurface|Surface d'Attaque]]