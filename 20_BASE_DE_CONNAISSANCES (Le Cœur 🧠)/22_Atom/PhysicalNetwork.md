---
tags:
  - types-de-cables
  - gestion-interferences
  - PhysicalSecurity
  - NetworkSegmentation
  - WirelessNetworkSecurity
aliases:
  - Réseau Physique
  - Physical Network
  - Réseau matériel
cssclasses:
  - max
---

# Réseau Physique

## 📥 Définition en une phrase
> Le [[PhysicalNetwork|réseau physique]] représente l'ensemble des [[Hardware|équipements]] et des [[NetworkMedia|supports de transmission]] tangibles (câbles, ondes radio, etc.) qui interconnectent les [[NetworkDevice|dispositifs réseau]] et les [[EndDevices|terminaux]] afin de permettre la [[DataTransmission|transmission de données]].

## 🧠 Concepts Clés / Fonctionnement
*   **Composants Physiques**: Il inclut les [[CopperWire|câbles en cuivre]] ([[TwistedPairCable|paires torsadées]], [[CoaxialCable|câbles coaxiaux]]), les [[FiberOpticCables|câbles à fibre optique]], et les [[WirelessMedia|supports sans fil]] qui utilisent des [[RadioWaves|ondes radio]], des [[Microwaves|micro-ondes]] ou des [[InfraredWaves|ondes infrarouges]].
*   **Dispositifs d'Interconnexion**: Des équipements tels que les [[Hub|concentrateurs]], les [[NetworkSwitch|commutateurs]], les [[Router|routeurs]] et les [[WirelessAccessPoint|points d'accès sans fil]] (AP) constituent l'infrastructure matérielle essentielle du [[PhysicalNetwork|réseau physique]].
*   **[[NetworkTopology|Topologie Physique]]**: Décrit la disposition spatiale et la connexion réelle des [[NetworkDevice|dispositifs]] et des [[NetworkMedia|câbles]] au sein d'un [[Network|réseau]], influençant sa [[Performance|performance]] et sa [[Redundancy|résilience]].
*   **[[PhysicalLayer|Couche Physique]] de l'[[OpenSystemsInterconnectionModel|OSI]]**: Le [[PhysicalNetwork|réseau physique]] opère principalement au niveau de la [[PhysicalLayer|couche physique]] (Couche 1) du [[OpenSystemsInterconnectionModel|modèle OSI]], gérant les aspects électriques, optiques ou radio de la [[SignalTransmission|transmission des signaux]] bruts.

## 🛡️ Risques / Menaces Associés
*   **[[UnauthorizedAccess|Accès Non Autorisé]] Physique**: L'accès physique non contrôlé aux [[NetworkDevice|équipements réseau]] et aux [[NetworkMedia|câbles]] peut permettre l'[[Eavesdropping|écoute clandestine]], le [[Tampering|sabotage]] ou le [[DataTheft|vol de données]].
*   **[[HardwareFailure|Défaillances Matérielles]]**: Les pannes de [[NetworkDevice|dispositifs]] ou de [[NetworkMedia|câbles]] peuvent entraîner une [[ServiceDisruption|interruption de service]] et une perte de [[Availability|disponibilité]] du [[Network|réseau]].
*   **Interférences**: Les [[ElectromagneticInterference|interférences électromagnétiques]] (EMI) ou d'autres formes d'[[ElectricalInterference|interférences électriques]] peuvent dégrader la qualité des [[WirelessSignals|signaux sans fil]] et des [[ElectricalSignals|signaux électriques]] transportés par les [[CopperWire|câbles en cuivre]], affectant le [[Throughput|débit]] et la [[Reliability|fiabilité]] de la [[NetworkCommunication|communication réseau]].
*   **Points d'Accès Non Sécurisés**: Un [[WirelessAccessPoint|point d'accès sans fil]] mal configuré (par exemple, un [[PublicAccessPoint|point d'accès public]] non sécurisé) peut devenir un [[AttackVector|vecteur d'attaque]] pour des [[UnauthorizedAccess|accès non autorisés]] au [[CorporateNetwork|réseau d'entreprise]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[PhysicalSecurity|Sécurité Physique]] Robuste**: Mise en place de contrôles d'accès physiques (verrous, caméras, systèmes d'alarme), de surveillance et de mesures de protection environnementale (contrôle de température, humidité) pour sécuriser les [[NetworkDevice|équipements réseau]] et l'[[NetworkInfrastructure|infrastructure de câblage]].
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Diviser le [[PhysicalNetwork|réseau physique]] en segments logiques (par exemple, en utilisant des [[VirtualLocalAreaNetwork|VLAN]]) pour isoler les services et les utilisateurs, limitant ainsi la portée des [[Attack|attaques]] et des [[ServiceDisruption|pannes]].
*   **[[WirelessNetworkSecurity|Sécurité des Réseaux Sans Fil]]**: Implémentation de protocoles de sécurité robustes comme [[WirelessProtectedAccessThree|WPA3]] ou [[WirelessProtectedAccessTwo|WPA2]], désactivation de la diffusion du [[ServiceSetIdentifier|SSID]], et utilisation du [[MacAddressFiltering|filtrage d'adresses MAC]] pour contrôler l'accès aux [[WirelessNetwork|réseaux sans fil]].
*   **[[Redundancy|Redondance]] de l'Infrastructure**: Duplication des [[NetworkDevice|composants critiques]] (ex: alimentations, cartes [[NetworkInterfaceCard|NIC]], liens réseau) et des chemins de [[DataTransmission|transmission]] pour assurer la [[HighAvailability|haute disponibilité]] et la continuité des services en cas de [[HardwareFailure|défaillance]] ou de sinistre.

## 🔗 Notes Connexes
*   [[LogicalNetwork|Réseau Logique]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkInfrastructure|Infrastructure Réseau]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[NetworkMedia|Supports de Transmission Réseau]]
*   [[NetworkDevice|Périphérique Réseau]]