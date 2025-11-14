---
tags:
  - câble-untp
  - cat5e-performance
  - diaphonie
  - cable-ethernet
  - interference-electromagnetique
  - reseau/communication
aliases:
  - Paire torsadée non blindée
  - UTP
  - Unshielded Twisted Pair
source:
  - null
cssclasses:
  - max
---

# Paire Torsadée Non Blindée (UTP)

## 📥 Définition en une phrase
> La [[UnshieldedTwistedPair|Paire Torsadée Non Blindée]] (UTP) est un type de [[TwistedPair|câble à paire torsadée]] couramment utilisé pour les [[NetworkCommunication|communications réseau]], caractérisé par l'absence de blindage métallique autour des paires de fils.

## 🧠 Concepts Clés / Fonctionnement
*   Composé de paires de [[CopperWire|fils de cuivre]] torsadés ensemble pour réduire l'[[ElectromagneticInterference|interférence électromagnétique]] (EMI) et la diaphonie entre les paires.
*   Contrairement à la [[ShieldedTwistedPair|paire torsadée blindée (STP)]], il n'intègre pas de blindage métallique (feuille ou tresse) pour isoler les paires individuelles ou l'ensemble du câble.
*   Très répandu dans les [[LocalAreaNetwork|LANs]] (Réseaux Locaux) et les applications [[Ethernet|Ethernet]] en raison de son coût inférieur et de sa flexibilité.
*   Disponible en différentes [[CableCategories|catégories]] (ex: Cat5e, Cat6, Cat6a) qui spécifient les performances en termes de [[DigitalBandwidth|bande passante numérique]] et de vitesse de transmission.
*   Facile à installer et à entretenir, il nécessite cependant une plus grande attention à l'environnement pour minimiser les sources d'interférence externe.

## 🛡️ Risques / Menaces Associés
*   **[[ElectromagneticInterference|Interférences Électromagnétiques]] (EMI):** Plus sensible aux interférences externes des [[PowerLines|lignes électriques]], des moteurs ou d'autres sources électromagnétiques, pouvant dégrader la [[SignalQuality|qualité du signal]].
*   **Diaphonie:** Sans blindage, il est plus susceptible à la diaphonie (crosstalk), où le signal d'une paire de fils interfère avec une paire adjacente, réduisant la fiabilité de la [[NetworkCommunication|communication réseau]].
*   **[[Eavesdropping|Écoute Clandestine]]:** Moins résistant à l'[[Eavesdropping|écoute clandestine]] physique ou à l'interception de signaux par des équipements sophistiqués, si les conditions sont favorables.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Gestion des câbles:** Mettre en œuvre des pratiques de gestion des câbles adéquates, en évitant les coudes serrés, les tractions excessives et le placement à proximité de sources d'[[ElectromagneticInterference|EMI]] (comme les [[PowerLines|lignes électriques]]).
*   **Sélection de la [[CableCategories|Catégorie]]:** Choisir une [[CableCategories|catégorie]] de câble UTP appropriée (ex: Cat6 ou Cat6a) qui répond aux exigences de [[DigitalBandwidth|bande passante numérique]] et de vitesse de l'application.
*   **Conformité aux normes:** S'assurer que l'installation respecte les normes de câblage structuré pour optimiser les performances et minimiser les problèmes de diaphonie.
*   **[[Security|Sécurité]] physique:** Protéger physiquement les chemins de câbles pour empêcher l'accès non autorisé et réduire le risque d'[[Eavesdropping|écoute clandestine]].

## 🔗 Notes Connexes
*   [[TwistedPair|Paire torsadée]]
*   [[ShieldedTwistedPair|Paire torsadée blindée (STP)]]
*   [[CopperWire|Fil de cuivre]]
*   [[NetworkMedia|Support réseau]]
*   [[Ethernet|Ethernet]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[NetworkCommunication|Communication réseau]]