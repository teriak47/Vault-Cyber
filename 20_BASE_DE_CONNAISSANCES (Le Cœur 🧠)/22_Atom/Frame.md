---
tags:
  - transmission/delimitation-trame
  - securite/inspection-arp-dynamique
  - trame/remorque
  - couche/liaison-donnees
  - ethernet/trame
  - reseau/encapsulation
aliases:
  - Trame
  - Cadre de données
source:
  - null
cssclasses:
  - max
---

# Trame (Frame)

## 📥 Définition en une phrase
> Une trame est l'unité de données de la couche liaison de données ([[DataLinkLayer|couche 2]] du [[OpenSystemsInterconnectionModel|modèle OSI]]) qui encapsule des informations provenant de la couche supérieure (souvent un [[Packet|paquet IP]]) pour sa transmission sur un médium physique.

## 🧠 Concepts Clés / Fonctionnement
*   **Encapsulation**: Une trame encapsule des données de la [[NetworkLayer|couche réseau]] (généralement des [[Packet|paquets]]) en y ajoutant un en-tête et une remorque ([[Trailer]]).
*   **Adresses Physiques**: L'en-tête de la trame contient les [[MediaAccessControlAddress|adresses MAC]] source et destination, utilisées pour l'acheminement local sur un segment de réseau.
*   **Structure**: Elle se compose généralement d'un préambule (synchronisation), d'un en-tête (adresses, type de [[Protocols|protocole]]), de la charge utile (données encapsulées) et d'une remorque (séquence de contrôle de trame pour la détection d'erreurs, ex: [[CyclicRedundancyCheck|CRC]]).
*   **Protocoles**: Les protocoles de couche 2, tels que [[Ethernet]] ou [[WirelessFidelity]], définissent la structure et les mécanismes de gestion des trames.
*   **Délimitation**: Les trames sont délimitées par des séquences spécifiques de bits pour permettre aux récepteurs d'identifier le début et la fin de chaque trame.

## 🛡️ Risques / Menaces Associés
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu]] (interception et manipulation de trames).
*   [[DenialOfService|Attaques par déni de service]] (inondation de trames, saturation du réseau).
*   [[MACSpoofing|Usurpation d'adresse MAC]] (modification de l'adresse MAC source pour contourner les contrôles d'accès).
*   [[VLANHopping|Saut de VLAN]] (contournement de la segmentation réseau via la manipulation de trames).

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] sur les commutateurs pour limiter les adresses MAC autorisées.
*   [[NetworkSegmentation|Segmentation réseau]] via des [[VirtualLocalAreaNetwork|VLANs]] pour isoler les domaines de diffusion.
*   Utilisation de protocoles sécurisés comme [[DynamicARPInspection|DAI]] (Dynamic ARP Inspection) pour prévenir l'[[AddressResolutionProtocolSpoofing|usurpation d'ARP]].
*   Implémentation de [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] (IDS) et [[IntrusionPreventionSystem|IPS]] pour surveiller le trafic de couche 2.
*   [[Encryption|Chiffrement]] du trafic sans fil (ex: [[WPA3]]) pour protéger les trames radio.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[Ethernet]]
*   [[Packet|Paquet]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[AddressResolutionProtocol|ARP]]