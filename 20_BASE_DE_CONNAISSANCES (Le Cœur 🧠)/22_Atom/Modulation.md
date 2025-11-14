---
tags:
  - modulation
  - signal-transmission
  - broadband
  - ecoute-clandestine
  - attaque-jamming
  - interference-electromagnétique
aliases:
  - Modulation
  - Modulation de signal
source:
  - null
cssclasses:
  - max
---

# Modulation

## 📥 Définition en une phrase
> La modulation est le processus de modification d'une ou plusieurs propriétés (amplitude, fréquence, phase) d'une [[Wave|onde]] porteuse par un [[InformationSignal|signal d'information]] afin de transmettre des [[Data|données]] de manière efficace et sur de longues distances.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif Principal** : Permettre la [[SignalTransmission|transmission de signal]] sur différents [[NetworkMedia|supports de transmission]] (comme l'[[WirelessMedia|air]] pour les [[RadioWaves|ondes radio]] ou les [[FiberOpticCable|fibres optiques]] pour les [[LightPulses|impulsions lumineuses]]) en adaptant le [[Message|signal]] aux caractéristiques du [[CommunicationChannel|canal de communication]].
*   **Onde Porteuse** : Une [[Wave|onde]] (généralement sinusoïdale) à haute fréquence qui ne contient pas d'information en elle-même mais sert de véhicule pour le [[InformationSignal|signal d'information]].
*   **Signal Modulateur (Information Signal)** : Le [[DigitalSignals|signal numérique]] ou [[AnalogSignal|analogique]] (qui sera une nouvelle note) qui contient les [[Data|informations]] à transmettre. C'est ce signal qui va modifier les propriétés de l'onde porteuse.
*   **Processus** : L'[[InformationSignal|information]] modifie l'amplitude, la fréquence ou la phase de l'onde porteuse. Les modulations les plus courantes sont :
    *   **Modulation d'Amplitude (AM)** : L'amplitude de l'onde porteuse est variée en fonction de l'amplitude du [[InformationSignal|signal d'information]].
    *   **Modulation de Fréquence (FM)** : La fréquence de l'onde porteuse est variée en fonction de l'amplitude du [[InformationSignal|signal d'information]].
    *   **Modulation de Phase (PM)** : La phase de l'onde porteuse est variée en fonction de l'amplitude du [[InformationSignal|signal d'information]].
    *   **Modulations Numériques** : Des techniques plus complexes (ex: PSK, QAM) sont utilisées pour moduler des [[DigitalSignals|signaux numériques]] et optimiser l'utilisation de la [[Bandwidth|bande passante]].
*   **[[Demodulation|Démodulation]]** : Le processus inverse, où le récepteur extrait le [[InformationSignal|signal d'information]] original de l'onde porteuse modulée.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute Clandestine]] : Sans [[Encryption|chiffrement]] adéquat, les [[Data|données]] modulées peuvent être interceptées et démodulées par des acteurs non autorisés.
*   [[ElectromagneticInterference|Interférence Électromagnétique]] (EMI) : Des signaux externes peuvent perturber le signal modulé, entraînant de la [[DataCorruption|corruption de données]] ou une [[ServiceDisruption|interruption de service]].
*   [[SignalJamming|Brouillage de signal]] : Une attaque intentionnelle visant à bloquer ou déformer la [[SignalTransmission|transmission]] en émettant un signal puissant sur la même fréquence.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Cryptography|Chiffrement]] : Appliquer le [[DataEncryption|chiffrement des données]] au [[InformationSignal|signal d'information]] avant la modulation pour assurer la [[Confidentiality|confidentialité]].
*   [[ErrorCorrectionCode|Codes de correction d'erreurs]] : Utiliser des algorithmes pour détecter et corriger les erreurs de [[Data|données]] causées par le bruit ou les interférences lors de la [[SignalTransmission|transmission]].
*   [[SpreadSpectrum|Techniques d'étalement de spectre]] : Comme le [[FrequencyHoppingSpreadSpectrum|FHSS]] ou le [[DirectSequenceSpreadSpectrum|DSSS]], qui dispersent le signal sur une [[Bandwidth|large bande passante]] pour rendre l'interception et le brouillage plus difficiles.
*   [[SignalFiltering|Filtrage de signal]] : Utiliser des filtres pour réduire les effets de l'[[ElectromagneticInterference|EMI]] et améliorer la qualité du signal.

## 🔗 Notes Connexes
*   [[SignalTransmission|Transmission de Signal]]
*   [[RadioWaves|Ondes Radio]]
*   [[ElectricalSignals|Signaux Électriques]]
*   [[DigitalSignals|Signaux Numériques]]
*   [[AnalogSignal|Signal Analogique]]
*   [[Demodulation|Démodulation]]
*   [[Bandwidth|Bande Passante]]
*   [[WirelessTransmission|Transmission sans fil]]