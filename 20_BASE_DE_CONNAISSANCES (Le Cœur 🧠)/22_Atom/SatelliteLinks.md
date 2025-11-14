---
tags:
  - communication-satellitaire
  - mitigation-brouillage
  - sécurité-stations-terrestres
  - signal-transmission
  - satellite
  - intrusion-detection-system
aliases:
  - Liaisons satellitaires
  - Communications par satellite
  - Satellite Links
cssclasses:
  - max
---

# Liaisons Satellitaires

## 📥 Définition en une phrase
> Les liaisons satellitaires désignent la [[SignalTransmission|transmission de signaux]] et de données via des [[Satellite|satellites]] artificiels en orbite terrestre, permettant une [[WirelessTransmission|communication sans fil]] sur de vastes zones, y compris les régions éloignées.

## 🧠 Concepts Clés / Fonctionnement
*   Utilisation de [[RadioWaves|ondes radio]] pour la [[SignalTransmission|transmission de signaux]] entre des [[GroundStation|stations terrestres]] et un ou plusieurs [[Satellite|satellites]].
*   Les [[Satellite|satellites]] sont positionnés sur différentes orbites, telles que l'orbite [[GeosynchronousOrbit|géosynchrone (GEO)]], l'orbite [[LowEarthOrbit|terrestre basse (LEO)]] ou l'orbite [[MediumEarthOrbit|terrestre moyenne (MEO)]], chacune offrant des caractéristiques de latence et de couverture différentes.
*   Les [[GroundStation|stations terrestres]] sont équipées d'[[Antenna|antennes]] paraboliques pour envoyer (liaison montante ou "uplink") et recevoir (liaison descendante ou "downlink") les signaux des [[Satellite|satellites]].
*   Ces systèmes offrent une couverture globale, essentielle pour l'[[Internet|Internet]], la télévision, la navigation GPS et les télécommunications dans des zones non desservies par les infrastructures terrestres.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Interception]] des signaux : Les [[RadioWaves|ondes radio]] peuvent être interceptées si les communications ne sont pas suffisamment chiffrées, compromettant la [[Confidentiality|confidentialité]].
*   [[DenialOfService|Déni de service (DoS)]] : Les liaisons satellitaires peuvent être ciblées par du [[Jamming|brouillage]] (intentionnel ou accidentel) ou une surcharge de trafic.
*   [[SpoofingAttack|Usurpation]] de signaux : Un attaquant peut émettre de faux signaux pour tromper les récepteurs ou perturber la [[Integrity|intégrité]] des données transmises.
*   [[DataCorruption|Corruption de données]] : Des interférences ou des attaques peuvent altérer les données transitant par la liaison.
*   [[Vulnerability|Vulnérabilités]] physiques : Les infrastructures des [[GroundStation|stations terrestres]] ou les [[Satellite|satellites]] eux-mêmes peuvent être sujets à des attaques physiques ou des pannes matérielles, impactant la [[Availability|disponibilité]] du service.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DataEncryption|Chiffrement des données]] : Utiliser des algorithmes de [[Encryption|chiffrement]] robustes (ex: AES) pour protéger la [[Confidentiality|confidentialité]] des communications satellitaires.
*   [[Authentication|Authentification]] forte : Mettre en place des mécanismes d'[[Authentication|authentification]] pour vérifier l'identité des terminaux et des utilisateurs accédant au réseau.
*   [[NetworkSecurity|Sécurité réseau]] des [[GroundStation|stations terrestres]] : Appliquer des politiques de [[NetworkSecurity|sécurité réseau]] rigoureuses, y compris la segmentation, les [[Firewall|pare-feu]] et les [[IntrusionDetectionSystem|systèmes de détection d'intrusion]].
*   Contrôles physiques : Protéger physiquement les [[GroundStation|stations terrestres]] et les équipements critiques contre l'accès non autorisé.
*   Techniques anti-[[Jamming|brouillage]] : Employer des technologies comme l'étalement de spectre ou la fréquence agile pour atténuer les effets du brouillage.

## 🔗 Notes Connexes
*   [[WirelessTransmission|Transmission sans fil]]
*   [[RadioWaves|Ondes Radio]]
*   [[NetworkCommunication|Communication réseau]]
*   [[InternetServiceProvider|Fournisseur d'Accès Internet]]
*   [[Cybersecurity|Cybersécurité]]