---
tags:
  - reseau
  - unite-de-donnees
aliases:
  - Trame
  - Cadre de données
  - Frame
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Trame (Frame)

## 🎯 Rôle et Couche OSI
> Une [[Frame|trame]] est l'unité de [[DataTransmission|données]] de base au niveau de la [[DataLinkLayer|couche liaison de données]] ([[DataLinkLayer|couche 2]]) du [[OpenSystemsInterconnectionModel|modèle OSI]]. Son rôle principal est d'[[Encapsulation|encapsuler]] les [[Packet|paquets IP]] ou autres [[Protocol|protocoles]] de [[NetworkLayer|couche réseau]] pour leur [[SignalTransmission|transmission]] fiable sur un [[NetworkMedia|support physique]] au sein d'un [[NetworkSegment|segment de réseau]] local.

## ⚙️ Fonctionnement
1.  **[[Encapsulation]]**: Une [[Frame|trame]] prend les [[Data|données]] (généralement un [[Packet|paquet]]) de la [[NetworkLayer|couche réseau]] et y ajoute un [[Header|en-tête]] et une [[Trailer|remorque]] spécifiques à la [[DataLinkLayer|couche de liaison de données]].
2.  **Adressage Physique**: L'[[Header|en-tête]] contient les [[MediaAccessControlAddress|adresses MAC]] source et destination, essentielles pour l'[[Unicast|acheminement local]] de la [[Frame|trame]] entre [[NetworkDevice|dispositifs]] sur le même [[BroadcastDomain|domaine de diffusion]].
3.  **Structure**: La [[Frame|trame]] typique inclut :
    *   Un [[Preamble|préambule]] (pour la synchronisation).
    *   Un [[Header|en-tête]] (contenant les [[SourceMacAddress|adresses MAC source]] et [[DestinationMacAddress|destination]], le type de [[Protocol|protocole]] encapsulé).
    *   La [[Payload|charge utile]] (les [[Data|données]] de la [[NetworkLayer|couche supérieure]]).
    *   Une [[FrameCheckSequence|séquence de vérification de trame]] (FCS), souvent un [[CyclicRedundancyCheck|CRC]], pour détecter les [[DataCorruption|erreurs de transmission]].
4.  **Délimitation et [[Protocol|Protocoles]]**: Des séquences de [[Bit|bits]] spécifiques ([[StartFrameDelimiter|délimiteurs]]) marquent le début et la fin de la [[Frame|trame]], permettant aux [[NetworkDevice|dispositifs]] de la reconnaître. Des [[NetworkProtocol|protocoles]] comme [[Ethernet]] et [[WirelessFidelity|Wi-Fi]] définissent la [[FrameFormat|structure]] et les règles de [[DataTransmission|transmission]] des [[Frame|trames]].

## 🛡️ Sécurité liée aux Trames
* **Vulnérabilités connues**:
  *   [[ManInTheMiddle|Attaques de l'homme du milieu]] : Interception, modification ou retransmission de [[Frame|trames]] sur le [[NetworkSegment|segment réseau]].
  *   [[DenialOfService|Attaques par déni de service]] : Inondation du [[Network|réseau]] avec un grand nombre de [[Frame|trames]] pour saturer les [[NetworkDevice|équipements]] (ex: [[NetworkSwitch|commutateurs]]) ou la [[Bandwidth|bande passante]].
  *   [[MACSpoofing|Usurpation d'adresse MAC]] : Un [[ThreatActor|attaquant]] modifie l'[[MediaAccessControlAddress|adresse MAC source]] de ses [[Frame|trames]] pour se faire passer pour un autre [[Host|hôte]] légitime, contournant les [[AccessControl|contrôles d'accès]].
  *   [[VLANHopping|Saut de VLAN]] : Manipulation de [[Frame|trames]] pour accéder à des [[VirtualLocalAreaNetwork|VLANs]] non autorisés.
  *   [[AddressResolutionProtocolPoisoning|Usurpation d'ARP]] : Envoi de fausses [[AddressResolutionProtocolRequest|requêtes ARP]] pour associer l'[[InternetProtocol|adresse IP]] d'un [[Host|hôte]] légitime à l'[[MediaAccessControlAddress|adresse MAC]] de l'[[ThreatActor|attaquant]].
* **Mesures de Protection**: Pour atténuer les [[SecurityVulnerabilities|vulnérabilités]] au niveau des [[Frame|trames]] et de la [[DataLinkLayer|couche liaison de données]], les stratégies suivantes sont recommandées :
  *   [[PortSecurity|Sécurité des ports]] : Configuration des [[NetworkSwitch|commutateurs]] pour limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] autorisées par [[LANPort|port]] et prévenir l'[[MACSpoofing|usurpation d'adresse MAC]].
  *   [[NetworkSegmentation|Segmentation réseau]] avec des [[VirtualLocalAreaNetwork|VLANs]] : Isolation logique des [[NetworkSegment|segments réseau]] pour réduire le [[AttackSurface|domaine de diffusion]] et limiter la propagation des [[Attack|attaques]].
  *   [[DynamicARPInspection|DAI]] (Dynamic [[AddressResolutionProtocol|ARP]] Inspection) : Protection contre l'[[AddressResolutionProtocolPoisoning|usurpation d'ARP]] en validant les [[AddressResolutionProtocol|paquets ARP]] par rapport aux informations DHCP.
  *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] ([[IntrusionDetectionSystem|IDS]]) et [[IntrusionPreventionSystem|systèmes de prévention d'intrusion]] ([[IntrusionPreventionSystem|IPS]]) : Surveillance du [[NetworkTrafficAnalysis|trafic]] de [[DataLinkLayer|couche 2]] pour détecter et bloquer les [[Attack|attaques]] basées sur les [[Frame|trames]].
  *   [[WirelessSecurity|Sécurité sans fil]] robuste : Utilisation de [[WirelessProtectedAccessThree|WPA3]] ou [[WirelessProtectedAccessTwo|WPA2]] avec [[Encryption|chiffrement]] fort pour protéger les [[WirelessSignals|trames radio]] contre l'[[Eavesdropping|interception]] et la manipulation.

## 🔗 Notes Connexes
* [[OpenSystemsInterconnectionModel|Modèle OSI]]
* [[DataLinkLayer|Couche Liaison de Données]]
* [[Ethernet]]
* [[Packet|Paquet]]
* [[MediaAccessControlAddress|Adresse MAC]]
* [[VirtualLocalAreaNetwork|VLAN]]
* [[AddressResolutionProtocol|ARP]]
* [[WirelessFidelity|Wi-Fi]]
* [[Wireshark]]