---
tags:
  - reseau
  - securite
aliases:
  - Canal de communication
  - Chaîne de communication
  - Voie de communication
  - Communication Channel
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Canal de Communication

## 📥 Définition en une phrase
> Un [[CommunicationChannel|canal de communication]] est le moyen physique ou logique par lequel l'information est transmise d'une entité à une autre, permettant l'échange de [[Message|messages]] entre un émetteur et un récepteur.

## 🧠 Concepts Clés / Piliers
*   **Support de Transmission**: Le [[CommunicationChannel|canal]] peut être un support [[PhysicalNetwork|physique]] comme le [[CopperWire|câble en cuivre]] ou la [[FiberOpticCable|fibre optique]], ou un support [[WirelessMedia|sans fil]] comme les [[RadioWaves|ondes radio]] et les [[Microwaves|micro-ondes]].
*   **Types de Transmission**: Les [[WirelessTransmission|transmissions]] peuvent être [[SimplexCommunication|simplex]] (unidirectionnelle, ex: radio), [[HalfDuplexCommunication|semi-duplex]] (bidirectionnelle alternée, ex: talkie-walkie) ou [[FullDuplexCommunication|duplex intégral]] (bidirectionnelle simultanée, ex: téléphone).
*   **Qualité du Canal**: Sa performance est évaluée par des métriques telles que la [[Bandwidth|bande passante]] (débit maximal), la [[Latency|latence]] (délai de transmission), et est affectée par le [[Noise|bruit]] ou les [[ElectromagneticInterference|interférences électromagnétiques]].
*   **Rôle OSI**: Au sein du [[OpenSystemsInterconnectionModel|modèle OSI]], le [[CommunicationChannel|canal de communication]] est principalement l'objet de la [[PhysicalLayer|Couche Physique]], qui gère les aspects électriques, mécaniques et fonctionnels de la [[SignalTransmission|transmission de signal]].

## 💡 Importance en Cybersécurité
> Le [[CommunicationChannel|canal de communication]] est le vecteur essentiel par lequel toutes les [[Data|données]] transitent, ce qui en fait une cible privilégiée pour les [[ThreatActor|acteurs de menace]]. Sa sécurité est fondamentale pour garantir la [[CIATriad|Triade CIA]] : la [[Confidentiality|confidentialité]] des [[Data|informations]] échangées, l'[[Integrity|intégrité]] de ces [[Data|données]] contre toute altération, et la [[Availability|disponibilité]] des [[NetworkCommunication|communications]] face aux [[DenialOfService|attaques par déni de service]]. Une compromission du [[CommunicationChannel|canal]] peut entraîner des [[DataTheft|vols de données]], des [[SystemCompromise|compromissions de système]] et des interruptions de [[ServiceDisruption|service]].

## 🔗 Notes Connexes
*   [[NetworkCommunication|Communication réseau]]
*   [[SignalTransmission|Transmission de signal]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkMedia|Supports réseau]]
*   [[NetworkProtocol|Protocole réseau]]
*   [[Eavesdropping|Écoute clandestine]]
*   [[ManInTheMiddle|Attaque de l'homme du milieu]]
*   [[DataEncryption|Chiffrement des données]]
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[CIATriad|Triade CIA]]
*   [[ErrorDetectionAndCorrection|Détection et Correction d'Erreurs]]