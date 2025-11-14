---
tags:
  - concept
aliases:
  - Couche d'Accès Réseau
  - Network Access Layer
source:
  - ComparaisonModeleOsiEtModeleTcpip_Cour.md
cssclasses:
  - max
---

# Couche d'Accès Réseau

## 📥 Définition en une phrase
> La couche d'accès réseau est le niveau le plus bas du [[InternetProtocolSuite|modèle TCP/IP]], combinant les fonctions des [[PhysicalLayer|couches physique]] et [[DataLinkLayer|liaison de données]] du [[OpenSystemsInterconnectionModel|modèle OSI]] pour gérer la transmission physique des [[Data|données]] et l'accès au [[NetworkMedia|support réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   **Intégration OSI** : Elle regroupe les fonctionnalités de la [[PhysicalLayer|couche physique]] (spécifications matérielles, transmission de [[DigitalSignals|signaux numériques]] ou [[ElectricalSignals|électriques]]) et de la [[DataLinkLayer|couche liaison de données]] (adressage [[MediaAccessControlAddress|MAC]], contrôle d'erreur, contrôle d'accès au support) du [[OpenSystemsInterconnectionModel|modèle OSI]].
*   **Transmission de Données** : Cette couche est responsable de la transmission des [[DataFrames|trames de données]] entre les [[NetworkDevice|périphériques réseau]] sur un [[LocalAreaNetwork|réseau local]] ou un [[CommunicationChannel|canal de communication]] direct.
*   **Adressage MAC** : Elle utilise les [[MediaAccessControlAddress|adresses MAC]] pour identifier de manière unique les [[NetworkInterfaceCard|cartes réseau]] des [[EndDevices|terminaux]] au sein d'un même [[BroadcastDomain|domaine de diffusion]].
*   **Support Physique** : Elle interagit directement avec le [[NetworkMedia|support réseau]] tel que les [[CopperWire|câbles de cuivre]] (ex: [[TwistedPair|paires torsadées]], [[CoaxialCable|câbles coaxiaux]]), la [[FiberOpticCable|fibre optique]] (via [[LightPulses|impulsions lumineuses]]) ou l'[[WirelessTransmission|air]] (via [[RadioWaves|ondes radio]], [[Microwaves|micro-ondes]], [[InfraredWaves|ondes infrarouges]]).

## 🛡️ Risques / Menaces Associés
*   [[MACSpoofing|Usurpation d'adresse MAC]] : Un attaquant peut modifier son [[MediaAccessControlAddress|adresse MAC]] pour se faire passer pour un autre [[NetworkDevice|dispositif]] sur le [[Network|réseau]].
*   [[AddressResolutionProtocolPoisoning|Empoisonnement ARP]] : L'attaquant envoie de fausses réponses [[AddressResolutionProtocol|ARP]] pour associer son [[InternetProtocolAddress|adresse IP]] à l'[[MediaAccessControlAddress|adresse MAC]] d'une [[Gateway|passerelle]] ou d'un autre [[Host|hôte]], facilitant les attaques [[ManInTheMiddle|homme du milieu]].
*   [[Eavesdropping|Écoute clandestine]] : Sur les [[WirelessTransmission|réseaux sans fil]] ou les [[Hub|concentrateurs]] (plutôt que les [[NetworkSwitch|commutateurs]]), un attaquant peut intercepter les [[NetworkCommunication|communications réseau]].
*   [[DenialOfService|Attaques par déni de service]] : Surcharge du [[NetworkDevice|périphérique réseau]] (ex: [[NetworkSwitch|commutateur]]) avec un trafic excessif ou de fausses informations.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] : Configurer les [[NetworkSwitch|commutateurs]] pour limiter le nombre d'[[MediaAccessControlAddress|adresses MAC]] autorisées par [[PortNumber|port]] et réagir aux violations (arrêt du port, alerte).
*   [[NetworkSegmentation|Segmentation réseau]] : Utiliser des [[VirtualLocalAreaNetwork|VLANs]] pour isoler les [[Network|réseaux]] et limiter la portée des attaques locales.
*   [[DynamicHostConfigurationProtocol|DHCP]] Snooping et [[AddressResolutionProtocol|ARP]] Inspection Dynamique : Des fonctionnalités de [[NetworkSwitch|commutateur]] qui aident à prévenir les attaques d'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]] et de [[DynamicHostConfigurationProtocol|DHCP]] non autorisées.
*   [[WirelessSecurity|Sécurité sans fil]] : Mettre en œuvre des protocoles de [[WirelessSecurity|sécurité robustes]] tels que [[WirelessProtectedAccessTwo|WPA2]] ou [[WirelessProtectedAccessThree|WPA3]] pour les [[WirelessTransmission|réseaux sans fil]].
*   Surveillance du [[Log|trafic réseau]] : Utilisation de [[IntrusionDetectionSystem|IDS]] ou [[SecurityInformationAndEventManagement|SIEM]] pour détecter les activités suspectes au niveau de cette couche.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[PhysicalLayer|Couche Physique]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[NetworkLayer|Couche Réseau]]
*   [[MediaAccessControlAddress|Adresse MAC]]