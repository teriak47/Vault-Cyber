---
tags:
  - materiel/carte-reseau
  - reseau/table-mac
  - reseau/adressage-mac
  - couche/liaison-donnees
  - usurpation/adresse-mac
aliases:
  - Adresse MAC Source
  - Source MAC Address
  - Source Media Access Control Address
source:
  - null
cssclasses:
  - max
---

# Adresse MAC Source

## 📥 Définition en une phrase
> L'adresse [[MediaAccessControlAddress|MAC]] source est l'identifiant physique unique de la [[NetworkInterfaceCard|carte réseau]] (NIC) de l'appareil qui initie une communication sur un [[LocalAreaNetwork|réseau local]].

## 🧠 Concepts Clés / Fonctionnement
*   **Identifiant Matériel** : Une adresse MAC est un numéro de série unique, codé en dur par le fabricant dans la NIC, souvent exprimé sous forme hexadécimale (ex: `00:1A:2B:3C:4D:5E`).
*   **Couche 2 du [[OpenSystemsInterconnectionModel|Modèle OSI]]** : Opère au niveau de la [[DataLinkLayer|couche de liaison de données]] (Couche 2), utilisée pour l'adressage physique au sein d'un même segment de réseau.
*   **Identification de l'Expéditeur** : Permet aux [[NetworkSwitch|commutateurs réseau]] d'identifier l'appareil émetteur d'une trame et de construire leurs tables [[ForwardingDatabase|FDB]] (Forwarding Database).
*   **Non Routable** : Contrairement à l'[[InternetProtocolAddress|adresse IP]], l'adresse MAC source n'est pas utilisée pour le routage de paquets entre différents [[Subnet|sous-réseaux]] ou sur Internet ; elle est remplacée à chaque saut par les adresses MAC des routeurs intermédiaires.
*   **Protocole [[AddressResolutionProtocol|ARP]]** : Essentiel pour la résolution entre les adresses IP et les adresses MAC sur un réseau local.

## 🛡️ Risques / Menaces Associés
*   [[MACSpoofing|Usurpation d'adresse MAC]] : Un attaquant peut modifier l'adresse MAC de son interface réseau pour se faire passer pour un autre appareil légitime, contourner des filtres ou masquer son identité.
*   [[DenialOfService|Attaques par déni de service]] (DoS) : En générant un grand nombre de fausses adresses MAC sources, un attaquant peut saturer les tables MAC des [[NetworkSwitch|commutateurs]], entraînant une dégradation des performances ou une attaque de type "[[MACFlooding|MAC Flooding]]".

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] : Configurer les [[NetworkSwitch|commutateurs]] pour n'autoriser qu'un nombre limité d'adresses MAC sur un port donné, ou pour n'autoriser que des adresses MAC spécifiques.
*   [[NetworkAccessControl|Contrôle d'accès réseau]] (NAC) : Utiliser des solutions NAC pour authentifier les appareils connectés et leur accorder l'accès en fonction de leur adresse MAC (entre autres critères).
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) : Surveiller le trafic réseau pour détecter des comportements anormaux liés aux adresses MAC, comme des changements soudains ou des tentatives d'usurpation.

## 🔗 Notes Connexes
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[DestinationMacAddress|Adresse MAC de Destination]]
*   [[AddressResolutionProtocol|ARP]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]