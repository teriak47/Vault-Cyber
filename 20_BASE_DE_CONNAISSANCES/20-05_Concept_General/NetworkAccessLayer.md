---
tags:
aliases:
  - Couche d'Accès Réseau
  - Network Access Layer
  - NetworkAccessLayer
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche d'Accès Réseau (Network Access Layer)

## 📥 Définition en une phrase
> La couche d'accès réseau est le niveau le plus bas du [[InternetProtocolSuite|modèle TCP/IP]], combinant les fonctions des [[PhysicalLayer|couches physique]] et [[DataLinkLayer|liaison de données]] du [[OpenSystemsInterconnectionModel|modèle OSI]] pour gérer la [[DataTransmission|transmission physique des données]] et l'accès au [[NetworkMedia|support réseau]].

## 🧠 Concepts Clés / Piliers
*   **Intégration des Fonctions OSI** : Cette couche fusionne les responsabilités de la [[PhysicalLayer|couche physique]] (définition des spécifications [[Hardware|matérielles]], [[SignalTransmission|transmission]] d'[[ElectricalSignals|impulsions électriques]] ou d'[[OpticalSignals|impulsions lumineuses]]) et de la [[DataLinkLayer|couche liaison de données]] (adressage [[MediaAccessControlAddress|MAC]], contrôle des erreurs et accès au [[NetworkMedia|support réseau]]) des [[OpenSystemsInterconnectionModel|modèles OSI]].
*   **Transmission et Encapsulation des Trames** : Elle est directement responsable de l'[[Encapsulation|encapsulation]] des [[Packet|paquets]] en [[DataFrames|trames de données]] et de leur [[DataTransmission|transmission]] entre [[NetworkDevice|périphériques réseau]] au sein d'un même [[LocalAreaNetwork|réseau local]] ou sur un [[CommunicationChannel|canal de communication]] direct.
*   **Adressage et Contrôle d'Accès au Support** : Elle utilise les [[MediaAccessControlAddress|adresses MAC]] pour identifier de manière unique les [[NetworkInterfaceCard|cartes d'interface réseau]] des [[EndDevices|dispositifs terminaux]] et pour gérer l'[[AccessControl|accès]] partagé au [[PhysicalNetwork|réseau physique]], notamment dans un [[BroadcastDomain|domaine de diffusion]].
*   **Interface avec le Support Physique** : Elle interagit directement avec divers [[NetworkMedia|supports réseau]], incluant les [[CopperWire|câbles de cuivre]] (comme les [[TwistedPair|paires torsadées]] et les [[CoaxialCable|câbles coaxiaux]]), la [[FiberOpticCable|fibre optique]] (par [[LightPulses|impulsions lumineuses]]) et l'[[WirelessTransmission|air]] (via les [[RadioWaves|ondes radio]], [[Microwaves|micro-ondes]] ou [[InfraredWaves|ondes infrarouges]]).

## 💡 Importance en Cybersécurité
> La couche d'accès réseau est fondamentale en [[Cybersecurity|cybersécurité]] car elle constitue le point d'entrée physique et logique des [[Data|données]] sur le [[Network|réseau]]. Les [[ThreatActor|acteurs de menace]] ciblent souvent cette couche pour des [[Reconnaissance|reconnaissances]], l'[[Eavesdropping|interception de trafic]] ou des [[DenialOfService|attaques par déni de service]], ce qui en fait un maillon critique pour la [[NetworkSecurity|sécurité réseau]] et la [[Confidentiality|confidentialité]] des [[Data|données]]. Une [[Security|sécurité]] robuste à ce niveau est essentielle pour prévenir l'[[UnauthorizedAccess|accès non autorisé]] et maintenir l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[CommunicationChannel|communications réseau]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkLayer|Couche Réseau]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[MACSpoofing|Usurpation d'adresse MAC]]
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]]
*   [[ManInTheMiddle|Attaque de l'homme du milieu]]
*   [[PortSecurity|Sécurité des ports]]
*   [[NetworkSegmentation|Segmentation réseau]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[DynamicHostConfigurationProtocol|DHCP]] Snooping (méthode de [[NetworkSecurity|sécurité réseau]] liée à [[DynamicHostConfigurationProtocol|DHCP]])
*   [[AddressResolutionProtocol|ARP]] Inspection Dynamique (méthode de [[NetworkSecurity|sécurité réseau]] liée à [[AddressResolutionProtocol|ARP]])
*   [[WirelessSecurity|Sécurité sans fil]]
*   [[WirelessProtectedAccessTwo|WPA2]]
*   [[WirelessProtectedAccessThree|WPA3]]
*   [[NetworkMonitoring|Surveillance réseau]]
*   [[IntrusionDetectionSystem|IDS]]
*   [[SecurityInformationAndEventManagement|SIEM]]