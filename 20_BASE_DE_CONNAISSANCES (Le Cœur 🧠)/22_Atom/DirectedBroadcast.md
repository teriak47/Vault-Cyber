---
tags:
  - diffusion-dirigée
  - attaque-smurf
  - reconnaissance
  - DistributedDenialOfService
  - DenialOfService
aliases:
  - Diffusion dirigée
  - Directed Broadcast
source:
  - null
cssclasses:
  - max
---

# Diffusion Dirigée (Directed Broadcast)

## 📥 Définition en une phrase
> Une diffusion dirigée est un type de [[Broadcast|diffusion]] où un [[Packet|paquet]] [[InternetProtocol|IP]] est envoyé à l'[[InternetProtocolAddress|adresse de broadcast]] d'un [[RemoteNetwork|réseau distant]] spécifique, plutôt qu'au [[LocalAreaNetwork|réseau local]] de l'expéditeur.

## 🧠 Concepts Clés / Fonctionnement
*   **Ciblage Spécifique** : Contrairement aux [[Broadcast|diffusions]] classiques qui inondent un [[LocalAreaNetwork|réseau local]], une diffusion dirigée cible un [[RemoteNetwork|réseau distant]] particulier.
*   **Relais par le [[Router|routeur]]** : Lorsqu'un [[Router|routeur]] reçoit un [[Packet|paquet]] dont l'[[DestinationInternetProtocolVersion4Address|adresse IP de destination]] correspond à l'[[BroadcastAddress|adresse de broadcast]] de l'un de ses [[NetworkInterface|interfaces réseau]] sur un [[RemoteNetwork|réseau distant]], il relaie ce [[Packet|paquet]] en tant que [[Broadcast|diffusion]] sur ce segment de [[Network|réseau]] cible.
*   **Exploitation Historique** : Historiquement, cette fonctionnalité a été utilisée dans des [[Attack|attaques]] de type [[DenialOfService|déni de service]], comme l'[[SmurfAttack|attaque Smurf]], en amplifiant le trafic malveillant.
*   **Désactivation par Défaut** : En raison des risques de sécurité, la plupart des [[Router|routeurs]] modernes ont cette fonctionnalité désactivée par défaut pour prévenir les [[DistributedDenialOfService|attaques par déni de service distribué]].

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service]] : Peut être utilisé pour des [[Attack|attaques]] d'amplification (ex: [[SmurfAttack|attaque Smurf]]) contre une [[Host|cible]].
*   [[Reconnaissance|Reconnaissance]] : Un [[ThreatActor|attaquant]] peut utiliser les réponses à une diffusion dirigée pour identifier les [[Host|hôtes]] actifs sur un [[RemoteNetwork|réseau distant]].
*   [[NetworkCongestion|Congestion du réseau]] : Un volume élevé de trafic de diffusion peut saturer le [[CommunicationChannel|canal de communication]] du [[Network|réseau]] cible.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Désactivation** : S'assurer que la fonctionnalité de diffusion dirigée est désactivée sur tous les [[Router|routeurs]] et [[NetworkDevice|équipements réseau]].
*   [[Firewall|Filtrage par Pare-feu]] : Configurer les [[Firewall|pare-feu]] pour bloquer tout trafic de diffusion dirigée entrant ou sortant du [[CorporateNetwork|réseau d'entreprise]].
*   [[NetworkSecurity|Politiques de sécurité réseau]] : Mettre en œuvre des politiques qui interdisent l'utilisation de ce type de [[Broadcast|diffusion]].

## 🔗 Notes Connexes
*   [[Broadcast|Diffusion]]
*   [[Multicast|Multidiffusion]]
*   [[Unicast|Unidiffusion]]
*   [[InternetProtocol|Protocole Internet]]
*   [[Router|Routeur]]
*   [[DenialOfService|Déni de Service]]
*   [[SmurfAttack|Attaque Smurf]]
*   [[BroadcastAddress|Adresse de Broadcast]]
---