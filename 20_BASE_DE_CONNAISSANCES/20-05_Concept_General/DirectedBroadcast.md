---
tags:
aliases:
  - Diffusion dirigée
  - Directed Broadcast
archetype: concept-general
source:
cssclasses:
  - max
---

# Diffusion Dirigée (Directed Broadcast)

## 🎯 Définition et Contexte
> Une [[DirectedBroadcast|diffusion dirigée]] est un type de [[Broadcast|diffusion]] [[InternetProtocol|IP]] où un [[Packet|paquet]] est spécifiquement adressé à l'[[BroadcastAddress|adresse de broadcast]] d'un [[RemoteNetwork|réseau distant]], plutôt qu'au [[LocalAreaNetwork|réseau local]] de l'expéditeur. Ce mécanisme permet de livrer un message à tous les [[Host|hôtes]] d'un [[NetworkSegment|segment de réseau]] cible situé au-delà du [[LocalAreaNetwork|réseau local]] de l'émetteur.

Opère principalement au niveau de la [[NetworkLayer|Couche Réseau]] du [[InternetProtocolSuite|modèle TCP/IP]].

## 🧠 Principes de Fonctionnement
1.  **Ciblage Spécifique**: Contrairement aux [[Broadcast|diffusions]] classiques qui inondent un [[LocalAreaNetwork|réseau local]], une [[DirectedBroadcast|diffusion dirigée]] cible un [[RemoteNetwork|réseau distant]] particulier en utilisant son [[BroadcastAddress|adresse de broadcast]] [[InternetProtocol|IP]].
2.  **Relais par les [[Router|routeurs]]**: Lorsqu'un [[Router|routeur]] reçoit un [[Packet|paquet]] dont l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]] correspond à l'[[BroadcastAddress|adresse de broadcast]] de l'une de ses [[NetworkInterface|interfaces réseau]] sur un [[RemoteNetwork|réseau distant]], il relaie ce [[Packet|paquet]] en tant que [[Broadcast|diffusion]] sur ce [[NetworkSegment|segment de réseau]] cible. Les [[Router|routeurs]] agissent comme des relais entre les différents [[Network|réseaux]].
3.  **Contexte Historique et Évolution**: Historiquement, cette fonctionnalité a été exploitée pour des [[Attack|attaques]] d'amplification de [[DenialOfService|déni de service]], notamment l'[[SmurfAttack|attaque Smurf]]. En raison de ces [[SecurityVulnerabilities|vulnérabilités de sécurité]], la plupart des [[Router|routeurs]] modernes ont la capacité de relayer des [[DirectedBroadcast|diffusions dirigées]] désactivée par défaut.

## ⚠️ Risques et Vulnérabilités
*   **[[DenialOfService|Déni de Service]] (DoS)**: La [[DirectedBroadcast|diffusion dirigée]] peut être utilisée pour lancer des [[Attack|attaques]] d'amplification, comme l'[[SmurfAttack|attaque Smurf]], où de petites requêtes génèrent de nombreuses réponses sur le [[Network|réseau]] cible, saturant ses [[Resource|ressources]].
*   **[[Reconnaissance|Reconnaissance]]**: Un [[ThreatActor|acteur de menace]] peut envoyer une [[DirectedBroadcast|diffusion dirigée]] à un [[RemoteNetwork|réseau distant]] pour identifier les [[Host|hôtes]] actifs en analysant les réponses, obtenant ainsi des informations précieuses pour de futures [[Attack|attaques]].
*   **[[NetworkCongestion|Congestion du Réseau]]**: Un trafic excessif de [[Broadcast|diffusion]] résultant d'une [[DirectedBroadcast|diffusion dirigée]] malveillante ou mal configurée peut entraîner une [[NetworkCongestion|congestion du réseau]], dégradant la [[NetworkPerformance|performance]] et la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]].

## 🛡️ Mesures d'Atténuation et Bonnes Pratiques
*   **Désactivation par Défaut**: Il est crucial de s'assurer que la fonctionnalité de relais de [[DirectedBroadcast|diffusion dirigée]] est désactivée sur tous les [[Router|routeurs]] et [[NetworkDevice|équipements réseau]] pour prévenir les [[DistributedDenialOfService|attaques par déni de service distribué]].
*   **[[Firewall|Filtrage par Pare-feu]]**: Configurer les [[Firewall|pare-feu]] pour bloquer tout trafic de [[DirectedBroadcast|diffusion dirigée]] entrant ou sortant du [[CorporateNetwork|réseau d'entreprise]] est une mesure de protection efficace.
*   **[[SecurityPolicy|Politiques de Sécurité]] Réseau**: Mettre en œuvre des [[SecurityPolicy|politiques de sécurité]] claires qui interdisent l'utilisation et le relais de ce type de [[Broadcast|diffusion]] contribue à renforcer la [[NetworkSecurity|sécurité réseau]] globale.

## 🔗 Notes Connexes
*   [[Broadcast|Diffusion]]
*   [[Multicast|Multidiffusion]]
*   [[Unicast|Unidiffusion]]
*   [[InternetProtocol|Protocole Internet]]
*   [[Router|Routeur]]
*   [[SmurfAttack|Attaque Smurf]]
*   [[BroadcastAddress|Adresse de Broadcast]]
*   [[NetworkLayer|Couche Réseau]]
---