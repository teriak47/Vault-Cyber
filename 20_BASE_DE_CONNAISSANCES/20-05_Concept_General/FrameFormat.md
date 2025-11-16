---
tags:
  - reseau
  - couche/liaison
aliases:
  - Format de Trame
  - Structure de Trame
  - Frame Format
  - Frame Structure
  - Data Frame Format
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Format de Trame

## 📥 Définition en une phrase
> Le [[FrameFormat|format de trame]] est la structure standardisée des [[Data|données]] encapsulées pour la [[DataTransmission|transmission de données]] sur la [[DataLinkLayer|couche liaison de données]] (couche 2 du [[OpenSystemsInterconnectionModel|modèle OSI]]) d'un [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Organisation des Bits**: Le [[FrameFormat|format de trame]] définit la manière dont les [[Bit|bits]] sont organisés pour former une [[Frame|trame]] logique, permettant aux [[NetworkDevice|équipements réseau]] d'interpréter et de traiter correctement les [[Message|messages]] transmis. C'est le squelette qui assure l'[[Interoperability|interopérabilité]] au niveau de la [[DataLinkLayer|couche liaison de données]].
*   **Spécificité Technologique**: Chaque [[WirelessTechnology|technologie sans fil]] ou filaire, comme [[Ethernet|Ethernet]] ou [[WirelessFidelity|Wi-Fi]], possède son propre [[FrameFormat|format de trame]] spécifique. Ces formats sont adaptés aux caractéristiques physiques et logiques du [[NetworkMedia|support réseau]] utilisé et au [[Protocol|protocole]] de la [[DataLinkLayer|couche liaison de données]] en question.
*   **Composants Essentiels**: Une [[Frame|trame]] est composée de plusieurs champs obligatoires, chacun ayant un rôle précis :
    *   **[[Preamble|Préambule]] / [[StartFrameDelimiter|Start-of-Frame Delimiter (SFD)]]**: Utilisé pour synchroniser les horloges de l'émetteur et du récepteur et signaler le début d'une nouvelle [[Frame|trame]].
    *   **[[DestinationMacAddress|Adresses MAC de Destination et Source]]**: Identifient l'[[MediaAccessControlAddress|adresse physique]] unique du destinataire et de l'expéditeur sur le [[NetworkSegment|segment de réseau]] local.
    *   **Type / Longueur**: Indique le [[Protocol|protocole]] de la [[NetworkLayer|couche réseau]] (par exemple, [[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]) qui est encapsulé dans le champ de [[Payload|données]], ou la longueur des [[Payload|données]] elles-mêmes.
    *   **[[Payload|Données]]**: Contient les informations réelles à transporter, souvent un [[Packet|paquet]] de [[NetworkLayer|couche réseau]] (ex: [[InternetProtocol|IP]]).
    *   **[[FrameCheckSequence|Frame Check Sequence (FCS)]] / [[CyclicRedundancyCheck|Cyclic Redundancy Check (CRC)]]**: Un mécanisme de [[Checksum|vérification d'erreurs]] qui permet au récepteur de détecter les corruptions de [[Data|données]] survenues pendant la [[WirelessTransmission|transmission sans fil]] ou filaire.

## 💡 Importance en Cybersécurité
> Le [[FrameFormat|format de trame]] est fondamental pour la [[NetworkCommunication|communication réseau]], mais sa conception présente des [[SecurityVulnerabilities|vulnérabilités de sécurité]] significatives s'il n'est pas correctement géré. Une compréhension et une sécurisation rigoureuses de la [[Frame|structure de trame]] sont essentielles pour prévenir les [[Attack|attaques]] de [[DataLinkLayer|couche liaison de données]], telles que l'[[MACSpoofing|usurpation d'adresse MAC]], l'[[ARPPoisoning|empoisonnement ARP]] ou les [[DenialOfService|attaques par déni de service]]. Des [[SecurityControl|mesures de sécurité]] comme le [[PortSecurity|filtrage des adresses MAC]] sur les [[NetworkSwitch|commutateurs]], la [[NetworkSegmentation|segmentation réseau]] via les [[VirtualLocalAreaNetwork|VLANs]], et la [[NetworkMonitoring|surveillance continue du trafic]] sont cruciales pour maintenir l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] du [[Network|réseau]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[Ethernet|Ethernet]]
*   [[WirelessFidelity|Wi-Fi]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Packet|Paquet]]
*   [[Protocol|Protocole]]
*   [[MACSpoofing|Usurpation d'adresse MAC]]
*   [[DenialOfService|Déni de Service]]
*   [[NetworkAccessControl|Contrôle d'Accès Réseau]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[NetworkMonitoring|Surveillance Réseau]]
*   [[Wireshark|Wireshark]]