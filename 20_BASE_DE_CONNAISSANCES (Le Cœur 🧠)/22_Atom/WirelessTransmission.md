---
tags:
  - scalabilite-reseau-sans-fil
  - attaque-mitm
  - wireless-media
  - wifi-standards
  - bluetooth
  - mobile
  - securite/chiffrement
aliases:
  - Transmission sans fil
  - Communication sans fil
  - Wireless communication
source:
  - null
cssclasses:
  - max
---

# Transmission Sans Fil

## 📥 Définition en une phrase
> La [[WirelessTransmission|transmission sans fil]] est une méthode de transfert d'informations et de données entre deux ou plusieurs points sans l'utilisation de conducteurs électriques physiques, de câbles optiques ou d'autres supports filaires, en s'appuyant plutôt sur les [[RadioWaves|ondes radio]], les [[Microwaves|micro-ondes]] ou les [[InfraredWaves|ondes infrarouges]].

## 🧠 Concepts Clés / Fonctionnement
*   Utilise différentes fréquences du spectre électromagnétique pour transmettre des [[ElectricalSignals|signaux électriques]] via l'air, l'espace ou d'autres milieux non-filaires.
*   Les technologies courantes incluent le [[IEEE80211|Wi-Fi]], le [[Bluetooth|Bluetooth]], les réseaux cellulaires ([[MobileCommunicationTechnologies_Cour|2G/3G/4G/5G]]) et les systèmes satellitaires.
*   La conversion des [[ElectricalPulses|impulsions électriques]] en [[RadioWaves|ondes radio]] (ou autres types d'ondes) se fait par des transmetteurs, et la reconversion par des récepteurs.
*   Offre une grande [[Scalability|évolutivité]] et [[Mobility|mobilité]], permettant aux appareils de se connecter à un [[Network|réseau]] ou entre eux sans contraintes physiques de câbles.
*   Est l'un des types de [[NetworkMedia|supports réseau]], contrastant avec la [[TwistedPair|paire torsadée]], le [[CopperWire|câble de cuivre]] ou le [[FiberOpticCable|câble à fibre optique]].

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : La diffusion des signaux dans l'air rend les transmissions vulnérables à l'interception par des entités non autorisées si elles ne sont pas chiffrées.
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu]] ([[MITM]]) : Un attaquant peut intercepter et potentiellement modifier la communication entre deux parties.
*   [[DenialOfService|Déni de Service]] ([[DoS]]) : L'interférence ou la surcharge du spectre sans fil peut empêcher les utilisateurs légitimes d'accéder au service.
*   [[MAC Spoofing|Usurpation d'adresse MAC]] : Les attaquants peuvent masquer leur identité en utilisant une [[MediaAccessControlAddress|adresse MAC]] falsifiée.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] fort : Utiliser des protocoles de [[Encryption|chiffrement]] robustes (ex: WPA3 pour le [[IEEE80211|Wi-Fi]]) pour protéger la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des données.
*   [[AccessControl|Contrôle d'accès]] strict : Implémenter l'[[MultiFactorAuthentication|MFA]] et des politiques d'[[AccessControl|accès]] pour restreindre l'accès aux réseaux sans fil.
*   [[NetworkSecurity|Sécurité réseau]] physique : Positionner les [[AccessPoint|points d'accès]] de manière sécurisée et désactiver les [[PublicAccessPoint|points d'accès publics]] non nécessaires.
*   [[NetworkSegmentation|Segmentation réseau]] : Séparer les réseaux sans fil (ex: invités, IoT) des réseaux internes pour limiter l'impact d'une compromission.

## 🔗 Notes Connexes
*   [[RadioWaves|Ondes Radio]]
*   [[Microwaves|Micro-ondes]]
*   [[InfraredWaves|Ondes Infrarouges]]
*   [[WirelessAndWiredTechnologies_Cour|Technologies Sans Fil et Filaire]]
*   [[IEEE80211|IEEE 802.11]]
*   [[MobileCommunicationTechnologies_Cour|Technologies de Communication Mobile]]
*   [[MobileWirelessSecurity_Cour|Sécurité Sans Fil Mobile]]