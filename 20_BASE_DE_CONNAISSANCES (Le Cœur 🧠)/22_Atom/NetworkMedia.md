---
tags:
  - media-physique
  - bande-passante
  - latence
  - infrastructure/reseau
  - infrastructure/cablage-reseau
aliases:
  - Support de transmission réseau
  - Support réseau
  - Supports de communication réseau
  - Network Media
source: null
cssclasses:
  - max
---

# Support de Transmission Réseau

## 📥 Définition en une phrase
> Les supports de transmission réseau désignent les voies physiques ou sans fil utilisées pour transporter les signaux de données entre les différents dispositifs connectés au sein d'un [[Network|réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   Ces supports constituent la fondation de la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]], permettant la [[SignalTransmission|transmission de signaux]] physiques (électriques, optiques ou radio) d'un point à un autre.
*   Les types les plus courants incluent les [[CopperWire|câbles en cuivre]] (transmettant des [[ElectricalPulses|impulsions électriques]]), les [[FiberOpticCable|câbles à fibre optique]] (transmettant des [[LightPulses|impulsions lumineuses]]) et les [[RadioWaves|ondes radio]] (transmettant des signaux électromagnétiques pour les communications [[WirelessAndWiredTechnologies_Cour|sans fil]]).
*   Le choix du support de transmission impacte directement la [[Bandwidth|bande passante]], la [[Latency|latence]] et la portée de la [[NetworkCommunication|communication réseau]].
*   Chaque type de support possède des caractéristiques uniques en termes de coût, de performance, de sécurité et d'environnement d'utilisation.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : Particulièrement sur les supports sans fil ou les câbles non sécurisés.
*   [[DataCorruption|Corruption de données]] : Interférences électromagnétiques pour les câbles en cuivre, ou atténuation et dispersion pour la fibre optique et les ondes radio.
*   [[HardwareFailure|Dommages physiques]] : Les câbles peuvent être coupés, endommagés ou déconnectés, entraînant une [[ServiceDisruption|interruption de service]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PhysicalSecurity|Sécurité physique]] : Protéger les câbles contre les dommages accidentels ou intentionnels.
*   [[Encryption|Chiffrement]] : Utiliser le chiffrement pour sécuriser les transmissions sur les supports sans fil, comme avec le [[IEEE80211Standard_Cour|standard IEEE 802.11]].
*   Choix du support : Sélectionner le type de média approprié en fonction des exigences de performance, de sécurité et des contraintes environnementales.
*   Maintien de l'intégrité : Assurer une bonne installation et maintenance des câbles pour minimiser la [[DataCorruption|corruption de données]].

## 🔗 Notes Connexes
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[SignalTransmission|Transmission de Signal]]
*   [[CopperWire|Fil de Cuivre]]
*   [[FiberOpticCable|Câble à Fibre Optique]]
*   [[RadioWaves|Ondes Radio]]