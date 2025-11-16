---
tags:
  - materiel
aliases:
  - câble de raccordement Ethernet
  - câble Ethernet
  - Patch Cable
  - Ethernet Cable
  - Ethernet Patch Cable
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Câble de Raccordement Ethernet

## 🎯 Rôle et Fonction
> Un [[EthernetPatchCable|câble de raccordement Ethernet]] est un type de [[TwistedPair|câble à paire torsadée]] équipé de [[RJ45Connector|connecteurs RJ45]] à ses extrémités. Son rôle principal est d'établir une [[NetworkCommunication|connexion physique directe]] entre des [[NetworkDevice|périphériques réseau]] (tels que des [[Computer|ordinateurs]], des [[NetworkSwitch|commutateurs réseau]] ou des [[WirelessRouter|routeurs sans fil]]) au sein d'un [[LocalAreaNetwork|réseau local (LAN)]], en adhérant aux [[Ethernet|normes Ethernet]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   Principalement des [[UnshieldedTwistedPair|câbles à paire torsadée non blindée (UTP)]] de différentes catégories (ex: [[Category5eCable|Cat5e]], Cat6, Cat7).
    *   Peut être droit (straight-through) pour connecter des types de [[NetworkDevice|périphériques]] différents, ou croisé (crossover) pour des [[NetworkDevice|périphériques]] similaires (moins nécessaire avec l'auto-MDI/MDIX moderne).
*   **Connectique**:
    *   Utilise des [[RJ45Connector|connecteurs RJ45]] (8 positions, 8 contacts, ou 8P8C) pour une insertion standardisée dans les [[EthernetPorts|ports Ethernet]].
*   **Performances**:
    *   Le [[Bandwidth|débit]] et la distance maximale supportée varient selon la catégorie du câble (ex: [[GigabitsPerSecond|Gbps]] pour Cat5e et plus).
    *   La torsion des paires de fils de [[CopperWire|cuivre]] minimise les [[Crosstalk|interférences]] et le [[Noise|bruit]] électrique, améliorant la [[SignalTransmission|transmission du signal]].
*   **Normes associées**:
    *   Conforme aux [[Ethernet|normes Ethernet]], notamment la famille [[IEEE80211|IEEE 802.3]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Fiabilité**: Offre une [[Reliability|connexion fiable]] et stable pour la [[DataTransmission|transmission de données]] sur de courtes à moyennes distances.
    *   **Simplicité**: Facile à installer et à gérer pour des [[SmallHomeNetworks|petits réseaux domestiques]] et des [[CorporateNetwork|réseaux d'entreprise]].
    *   **Performance**: Permet des débits élevés selon la catégorie, essentiels pour des applications exigeantes.
*   **Inconvénients**:
    *   **Vulnérabilité Physique**: Sensible aux [[PhysicalDamage|dommages physiques]] (coupures, pliures, écrasement) pouvant entraîner une [[ServiceDisruption|interruption de service]] ou une [[DataCorruption|corruption de données]].
    *   **Portée Limitée**: Les distances de transmission sont limitées par rapport aux [[FiberOpticCable|câbles à fibre optique]].
    *   **Interférences**: Bien que conçu pour les réduire, il peut être sujet aux [[ElectromagneticInterference|interférences électromagnétiques]] dans des environnements bruyants si le blindage est insuffisant ou inexistant (UTP).

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: Les câbles doivent être acheminés dans des conduits sécurisés ou des zones à accès restreint pour prévenir le [[Tampering|sabotage]] ou l'[[Eavesdropping|interception physique]] du [[SignalTransmission|signal]], surtout lors de la transmission de [[SensitiveData|données sensibles]].
*   Gestion des câbles: Une gestion ordonnée des câbles aide à prévenir les dommages physiques accidentels et facilite l'identification et l'isolation des problèmes.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]] (Couche Physique)
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[TwistedPair|Câble à Paire Torsadée]]
*   [[RJ45Connector|Connecteur RJ45]]
*   [[NetworkMedia|Support Réseau]]
*   [[PhysicalLayer|Couche Physique]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkDevice|Périphérique Réseau]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[WirelessRouter|Routeur Sans Fil]]
*   [[Crosstalk|Diaphonie]]
*   [[Noise|Bruit]]
*   [[ElectromagneticInterference|Interférence Électromagnétique]]
*   [[Reliability|Fiabilité]]
*   [[Performance|Performance]]
*   [[IEEE8023|Standard IEEE 802.3]]