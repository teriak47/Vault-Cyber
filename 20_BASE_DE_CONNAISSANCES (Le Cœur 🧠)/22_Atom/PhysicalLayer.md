---
tags:
  - transmission/signalisation-bits
  - infrastructure/support-transmission
  - securite/blindage-electromagnetique
  - couche/physique
  - modele/osi
  - transmission/mode-physique
aliases:
  - Couche Physique
  - Physical Layer
source:
  - null
cssclasses:
  - max
---

# Couche Physique

## 📥 Définition en une phrase
> La couche physique est la première couche du [[OpenSystemsInterconnectionModel|modèle OSI]], responsable de la transmission et de la réception brutes des données (bits) sur le support physique du réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Support de Transmission**: Définit le type de support utilisé (câbles en cuivre, fibre optique, [[WirelessSignals|ondes radio]]) et ses caractéristiques (bande passante, connecteurs, tensions).
*   **Transmission de Bits**: Gère la conversion des données numériques en signaux analogiques (électriques, optiques, radiofréquences) pour leur propagation et inversement.
*   **Spécifications Matérielles**: Inclut les spécifications mécaniques (câbles, connecteurs), électriques (niveaux de tension, fréquences) et fonctionnelles pour activer, maintenir et désactiver les liens physiques.
*   **Codage et Synchronisation**: Détermine la manière dont les bits sont représentés par les signaux et assure la synchronisation entre l'émetteur et le récepteur.
*   **Topologie Physique**: Influence la disposition physique des appareils sur le réseau (étoile, bus, anneau).

## 🛡️ Risques / Menaces Associés
*   [[PhysicalSecurity|Accès physique non autorisé]] aux infrastructures réseau.
*   [[Eavesdropping|Écoute clandestine]] des transmissions (par exemple, "wiretapping", interception sans fil).
*   [[DenialOfService|Attaques par déni de service]] via la coupure de câbles, le brouillage de signaux ou la surcharge.
*   [[Tampering|Altération ou vol]] d'équipements réseau (hubs, répéteurs, cartes réseau).
*   [[ElectromagneticInterference|Interférences électromagnétiques]] ou acoustiques qui dégradent les signaux.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PhysicalSecurity|Mise en œuvre de contrôles de sécurité physique]] robustes (serrures, caméras, contrôle d'accès aux salles serveurs).
*   [[CableManagement|Gestion et protection adéquate des câbles]] (goulottes, conduits blindés, cheminement sécurisé).
*   [[ElectromagneticShielding|Blindage électromagnétique]] pour protéger contre les interférences et les fuites d'informations (TEMPEST).
*   [[Redundancy|Redondance des liaisons physiques]] et des équipements pour assurer la continuité de service.
*   [[NetworkMonitoring|Surveillance physique]] et environnementale des infrastructures.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkHardware|Matériel Réseau]]
*   [[PhysicalSecurity|Sécurité Physique]]
*   [[NetworkTopology|Topologie Réseau]]