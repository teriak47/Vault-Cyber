---
tags:
  - concept/general
  - reseau
  - reseau/segmentation
aliases:
  - Sub-network
  - Sous-réseau
  - Subnet
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sous-réseau (Subnet)

## 📥 Définition en une phrase
> Une subdivision logique d'un [[InternetProtocol|espace d'adressage IP]] au sein d'un [[Network|réseau]] plus vaste, optimisant l'[[NetworkConfiguration|organisation]], la [[NetworkSecurity|sécurité]] et la [[NetworkPerformance|performance réseau]].

## 🧠 Concepts Clés / Piliers
*   **Segmentation**: Un [[Subnet|sous-réseau]] divise un grand [[Network|réseau]] en plusieurs [[NetworkSegment|segments]] plus petits, logiquement distincts et gérables, limitant ainsi la taille des [[BroadcastDomain|domaines de diffusion]].
*   **Identification**: Il est défini par une [[InternetProtocol|adresse IP]] et un [[SubnetMask|masque de sous-réseau]] qui identifie la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]] de l'adresse.
*   **Contrôle du Trafic**: La pratique du [[Subnetting|subnetting]] permet de contrôler le [[NetworkTrafficAnalysis|trafic réseau]], de réduire la taille des domaines de [[Broadcast|diffusion]] et d'améliorer l'efficacité du [[Routing|routage]].
*   **Routage**: Les [[NetworkDevice|dispositifs réseau]] tels que les [[Router|routeurs]] utilisent le [[SubnetMask|masque de sous-réseau]] pour déterminer si un [[Packet|paquet]] est destiné à un [[Host|hôte]] sur le même [[Subnet|sous-réseau]] ou s'il doit être routé vers un autre [[RemoteNetwork|réseau distant]].

## 💡 Importance en Cybersécurité
> La création de [[Subnet|sous-réseaux]] est une [[SecurityControl|mesure de sécurité]] essentielle. Elle permet une [[NetworkSegmentation|segmentation réseau]] qui isole les [[System|systèmes]] critiques ou les [[SensitiveData|données sensibles]], réduisant ainsi la [[AttackSurface|surface d'attaque]]. En cas de [[SystemCompromise|compromission]] d'un [[NetworkSegment|segment]], l'[[Attack|attaquant]] est confiné à ce [[Subnet|sous-réseau]], limitant la [[Propagation|propagation]] latérale et les [[FinancialLoss|pertes financières]]. Elle facilite également la [[NetworkMonitoring|surveillance réseau]] et l'application de [[SecurityPolicy|politiques de sécurité]] granulaires.

## 🔗 Notes Connexes
*   [[Subnetting|Subnetting]]
*   [[SubnetMask|Masque de Sous-réseau]]
*   [[ClasslessInterDomainRouting|CIDR]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[InternetProtocol|Protocole Internet (IP)]]
*   [[Routing|Routage]]
*   [[NetworkLayer|Couche Réseau]]