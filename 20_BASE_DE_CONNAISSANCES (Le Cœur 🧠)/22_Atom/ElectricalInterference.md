---
tags:
  - interference-electrique
  - filtrage-circuit
  - mise-a-terre
  - ElectromagneticInterference
  - DataCorruption
  - ServiceDisruption
aliases:
  - Interférence Électrique
  - Electrical Interference
source:
  - null
cssclasses:
  - max
---

# Interférence Électrique

## 📥 Définition en une phrase
> L'interférence électrique est une perturbation indésirable qui affecte la qualité des [[ElectricalSignals|signaux électriques]] et la performance des [[System|systèmes]] électroniques, souvent due à des sources électromagnétiques externes ou internes.

## 🧠 Concepts Clés / Fonctionnement
*   **Sources**: Peut provenir de [[ElectricalSignals|signaux électriques]] d'autres appareils, de moteurs, d'éclairages, de lignes électriques à haute tension, ou être une forme de [[ElectromagneticInterference|interférence électromagnétique]] (EMI).
*   **Propagation**: Les interférences peuvent se propager par conduction (via un contact physique, comme des [[CopperWire|câbles en cuivre]]) ou par rayonnement (via des [[ElectromagneticWaves|ondes électromagnétiques]] dans l'air).
*   **Effets**: Elles peuvent entraîner une [[DataCorruption|corruption de données]], une dégradation du [[SignalTransmission|signal de transmission]], des erreurs de [[NetworkCommunication|communication réseau]], ou des [[ServiceDisruption|interruptions de service]].
*   **Fréquence**: Les interférences sont souvent caractérisées par leur fréquence et leur amplitude, qui déterminent leur impact sur différents [[NetworkDevice|dispositifs réseau]] et électroniques.

## 🛡️ Risques / Menaces Associés
*   [[DataCorruption|Corruption de données]] : Les interférences peuvent altérer l'intégrité des [[Data|données]] transmises ou stockées.
*   [[ServiceDisruption|Interruption de service]] : Des perturbations intenses peuvent rendre un [[System|système]] ou un [[Network|réseau]] inopérant.
*   [[Vulnerability|Vulnérabilité]] aux écoutes : Dans certains cas, les émissions parasites peuvent être exploitées pour l'[[Eavesdropping|écoute clandestine]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Blindage (Shielding)** : Utilisation de matériaux conducteurs pour bloquer la propagation des [[ElectromagneticWaves|ondes électromagnétiques]] et protéger les [[CopperWire|câbles]] et les composants.
*   **Mise à la Terre (Grounding)** : Connexion appropriée des équipements à la terre pour évacuer les courants parasites indésirables et les surtensions.
*   **Filtrage (Filtering)** : Ajout de filtres sur les lignes d'alimentation et de [[CommunicationChannel|communication]] pour atténuer les fréquences d'interférence.
*   **Séparation des Circuits** : Maintenir une distance physique entre les circuits sensibles et les sources potentielles d'interférence.
*   [[SecurityControl|Contrôles de Sécurité]] physiques pour protéger les infrastructures sensibles.

## 🔗 Notes Connexes
*   [[ElectromagneticInterference|Interférence Électromagnétique]]
*   [[ElectricalSignals|Signaux Électriques]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[NetworkMedia|Support de transmission réseau]]