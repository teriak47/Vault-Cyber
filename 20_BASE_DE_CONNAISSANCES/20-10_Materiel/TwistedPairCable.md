---
tags:
  - materiel
  - materiel/cable
aliases:
  - Paire torsadée
  - Twisted Pair Cable
  - Câble paire torsadée
  - UTP
  - STP
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Câble à Paire Torsadée (Twisted Pair Cable)

## 🎯 Rôle et Fonction
> Le [[TwistedPairCable|câble à paire torsadée]] est un type de [[NetworkMedia|support de transmission réseau]] couramment utilisé pour la [[NetworkCommunication|communication réseau]], en particulier dans les [[LocalAreaNetwork|réseaux locaux]] ([[LocalAreaNetwork|LAN]]). Il consiste en deux conducteurs isolés torsadés ensemble pour réduire l'[[ElectromagneticInterference|interférence électromagnétique]] (EMI) provenant de sources externes et la diaphonie entre les paires.

## 🛠️ Caractéristiques Techniques
* **Type / Catégories**:
  *   [[UnshieldedTwistedPair|Paire Torsadée Non Blindée (UTP)]] : Le type le plus répandu, sans blindage supplémentaire, utilisé pour la plupart des [[Ethernet|réseaux Ethernet]].
  *   [[ShieldedTwistedPair|Paire Torsadée Blindée (STP)]] : Comprend un blindage métallique autour des paires, ou autour de toutes les paires, pour une meilleure protection contre les interférences.
  *   Catégories : De Cat3 à Cat8, définissant les performances de [[Bandwidth|bande passante]] et de [[Throughput|débit]]. Les plus courantes sont [[Category5eCable|Cat5e]] et Cat6.
* **Connectique**: Généralement équipé de [[RJ45Connector|connecteurs RJ45]] aux extrémités pour se connecter aux [[NetworkInterfaceCard|cartes réseau]] et aux [[NetworkSwitch|commutateurs réseau]].
* **Performances**:
  *   Supporte des débits allant de 10 Mbps (Cat3) à 10 Gbps (Cat6a, Cat7) et même 40 Gbps (Cat8) sur de courtes distances.
  *   Distance maximale : 100 mètres pour les applications [[Ethernet|Ethernet]] standard.
* **Normes associées**: Principalement défini par les normes [[InstituteOfElectricalAndElectronicsEngineers|IEEE]] 802.3 pour l'[[EthernetProtocol|Ethernet]].

## ✅ Avantages et Inconvénients
* **Avantages**:
  *   **Coût-Efficacité**: Moins cher que le [[FiberOpticCable|câble à fibre optique]].
  *   **Facilité d'Installation**: Relativement facile à installer et à terminaison.
  *   **Flexibilité**: Assez flexible pour les déploiements dans les bureaux et les domiciles.
* **Inconvénients**:
  *   **Sensibilité aux Interférences**: Plus susceptible aux [[ElectromagneticInterference|interférences électromagnétiques]] que le câble à fibre optique.
  *   **Distance Limitée**: Efficace sur des distances plus courtes (max 100m) comparé à la fibre optique.
  *   **Débit Inférieur**: Généralement un [[Throughput|débit]] inférieur à la fibre optique pour les longues distances.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: Assurer que les câbles sont acheminés dans des conduits sécurisés ou des zones à accès contrôlé pour prévenir le [[Tampering|sabotage]] physique ou l'[[Eavesdropping|écoute clandestine]].
*   Contrôles environnementaux (température, humidité): Bien que robustes, des conditions extrêmes peuvent affecter la performance et la durée de vie du câble.

## 🔗 Notes Connexes
*   **Couche OSI**: [[PhysicalLayer|Couche Physique]]
*   **Standard de réseau**: [[EthernetProtocol|Protocole Ethernet]]
*   **Type spécifique**: [[UnshieldedTwistedPair|Paire torsadée non blindée]]
*   **Alternative physique**: [[FiberOpticCable|Câble à fibre optique]]
*   **Connecteur associé**: [[RJ45Connector|Connecteur RJ45]]