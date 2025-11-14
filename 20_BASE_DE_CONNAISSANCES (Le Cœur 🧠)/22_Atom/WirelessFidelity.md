---
tags:
  - norme/ieee-802-11
  - protocole/wpa3
  - reseau
  - securite/sans-fil
aliases:
  - Wi-Fi
  - WiFi
  - Wireless Fidelity
  - Réseau sans fil
  - IEEE 802.11
source:
  - https://www.wi-fi.org/
cssclasses:
  - max
---

# Wi-Fi (Wireless Fidelity)

## 📥 Définition en une phrase
> Le Wi-Fi est une famille de technologies de réseau local sans fil (WLAN) basée sur les normes [[IEEE80211|IEEE 802.11]], permettant aux appareils de communiquer sans câble via des [[WirelessSignals|ondes radio]].

## 🧠 Concepts Clés / Fonctionnement
*   **Standards IEEE 802.11**: Différentes versions (a, b, g, n, ac, ax/Wi-Fi 6, be/Wi-Fi 7) spécifiant les fréquences, les débits et les méthodes de modulation.
*   **Fréquences**: Utilise principalement les bandes de fréquences 2.4 GHz, 5 GHz et plus récemment 6 GHz (pour le [[WiFi6E|Wi-Fi 6E]] et [[WiFi7|Wi-Fi 7]]).
*   **Modes de Fonctionnement**:
    *   **Mode Infrastructure**: Le plus courant, où les appareils se connectent à un [[AccessPoint|Point d'Accès]] (AP) qui sert de pont vers un réseau filaire.
    *   **Mode Ad-hoc**: Connexion directe entre deux appareils sans point d'accès central, moins courant et moins sécurisé.
*   **Sécurité**: Historiquement WEP (obsolète), puis WPA, [[WirelessProtectedAccessTwo|WPA2]] et désormais [[WPA3|WPA3]], utilisant des protocoles de chiffrement et d'authentification pour sécuriser les communications.
*   **SSID (Service Set Identifier)**: Nom du réseau Wi-Fi, diffusé ou masqué, permettant aux appareils de l'identifier et de s'y connecter.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfServiceAttack|Attaques par déni de service (DoS)]] via désauthentification.
*   [[EvilTwinAttack|Attaques de l'homme du milieu (Evil Twin)]] par la création de points d'accès malveillants.
*   [[BruteForceAttack|Attaques par force brute]] sur les clés pré-partagées (WPA/WPA2-PSK).
*   [[Eavesdropping|Interception des données]] si le chiffrement est faible ou absent.
*   [[Vulnerability|Vulnérabilités]] protocolaires (ex: KRACK sur WPA2).
*   [[UnauthorizedAccess|Accès non autorisé]] à un réseau interne via un point d'accès mal configuré.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser la dernière version de sécurité disponible : [[WPA3|WPA3]] est fortement recommandé.
*   Mettre en place des [[StrongPassword|mots de passe forts]] et complexes pour l'accès au réseau.
*   Désactiver la fonctionnalité [[WPS|WPS (Wi-Fi Protected Setup)]] en raison de ses faiblesses.
*   Mettre à jour régulièrement le firmware des [[AccessPoint|points d'accès]] et routeurs.
*   Utiliser la [[NetworkSegmentation|segmentation réseau]] (ex: [[VirtualLocalAreaNetwork|VLANs]]) pour isoler le trafic invité du réseau interne.
*   Mettre en œuvre des [[WirelessIntrusionDetectionSystem|Systèmes de Détection d'Intrusion Sans Fil (WIDS)]].
*   Désactiver le SSID Broadcast si une sécurité par obscurité est souhaitée (à compléter par d'autres mesures).
*   Utiliser un [[VirtualPrivateNetwork|VirtualPrivateNetwork]] pour chiffrer les communications sur des réseaux Wi-Fi publics non fiables.

## 🔗 Notes Connexes
*   [[IEEE80211|Standard IEEE 802.11]]
*   [[WirelessLocalAreaNetwork|Réseau Local Sans Fil (WLAN)]]
*   [[WPA3|WPA3]]
*   [[WirelessSecurity|Sécurité Sans Fil]]
*   [[AccessPoint|Point d'Accès]]
*   [[Bluetooth|Bluetooth]]
*   [[Ethernet|Ethernet]]