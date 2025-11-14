---
tags:
  - adresses-mac
  - adresses-ip
  - encapsulation-osi
  - adressage
  - adressage/ip-mac
  - segmentation-reseau
aliases:
  - Information d'Adressage
  - Adressage
source:
  - null
cssclasses:
  - max
---

# Information d'Adressage

## 📥 Définition en une phrase
> L'information d'adressage désigne les identifiants uniques (tels que les [[MediaAccessControlAddress|adresses MAC]] et les [[InternetProtocolAddress|adresses IP]]) utilisés par les dispositifs réseau pour localiser et communiquer entre eux au sein d'un [[Network|réseau]] ou sur [[Internet|Internet]].

## 🧠 Concepts Clés / Fonctionnement
*   **Identification des Dispositifs** : Chaque dispositif connecté à un [[Network|réseau]] possède une adresse unique qui lui permet d'être identifié.
*   **Adresses Physiques ([[DataLinkLayer|Couche Liaison de Données]])** : Les [[MediaAccessControlAddress|adresses MAC]] sont des identifiants matériels gravés dans l'interface réseau, utilisées pour la communication au sein d'un [[LocalAreaNetwork|LAN]]. Elles sont essentielles pour le fonctionnement de la [[DataLinkLayer|couche liaison de données]].
*   **Adresses Logiques ([[NetworkLayer|Couche Réseau]])** : Les [[InternetProtocolAddress|adresses IP]] (notamment [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]]) sont des identifiants logiques attribués aux dispositifs, permettant la [[NetworkCommunication|communication réseau]] à travers différents [[Network|réseaux]] et [[Internet|Internet]]. Elles sont gérées par la [[NetworkLayer|couche réseau]].
*   **Rôle dans l'[[Encapsulation|Encapsulation]]** : Les informations d'adressage sont ajoutées aux paquets de données (sous forme d'[[Header|en-têtes]]) lors de l'[[Encapsulation|encapsulation]] à chaque couche du [[OpenSystemsInterconnectionModel|modèle OSI]] ou [[ProtocolStack|pile de protocoles]] [[ComparaisonModeleOsiEtModeleTcpip_Cour|TCP/IP]], indiquant la source et la destination du message.

## 🛡️ Risques / Menaces Associés
*   [[SpoofingAttack|Usurpation d'adresse]] (IP ou MAC) : Un attaquant peut falsifier son [[InternetProtocolAddress|adresse IP]] ou son [[MediaAccessControlAddress|adresse MAC]] pour se faire passer pour un autre dispositif.
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MITM)]] : L'attaquant intercepte et potentiellement modifie le trafic en se plaçant entre deux dispositifs, souvent en manipulant les informations d'adressage.
*   [[Eavesdropping|Écoute clandestine]] : Sans [[Encryption|chiffrement]], l'information d'adressage peut révéler des détails sur les points de terminaison de la communication, facilitant l'interception.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation réseau]] : L'utilisation de VLANs ou de sous-réseaux pour isoler le trafic et limiter la portée des attaques basées sur l'adressage.
*   [[PortSecurity|Sécurité des ports]] : Configurer les [[NetworkSwitch|commutateurs réseau]] pour associer des [[MediaAccessControlAddress|adresses MAC]] spécifiques à des [[EthernetPorts|ports Ethernet]] physiques, empêchant l'[[SpoofingAttack|usurpation d'adresse MAC]].
*   [[Encryption|Chiffrement]] : Protéger le contenu des messages pour empêcher l'exploitation des informations révélées par l'adressage.
*   [[IntrusionDetectionSystem|IDS]] / [[IntrusionPreventionSystem|IPS]] : Déployer des systèmes pour détecter et prévenir les anomalies liées aux informations d'adressage (ex: [[AddressResolutionProtocolPoisoning|ARP Poisoning]]).

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkAddressTranslation|Network Address Translation (NAT)]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[AddressResolutionProtocol|ARP]]