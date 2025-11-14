---
tags:
  - reseau/topologie
  - reseau/classification/geographique
  - infrastructure/equipements-actifs
  - modele/osi
  - cyberattaque/deni-service
  - securite/segmentation-reseau
aliases:
  - Réseau
  - Computer Network
  - Networking
source:
  - null
cssclasses:
  - max
---

# Réseau Informatique

## 📥 Définition en une phrase
> Un réseau informatique est un ensemble de dispositifs interconnectés (ordinateurs, serveurs, périphériques) permettant l'échange de données et le partage de ressources.

## 🧠 Concepts Clés / Fonctionnement
*   **Topologie :** La disposition physique ou logique des éléments d'un réseau (ex: étoile, bus, anneau, maille).
*   **Protocoles :** Des ensembles de règles standardisées qui régissent la communication entre les dispositifs (ex: [[TransmissionControlProtocolInternetProtocol|TCP/IP]], HTTP, FTP).
*   **Équipements :** Composants matériels essentiels tels que les routeurs, les commutateurs ([[NetworkSwitch|Switch]]), les points d'accès ([[WirelessAccessPoint|WAP]]) et les câbles.
*   **Modèle OSI :** Un cadre conceptuel à sept couches qui décrit comment les applications réseau communiquent sur un réseau (ex: [[OpenSystemsInterconnectionModel|Couche Physique]], [[DataLinkLayer|Couche Liaison de Données]], [[NetworkLayer|Couche Réseau]]).
*   **Adresses IP :** Identifiants numériques uniques attribués à chaque dispositif connecté pour permettre leur localisation et leur routage sur le réseau.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS/DDoS)]]
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]]
*   [[NetworkScanning|Balayage de réseau]] et [[PortScanning|Scan de ports]]
*   [[UnauthorizedAccess|Accès non autorisé]]
*   [[Eavesdropping|Écoute clandestine]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Pare-feu]] : Contrôle le trafic entrant et sortant.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion (IPS)]] : Surveillent les activités malveillantes.
*   [[VirtualPrivateNetwork|VPN]] : Crée une connexion sécurisée et chiffrée sur un [[PublicNetwork|réseau public]].
*   [[NetworkSegmentation|Segmentation réseau]] : Divise le réseau en sous-réseaux isolés pour limiter la propagation des attaques.
*   [[AccessControl|Contrôle d'accès]] strict : Gère qui peut accéder à quelles ressources réseau.
*   Chiffrement des communications : Protège la confidentialité et l'intégrité des données en transit.

## 🔗 Notes Connexes
*   [[LocalAreaNetwork|LAN]]
*   [[WideAreaNetwork|WAN]]
*   [[MetropolitanAreaNetwork|MAN]]
*   [[WirelessLocalAreaNetwork|WLAN]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[TransmissionControlProtocolInternetProtocol|TCP/IP]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]