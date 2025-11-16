---
tags:
aliases:
  - Couche de Distribution
  - Distribution Layer
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche de Distribution

## 📥 Définition en une phrase
> La couche de distribution est la couche intermédiaire d'une [[HierarchicalNetworkDesign|conception de réseau hiérarchique]], agissant comme un point d'agrégation pour la [[AccessLayer|couche d'accès]] et fournissant des services de [[Routing|routage]], de [[NetworkSegmentation|segmentation réseau]] et de [[AccessControl|contrôle d'accès]] basés sur des politiques.

## 🧠 Concepts Clés / Piliers
*   **Agrégation des Flux**: Elle consolide les [[NetworkCommunication|flux de données]] provenant de la [[AccessLayer|couche d'accès]], où les [[EndDevices|terminaux]] sont connectés, avant de les transmettre à la [[CoreLayer|couche cœur]] du [[Network|réseau]].
*   **Routage Inter-VLAN et Sécurité**: La [[DistributionLayer|couche de distribution]] est responsable du [[Routing|routage]] entre les différents [[VirtualLocalAreaNetwork|VLANs]] (routage inter-VLAN) et applique des [[SecurityPolicy|politiques de sécurité]] spécifiques, telles que les [[AccessControl|listes de contrôle d'accès]], pour filtrer et contrôler le [[NetworkTrafficAnalysis|trafic réseau]].
*   **Qualité de Service (QoS)**: Elle met en œuvre des mécanismes de [[QualityOfService|Qualité de Service]] pour prioriser le [[NetworkTrafficAnalysis|trafic]] critique, assurant ainsi une [[NetworkPerformance|performance réseau]] optimale pour les applications essentielles.
*   **Redondance et [[HighAvailability|Haute Disponibilité]]**: Pour garantir la [[BusinessContinuity|continuité des activités]], cette couche est souvent dotée d'équipements redondants, réduisant l'impact d'une éventuelle [[HardwareFailure|panne matérielle]].

## 💡 Importance en Cybersécurité
> La [[DistributionLayer|couche de distribution]] est un élément pivot de la [[Cybersecurity|cybersécurité]] car elle fournit un point d'application stratégique pour les [[SecurityControl|contrôles de sécurité]] au sein du [[CorporateNetwork|réseau d'entreprise]]. En gérant le [[Routing|routage]] inter-VLAN et en appliquant des [[SecurityPolicy|politiques de sécurité]] granulaires, elle permet de contenir la propagation des [[Malware|logiciels malveillants]], de segmenter les zones de [[SensitiveData|données sensibles]] et de réguler précisément l'[[UnauthorizedAccess|accès non autorisé]] entre les différentes parties du [[Network|réseau]]. Elle renforce significativement la [[DefenseInDepth|défense en profondeur]] en agissant comme une barrière intermédiaire essentielle.

## 🔗 Notes Connexes
*   [[HierarchicalNetworkDesign|Conception de Réseau Hiérarchique]]
*   [[AccessLayer|Couche d'Accès]]
*   [[CoreLayer|Couche Cœur]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel (VLAN)]]
*   [[Routing|Routage]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[NetworkSecurity|Sécurité Réseau]]