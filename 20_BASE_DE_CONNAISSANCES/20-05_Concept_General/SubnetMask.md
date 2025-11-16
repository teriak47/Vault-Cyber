---
tags:
  - concept/general
  - reseau/segmentation
  - reseau
  - calcul/reseau
  - adressage
aliases:
  - Masque de sous-réseau
  - Subnet Mask
  - Subnetmask
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Masque de Sous-réseau

## 📥 Définition en une phrase
> Le [[SubnetMask|masque de sous-réseau]] est un nombre binaire de 32 bits (pour [[InternetProtocolVersion4|IPv4]]) utilisé pour séparer la [[NetworkPortion|portion réseau]] de la [[HostPortion|portion hôte]] d'une [[InternetProtocol|adresse IP]], facilitant ainsi la [[NetworkSegmentation|segmentation réseau]] en [[Subnet|sous-réseaux]].

## 🧠 Concepts Clés / Piliers
*   **Identification des Composants d'une [[InternetProtocol|Adresse IP]]**: Il permet à un [[Computer|appareil]] de déterminer si une autre [[InternetProtocol|adresse IP]] se trouve sur le même [[LocalAreaNetwork|réseau local]] ou sur un [[RemoteNetwork|réseau distant]], en différenciant les identifiants de [[Network|réseau]] et d'[[Host|hôte]].
*   **Format et Notation**: Représenté par une suite de bits à 1 pour la [[NetworkPortion|partie réseau]] et de bits à 0 pour la [[HostPortion|partie hôte]] (par exemple, `255.255.255.0` en décimal). Il est souvent exprimé via la [[ClasslessInterDomainRouting|notation Classless Inter-Domain Routing (CIDR)]] (ex: `/24`) qui indique le nombre de bits alloués à la [[NetworkPortion|portion réseau]].
*   **[[Routing|Calcul de Routage]]**: Un [[Computer|appareil]] utilise le [[SubnetMask|masque de sous-réseau]] pour effectuer une opération AND logique entre sa propre [[InternetProtocol|adresse IP]] et le masque, afin d'obtenir l'[[NetworkAddress|adresse réseau]] à laquelle il appartient. Cette information est cruciale pour le [[Routing|routage]] correct des [[Packet|paquets]] de [[DataTransmission|données]].
*   **[[Subnetting|Optimisation et Segmentation]]**: L'utilisation du [[SubnetMask|masque de sous-réseau]] est fondamentale pour le [[Subnetting|sous-réseautage]], permettant de diviser un grand [[Network|réseau]] en plusieurs [[Subnet|sous-réseaux]] plus petits. Ceci optimise l'utilisation des [[InternetProtocol|adresses IP]] et améliore la [[NetworkSegmentation|segmentation réseau]] pour des raisons de performance, de [[Scalability|scalabilité]] et de [[NetworkSecurity|sécurité]].

## 💡 Importance en Cybersécurité
> Le [[SubnetMask|masque de sous-réseau]] est un [[SecurityControl|contrôle de sécurité]] fondamental en [[NetworkSecurity|cybersécurité réseau]] car il permet une [[NetworkSegmentation|segmentation réseau]] efficace. Cette segmentation est essentielle pour isoler les [[System|systèmes]] critiques, contenir la propagation d'[[Malware|logiciels malveillants]] ou d'[[Attack|attaques]], et réduire la [[AttackSurface|surface d'attaque]]. Une configuration appropriée des masques de sous-réseau, dans le cadre d'une [[SecurityPolicy|politique de sécurité]] robuste, facilite la mise en œuvre du [[PrincipleOfLeastPrivilege|principe du moindre privilège]] en limitant la [[NetworkCommunication|communication réseau]] entre les [[Subnet|sous-réseaux]], et améliore la capacité de [[NetworkMonitoring|surveillance]] et d'[[IncidentResponse|intervention en cas d'incident]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[Subnetting|Sous-réseautage]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[ClasslessInterDomainRouting|Classless Inter-Domain Routing (CIDR)]]
*   [[NetworkAddress|Adresse Réseau]]
*   [[HostAddress|Adresse d'Hôte]]
*   [[BroadcastAddress|Adresse de Diffusion]]