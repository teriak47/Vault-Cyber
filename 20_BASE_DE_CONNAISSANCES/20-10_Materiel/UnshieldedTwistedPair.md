---
tags:
  - materiel
  - reseau
  - materiel/cable
aliases:
  - Paire torsadée non blindée
  - UTP
  - Unshielded Twisted Pair
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Paire Torsadée Non Blindée (UTP)

## 🎯 Rôle et Fonction
> Le câble [[UnshieldedTwistedPair|UTP]] est un type de [[TwistedPair|câble à paire torsadée]] fondamentalement utilisé pour la [[DataTransmission|transmission de données]] et les [[NetworkCommunication|communications réseau]], notamment dans les [[LocalAreaNetwork|réseaux locaux (LAN)]]. Son rôle principal est de fournir une connexion physique fiable pour les [[EndDevices|dispositifs terminaux]] et les [[IntermediateDevice|dispositifs intermédiaires]] dans un [[Network|réseau]].

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Composé de paires de [[CopperWire|fils de cuivre]] torsadés. Disponible en plusieurs [[CableCategories|catégories]] standardisées (par exemple, [[Category5eCable|Cat5e]], Cat6, Cat6a), chacune spécifiant des performances et des fréquences de fonctionnement différentes.
*   **Connectique**: Généralement terminé par des [[RJ45Connector|connecteurs RJ45]] pour la connexion aux ports [[EthernetPorts|Ethernet]] des [[NetworkDevice|périphériques réseau]].
*   **Performances**: Les performances varient selon la catégorie, mais elles sont mesurées en termes de [[DigitalBandwidth|bande passante numérique]] (par exemple, jusqu'à 1 Gbps pour Cat5e, 10 Gbps pour Cat6a sur des distances limitées) et de réduction de la diaphonie.
*   **Normes associées**: Conforme aux normes [[EthernetProtocol|IEEE 802.3]] pour les réseaux câblés, ce qui assure l'[[Interoperability|interopérabilité]] entre différents équipements.

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Coût**: Généralement moins cher à l'achat et à l'installation que les câbles blindés ou à fibre optique.
    *   **Flexibilité**: Plus souple et plus facile à manipuler et à installer que les câbles [[ShieldedTwistedPair|STP]] (Shielded Twisted Pair).
    *   **Facilité d'installation**: Ne nécessite pas de mise à la terre spécifique ou de techniques de terminaison complexes comme le blindage.
*   **Inconvénients**:
    *   **Sensibilité aux interférences**: L'absence de blindage le rend plus vulnérable aux [[ElectromagneticInterference|interférences électromagnétiques (EMI)]] externes et à la diaphonie (crosstalk), surtout dans des environnements bruyants ou sur de longues distances.
    *   **Distance limitée**: Les performances diminuent significativement sur de longues distances, ce qui limite son utilisation aux [[LocalAreaNetwork|LANs]] ou aux [[SOHONetwork|réseaux SOHO]].
    *   **Sécurité**: Plus susceptible à l'[[Eavesdropping|écoute clandestine]] (eavesdropping) si le câble n'est pas physiquement sécurisé, bien que la torsion des paires offre une certaine protection.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]] : Le câble [[UnshieldedTwistedPair|UTP]], comme tout [[NetworkMedia|support réseau]], doit être installé dans des conduits sécurisés ou des zones à accès restreint pour prévenir le [[Tampering|sabotage]] ou l'interception non autorisée des [[ElectricalSignals|signaux électriques]].
*   [[EnvironmentalControls|Contrôles environnementaux]] : Il est sensible aux sources d'[[ElectricalInterference|interférence électrique]] et [[ElectromagneticInterference|électromagnétique]]. Une planification attentive de l'acheminement des câbles est cruciale pour éviter la proximité avec des moteurs, des transformateurs ou des lignes électriques.

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche Physique]] : Le câble UTP opère à la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]].
*   [[EthernetProtocol|Protocole Ethernet]] : Le câble UTP est le support physique le plus couramment utilisé pour les implémentations du [[EthernetProtocol|protocole Ethernet]].
*   [[FiberOpticCable|Câble à fibre optique]] : Une [[AlternativeMateriel|alternative]] offrant des débits plus élevés et une immunité aux [[ElectromagneticInterference|interférences électromagnétiques]].
*   [[ShieldedTwistedPair|Paire torsadée blindée (STP)]] : Une [[AlternativeMateriel|alternative]] blindée offrant une meilleure protection contre les interférences, mais plus coûteuse et rigide.