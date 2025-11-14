---
tags:
  - cable-torsade
  - ethernet-connexion
  - shielded-twisted-pair
aliases:
  - Paire torsadée
  - Twisted Pair Cable
source:
  - null
cssclasses:
  - max
---

# Paire Torsadée

## 📥 Définition en une phrase
> Un type de [[NetworkMedia|câble réseau]] où des paires de [[CopperWire|fils de cuivre]] sont torsadées ensemble pour réduire les [[ElectromagneticInterference|interférences électromagnétiques]] et la [[Crosstalk|diaphonie]].

## 🧠 Concepts Clés / Fonctionnement
*   Composé de paires de [[CopperWire|fils de cuivre]] isolés, torsadés les uns autour des autres.
*   La torsion des fils annule une partie des [[ElectromagneticInterference|interférences électromagnétiques]] (EMI) provenant de sources externes et réduit la [[Crosstalk|diaphonie]] (interférence entre les paires de fils à l'intérieur du même câble).
*   Il existe deux types principaux :
    *   **[[UnshieldedTwistedPair|UTP (Unshielded Twisted Pair)]]** : Câble non blindé, le plus courant pour les [[LocalAreaNetwork|réseaux locaux]] (LAN) en [[Ethernet|Ethernet]]. Il est moins cher et plus facile à installer.
    *   **[[ShieldedTwistedPair|STP (Shielded Twisted Pair)]]** : Câble blindé qui inclut une feuille métallique ou un tressage autour des paires de fils (ou de l'ensemble du câble) pour une meilleure protection contre les [[ElectromagneticInterference|interférences]]. Plus coûteux et rigide.
*   Classifié par catégories (ex: Cat 5e, Cat 6, Cat 7), qui déterminent sa [[Bandwidth|bande passante]] et sa performance pour la [[SignalTransmission|transmission de signal]].

## 🛡️ Risques / Menaces Associés
*   **[[SignalDegradation|Dégradation du signal]]** : Sur de longues distances ou en présence de fortes [[ElectromagneticInterference|interférences électromagnétiques]] (pour les câbles UTP), le signal peut se dégrader.
*   **[[PhysicalDamage|Dommages physiques]]** : Les câbles peuvent être endommagés par une mauvaise installation, des pliures excessives ou une usure physique, affectant la performance.
*   **[[Eavesdropping|Écoute clandestine]]** : Bien que la torsion aide à réduire les fuites de signal, une attaque physique ciblée peut toujours permettre l'[[Eavesdropping|interception de données]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Choix du type de câble** : Utiliser des câbles [[ShieldedTwistedPair|STP]] dans des environnements avec des niveaux élevés d'[[ElectromagneticInterference|interférences électromagnétiques]].
*   **Installation correcte** : Respecter les rayons de courbure minimaux, éviter les sources d'interférences (câbles électriques, moteurs) et utiliser des longueurs de câble appropriées pour éviter la [[SignalDegradation|dégradation du signal]].
*   **Catégorie de câble** : Choisir une catégorie de câble (ex: Cat 6a, Cat 7) adaptée aux exigences de [[Bandwidth|bande passante]] et de distance du [[Network|réseau]].

## 🔗 Notes Connexes
*   [[NetworkMedia|Supports Réseau]]
*   [[PhysicalLayer|Couche Physique]]
*   [[Ethernet|Ethernet]]
*   [[CopperWire|Fil de cuivre]]
*   [[SignalTransmission|Transmission de Signal]]
*   [[Crosstalk|Diaphonie]]
*   [[ElectromagneticInterference|Interférences électromagnétiques]]
*   [[UnshieldedTwistedPair|Paire Torsadée Non Blindée (UTP)]]
*   [[ShieldedTwistedPair|Paire Torsadée Blindée (STP)]]