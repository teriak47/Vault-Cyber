---
tags:
  - emc
  - side-channel-attack
  - data-corruption
  - interference-electromagnétique
  - blindage-rf
  - mise-a-terre
aliases:
  - Interférence Électromagnétique
  - EMI
  - Electromagnetic Interference
cssclasses:
  - max
---

# Interférence Électromagnétique (EMI)

## 📥 Définition en une phrase
> L'[[ElectromagneticInterference|interférence électromagnétique]] (EMI) est une perturbation qui affecte un circuit électrique en raison de l'induction électromagnétique, du couplage électrostatique ou de la conduction à partir d'une source externe, pouvant dégrader les performances ou provoquer des pannes.

## 🧠 Concepts Clés / Fonctionnement
*   **Sources**: L'[[ElectromagneticInterference|EMI]] peut provenir de sources naturelles (foudre, phénomènes atmosphériques) ou artificielles (moteurs électriques, appareils électroniques, lignes électriques, émetteurs [[RadioWaves|radio]]).
*   **Propagation**: Elle peut se propager par [[WirelessTransmission|rayonnement]] (ondes électromagnétiques dans l'air, affectant les [[WirelessMedia|supports sans fil]]) ou par [[SignalTransmission|conduction]] (courants électriques parasites via des câbles comme le [[CopperWire|fil de cuivre]] ou le [[CoaxialCable|câble coaxial]]).
*   **Impact**: Les interférences peuvent causer une [[DataCorruption|corruption de données]], une [[ServiceDisruption|interruption de service]], des dysfonctionnements d'équipements, ou réduire la [[Bandwidth|bande passante]] utile.
*   **Types**: On distingue l'[[ElectromagneticInterference|EMI]] conduite (via les câbles) et l'[[ElectromagneticInterference|EMI]] rayonnée (via l'air).

## 🛡️ Risques / Menaces Associés
*   [[ServiceDisruption|Interruption de service]] due à des dysfonctionnements des équipements réseau ou informatiques.
*   [[DataCorruption|Corruption de données]] ou perte de paquets dans les transmissions numériques, compromettant l'[[Integrity|intégrité]] de l'information.
*   [[Vulnerability|Vulnérabilité]] des systèmes industriels ou de contrôle, pouvant mener à des erreurs critiques.
*   Dans des cas spécifiques, l'[[Eavesdropping|écoute clandestine]] par analyse des émissions électromagnétiques parasites (side-channel attacks).

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Shielding|Blindage]]**: Utilisation de matériaux conducteurs pour bloquer la propagation des [[ElectromagneticWaves|ondes électromagnétiques]].
*   **[[Grounding|Mise à la terre]]**: Connexion des équipements à la terre pour dissiper les courants parasites et minimiser les boucles de masse.
*   **[[Filtering|Filtrage]]**: Utilisation de filtres (ex: filtres passe-bas, passe-haut) pour atténuer les fréquences indésirables.
*   **Séparation des Câbles**: Maintenir une distance adéquate entre les câbles de puissance et les câbles de données.
*   **Conformité aux Normes**: Adhérer aux normes de [[ElectromagneticCompatibility|Compatibilité Électromagnétique]] (EMC) pour garantir que les équipements ne génèrent pas d'interférences excessives et y sont résistants.

## 🔗 Notes Connexes
*   [[SignalTransmission|Transmission de Signal]]
*   [[NetworkMedia|Supports Réseau]]
*   [[WirelessTransmission|Transmission sans fil]]
*   [[ElectricalSignals|Signaux Électriques]]
*   [[ElectromagneticWaves|Ondes Électromagnétiques]]