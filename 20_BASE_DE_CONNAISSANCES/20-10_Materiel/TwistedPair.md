---
tags:
  - materiel
  - materiel/cable
aliases:
  - Paire torsadée
  - Twisted Pair Cable
  - Paire torsadée non blindée
  - Paire torsadée blindée
  - UTP
  - STP
archetype: materiel
source:
  -
cssclasses:
  - max
---

# Paire Torsadée

## 🎯 Rôle et Fonction
> La [[TwistedPair|paire torsadée]] est un type de [[NetworkMedia|câble réseau]] fondamental, servant de [[PhysicalLayer|support de transmission]] pour relier les [[NetworkDevice|dispositifs réseau]] au sein des [[LocalAreaNetwork|réseaux locaux]] (LANs). Sa fonction principale est de permettre la [[DataTransmission|transmission de données]] tout en minimisant les [[ElectromagneticInterference|interférences électromagnétiques]] externes et la [[Crosstalk|diaphonie]] interne, garantissant ainsi l'[[Integrity|intégrité]] et la fiabilité du [[SignalTransmission|signal]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   [[UnshieldedTwistedPair|UTP]] (Unshielded Twisted Pair) : Le type le plus courant, non blindé.
    *   [[ShieldedTwistedPair|STP]] (Shielded Twisted Pair) : Blindé avec une feuille métallique ou un tressage pour une meilleure protection contre les [[ElectromagneticInterference|interférences]].
    *   Classifications : [[Category5eCable|Catégorie 5e]], Cat 6, Cat 6a, Cat 7, etc., déterminant la [[Bandwidth|bande passante]] et les performances.
*   **Connectique**: Généralement équipé de [[RJ45Connector|connecteurs RJ45]] pour la connexion aux [[NetworkInterfaceCard|cartes d'interface réseau]] et aux [[NetworkSwitch|commutateurs réseau]].
*   **Performances**:
    *   [[Bandwidth|Bande passante]] : Peut supporter des débits allant de 10 [[MegabitsPerSecond|Mbps]] à 10 [[GigabitsPerSecond|Gbps]] (pour les catégories supérieures comme Cat 6a ou Cat 7).
    *   Distance : La [[DataTransmission|transmission]] efficace est généralement limitée à environ 100 mètres pour les réseaux [[Ethernet|Ethernet]].
    *   [[Latency|Latence]] : Faible [[Latency|latence]] sur de courtes distances.
*   **Normes associées**: Largement normalisé et utilisé dans le cadre des protocoles [[Ethernet|Ethernet]] (famille de normes [[InstituteOfElectricalAndElectronicsEngineers|IEEE]] 802.3).

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Coût d'acquisition et d'installation relativement bas, surtout pour l'[[UnshieldedTwistedPair|UTP]].
    *   Facilité d'installation et de maintenance.
    *   Flexibilité et adaptabilité à diverses configurations de [[LocalAreaNetwork|réseaux locaux]].
    *   Bonne résilience aux [[ElectromagneticInterference|interférences]] grâce à la torsion des fils.
*   **Inconvénients**:
    *   Sensibilité aux [[ElectromagneticInterference|interférences électromagnétiques]] (EMI) sur des longues distances, particulièrement pour l'[[UnshieldedTwistedPair|UTP]].
    *   Distance de [[DataTransmission|transmission]] limitée à 100 mètres, nécessitant des [[NetworkDevice|dispositifs intermédiaires]] pour étendre la portée.
    *   Moins performant en termes de [[Bandwidth|bande passante]] et de distance que la [[FiberOpticCable|fibre optique]].

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] : Les câbles doivent être sécurisés pour empêcher le [[PacketSniffing|sniffing de paquets]] ou le [[Tampering|sabotage]] physique.
*   Cheminement des câbles : Un acheminement réfléchi réduit les risques de dommages physiques accidentels et les [[ElectromagneticInterference|interférences électriques]].
*   [[EnvironmentalControls|Contrôles environnementaux]] : Les câbles doivent être protégés des conditions environnementales extrêmes (température, humidité) qui peuvent dégrader leurs performances et leur durée de vie.

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche Physique]]
*   [[Ethernet|Protocole Ethernet]]
*   [[UnshieldedTwistedPair|UTP]]
*   [[ShieldedTwistedPair|STP]]
*   [[RJ45Connector|Connecteur RJ45]]
*   [[FiberOpticCable|Câble à fibre optique]] (Alternative)
*   [[CoaxialCable|Câble coaxial]] (Alternative)
*   [[Crosstalk|Diaphonie]]
*   [[EnvironmentalControls|Contrôles environnementaux]]
---