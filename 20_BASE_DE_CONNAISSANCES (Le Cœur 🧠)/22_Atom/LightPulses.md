---
tags:
  - impulsion-lumineuse
  - tapotement-fibre
  - chiffrement
aliases:
  - Impulsions Lumineuses
  - Optical Pulses
  - Fibre Optique (transmission)
source:
  - 
cssclasses:
  - max
---

# Impulsions Lumineuses

## 📥 Définition en une phrase
> Les impulsions lumineuses sont la méthode fondamentale de transmission de données à travers les câbles à [[OpticalFiber|Fibre Optique]], où l'information est encodée sous forme de flashs de lumière.

## 🧠 Concepts Clés / Fonctionnement
*   **Encodage Numérique:** Les bits (0 et 1) sont représentés par la présence (impulsion) ou l'absence (pas d'impulsion) de lumière à des intervalles de temps précis.
*   **Transmission Optique:** Ces impulsions voyagent à travers le cœur d'un câble de [[OpticalFiber|Fibre Optique]], guidées par le principe de la réflexion totale interne.
*   **Hautes Vitesses et Bande Passante:** Permettent des débits de données extrêmement élevés sur de longues distances avec une latence minimale, cruciaux pour les backbones internet et les centres de données.
*   **Immunité aux Interférences Électromagnétiques (EMI):** Contrairement aux câbles en cuivre, les fibres optiques sont insensibles aux interférences électromagnétiques, ce qui garantit une transmission de données plus propre et plus stable.

## 🛡️ Risques / Menaces Associés
*   [[FiberTapping|Tapotement de Fibre]]: Interception physique du signal lumineux, souvent difficile à détecter, permettant la copie de données sans altérer le trafic.
*   [[PhysicalDamage|Dommage Physique]]: La rupture ou l'endommagement d'un [[FiberOpticCable|câble à fibre optique]] (par exemple, par des travaux de construction ou des actes malveillants) peut entraîner une [[DenialOfService|interruption de service]] complète.
*   [[SignalDegradation|Dégradation du Signal]]: La perte de puissance du signal sur de très longues distances ou due à des courbures excessives du câble peut entraîner des erreurs de transmission, des pertes de données ou une baisse de performance.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PhysicalSecurity|Sécurité Physique]]: Mettre en place des mesures de sécurité robustes (conduits souterrains, surveillance, contrôle d'accès) pour protéger les infrastructures de câblage.
*   [[Encryption|Chiffrement]]: Utiliser le [[TransportLayerSecurity|chiffrement]] de bout en bout pour protéger la confidentialité et l'intégrité des données transmises, même en cas d'interception.
*   [[Redundancy|Redondance]] et Diversification des Chemins: Déployer des chemins de fibre optique multiples et géographiquement diversifiés pour assurer la continuité du service en cas de défaillance d'un chemin principal.
*   [[OpticalTimeDomainReflectometer|OTDR]]: Utiliser des équipements de test comme les réflectomètres optiques dans le domaine temporel pour détecter les anomalies (coupures, courbures, tentatives de tapotement) le long de la fibre.

## 🔗 Notes Connexes
*   [[OpticalFiberCommunication|Communication par Fibre Optique]]
*   [[PhysicalLayerSecurity|Sécurité de la Couche Physique]]
*   [[DataTransmission|Transmission de Données]]
*   [[TelecommunicationsSecurity|Sécurité des Télécommunications]]