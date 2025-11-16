---
aliases:
  - Information d'Adressage
  - Adressage
  - Addressing Information
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Information d'Adressage

## 📥 Définition en une phrase
> L'[[AddressingInformation|information d'adressage]] désigne les identifiants uniques (tels que les [[MediaAccessControlAddress|adresses MAC]] et les [[InternetProtocol|adresses IP]]) utilisés par les [[NetworkDevice|dispositifs réseau]] pour localiser et communiquer entre eux au sein d'un [[Network|réseau]] ou sur [[Internet|Internet]].

## 🧠 Concepts Clés / Piliers
*   **Identifiants Uniques**: Chaque [[NetworkDevice|dispositif réseau]] requiert des identifiants spécifiques ([[InternetProtocol|adresses IP]], [[MediaAccessControlAddress|adresses MAC]]) pour être localisé et communiquer efficacement dans un [[Network|réseau]].
*   **Adresses Physiques (MAC)**: Opérant au niveau de la [[DataLinkLayer|couche liaison de données]] du [[OpenSystemsInterconnectionModel|modèle OSI]], les [[MediaAccessControlAddress|adresses MAC]] identifient de manière unique les interfaces réseau au sein d'un [[LocalAreaNetwork|réseau local]] grâce à un identifiant matériel.
*   **Adresses Logiques (IP)**: Utilisées par la [[NetworkLayer|couche réseau]], les [[InternetProtocol|adresses IP]] (telles que [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]]) permettent l'[[IPAddressing|adressage]] et le [[Routing|routage]] des [[Packet|paquets]] à travers différents [[Network|réseaux]] et sur [[Internet|Internet]].
*   **Encapsulation Hiérarchique**: L'[[AddressingInformation|information d'adressage]] est structurée hiérarchiquement et intégrée sous forme d'[[Header|en-têtes]] lors de l'[[Encapsulation|encapsulation]] des [[Data|données]] à travers les [[ProtocolStack|couches de protocoles]] ([[OpenSystemsInterconnectionModel|OSI]] et [[InternetProtocolSuite|TCP/IP]]), indiquant la source et la destination.

## 💡 Importance en Cybersécurité
L'[[AddressingInformation|information d'adressage]] est le fondement de toute [[NetworkCommunication|communication réseau]], permettant l'identification et la localisation des [[NetworkDevice|dispositifs]] pour un [[DataTransmission|acheminement précis des données]]. En [[Cybersecurity|cybersécurité]], sa compréhension est cruciale car elle est la cible de nombreuses [[Attack|attaques]] ([[Spoofing|usurpation]], [[ManInTheMiddle|MITM]]) qui exploitent les faiblesses d'[[AddressingInformation|adressage]] pour compromettre la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] ou l'[[Availability|disponibilité]] des [[System|systèmes]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[Encapsulation|Encapsulation]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[AddressResolutionProtocol|ARP]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[Spoofing|Attaque par usurpation]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[Cybersecurity|Cybersécurité]]