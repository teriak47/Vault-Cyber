---
tags:
  - spread-spectrum
  - attaque-jamming
  - localisation-pistage
  - interference-electromagnetique
  - chiffrement
  - securite/sans-fil
aliases:
  - Ondes électromagnétiques
  - EM Waves
  - Electromagnetic Waves
source:
  - null
cssclasses:
  - max
---

# Ondes Électromagnétiques

## 📥 Définition en une phrase
> Les ondes électromagnétiques sont des oscillations couplées de champs électriques et magnétiques qui se propagent dans l'espace, transportant de l'énergie sans nécessiter de support matériel.

## 🧠 Concepts Clés / Fonctionnement
*   Elles sont composées de champs électriques et magnétiques qui oscillent perpendiculairement l'un à l'autre et à la direction de propagation.
*   Elles se propagent à la [[SpeedOfLight|vitesse de la lumière]] (environ 300 000 km/s dans le vide).
*   Caractérisées par leur [[Wavelength|longueur d'onde]] (distance entre deux crêtes successives) et leur [[Frequency|fréquence]] (nombre d'oscillations par seconde), inversement proportionnelles.
*   Forme le [[ElectromagneticSpectrum|spectre électromagnétique]], qui inclut les [[RadioWaves|ondes radio]], les [[Microwaves|micro-ondes]], les [[InfraredWaves|ondes infrarouges]], la lumière visible, les ultraviolets, les rayons X et les rayons gamma.
*   Utilisées dans la [[WirelessTransmission|transmission sans fil]] pour véhiculer des informations, en modulant leurs propriétés (amplitude, fréquence, phase) pour encoder des [[BinaryDigit|bits]] de données.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] (ou "sniffing") des communications [[WirelessTransmission|sans fil]] non chiffrées, permettant la [[DataTheft|vol de données]] ou l'[[PrivacyInvasion|invasion de la vie privée]].
*   [[Interference|Interférence]] avec d'autres signaux électromagnétiques, pouvant causer une [[DataCorruption|corruption de données]], des erreurs de transmission ou une [[ServiceDisruption|interruption de service]].
*   [[JammingAttack|Attaques par brouillage]] (jamming) qui visent à perturber ou bloquer délibérément la transmission des signaux, rendant les services indisponibles.
*   Exploitation de la [[LocationData|localisation]] basée sur la détection des signaux pour le [[PrivacyInvasion|pistage]] et la surveillance.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] robuste des données transmises pour garantir la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]], même en cas d'[[Eavesdropping|interception]].
*   Utilisation de techniques de [[SpreadSpectrum|spectre étalé]], comme le [[FrequencyHoppingSpreadSpectrum|saut de fréquence]], pour améliorer la résilience aux [[Interference|interférences]] et à l'[[Eavesdropping|écoute]].
*   [[Shielding|Blindage]] physique des équipements ou des zones sensibles pour contenir les ondes ou bloquer les signaux indésirables.
*   Mise en œuvre de protocoles de [[NetworkSecurity|sécurité réseau]] comme [[IEEE80211|Wi-Fi Protected Access (WPA)]] pour protéger les réseaux [[WirelessTransmission|sans fil]].
*   Gestion et planification des fréquences pour minimiser les [[Interference|interférences]] et optimiser la qualité du signal.

## 🔗 Notes Connexes
*   [[RadioWaves|Ondes Radio]]
*   [[Microwaves|Micro-ondes]]
*   [[InfraredWaves|Ondes Infrarouges]]
*   [[WirelessTransmission|Transmission sans fil]]
*   [[NetworkMedia|Supports de communication réseau]]