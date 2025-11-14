---
tags:
  - securite/sans-fil
  - infrastructure/point-acces
  - reseau
  - sans-fil/wi-fi
aliases:
  - Réseau Local Sans Fil
  - WLAN
  - Wireless Local Area Network
source:
  - 
cssclasses:
  - max
---

# Réseau Local Sans Fil (WLAN)

## 📥 Définition en une phrase
> Un Réseau Local Sans Fil (WLAN) est une technologie réseau qui permet à des appareils de communiquer et d'échanger des données sans fil sur une zone géographique limitée, en utilisant des [[WirelessSignals|ondes radio]] pour créer des connexions.

## 🧠 Concepts Clés / Fonctionnement
*   Basé sur la famille de normes [[IEEE80211|IEEE 802.11]], plus communément connue sous le nom de [[WirelessFidelity|WirelessFidelity]].
*   Permet aux appareils clients (ordinateurs portables, smartphones, IoT) de se connecter à un réseau filaire existant via un [[AccessPoint|Point d'Accès]] (AP) sans nécessiter de câblage physique.
*   Utilise différentes bandes de fréquences radio, notamment 2.4 GHz et 5 GHz, pour la transmission des données.
*   Offre une flexibilité et une mobilité accrues par rapport aux [[LocalAreaNetwork|réseaux locaux]] filaires, permettant aux utilisateurs de se déplacer tout en restant connectés.
*   Chaque [[AccessPoint|Point d'Accès]] diffuse un ou plusieurs [[ServiceSetIdentifier|SSID]] (nom du réseau) pour que les clients puissent s'y connecter.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] des communications si le [[Encryption|chiffrement]] est faible, mal configuré ou absent.
*   [[DenialOfService|Attaques par déni de service]] (DoS) ciblant les points d'accès ou les clients, perturbant la connectivité.
*   [[ManInTheMiddle|Attaques de l'homme du milieu]] via des [[EvilTwinAttack|points d'accès malveillants]] (Evil Twin) qui imitent un réseau légitime.
*   [[RogueAccessPoint|Points d'accès non autorisés]] (Rogue APs) installés par des attaquants ou des employés non autorisés, créant des passerelles non sécurisées vers le réseau interne.
*   [[WarDriving|War Driving]] pour découvrir et cartographier les WLANs vulnérables ou mal sécurisés.
*   Accès non autorisé au réseau par [[BruteForceAttack|force brute]] sur les mots de passe de [[Wi-FiProtectedAccess|WPA/WPA2/WPA3]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser des protocoles d'[[Encryption|Encryption]] robustes tels que [[Wi-FiProtectedAccess|WPA3]] pour protéger la confidentialité et l'intégrité des données.
*   Implémenter des [[StrongAuthentication|mécanismes d'authentification forte]] comme [[8021xAuthentication|IEEE 802.1X]] avec un serveur RADIUS pour l'accès au réseau.
*   [[NetworkSegmentation|Segmenter le réseau]] à l'aide de [[VirtualLocalAreaNetwork|VLAN]] pour isoler le trafic sans fil et limiter l'étendue des compromissions.
*   Déployer des [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion sans fil]] (WIDS) ou [[IntrusionPreventionSystem|de Prévention d'Intrusion sans fil]] (WIPS) pour détecter et bloquer les menaces.
*   Mettre en œuvre des politiques de mots de passe complexes et les changer régulièrement pour les accès aux points d'accès.
*   Désactiver la diffusion du [[ServiceSetIdentifier|SSID]] (bien que ce ne soit pas une mesure de sécurité robuste, elle aide à la discrétion).
*   Mettre à jour régulièrement le firmware des points d'accès et des routeurs sans fil pour corriger les [[Vulnerability|vulnérabilités]] connues.

## 🔗 Notes Connexes
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[WirelessFidelity|WirelessFidelity]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[AccessPoint|Point d'Accès]]
*   [[RadioFrequency|Radiofréquence]]