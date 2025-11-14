---
tags:
  - couche/physique
  - traitement/trame
  - synchronisation-bits
  - ethernet
  - transmission/synchronisation
  - trame/delimiteur-debut
aliases:
  - Préambule
  - Ethernet Preamble
source:
  - Ethernet Standard
cssclasses:
  - max
---

# Préambule Ethernet

## 📥 Définition en une phrase
> Le préambule Ethernet est une séquence de bits au début d'une [[EthernetFrame|trame Ethernet]] utilisée pour la synchronisation du signal entre les périphériques d'émission et de réception.

## 🧠 Concepts Clés / Fonctionnement
*   Le préambule se compose de 7 octets (56 bits) de 10101010 répétés, suivis d'un [[StartFrameDelimiter|délimiteur de début de trame (SFD)]] d'un octet (10101011).
*   Il est généré par la [[NetworkInterfaceCard|carte réseau (NIC)]] émettrice et sert à préparer la NIC réceptrice à l'arrivée de la trame réelle en synchronisant son horloge avec le flux de bits entrant.
*   Le préambule et le SFD ne sont pas considérés comme faisant partie des données réelles de la trame et ne sont généralement pas comptabilisés dans sa taille.
*   Ils sont généralement retirés par la carte réseau réceptrice avant que la trame ne soit traitée par les couches supérieures du modèle [[OpenSystemsInterconnectionModel|OSI]].
*   Sur les réseaux à 10 Mbps, le préambule est crucial pour la synchronisation bit par bit ; sur les réseaux plus rapides, il est toujours présent pour la compatibilité mais la synchronisation est souvent gérée par des mécanismes plus sophistiqués au niveau de la [[PhysicalLayer|couche physique]].

## 🛡️ Risques / Menaces Associés
*   [[Desynchronization|Désynchronisation]] : Une mauvaise synchronisation due à des problèmes de signal ou de support physique peut entraîner la perte ou la corruption de la trame.
*   [[DataCorruption|Corruption de Données]] : Sans une synchronisation correcte, la carte réseau réceptrice pourrait mal interpréter les bits de la trame.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[QualityCabling|Câblage de Qualité]] : Utiliser des câbles réseau conformes aux normes pour minimiser les interférences et les pertes de signal.
*   [[ProperNetworkHardware|Matériel Réseau Approprié]] : Assurer l'utilisation de cartes réseau et d'équipements actifs (switches, routeurs) conformes aux normes Ethernet.

## 🔗 Notes Connexes
*   [[EthernetFrame|Trame Ethernet]]
*   [[StartFrameDelimiter|Start Frame Delimiter (SFD)]]
*   [[PhysicalLayer|Couche Physique]]
*   [[NetworkInterfaceCard|Carte Réseau (NIC)]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]