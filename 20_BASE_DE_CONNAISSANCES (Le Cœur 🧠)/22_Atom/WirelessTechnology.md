---
tags:
  - technologie-sans-fil
  - frequence-radio
  - segmentation-reseau
  - sans-fil/wi-fi
  - sans-fil/bluetooth
  - securite/chiffrement
aliases:
  - Technologie sans fil
  - Wireless Technology
source: null
cssclasses:
  - max
---

# Technologie Sans Fil (Wireless Technology)

## 📥 Définition en une phrase
> Ensemble de technologies permettant la communication entre des dispositifs sans l'utilisation de câbles physiques, s'appuyant sur des ondes radio, des ondes millimétriques ou d'autres formes de rayonnement électromagnétique pour transmettre des données.

## 🧠 Concepts Clés / Fonctionnement
* Utilise des [[RadioFrequency|ondes radio]] (RF), [[Infrared|infrarouge]], ou des micro-ondes pour la transmission de données.
* Nécessite des émetteurs et des récepteurs pour moduler et démoduler les signaux.
* Caractérisée par sa portée, sa bande passante et sa sensibilité aux interférences environnementales.
* Inclut diverses normes et protocoles comme le [[WirelessFidelity]], [[Bluetooth]], [[NearFieldCommunication|NFC]] et les [[CellularNetwork|réseaux cellulaires]].
* La communication est diffusée dans l'air, la rendant accessible à quiconque se trouve à portée.

## 🛡️ Risques / Menaces Associés
* [[Eavesdropping|Écoute clandestine]] et [[TrafficSniffing|interception de trafic]] si les communications ne sont pas chiffrées.
* [[UnauthorizedAccess|Accès non autorisé]] au réseau via des [[RogueAccessPoint|points d'accès non sécurisés]] ou non légitimes.
* [[DenialOfService|Attaques par déni de service]] (DoS) par brouillage des fréquences ou saturation du réseau.
* [[ManInTheMiddle|Attaques de l'homme du milieu]] (MitM) facilitées par la nature broadcast des ondes.
* Vulnérabilités dans les protocoles de chiffrement (ex: anciennes versions de WEP/WPA).

## 💎 Mesures de Protection / Bonnes Pratiques
* Implémentation de [[WirelessEncryption|chiffrement fort]] pour toutes les communications (ex: [[WPA3|WPA3]] pour le [[WirelessFidelity]]).
* Utilisation d'une [[StrongAuthentication|authentification forte]] (ex: [[8021X|802.1X]] avec [[MultiFactorAuthentication|MFA]]).
* [[NetworkSegmentation|Segmentation réseau]] pour isoler les réseaux sans fil et limiter l'accès aux ressources critiques.
* Désactivation des [[ServiceSetIdentifier|SSID]] de diffusion pour réduire la visibilité (bien que cela n'offre pas une sécurité robuste).
* Mises à jour régulières du firmware des équipements sans fil pour corriger les [[Vulnerability|vulnérabilités]].
* [[SiteSurvey|Audits réguliers]] et [[VulnerabilityAssessment|évaluations de vulnérabilité]] des infrastructures sans fil.

## 🔗 Notes Connexes
* [[WirelessFidelity|Wi-Fi]]
* [[Bluetooth|Bluetooth]]
* [[RadioFrequency|Radiofréquence]]
* [[NetworkSecurity|Sécurité Réseau]]
* [[Cryptography|Cryptographie]]