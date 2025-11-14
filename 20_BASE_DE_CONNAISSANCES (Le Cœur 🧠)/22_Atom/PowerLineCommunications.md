---
tags:
  - power-line-communications
  - cpl
  - network-media
  - acces/non-autorise
  - electromagnetic-interference
  - attacks-dos
aliases:
  - Power Line Communications
  - CPL
  - Communications par Courants Porteurs en Ligne
source:
  - null
cssclasses:
  - max
---

# Communications par Courants Porteurs en Ligne (CPL)

## 📥 Définition en une phrase
> La [[PowerLineCommunications|CPL]] est une technologie permettant la [[DataTransmission|transmission de données]] via les lignes électriques existantes, transformant le câblage électrique en un [[Network|réseau de communication]].

## 🧠 Concepts Clés / Fonctionnement
*   Utilise le câblage électrique domestique ou industriel comme [[NetworkMedia|support de transmission réseau]].
*   Les [[Data|données]] numériques sont modulées sur des [[ElectricalSignals|signaux électriques]] à haute fréquence, puis injectées sur le réseau électrique.
*   Permet d'étendre la [[Network|connectivité réseau]] sans installer de nouveaux câbles dédiés à la [[NetworkCommunication|communication réseau]].
*   Existe en deux catégories principales : [[PowerLineCommunications|CPL]] bas débit (pour le contrôle et l'automatisation) et [[PowerLineCommunications|CPL]] haut débit (pour l'accès [[Internet|Internet]] et les [[LocalAreaNetwork|réseaux locaux]]).
*   La [[Modulation|modulation]] des signaux permet de superposer les informations aux courants électriques standard (50/60 Hz) sans interférence.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute Clandestine]]: Les signaux [[PowerLineCommunications|CPL]] peuvent parfois "fuir" du réseau électrique et être captés par des dispositifs externes ou des voisins sur le même circuit électrique.
*   [[UnauthorizedAccess|Accès Non Autorisé]]: Sans [[Encryption|chiffrement]] ou configuration sécurisée, un attaquant ayant accès au même circuit électrique (par exemple, dans un appartement voisin) pourrait intercepter ou injecter des [[Data|données]] sur le [[LocalAreaNetwork|réseau local]].
*   [[ElectromagneticInterference|Interférence Électromagnétique]] (EMI): La technologie [[PowerLineCommunications|CPL]] peut elle-même générer des interférences avec d'autres équipements électroniques ou radiofréquences, et sa performance peut être dégradée par le bruit électrique ambiant.
*   [[DenialOfService|Déni de Service]] (DoS): Des interférences importantes ou une surcharge du réseau électrique peuvent perturber la [[NetworkCommunication|communication CPL]], entraînant une [[ServiceDisruption|interruption de service]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Activer le [[Encryption|chiffrement]] intégré (souvent AES 128 bits) sur les adaptateurs [[PowerLineCommunications|CPL]] pour protéger la [[Confidentiality|confidentialité]] des [[Data|données]].
*   Changer le [[Password|mot de passe]] par défaut des adaptateurs [[PowerLineCommunications|CPL]] pour prévenir l'[[UnauthorizedAccess|accès non autorisé]] à la configuration.
*   Utiliser la fonction de jumelage (pairing) des adaptateurs pour s'assurer que seuls les [[NetworkDevice|dispositifs]] autorisés peuvent communiquer sur le [[Network|réseau CPL]].
*   Maintenir le [[Firmware|micrologiciel]] des adaptateurs à jour pour corriger les [[Vulnerability|vulnérabilités]] connues et améliorer la [[Security|sécurité]].
*   Considérer la [[PhysicalSecurity|sécurité physique]] des adaptateurs [[PowerLineCommunications|CPL]] pour empêcher toute manipulation ou remplacement par des [[NetworkDevice|dispositifs]] malveillants.

## 🔗 Notes Connexes
*   [[NetworkMedia|Support de transmission réseau]]
*   [[ElectricalSignals|Signaux Électriques]]
*   [[Network|Réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[WirelessTechnology|Technologie sans fil]]
*   [[Ethernet|Ethernet]]
*   [[DataTransmission|Transmission de Données]]
*   [[PhysicalSecurity|Sécurité Physique]]