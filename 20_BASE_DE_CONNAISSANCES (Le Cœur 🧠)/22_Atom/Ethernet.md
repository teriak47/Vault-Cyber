---
tags:
  - acces-media/csma-cd
  - architecture/reseau-local
  - securite/segmentation-vlan
  - ethernet
  - norme/ieee-802-3
  - couche/liaison-donnees
aliases:
  - Réseau Ethernet
  - IEEE 802.3
  - Ethernet
source:
  - null
cssclasses:
  - max
---

# Ethernet

## 📥 Définition en une phrase
> Ethernet est une famille de technologies réseau standardisées, principalement utilisée pour les [[LocalAreaNetwork|réseaux locaux]] (LAN), qui définit les protocoles et les spécifications physiques pour la transmission de données.

## 🧠 Concepts Clés / Fonctionnement
*   **Standardisation**: Principalement défini par la norme [[IEEE8023|IEEE 802.3]], qui spécifie les couches physique et liaison de données du [[OpenSystemsInterconnectionModel|modèle OSI]].
*   **Trames Ethernet**: Les données sont encapsulées dans des [[EthernetFrame|trames Ethernet]], qui contiennent les adresses [[MediaAccessControlAddress|MAC]] source et destination, les informations de type/longueur, et les données de charge utile.
*   **Accès au média**: Historiquement, Ethernet utilisait [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]] pour gérer l'accès partagé au médium. Aujourd'hui, avec l'utilisation généralisée des [[NetworkSwitch|commutateurs]], la détection de collision est moins pertinente car chaque port de commutateur crée un domaine de collision dédié.
*   **Topologie**: Peut supporter diverses topologies (bus, étoile) mais est majoritairement déployé en étoile avec des commutateurs.
*   **Vitesse et Médias**: Prend en charge une large gamme de vitesses (Fast Ethernet, Gigabit Ethernet, 10 Gigabit Ethernet et plus) et de médias physiques (câbles en paires torsadées, fibre optique).
*   **Couches OSI**: Opère principalement au niveau de la [[PhysicalLayer|couche Physique]] (couche 1) et de la [[DataLinkLayer|couche Liaison de Données]] (couche 2) du modèle OSI.

## 🛡️ Risques / Menaces Associés
*   [[EthernetSpoofing|Usurpation d'adresses MAC]] (MAC Spoofing)
*   [[ARPSpoofing|Usurpation d'ARP]] (ARP Spoofing), permettant des attaques de type [[ManInTheMiddle|homme du milieu]]
*   [[DenialOfService|Attaques par déni de service]] via des inondations de trames ou de tables MAC sur les commutateurs
*   Interception passive du trafic réseau si la [[PhysicalSecurity|sécurité physique]] ou logique est compromise

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation réseau]] à l'aide de [[VirtualLocalAreaNetwork|VLANs]] pour isoler les domaines de diffusion et restreindre l'accès.
*   [[PortSecurity|Sécurité des ports]] sur les commutateurs (ex: limitation des adresses MAC, MAC filtering, DHCP Snooping).
*   Utilisation de [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] (IDS) et de [[IntrusionPreventionSystem|systèmes de prévention d'intrusion]] (IPS) pour surveiller le trafic.
*   Mise en œuvre de la [[PhysicalSecurity|sécurité physique]] pour protéger les commutateurs et les câbles réseau.
*   Application de [[NetworkAccessControl|contrôles d'accès réseau]] (NAC) pour authentifier les périphériques connectés.

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|ARP]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkSwitch|Commutateur]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[TcpIpModel|Modèle TCP/IP]]