---
tags:
  - modele
  - modele/osi
  - couche/physique
  - reseau
  - communication
  - materiel
archetype: modele
source:
  - 
cssclasses:
  - max
---

# Couche Physique (Physical Layer)

## 🎯 Principe Fondamental
> La [[PhysicalLayer|Couche Physique]] (ou Couche 1) est la couche la plus basse du [[OpenSystemsInterconnectionModel|Modèle OSI]]. Son rôle principal est de définir les spécifications électriques, mécaniques, procédurales et fonctionnelles pour l'activation, le maintien et la désactivation des liaisons physiques entre les [[NetworkDevice|périphériques réseau]]. Elle est responsable de la [[DataTransmission|transmission]] brute des bits sur un [[NetworkMedia|support physique]].

## 🧩 Composants / Éléments Clés
*   **Supports Physiques**: Comprend tous les [[NetworkMedia|médias de transmission]] comme les [[TwistedPair|câbles à paire torsadée]] ([[UnshieldedTwistedPair|UTP]], [[ShieldedTwistedPair|STP]]), les [[CoaxialCable|câbles coaxiaux]], les [[FiberOpticCable|fibres optiques]] et les [[WirelessMedia|supports sans fil]] ([[RadioWaves|ondes radio]], [[InfraredWaves|infrarouges]]).
*   **Connecteurs**: Les interfaces physiques telles que les [[RJ45Connector|connecteurs RJ45]] pour les câbles [[Ethernet]], les connecteurs SC/LC pour la fibre optique, ou les ports USB.
*   **Dispositifs Réseau**: Équipements qui opèrent à ce niveau, comme les [[NetworkInterfaceCard|cartes d'interface réseau (NIC)]], les [[Hub|concentrateurs]], les répéteurs et les modems.
*   **Signalisation**: Les méthodes de conversion des bits numériques en signaux physiques ([[ElectricalSignals|signaux électriques]], [[OpticalSignals|signaux optiques]], [[WirelessSignals|signaux sans fil]]) et la façon dont ces signaux sont envoyés sur le support.

## 📜 Règles de Fonctionnement
*   **Encodage des Données**: Définit comment les bits (0 et 1) sont représentés par des signaux physiques (ex: niveaux de tension, impulsions lumineuses, fréquences radio).
*   **[[Modulation|Modulation]]/Démodulation**: Pour les signaux analogiques, elle décrit comment les données numériques sont converties en signaux analogiques (modulation) et vice-versa (démodulation).
*   **Synchronisation**: Assure que les horloges de l'expéditeur et du destinataire sont synchronisées pour interpréter correctement le flux de bits.
*   **Topologie Physique**: Influence la manière dont les [[EndDevices|terminaux]] sont connectés physiquement (ex: étoile, bus, anneau).
*   **Spécifications Matérielles**: Établit les normes pour les câbles (longueur maximale, types de blindage), les connecteurs et les niveaux de puissance.

## 📊 Diagramme Conceptuel

```mermaid
graph TD
    classDef link fill:#fff2cc,stroke:#b8860b,stroke-width:2px;
    classDef phys fill:#e8f8ff,stroke:#2980b9,stroke-width:2px;
    classDef sig fill:#fdebd0,stroke:#d35400,stroke-width:2px;

    A["🟨 Couche Liaison de Données<br/>(Trames Ethernet)"]:::link
    B["🔵 Couche Physique<br/>(Transmission des bits)"]:::phys

    S1["📡 Type de signal<br/>Électrique / Optique / Radio"]:::sig
    S2["🔀 Codage des bits<br/>NRZ / Manchester / 4B5B"]:::sig
    S3["📶 Support physique<br/>Cuivre, Fibre, Wi-Fi"]:::sig
    S4["🔌 Connecteurs<br/>RJ45, SFP, antennes"]:::sig
    S5["⚡ Transmission brute des 0 et 1"]:::sig

    A --> B
    B --> S1 --> S2 --> S3 --> S4 --> S5

```
---


```mermaid
graph TD
    classDef bit fill:#e9ffe0,stroke:#27ae60,stroke-width:2px;
    classDef enc fill:#d6f5ff,stroke:#0b79c1,stroke-width:2px;
    classDef wave fill:#ffe0e0,stroke:#c0392b,stroke-width:2px;
    classDef med fill:#fff2cc,stroke:#b8860b,stroke-width:2px;

    B0["🧩 Bits logiques<br/>Suite de 0 et 1"]:::bit
    C1["🔤 Codage physique<br/>NRZ, Manchester, PAM"]:::enc
    W1["📉 Signal transmis<br/>Tension / Lumière / Onde"]:::wave
    M1["🔌 Médium physique<br/>Cuivre, Fibre, Radio"]:::med
    R1["📥 Réception du signal<br/>Décodage inverse"]:::bit

    B0 --> C1 --> W1 --> M1 --> R1

```

---

## 💡 Applications Pratiques
*   **Réseaux [[Ethernet]]**: Standard largement utilisé pour les [[LocalAreaNetwork|réseaux locaux câblés]], définissant les caractéristiques des câbles, des connecteurs et la transmission des signaux.
*   **[[WirelessFidelity|Wi-Fi]] ([[IEEE80211|IEEE 802.11]])**: Ensemble de normes pour les [[WirelessNetwork|réseaux sans fil]], utilisant des [[RadioWaves|ondes radio]] pour la [[WirelessTransmission|transmission de données]].
*   **[[Bluetooth]]**: Technologie sans fil à courte portée pour connecter des [[WirelessDevices|appareils]] personnels.
*   **[[DigitalSubscriberLine|DSL]] et [[CableInternet|Internet par câble]]**: Technologies qui utilisent les [[TelephoneLines|lignes téléphoniques]] ou les [[CoaxialCable|câbles coaxiaux]] pour fournir un accès [[Internet]] à haut débit.

## ✅ Avantages et Limites
*   **Avantages**:
    *   Fournit le fondement matériel indispensable à toute [[NetworkCommunication|communication réseau]].
    *   Permet l'interopérabilité entre différents fabricants de matériel via des normes établies.
    *   Offre potentiellement de très [[Bandwidth|hauts débits]] et une [[Reliability|fiabilité]] sur des liaisons dédiées (ex: fibre optique).
*   **Limites**:
    *   Sensible aux [[ElectromagneticInterference|interférences électromagnétiques]] et à l'atténuation du signal, qui peuvent dégrader la qualité des [[DigitalSignals|signaux numériques]].
    *   Portée limitée par les propriétés physiques du [[NetworkMedia|support]].
    *   Ne gère pas la [[ErrorDetectionAndCorrection|correction d'erreurs]] ni la segmentation des données, ce qui est le rôle des couches supérieures.
    *   Vulnérabilités liées à la [[PhysicalSecurity|sécurité physique]] (coupure de câble, [[Eavesdropping|écoute clandestine]]) qui peuvent compromettre l'[[Availability|disponibilité]] ou la [[Confidentiality|confidentialité]].

## 🔗 Notes Connexes
*   **Couche supérieure**: [[DataLinkLayer|Couche Liaison de Données]]
*   **Technologies associées**: [[Ethernet]], [[WirelessFidelity|Wi-Fi]]
*   **Concept fondamental**: [[NetworkMedia|Supports réseau]]
*   **Aspect connexe**: [[SignalTransmission|Transmission de Signal]]
*   **Menace directe**: [[Eavesdropping|Écoute clandestine]]