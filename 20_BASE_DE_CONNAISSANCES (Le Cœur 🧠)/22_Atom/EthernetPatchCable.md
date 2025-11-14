---
tags:
  - câble-ethernet
  - paires-torsadées
  - gestion-câbles
  - ethernet
aliases:
  - câble de raccordement Ethernet
  - câble Ethernet
  - Patch Cable
  - Ethernet Cable
source:
  - null
cssclasses:
  - max
---

# Câble de Raccordement Ethernet

## 📥 Définition en une phrase
> Un câble de raccordement Ethernet est un type de [[TwistedPairCable|câble à paire torsadée]] doté de connecteurs [[RJ45Connector|RJ45]] à chaque extrémité, utilisé pour connecter directement des [[NetworkDevice|périphériques réseau]] au sein d'un [[LocalAreaNetwork|réseau local (LAN)]] et permettre la [[NetworkCommunication|communication réseau]] selon les [[Ethernet|normes Ethernet]].

## 🧠 Concepts Clés / Fonctionnement
*   **Connectivité Point à Point**: Permet une connexion physique directe entre deux [[NetworkDevice|dispositifs réseau]] tels qu'un [[Computer|ordinateur]] et un [[NetworkSwitch|commutateur réseau]], ou un [[WirelessRouter|routeur sans fil]].
*   **Standard [[Ethernet|Ethernet]]**: Conçu pour prendre en charge les [[NetworkProtocol|protocoles réseau]] [[EthernetProtocol|Ethernet]] qui définissent les règles de [[Data|transmission de données]] sur un [[LocalAreaNetwork|LAN]].
*   **Composition**: Généralement constitué de plusieurs paires de fils de [[CopperWire|cuivre]] torsadées (catégories comme Cat5e, Cat6, Cat7), ce qui aide à réduire les [[Crosstalk|interférences]] et le [[Noise|bruit]] électrique.
*   **Connecteurs [[RJ45Connector|RJ45]]**: Utilise des connecteurs modulaires 8P8C (8 positions, 8 contacts), communément appelés RJ45, pour une insertion facile dans les [[EthernetPorts|ports Ethernet]] des [[NetworkDevice|périphériques]].
*   **Types**: Peut être droit (straight-through) pour connecter différents types de [[NetworkDevice|périphériques]] (ex: [[Computer|ordinateur]] à [[NetworkSwitch|commutateur]]) ou croisé (crossover) pour connecter des [[NetworkDevice|périphériques]] similaires (ex: [[Computer|ordinateur]] à [[Computer|ordinateur]], [[NetworkSwitch|commutateur]] à [[NetworkSwitch|commutateur]]), bien que la plupart des [[NetworkDevice|équipements modernes]] prennent en charge l'auto-MDI/MDIX rendant les câbles croisés moins nécessaires.

## 🛡️ Risques / Menaces Associés
*   **Dommages Physiques**: Un câble endommagé physiquement (coupé, plié excessivement) peut entraîner une [[ServiceDisruption|interruption de service]] ou une [[DataCorruption|corruption de données]].
*   **[[Eavesdropping|Écoutes Clandestines]] Physiques**: Bien que les [[TwistedPairCable|paires torsadées]] offrent une certaine protection contre les [[ElectromagneticInterference|interférences électromagnétiques]], une attaque physique pour intercepter le [[SignalTransmission|signal]] est possible si le câble n'est pas sécurisé.
*   **Vulnérabilités de la [[PhysicalLayer|Couche Physique]]**: Les problèmes au niveau du câblage peuvent être des points faibles exploitables pour des [[Attack|attaques]] physiques ou pour perturber la [[Availability|disponibilité]] du [[Network|réseau]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Gestion des Câbles**: Utiliser des systèmes de gestion des câbles pour éviter l'encombrement, les dommages physiques et faciliter la maintenance.
*   **Câbles de Qualité**: Utiliser des câbles certifiés de catégorie appropriée pour la [[Bandwidth|bande passante]] et la distance requises afin d'assurer une [[Reliability|fiabilité]] et une [[Performance|performance]] optimales.
*   **[[PhysicalSecurity|Sécurité Physique]]**: Assurer la [[PhysicalSecurity|sécurité physique]] des câbles en les acheminant dans des conduits sécurisés ou des zones d'accès restreint, particulièrement pour les [[SensitiveData|données sensibles]].
*   **Tests Réguliers**: Effectuer des tests de câblage pour vérifier l'intégrité du [[SignalTransmission|signal]] et identifier les problèmes potentiels avant qu'ils n'affectent la [[NetworkCommunication|communication]].

## 🔗 Notes Connexes
*   [[Ethernet|Ethernet]]
*   [[TwistedPairCable|Câble à Paire Torsadée]]
*   [[NetworkMedia|Support Réseau]]
*   [[PhysicalLayer|Couche Physique]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkDevice|Périphérique Réseau]]
*   [[RJ45Connector|Connecteur RJ45]]
*   [[Crosstalk|Diaphonie]]
*   [[Noise|Bruit]]