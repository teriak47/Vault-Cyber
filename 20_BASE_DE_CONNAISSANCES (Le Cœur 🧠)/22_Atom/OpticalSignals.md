---
tags:
  - fibre-optique
  - wdm
  - tapping-fibre
  - transmission-luminescente
  - chiffrement
  - interferences-electromagnetiques
aliases:
  - Signaux Optiques
  - Optical Signals
source:
  - null
cssclasses:
  - max
---

# Signaux Optiques

## 📥 Définition en une phrase
> Les signaux optiques sont des informations transmises sous forme de lumière, généralement via des câbles à [[FiberOptics|fibres optiques]], utilisés pour des communications à haute vitesse et longue distance dans les réseaux modernes.

## 🧠 Concepts Clés / Fonctionnement
*   **Transmission par la lumière** : L'information numérique (bits) est convertie en [[LightPulses|impulsions lumineuses]] (photons) qui voyagent à travers le cœur d'une fibre optique.
*   **[[FiberOptics|Fibres Optiques]]** : Constituants des câbles, ces brins de verre ou de plastique pur sont conçus pour guider la lumière sur de longues distances avec une perte minimale de signal.
*   **Immunité aux Interférences** : Contrairement aux signaux électriques, les signaux optiques ne sont pas affectés par les [[ElectromagneticInterference|interférences électromagnétiques]] (EMI) ni par la diaphonie, offrant une transmission plus fiable et sécurisée.
*   **Hauts débits** : La technologie optique permet des débits de données considérablement plus élevés et sur de plus grandes distances que les câbles en cuivre traditionnels.
*   **Wavelength Division Multiplexing (WDM)** : Technique permettant de transmettre simultanément plusieurs signaux optiques à différentes longueurs d'onde (couleurs) sur une seule fibre optique, augmentant massivement la capacité.
*   **Conversion Optique-Électrique** : Aux extrémités de la liaison, des transceivers convertissent les signaux électriques en optiques pour la transmission et vice-versa pour la réception.

## 🛡️ Risques / Menaces Associés
*   [[PhysicalTampering|Altération physique]] : Les câbles de fibres optiques peuvent être coupés, endommagés ou dégradés, entraînant une [[DenialOfService|interruption de service]].
*   [[FiberTapping|Tapping de fibre]] : Bien que plus difficile que l'écoute sur cuivre, des techniques sophistiquées peuvent permettre d'extraire une partie du signal lumineux sans le couper entièrement pour l'[[Eavesdropping|écoute clandestine]].
*   [[ReflectiveDenialOfService|Attaques par réflexion]] : Des signaux lumineux malveillants peuvent être injectés ou réfléchis pour perturber la communication.
*   Vulnérabilités physiques : Les points de raccordement ou les équipements de conversion optique-électrique peuvent être des cibles pour des attaques physiques ou logicielles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PhysicalSecurity|Sécurité physique]] renforcée : Protéger les chemins de câbles, les salles d'équipement et les points de raccordement contre l'accès non autorisé et les dommages.
*   [[Encryption|Chiffrement]] des données : Assurer que les données transmises via les signaux optiques sont chiffrées avant leur conversion en lumière et déchiffrées après leur conversion en électricité.
*   [[Monitoring|Surveillance]] optique : Utiliser des systèmes de surveillance optique pour détecter les variations de signal ou les tentatives d'[[FiberTapping|tapping de fibre]].
*   [[Redundancy|Redondance]] et chemins diversifiés : Mettre en place des chemins de fibres optiques redondants et géographiquement diversifiés pour assurer la continuité de service en cas de défaillance.
*   Inspection et maintenance régulières : Vérifier l'intégrité physique des câbles et des connecteurs pour prévenir les pannes.

## 🔗 Notes Connexes
*   [[FiberOptics|Fibres Optiques]]
*   [[DataTransmission|Transmission de Données]]
*   [[NetworkLayer|Couche Réseau]]
*   [[ElectromagneticInterference|Interférences Électromagnétiques]]
*   [[PassiveOpticalNetwork|Réseau Optique Passif]]