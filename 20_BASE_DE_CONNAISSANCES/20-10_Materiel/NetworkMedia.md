---
tags:
  - materiel
aliases:
  - Support de transmission réseau
  - Support réseau
  - Supports de communication réseau
  - Network Media
archetype: materiel
source:
  -
cssclasses:
  - max
---

# Support de Transmission Réseau

## 🎯 Rôle et Fonction
> Les [[NetworkMedia|supports de transmission réseau]] désignent les voies physiques ou sans fil, constituant la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]], utilisées pour acheminer les [[DigitalSignals|signaux de données]] (électriques, optiques ou [[ElectromagneticWaves|ondes électromagnétiques]]) entre les [[NetworkDevice|périphériques réseau]]. Ils sont essentiels à la [[NetworkCommunication|communication réseau]] et influencent directement sa [[NetworkPerformance|performance]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   **Filaires**:
        *   [[CopperWire|Câbles en cuivre]] ([[TwistedPair|Paire torsadée]], [[CoaxialCable|Câble coaxial]]): Transmettent des [[ElectricalPulses|impulsions électriques]].
        *   [[FiberOpticCable|Câbles à fibre optique]]: Transmettent des [[LightPulses|impulsions lumineuses]].
    *   **Sans fil**:
        *   [[WirelessMedia|Supports sans fil]] ([[RadioWaves|Ondes radio]], [[Microwaves|Micro-ondes]], [[InfraredWaves|Ondes infrarouges]]): Transmettent des [[WirelessSignals|signaux sans fil]] à travers l'[[ElectromagneticSpectrum|spectre électromagnétique]].
*   **Connectique**: Varie selon le type (ex: [[RJ45Connector|RJ45]] pour [[UnshieldedTwistedPair|UTP]], connecteurs optiques pour la fibre).
*   **Performances**:
    *   [[Bandwidth|Bande passante]] ([[BitsPerSecond|bps]], [[MegabitsPerSecond|Mbps]], [[GigabitsPerSecond|Gbps]]): Capacité de transfert de données.
    *   [[Latency|Latence]]: Temps de propagation des signaux.
    *   Portée: Distance maximale de transmission fiable.
*   **Normes associées**:
    *   [[Ethernet|IEEE 802.3]] pour les technologies câblées.
    *   [[WirelessFidelity|IEEE 802.11]] pour les technologies sans fil.

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Fournit la fondation indispensable pour toute [[Network|infrastructure réseau]].
    *   Diversité des options pour s'adapter à différents environnements et besoins (coût, performance, distance).
    *   Faible [[Latency|latence]] et haute [[Bandwidth|bande passante]] avec la [[FiberOpticCable|fibre optique]].
    *   Flexibilité et mobilité accrues avec les [[WirelessMedia|supports sans fil]].
*   **Inconvénients**:
    *   Vulnérabilité à l'[[Eavesdropping|écoute clandestine]] (notamment sans fil) et à la [[DataCorruption|corruption de données]] (interférences pour le cuivre, atténuation pour le sans fil).
    *   Sensibilité aux [[HardwareFailure|dommages physiques]] (coupures, usure) et aux [[EnvironmentalFactors|facteurs environnementaux]].
    *   Coût d'installation et de maintenance potentiellement élevé pour certaines technologies (fibre optique).
    *   Risques d'[[NetworkCongestion|congestion réseau]] et d'[[Interference|interférences]] pour les [[WirelessNetwork|réseaux sans fil]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] et le [[Tampering|sabotage]] des câbles et des [[AccessPoint|points d'accès sans fil]].
*   Utilisation de [[ShieldedCabling|câbles blindés]] pour atténuer l'[[ElectromagneticInterference|interférence électromagnétique]] et réduire les risques d'[[Eavesdropping|écoute clandestine]].
*   Mise en œuvre de protocoles de [[WirelessSecurity|sécurité sans fil]] robustes comme [[WirelessProtectedAccessThree|WPA3]] pour les [[WirelessNetwork|réseaux sans fil]].
*   [[SecurityMonitoring|Surveillance]] régulière des infrastructures physiques pour détecter toute anomalie.
*   [[EnvironmentalControls|Contrôles environnementaux]] (température, humidité) dans les centres de données et les locaux techniques pour préserver l'intégrité des équipements.

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche Physique]] (Couche OSI correspondante)
*   [[Ethernet|Ethernet]] (Protocole utilisant ce matériel)
*   [[WirelessFidelity|Wi-Fi]] (Protocole utilisant ce matériel)
*   [[CopperWire|Fil de Cuivre]] (Type de support)
*   [[FiberOpticCable|Câble à Fibre Optique]] (Type de support)
*   [[WirelessMedia|Supports sans fil]] (Type de support)