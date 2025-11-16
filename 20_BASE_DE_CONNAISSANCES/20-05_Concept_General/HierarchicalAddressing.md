---
tags:
aliases:
  - Adressage Hiérarchique
  - Hierarchical Addressing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage Hiérarchique

## 📥 Définition en une phrase
> L'adressage hiérarchique est une méthode structurée d'affectation des [[InternetProtocol|adresses IP]] qui divise logiquement un [[Network|réseau]] en [[Subnet|sous-réseaux]] plus petits, facilitant un [[EfficientRouting|routage efficace]] et une gestion simplifiée de l'[[IPAddressing|adressage IP]] à grande échelle.

## 🧠 Concepts Clés / Piliers
*   **Division Logique: Une [[InternetProtocol|adresse IP]] est logiquement séparée en une [[NetworkPortion|partie réseau]] et une [[HostPortion|partie hôte]]. La partie réseau identifie le [[Network|réseau]] (souvent un [[LocalAreaNetwork|LAN]] ou [[WideAreaNetwork|WAN]]), et la partie hôte désigne l'[[Host|hôte]] unique au sein de ce [[Network|réseau]].
*   **[[EfficientRouting|Routage Efficace]]**: Les [[Router|routeurs]] exploitent principalement la [[NetworkPortion|partie réseau]] pour diriger les [[Packet|paquets]] vers le [[Network|réseau]] de destination approprié. Cette approche réduit significativement la taille et la complexité des [[RoutingTable|tables de routage]], car il n'est pas nécessaire de stocker des entrées pour chaque [[Host|hôte]] individuel.
*   **[[Subnetting|Subdivision de Réseau]]**: L'utilisation du [[SubnetMask|masque de sous-réseau]] permet de définir la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]] d'une [[InternetProtocol|adresse IP]], facilitant la création de [[NetworkSegmentation|segments réseau]] plus petits, appelés [[Subnet|sous-réseaux]].
*   **[[Scalability|Évolutivité]] et Gestion**: Ce modèle d'adressage améliore l'[[Scalability|évolutivité]] des [[Network|réseaux]]. Les [[Enterprise|entreprises]] et les [[InternetServiceProvider|FAI]] peuvent ajouter de nouveaux [[Subnet|sous-réseaux]] ou [[RemoteNetwork|réseaux distants]] sans avoir à réaffecter l'ensemble de l'[[IPAddressing|adressage IP]].
*   **Indépendance Logique**: L'[[IPAddressing|adressage IP]] représente une adresse logique de la [[NetworkLayer|couche réseau]] ([[InternetProtocolSuite|Modèle TCP/IP]]), qui est distincte de l'[[MediaAccessControlAddress|adresse MAC]] physique de la [[NetworkInterfaceCard|carte d'interface réseau]].

## 💡 Importance en Cybersécurité
> L'adressage hiérarchique est fondamental pour la [[Cybersecurity|cybersécurité]] car il permet une [[NetworkSegmentation|segmentation réseau]] efficace, un [[SecurityControl|contrôle de sécurité]] essentiel pour isoler les systèmes et limiter la propagation des [[Malware|logiciels malveillants]] et des [[Attack|attaques]]. Une bonne conception facilite l'application de [[AccessControl|contrôles d'accès]] granulaires et du [[PrincipleOfLeastPrivilege|principe du moindre privilège]], réduisant ainsi l'[[AttackSurface|surface d'attaque]]. Inversement, une mauvaise [[NetworkConfiguration|configuration réseau]] peut introduire des [[SecurityVulnerabilities|vulnérabilités de sécurité]] significatives, conduisant à des [[UnauthorizedAccess|accès non autorisés]] et à une [[SystemCompromise|compromission de système]]. Une [[SecurityPolicy|politique de sécurité]] rigoureuse et l'utilisation de [[SecureRoutingProtocols|protocoles de routage sécurisés]] sont indispensables pour maintenir l'[[Integrity|intégrité]] et la [[Confidentiality|confidentialité]] des [[Data|données]] au sein d'une architecture hiérarchique.

## 🔗 Notes Connexes
*   [[IPAddressing|Adressage IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocol|Protocole Internet]]
*   [[SubnetMask|Masque de Sous-réseau]]
*   [[RoutingTable|Table de Routage]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[Routing|Routage]]
*   [[Subnetting|Subdivision de réseau]]
*   [[HierarchicalNetworkDesign|Conception de Réseau Hiérarchique]]
*   [[SecurityControl|Contrôle de Sécurité]]