---
tags:
  - protocole
  - norme/ieee8023
  - trame/ethernet
aliases:
  - Délimiteur de Début de Trame
  - Start Frame Delimiter
  - SFD
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Délimiteur de Début de Trame (SFD)

## 🎯 Rôle et Couche OSI
> Le [[StartFrameDelimiter|Délimiteur de Début de Trame]] (SFD) est un champ d'un octet qui suit immédiatement le [[Preamble|Préambule]] dans une [[EthernetFrame|trame Ethernet]]. Son rôle principal est de signaler la fin de la phase de synchronisation au niveau du bit et de marquer le début effectif des données de la [[EthernetFrame|trame]]. Il opère à la [[PhysicalLayer|couche Physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et à la [[NetworkAccessLayer|couche d'Accès Réseau]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
1.  **Localisation**: Le [[StartFrameDelimiter|SFD]] est le huitième et dernier octet de la séquence d'introduction de 8 octets d'une [[EthernetFrame|trame Ethernet]]. Il est positionné juste après le [[Preamble|Préambule]] et précède directement le champ de l'[[DestinationMacAddress|adresse MAC de destination]].
2.  **Fonction de Marquage**: Il agit comme un indicateur clair pour les [[NetworkInterfaceCard|cartes d'interface réseau]] réceptrices, leur signalant que les octets suivants constituent le début des informations importantes de la [[EthernetFrame|trame Ethernet]].
3.  **Modèle Binaire Spécifique**: Le [[StartFrameDelimiter|SFD]] est standardisé et est toujours représenté par le modèle binaire `10101011` (correspondant à la valeur hexadécimale `0xAB`).
4.  **Différenciation avec le Préambule**: Alors que le [[Preamble|Préambule]] se compose de sept octets du modèle `10101010` pour la synchronisation bit-à-bit, le dernier bit du [[StartFrameDelimiter|SFD]] (`1`) rompt cette séquence répétitive. Cette rupture (`...10101010 10101011`) sert de signal distinctif et non ambigu du début de la [[EthernetFrame|trame]].
5.  **Synchronisation au Niveau de l'Octet**: En complément de la synchronisation au niveau du bit initiée par le [[Preamble|Préambule]], le [[StartFrameDelimiter|SFD]] permet aux récepteurs de s'aligner précisément sur les frontières des octets (octets framing) de la [[EthernetFrame|trame]], assurant une interprétation correcte des données suivantes.
*   **Norme**: Le [[StartFrameDelimiter|SFD]] est une composante obligatoire et standardisée de la structure des [[EthernetFrame|trames Ethernet]], telle que définie par la norme [[InstituteOfElectricalAndElectronicsEngineers|IEEE]] [[EthernetProtocol|802.3]].

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**: En tant que marqueur de bas niveau au sein de la [[PhysicalLayer|couche physique]] des [[NetworkProtocol|protocoles réseau]], le [[StartFrameDelimiter|SFD]] lui-même n'est pas directement la cible de [[Attack|vulnérabilités]] logiques spécifiques. Toute [[Attack|attaque]] impliquant le [[StartFrameDelimiter|SFD]] nécessiterait une compromission profonde de la [[PhysicalLayer|couche physique]] ou de la [[DataLinkLayer|couche liaison de données]] pour manipuler ou falsifier les [[EthernetFrame|trames]].
*   **Versions sécurisées**: Il n'existe pas de "version sécurisée" du [[StartFrameDelimiter|SFD]], car sa fonction est un élément fondamental et non modifiable de la spécification [[EthernetProtocol|Ethernet]]. La [[Security|sécurité]] des [[EthernetFrame|trames Ethernet]] est assurée par des mécanismes de sécurité des [[NetworkProtocol|protocoles]] de couches supérieures ou des mesures de [[PhysicalSecurity|sécurité physique]] du [[Network|réseau]].

## 🔗 Notes Connexes
*   [[Preamble|Préambule]]
*   [[EthernetFrame|Trame Ethernet]]
*   [[EthernetProtocol|Protocole Ethernet]]
*   [[PhysicalLayer|Couche Physique]]
*   [[InstituteOfElectricalAndElectronicsEngineers|IEEE 802.3]]
*   [[NetworkAccessLayer|Couche d'Accès Réseau]]
*   [[MediaAccessControlAddress|Adresse MAC]]