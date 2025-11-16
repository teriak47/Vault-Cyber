---
tags:
  - concept/general
  - reseau
  - reseau/segmentation
aliases:
  - Subdivision de réseau
  - Subnetting IP
  - Subnetting
  - IP Subnetting
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Subdivision de Réseau (Subnetting)

## 📥 Définition en une phrase
> Le [[Subnetting]] est le processus de division d'un [[InternetProtocol|réseau IP]] en plusieurs [[Subnet|sous-réseaux]] plus petits et logiquement distincts, facilitée par l'utilisation d'un [[SubnetMask|masque de sous-réseau]] étendu.

## 🧠 Concepts Clés / Piliers
*   **Création de Sous-Réseaux**: Implique l'"emprunt" de bits de la [[HostPortion|partie hôte]] d'une [[InternetProtocol|adresse IP]] pour les intégrer à la [[NetworkPortion|partie réseau]], définissant ainsi des sous-réseaux uniques.
*   **Masque de Sous-Réseau**: Un [[SubnetMask|masque de sous-réseau]] est utilisé pour déterminer la partie de l'[[InternetProtocol|adresse IP]] qui identifie le [[Network|réseau]] et celle qui identifie l'[[Host|hôte]] au sein de ce [[Subnet|sous-réseau]].
*   **Calcul Binaire**: La mise en œuvre du [[Subnetting]] repose sur des calculs binaires pour attribuer des plages d'[[InternetProtocol|adresses IP]] valides, l'[[NetworkAddress|adresse réseau]] et l'[[BroadcastAddress|adresse de diffusion]] pour chaque [[Subnet|sous-réseau]].
*   **Domaines de Diffusion**: Chaque [[Subnet|sous-réseau]] créé correspond à un [[BroadcastDomain|domaine de diffusion]] distinct, réduisant la taille des domaines et le volume de [[Broadcast|trafic de diffusion]].

## 💡 Importance en Cybersécurité
> Le [[Subnetting]] est fondamental pour la [[NetworkSecurity|cybersécurité]] car il permet une [[NetworkSegmentation|segmentation réseau]] efficace. Cette segmentation isole les [[NetworkSegment|segments réseau]], limitant la propagation des [[Malware|logiciels malveillants]] et des [[Attack|attaques]], et facilitant la mise en œuvre de [[AccessControl|contrôles d'accès]] granulaires. En réduisant la taille des [[BroadcastDomain|domaines de diffusion]], il diminue également la [[AttackSurface|surface d'attaque]] et améliore la [[NetworkPerformance|performance réseau]] en réduisant la [[NetworkCongestion|congestion]]. Il optimise l'utilisation des [[InternetProtocol|adresses IP]] et aide à l'organisation des [[EnterpriseNetwork|réseaux d'entreprise]].

## 🔗 Notes Connexes
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[InternetProtocolAddressBlocks|Blocs d'adresses IP]]
*   [[SubnetMask|Masque de Sous-Réseau]]
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[InternetProtocol|Protocole Internet]]