---
tags:
  - propagation-radio
  - modulation-radio
  - spectre-electromagnetique
  - sans-fil/wi-fi
  - securite/chiffrement
  - securite/authentification
aliases:
  - Ondes Radio
  - Radio Waves
source:
  - null
cssclasses:
  - max
---

# Ondes Radio

## 📥 Définition en une phrase
> Les ondes radio sont un type d'ondes électromagnétiques, faisant partie du spectre électromagnétique, utilisées pour la transmission sans fil d'informations sur de courtes ou longues distances.

## 🧠 Concepts Clés / Fonctionnement
*   **Propagation** : Elles peuvent se propager dans le vide et dans l'air, voyageant à la vitesse de la lumière.
*   **Fréquence et Longueur d'Onde** : Caractérisées par leur fréquence (nombre d'oscillations par seconde, mesurée en Hertz) et leur longueur d'onde (distance entre deux crêtes successives). Ces deux propriétés sont inversement proportionnelles.
*   **Modulation** : Les informations (audio, vidéo, données) sont encodées sur l'onde porteuse via des techniques de modulation (amplitude, fréquence, phase).
*   **Applications** : Elles sont la base de nombreuses technologies sans fil telles que la [[RadioCommunication|radio diffusion]], la [[Television|télévision]], les [[MobileCommunication|communications mobiles]] (téléphonie cellulaire), le [[WirelessFidelity|Wi-Fi]], le [[Bluetooth|Bluetooth]], le [[GlobalPositioningSystem|GPS]] et les [[RadarSystem|systèmes radar]].
*   **Spectre Électromagnétique** : Elles occupent la partie basse fréquence du [[ElectromagneticSpectrum|spectre électromagnétique]].

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] : Interception des transmissions sans fil, notamment si elles ne sont pas chiffrées.
*   [[DenialOfService|Déni de Service]] (brouillage) : Interférence volontaire ou involontaire qui empêche la réception des signaux radio légitimes.
*   [[ReplayAttack|Attaque par rejeu]] : Capture et retransmission de signaux radio authentiques pour manipuler un système (ex: ouverture de portes de garage, désactivation d'alarmes).
*   [[SideChannelAttack|Attaques par canaux auxiliaires]] : Exploitation des émissions électromagnétiques parasites pour extraire des [[SensitiveData|informations sensibles]] (ex: cryptographie).

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] des Communications : Utilisation de protocoles de chiffrement robustes (ex: WPA3 pour le Wi-Fi, TLS/SSL pour les communications sur réseau) pour protéger la confidentialité.
*   [[Authentication|Authentification]] Forte : Mise en place de mécanismes d'authentification pour s'assurer que seuls les appareils et utilisateurs autorisés peuvent transmettre ou recevoir.
*   [[FrequencyHoppingSpreadSpectrum|Saut de fréquence]] et [[SpreadSpectrum|étalement de spectre]] : Techniques pour rendre les transmissions plus résilientes aux interférences et plus difficiles à intercepter.
*   Gestion de la puissance d'émission : Limiter la portée des signaux pour réduire la zone d'exposition aux menaces.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] sans fil : Pour identifier les activités anormales ou les tentatives de brouillage.

## 🔗 Notes Connexes
*   [[WirelessCommunication|Communication Sans Fil]]
*   [[ElectromagneticSpectrum|Spectre Électromagnétique]]
*   [[Antenna|Antenne]]
*   [[SignalJamming|Brouillage de Signal]]