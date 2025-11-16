---
tags:
  - modele
  - modele/reseau
  - couche/acces
aliases:
  - Couche d'Accès
  - Access Layer
  - Couche d'accès (réseau)
archetype: modele
source:
  - 
cssclasses:
  - max
---

# Couche d'Accès (Access Layer)

## 🎯 Principe Fondamental
> La [[AccessLayer|Couche d'Accès]] est le niveau le plus bas et le point d'entrée initial d'une [[HierarchicalNetworkDesign|architecture de réseau hiérarchique]]. Son rôle est de permettre aux [[EndDevices|dispositifs terminaux]] et aux [[User|utilisateurs]] de se connecter au [[Network|réseau]], d'agréger leur [[NetworkTraffic|trafic]], et d'appliquer les premières mesures de [[Security|sécurité]] et de gestion de service.

## 🧩 Composants / Éléments Clés
*   **[[NetworkSwitch|Commutateurs d'accès]]**: Ce sont les [[NetworkDevice|périphériques réseau]] primaires de cette couche, connectant directement les [[EndDevices|terminaux]] (comme les [[Computer|ordinateurs]], [[NetworkPrinter|imprimantes]], [[VoiceOverIP|téléphones VoIP]]) au [[Network|réseau]]. Ils offrent des [[EthernetPorts|ports Ethernet]] pour la connectivité filaire.
*   **[[WirelessAccessPoint|Points d'Accès Sans Fil (WAP)]]**: Permettent la connectivité des [[WirelessDevices|appareils sans fil]] (tels que les [[Smartphone|smartphones]] et [[Tablet|tablettes]]) au [[Network|réseau]] en convertissant les [[WirelessSignals|signaux sans fil]] en [[ElectricalSignals|signaux électriques]] ou [[OpticalSignals|optiques]].
*   **[[EndDevices|Dispositifs Terminaux]]**: Représentent les [[User|utilisateurs]] finaux et leurs [[NetworkDevice|appareils]] (ordinateurs de bureau, ordinateurs portables, [[NetworkPrinter|imprimantes]], [[InternetofThings|appareils IoT]], etc.) qui se connectent à la couche d'accès.

## 📜 Règles de Fonctionnement
*   **Connectivité et Agrégation**: La [[AccessLayer|couche d'accès]] est responsable de la collecte et de la consolidation du [[NetworkTraffic|trafic réseau]] émanant de tous les [[EndDevices|terminaux]] connectés avant de le transférer vers la [[DistributionLayer|couche de distribution]] supérieure.
*   **[[NetworkSegmentation|Segmentation Logique]]**: Elle implémente des [[VirtualLocalAreaNetwork|Réseaux Locaux Virtuels (VLAN)]] pour la [[NetworkSegmentation|segmentation réseau]] logique, isolant les groupes d'[[User|utilisateurs]] ou de [[NetworkDevice|dispositifs]] pour améliorer la [[Security|sécurité]] et la [[NetworkPerformance|performance du réseau]].
*   **[[QualityOfService|Priorisation du Trafic (QoS)]]**: Permet la mise en œuvre de politiques de [[QualityOfService|Qualité de Service]] pour prioriser certains types de [[NetworkTraffic|trafic]] (ex: [[VoiceOverIP|voix sur IP]], vidéo) afin de garantir une [[UserExperience|expérience utilisateur]] optimale.
*   **[[PowerOverEthernet|Alimentation via Ethernet (PoE)]]**: Fournit de l'alimentation électrique aux [[NetworkDevice|appareils]] compatibles (ex: [[WirelessAccessPoint|points d'accès sans fil]], [[VoiceOverIP|téléphones VoIP]], caméras IP) directement via le [[EthernetPatchCable|câble Ethernet]], simplifiant le déploiement.
*   **Contrôles d'[[AccessControl|Accès]] Initiaux**: C'est la première ligne de [[Security|défense]] où des mesures telles que la [[PortSecurity|sécurité des ports]] (pour lier des [[MediaAccessControlAddress|adresses MAC]] spécifiques à des [[EthernetPorts|ports]]) et l'[[EightZeroTwoOneXAuthentication|authentification 802.1X]] sont appliquées pour valider les [[NetworkDevice|dispositifs]] avant qu'ils ne puissent accéder au [[Network|réseau]].

## 💡 Applications Pratiques
*   **[[EnterpriseNetwork|Réseaux d'Entreprise]] et Campus**: La conception la plus courante pour connecter les [[User|utilisateurs]] et [[EndDevices|appareils]] aux ressources du [[CorporateNetwork|réseau d'entreprise]], souvent avec une infrastructure redondante.
*   **[[SmallHomeNetworks|Petits Réseaux Domestiques]] et [[SOHONetwork|SOHO]]**: Bien que moins structurée, la fonction d'accès est présente, généralement via un [[WirelessRouter|routeur sans fil]] qui connecte les [[EndDevices|appareils]] au [[Internet|réseau]] principal et fournit des services d'accès de base.

## 📊 Diagramme Conceptuel d'une Architecture Hiérarchique
La [[AccessLayer|Couche d'Accès]] est la base d'une [[HierarchicalNetworkDesign|conception de réseau hiérarchique]], où elle est reliée à la [[DistributionLayer|Couche de Distribution]] qui elle-même se connecte à la [[CoreLayer|Couche Cœur]].

```mermaid
graph TD
    subgraph "Niveau 3: Cœur"
        A[(CoreLayer) Couche Cœur]
    end

    subgraph "Niveau 2: Distribution"
        B[(DistributionLayer) Couche de Distribution]
    end

    subgraph "Niveau 1: Accès"
        C[(AccessLayer) Couche d'Accès]
    end

    A -- "Connecte les couches de distribution" --> B
    B -- "Connecte les couches d'accès" --> C
    C -- "Connecte les terminaux" --> D[(EndDevices) Dispositifs Terminaux]
    C -- "Fournit accès filaire/sans fil" --> E[(WirelessDevices) Appareils Sans Fil / (Computer) Ordinateurs]
```

## ✅ Avantages et Limites
*   **Avantages**:
    *   **Connectivité Efficace**: Fournit un point de connexion direct et fiable pour les [[EndDevices|dispositifs terminaux]].
    *   **Gestion Granulaire du Trafic**: Permet une agrégation et une gestion fine du [[NetworkTraffic|trafic]] au plus proche de sa [[SourceInternetProtocolVersion4Address|source]].
    *   **Application de [[SecurityControl|Contrôles de Sécurité]]**: Point stratégique pour l'application des premières lignes de [[Security|défense]] et de [[AccessControl|contrôle d'accès]] au [[Network|réseau]].
    *   **Évolutivité Locale**: Facilite l'ajout ou la suppression de [[EndDevices|dispositifs]] sans perturber le reste du [[Network|réseau]].
*   **Limites**:
    *   **Potentiel de Surcharge**: Une mauvaise conception ou un nombre excessif de [[EndDevices|terminaux]] peut entraîner une [[NetworkCongestion|congestion réseau]] et des [[NetworkPerformance|performances]] dégradées si la bande passante est insuffisante vers la [[DistributionLayer|couche de distribution]].
    *   **Point d'[[AttackSurface|Attaque]]**: Étant le point d'entrée, la [[AccessLayer|couche d'accès]] est une [[AttackSurface|surface d'attaque]] privilégiée. Les [[SecurityVulnerabilities|vulnérabilités]] à ce niveau peuvent permettre l'[[UnauthorizedAccess|accès non autorisé]] au [[Network|réseau]].

## 🔗 Notes Connexes
*   [[HierarchicalNetworkDesign|Conception de Réseau Hiérarchique]]
*   [[DistributionLayer|Couche de Distribution]]
*   [[CoreLayer|Couche Cœur]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[PortSecurity|Sécurité des Ports]]
*   [[QualityOfService|Qualité de Service (QoS)]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[EndDevices|Dispositifs Terminaux]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[PowerOverEthernet|Power over Ethernet]]
*   [[EightZeroTwoOneXAuthentication|Authentification 802.1X]]
*   [[VoiceOverIP|Voix sur IP]]
*   [[NetworkSegmentation|Segmentation Réseau]]