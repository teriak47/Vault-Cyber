---
tags:
  - man-in-the-middle
  - canal-de-communication
  - réseau/communication
  - couche/physique
  - chiffrement
aliases:
  - Canal de communication
  - Chaîne de communication
  - Voie de communication
source:
  - null
cssclasses:
  - max
---

# Canal de Communication

## 📥 Définition en une phrase
> Un canal de communication est le moyen physique ou logique par lequel l'information est transmise d'une entité à une autre.

## 🧠 Concepts Clés / Fonctionnement
*   Un canal établit la connexion entre un émetteur et un récepteur pour permettre l'échange de [[Message|messages]].
*   Il peut être physique (ex: [[CopperWire|câble en cuivre]], [[FiberOpticCable|fibre optique]], [[RadioWaves|ondes radio]]) ou logique (ex: un [[NetworkProtocol|protocole réseau]] sur un [[Network|réseau]]).
*   La qualité et la fiabilité d'un canal sont affectées par des facteurs tels que la [[Bandwidth|bande passante]], la [[Latency|latence]] et le bruit.
*   Les canaux peuvent être unidirectionnels (simplex), semi-duplex (transmission alternée) ou duplex intégral (transmission simultanée).
*   La [[PhysicalLayer|Couche Physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]] est principalement concernée par les caractéristiques des canaux de communication physiques.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : Interception non autorisée des données transitant sur le canal.
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] : Un attaquant intercepte et potentiellement modifie les communications entre deux parties.
*   [[DataCorruption|Corruption de données]] : Erreurs ou altérations des données pendant la [[SignalTransmission|transmission de signal]].
*   [[DenialOfService|Déni de service]] : Surcharge ou perturbation du canal rendant la communication impossible.
*   [[PrivacyInvasion|Invasion de la vie privée]] : Fuite d'informations sensibles via un canal non sécurisé.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataEncryption|Chiffrement des données]] : Assurer la [[Confidentiality|confidentialité]] des informations transmises.
*   Utilisation de [[NetworkProtocol|protocoles réseau]] sécurisés (ex: [[SecureSocketLayer|SSL]]/[[SecureSocketsLayer|TLS]]).
*   [[SecurityControl|Contrôles de sécurité]] physiques : Protéger les [[NetworkMediaTypes_Cour|supports réseau]] physiques contre l'accès non autorisé.
*   [[ErrorDetectionAndCorrection|Détection et Correction d'Erreurs]] : Mécanismes pour maintenir l'[[Integrity|intégrité]] des données.
*   [[NetworkSegmentation|Segmentation réseau]] : Isoler les communications sensibles sur des canaux dédiés.

## 🔗 Notes Connexes
*   [[NetworkCommunication|Communication réseau]]
*   [[SignalTransmission|Transmission de signal]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkMediaTypes_Cour|Types de supports réseau]]
*   [[NetworkProtocol|Protocole réseau]]