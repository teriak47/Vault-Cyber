---
tags:
  - sous-reseau
  - masque-de-sous-reseau
  - isolation-vlan
  - Subnetting
  - NetworkSegmentation
  - Firewall
aliases:
  - Sub-network
  - Sous-réseau
source:
  - null
cssclasses:
  - max
---

# Sous-réseau (Subnet)

## 📥 Définition en une phrase
> Un [[Subnet|sous-réseau]] est une subdivision logique d'un [[InternetProtocolAddress|espace d'adressage IP]] au sein d'un [[Network|réseau]] plus grand, permettant une meilleure organisation, [[Security|sécurité]] et [[NetworkPerformance|performance réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   Un [[Subnet|sous-réseau]] divise un grand [[Network|réseau]] en plusieurs [[NetworkSegment|segments]] plus petits, logiquement distincts et gérables.
*   Il est défini par un [[InternetProtocolAddress|adresse IP]] et un [[SubnetMask|masque de sous-réseau]] qui identifie la partie [[NetworkAddress|réseau]] et la partie [[HostAddress|hôte]] de l'adresse.
*   Le [[Subnetting|subnetting]] permet de contrôler le [[NetworkTrafficAnalysis|trafic réseau]], de réduire la taille des domaines de [[Broadcast|diffusion]] et d'améliorer l'efficacité du [[Routing|routage]].
*   Les [[NetworkDevice|dispositifs réseau]] tels que les [[Router|routeurs]] utilisent le [[SubnetMask|masque de sous-réseau]] pour déterminer si un paquet est destiné à un hôte sur le même [[Subnet|sous-réseau]] ou s'il doit être routé vers un autre.

## 🛡️ Risques / Menaces Associés
*   [[NetworkCongestion|Congestion réseau]] et [[ServiceDisruption|interruption de service]] si le [[Subnetting|plan de sous-réseautage]] est mal conçu ou sous-dimensionné.
*   [[UnauthorizedAccess|Accès non autorisé]] entre [[NetworkSegment|segments]] de réseau si les [[AccessControl|contrôles d'accès]] et les politiques de [[NetworkSegmentation|segmentation]] ne sont pas correctement appliqués.
*   [[SecurityVulnerabilities|Vulnérabilités de sécurité]] dues à une [[NetworkConfiguration|configuration réseau]] incorrecte, exposant potentiellement des [[SensitiveData|données sensibles]] ou des systèmes critiques.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Planification et conception rigoureuses de l'[[IPAddressing|adressage IP]] et du [[Subnetting|sous-réseautage]] pour optimiser l'utilisation des adresses et la [[NetworkPerformance|performance]].
*   Mise en œuvre de [[Firewall|pare-feu]] et de [[AccessControl|listes de contrôle d'accès]] (ACL) entre les [[Subnet|sous-réseaux]] pour filtrer le [[NetworkTrafficAnalysis|trafic]] et appliquer des politiques de [[Security|sécurité]].
*   Utilisation de [[VirtualLocalAreaNetwork|VLAN]] pour une [[NetworkSegmentation|segmentation réseau]] logique, offrant une isolation accrue et une gestion flexible des ressources.
*   [[NetworkMonitoring|Surveillance réseau]] et [[NetworkTrafficAnalysis|analyse du trafic]] pour détecter et répondre rapidement aux activités suspectes ou aux anomalies.

## 🔗 Notes Connexes
*   [[Subnetting|Subnetting]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[NetworkSegment|Segment Réseau]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[Routing|Routage]]