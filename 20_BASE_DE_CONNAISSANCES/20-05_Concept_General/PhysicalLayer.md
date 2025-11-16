---
tags:
aliases:
  - Couche Physique
  - Physical Layer
  - Couche 1 OSI
  - OSI Layer 1
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche Physique

## 📥 Définition en une phrase
> La [[PhysicalLayer|couche physique]] est la première couche du [[OpenSystemsInterconnectionModel|modèle OSI]], responsable de la [[DataTransmission|transmission]] et de la réception brutes des [[Bit|bits]] sur le [[NetworkMedia|support physique]] du [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Support de Transmission**: Définit les types de [[NetworkMedia|supports de transmission]] utilisés, tels que les [[CopperWire|câbles en cuivre]], la [[FiberOpticCable|fibre optique]] ou les [[WirelessSignals|ondes radio]], en spécifiant leurs caractéristiques physiques, leur [[Bandwidth|bande passante]] et les connecteurs associés.
*   **Transmission de Bits**: Gère la conversion des [[DigitalSignals|données numériques]] en [[ElectricalSignals|signaux électriques]], [[OpticalSignals|optiques]] ou [[WirelessSignals|radiofréquences]] pour leur [[SignalTransmission|propagation]] sur le [[PhysicalNetwork|réseau physique]], et vice-versa lors de la réception ([[Decapsulation|décapsulation]]).
*   **Spécifications Matérielles**: Établit les normes pour les composants matériels impliqués, y compris les spécifications mécaniques des câbles et connecteurs (ex: [[RJ45Connector|RJ45]]), les caractéristiques électriques (niveaux de tension) et les aspects fonctionnels nécessaires à l'établissement, au maintien et à la désactivation des liens physiques.
*   **Codage et Synchronisation**: Détermine la méthode d'[[Encoding|encodage]] par laquelle les [[Bit|bits]] sont représentés par les signaux physiques, et assure la [[Timing|synchronisation]] précise entre l'[[EndDevices|émetteur]] et le [[EndDevices|récepteur]] pour une interprétation correcte des données.
*   **Topologie Physique**: Influence la disposition géographique et le câblage des [[NetworkDevice|périphériques réseau]], définissant comment les [[EndDevices|appareils]] sont interconnectés dans une [[NetworkTopology|topologie]] spécifique (ex: étoile, bus).

## 💡 Importance en Cybersécurité
> La [[PhysicalLayer|couche physique]] est le fondement de la [[NetworkCommunication|communication réseau]], rendant sa [[Security|sécurité]] primordiale. Toute [[Vulnerability|vulnérabilité]] ou [[Attack|attaque]] à ce niveau peut compromettre l'intégralité du [[System|système]]. Des menaces comme l'[[Eavesdropping|écoute clandestine]] (`wiretapping`), les [[DenialOfService|attaques par déni de service]] physique (coupure de câbles, brouillage de [[WirelessSignals|signaux sans fil]]) ou le [[Tampering|vol]] d'[[NetworkDevice|équipements réseau]] peuvent entraîner une [[ServiceDisruption|interruption de service]] et des [[DataBreach|fuites de données]]. Les [[ElectromagneticInterference|interférences électromagnétiques]] peuvent également dégrader les [[WirelessSignals|signaux]], affectant l'[[Integrity|intégrité des données]]. La mise en œuvre de [[PhysicalSecurity|contrôles de sécurité physique]] robustes (contrôle d'[[AccessControl|accès]], [[NetworkMonitoring|surveillance]]), une [[CableManagement|gestion des câbles]] adéquate, un [[ElectromagneticShielding|blindage électromagnétique]] (par exemple, pour la protection [[TEMPEST|TEMPEST]]) et la [[Redundancy|redondance]] des liaisons sont des mesures essentielles pour garantir la [[Availability|disponibilité]] et la [[Confidentiality|confidentialité]] des [[Data|données]] transitant par cette couche.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkDevice|Périphérique Réseau]]
*   [[PhysicalSecurity|Sécurité Physique]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[ElectromagneticSpectrum|Spectre Électromagnétique]]