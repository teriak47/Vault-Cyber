---
tags:
  - materiel
  - reseau
aliases:
  - Dispositifs intermédiaires
  - Intermediate Devices
  - Intermediate Device
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Dispositifs Intermédiaires

## 🎯 Rôle et Fonction
> Les [[IntermediateDevice|dispositifs intermédiaires]] sont des composants essentiels de l'[[NetworkInfrastructure|infrastructure réseau]]. Leur rôle principal est de connecter les [[EndDevices|dispositifs terminaux]] et de faciliter le flux de [[NetworkCommunication|communication réseau]] à la fois au sein des [[Network|réseaux]] locaux et entre différents [[Network|réseaux]]. Ils jouent un rôle de régulateur et de distributeur pour les [[Data|données]] qui transitent.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   [[Router|Routeurs]] (dirigent le trafic entre les [[Network|réseaux]])
    *   [[NetworkSwitch|Commutateurs réseau]] (connectent les [[EndDevices|dispositifs terminaux]] au sein d'un même [[LocalAreaNetwork|LAN]])
    *   [[Hub|Concentrateurs]] (répéteurs de signaux pour tous les dispositifs connectés)
    *   [[AccessPoint|Points d'accès]] sans fil (permettent la connexion de [[WirelessDevices|dispositifs sans fil]] à un [[WirelessNetwork|réseau sans fil]])
*   **Performances**: Gèrent et dirigent le [[NetworkTraffic|trafic réseau]] via des mécanismes de filtrage et de redirection de [[Packet|paquets]], contribuant à l'amélioration de la [[NetworkPerformance|performance]], de la [[NetworkSecurity|sécurité]] et de la [[Scalability|scalabilité]] du [[Network|réseau]].
*   **Normes associées**: Varient selon le type de dispositif (ex: [[IEEE80211|IEEE 802.11]] pour les [[AccessPoint|points d'accès sans fil]], [[Ethernet|IEEE 802.3]] pour les [[NetworkSwitch|commutateurs]]).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Assurent la [[NetworkCommunication|connectivité]] et la [[DataTransmission|transmission de données]] entre tous les [[Computer|ordinateurs]] et [[NetworkDevice|périphériques réseau]].
    *   Améliorent la [[NetworkPerformance|performance réseau]] en dirigeant intelligemment le [[NetworkTraffic|trafic]] et en réduisant les [[Collision|collisions]].
    *   Contribuent à la [[NetworkSecurity|sécurité réseau]] en permettant la [[NetworkSegmentation|segmentation]] et l'application de [[SecurityControl|politiques de sécurité]].
    *   Facilitent la [[Scalability|scalabilité]] des [[Network|réseaux]] en permettant l'ajout de nouveaux [[EndDevices|dispositifs]] et [[NetworkSegment|segments]].
*   **Inconvénients**:
    *   Peuvent être des points de défaillance uniques si la [[Redundancy|redondance]] n'est pas mise en œuvre.
    *   Cibles privilégiées pour les [[DigitalAttack|attaques numériques]] comme les [[DistributedDenialOfService|attaques DDoS]], pouvant entraîner des [[ServiceDisruption|interruptions de service]].
    *   Les [[ConfigurationDrift|erreurs de configuration]] ou les [[SoftwareVulnerability|vulnérabilités logicielles]]/[[HardwareFailure|matérielles]] peuvent créer des [[Vulnerability|failles de sécurité]] importantes.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] : Les [[IntermediateDevice|dispositifs intermédiaires]] doivent être installés dans des locaux sécurisés (armoires, salles serveurs) pour empêcher la manipulation physique ou le [[UnauthorizedAccess|branchement non autorisé]].
*   [[EnvironmentalControls|Contrôles environnementaux (température, humidité)]] : Assurer des conditions environnementales stables est crucial pour la fiabilité et la longévité de ces équipements, réduisant ainsi les risques de [[HardwareFailure|pannes matérielles]].

## 🔗 Notes Connexes
*   [[EndDevices|Dispositifs terminaux]]
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[Router|Routeur]]
*   [[NetworkSwitch|Commutateur réseau]]
*   [[Hub|Concentrateur]]
*   [[AccessPoint|Point d'Accès]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[NetworkProtocol|Protocoles Réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Availability|Disponibilité]]
*   [[EnvironmentalControls|Contrôles environnementaux]]