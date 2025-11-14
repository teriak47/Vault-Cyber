---
tags:
  - hierarchical-addressing
  - efficient-routing
  - scalabilité-reseaux
  - adressage-ip
  - networksegmentation
  - subnet-mask
aliases:
  - Adressage Hiérarchique
  - Hierarchical Addressing
source:
  - null
cssclasses:
  - max
---

# Adressage Hiérarchique

## 📥 Définition en une phrase
> L'adressage hiérarchique est une méthode structurée d'affectation des [[InternetProtocolAddress|adresses IP]] qui divise logiquement un [[Network|réseau]] en sous-réseaux plus petits, facilitant un [[EfficientRouting|routage efficace]] et une gestion simplifiée de l'[[IPAddressing|adressage IP]] à grande échelle.

## 🧠 Concepts Clés / Fonctionnement
*   **Structure d'Adresse :** Une [[InternetProtocolAddress|adresse IP]] est logiquement séparée en une [[NetworkPortion|partie réseau]] et une [[HostPortion|partie hôte]]. La [[NetworkPortion|partie réseau]] identifie le [[LocalAreaNetwork|LAN]] ou le [[WideAreaNetwork|WAN]] auquel l'appareil est connecté, tandis que la [[HostPortion|partie hôte]] identifie l'[[Host|hôte]] unique au sein de ce [[Network|réseau]].
*   **Routage Efficace :** Les [[Router|routeurs]] utilisent uniquement la [[NetworkPortion|partie réseau]] de l'[[InternetProtocolAddress|adresse IP]] pour diriger les [[Packet|paquets]] vers le [[Network|réseau]] approprié. Cela réduit la taille des [[RoutingTable|tables de routage]] car il n'est pas nécessaire de stocker une entrée pour chaque [[Host|hôte]] individuel.
*   **[[SubnetMask|Masque de sous-réseau]] :** Un [[SubnetMask|masque de sous-réseau]] est utilisé pour identifier la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]] d'une [[InternetProtocolAddress|adresse IP]]. Cela permet de créer des [[NetworkSegmentation|segments réseau]] plus petits, appelés sous-réseaux.
*   **Évolutivité :** L'adressage hiérarchique améliore l'[[Scalability|évolutivité]] des [[Network|réseaux]] en permettant aux [[Enterprise|entreprises]] et aux [[InternetServiceProvider|FAI]] d'ajouter de nouveaux sous-réseaux ou de [[RemoteNetwork|réseaux distants]] sans avoir à réaffecter l'ensemble de l'[[IPAddressing|adressage IP]].
*   **Indépendance du Support :** L'[[IPAddressing|adressage IP]] est une adresse logique de la [[NetworkLayer|couche réseau]] et est indépendante de l'[[MediaAccessControlAddress|adresse MAC]] physique de l'[[NetworkInterfaceCard|interface réseau]].

## 🛡️ Risques / Menaces Associés
*   **Complexité de Conception :** Une planification et une [[NetworkConfiguration|configuration réseau]] médiocres de l'[[IPAddressing|adressage IP]] hiérarchique peuvent entraîner des chevauchements d'adresses ou une utilisation inefficace de l'espace d'adresses, affectant la [[NetworkPerformance|performance réseau]] et la [[Security.md|sécurité]].
*   **Mauvaise [[NetworkSegmentation|Segmentation Réseau]] :** Une hiérarchie mal conçue peut ne pas fournir une [[NetworkSegmentation|segmentation réseau]] adéquate, augmentant l'[[AttackSurface|surface d'attaque]] et le risque de [[UnauthorizedAccess|accès non autorisé]] entre les segments.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Planification Stratégique :** Mettre en œuvre une planification rigoureuse pour l'[[IPAddressing|adressage IP]] et la [[NetworkSegmentation|segmentation réseau]] afin d'optimiser l'efficacité et la [[Security.md|sécurité]].
*   **Application du principe du moindre privilège :** Restreindre la communication entre les sous-réseaux en utilisant des [[Firewall|pare-feu]] et des [[AccessControl|contrôles d'accès]].
*   **Utilisation de [[SecureRoutingProtocols|protocoles de routage sécurisés]] :** Employer des [[SecureRoutingProtocols|protocoles de routage sécurisés]] pour protéger l'intégrité des [[RoutingTable|tables de routage]] contre les [[SpoofingAttack|attaques d'usurpation]].

## 🔗 Notes Connexes
*   [[IPAddressing|Adressage IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocol|Protocole Internet]]
*   [[SubnetMask|Masque de Sous-réseau]]
*   [[RoutingTable|Table de Routage]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[EfficientRouting|Routage Efficace]]