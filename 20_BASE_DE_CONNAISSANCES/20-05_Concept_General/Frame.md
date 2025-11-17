---
tags:
  - trame
  - trame/ethernet
  - reseau
  - couche/liaison/donnees
  - modele/osi
  - encapsulation
  - protocole
  - communication/reseau
aliases:
  - Trame
  - Cadre de données
  - Frame
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Trame (Frame)

## 📥 Définition en une phrase
> Une trame est une unité de données de protocole (PDU) de la [[DataLinkLayer|couche Liaison de Données]] du [[OpenSystemsInterconnectionModel|modèle OSI]] qui encapsule les données des couches supérieures pour la transmission sur un support physique.

## 🧠 Concepts Clés / Piliers
* **Structure Standardisée**: Chaque trame possède un format précis incluant un en-tête (contenant des informations de contrôle et des [[SourceMacAddress|adresses MAC]] source et [[DestinationMacAddress|destination]]), une charge utile (les données proprement dites), et un "trailer" (généralement une [[FrameCheckSequence|séquence de vérification de trame]]) pour la détection d'erreurs.
* **[[Encapsulation|Encapsulation]]**: Les données provenant des couches supérieures (comme les [[InternetProtocol|paquets IP]] de la [[NetworkLayer|couche Réseau]]) sont encapsulées à l'intérieur de la charge utile de la trame, à laquelle sont ajoutés l'en-tête et le "trailer".
* **Adressage Physique**: Contrairement aux adresses logiques ([[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]) utilisées à la [[NetworkLayer|couche Réseau]], les trames utilisent des [[MediaAccessControlAddress|adresses MAC]] pour identifier les dispositifs sources et destinations au sein d'un même [[LocalAreaNetwork|réseau local]].
* **Détection d'Erreurs**: La [[FrameCheckSequence|séquence de vérification de trame]] (FCS) est un mécanisme intégré dans le "trailer" de la trame, permettant aux dispositifs récepteurs de détecter si des erreurs se sont produites pendant la transmission des données et de rejeter les trames corrompues.

## 💡 Importance en Cybersécurité
> La compréhension des trames est fondamentale en [[Cybersecurity|cybersécurité]] car elles représentent la première couche d'interaction directe avec le réseau physique. L'analyse des trames via des outils de [[PacketSniffing|capture de paquets]] (comme [[Wireshark]]) est essentielle pour la [[NetworkMonitoring|surveillance réseau]], la détection d'[[Attack|attaques]] telles que le [[MACSpoofing|MAC Spoofing]] ou l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]], et le [[Troubleshooting|dépannage]] des problèmes de [[NetworkCommunication|communication réseau]]. Une manipulation ou une falsification des informations contenues dans les trames peut mener à des [[UnauthorizedAccess|accès non autorisés]] ou des [[DenialOfService|dénis de service]].

## 🔗 Notes Connexes
* **Couche d'Opération**: [[DataLinkLayer|Couche Liaison de Données]]
* **Concept d'Emballage**: [[Encapsulation|Encapsulation]]
* **Exemple Spécifique**: [[EthernetFrame|Trame Ethernet]]
* **Identification d'Appareil**: [[MediaAccessControlAddress|Adresse MAC]]
* **Mécanisme de Contrôle**: [[FrameCheckSequence|Séquence de Vérification de Trame]]