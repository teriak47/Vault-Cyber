---
tags:
  - usurpation/adresse-mac
  - reseau/segment-local
  - reseau/adressage-mac
  - couche-liaison
aliases:
  - Adresse MAC
  - MAC
  - Media Access Control Address
source:
  - 
cssclasses:
  - max
---

# Adresse MAC (MAC)

## 📥 Définition en une phrase
> Une adresse MAC (Media Access Control) est un identifiant unique attribué de manière permanente à une interface réseau pour les communications au sein d'un segment de réseau local.

## 🧠 Concepts Clés / Fonctionnement
*   **Identifiant Unique :** Chaque [[NetworkInterfaceCard|carte réseau]] (NIC) se voit attribuer une adresse MAC unique par le fabricant.
*   **Format :** C'est une adresse de 48 bits (6 octets), généralement représentée sous forme hexadécimale, séparée par des deux-points ou des tirets (ex: `00:1A:2B:3C:4D:5E`).
*   **Couche 2 (Modèle OSI) :** Opère au niveau de la couche liaison de données ([[OpenSystemsInterconnectionModel|couche 2 du modèle OSI]]), gérant l'adressage physique et l'accès au média partagé.
*   **Organisation Unique Identifier (OUI) :** Les trois premiers octets de l'adresse MAC identifient le fabricant de la carte réseau (l'OUI), tandis que les trois derniers sont un numéro de série unique attribué par le fabricant.
*   **Non Routable :** Contrairement aux adresses IP, les adresses MAC ne sont pas utilisées pour le routage entre différents réseaux. Elles sont utilisées uniquement pour identifier les hôtes sur un même segment de réseau local.
*   **[[AddressResolutionProtocol|ARP]] :** Le protocole ARP est utilisé pour résoudre une adresse IP en une adresse MAC correspondante sur un réseau local.

## 🛡️ Risques / Menaces Associés
*   [[MacSpoofing|Usurpation d'adresse MAC (MAC Spoofing)]] : Un attaquant modifie son adresse MAC pour se faire passer pour un autre appareil, contourner les contrôles d'accès ou masquer son identité.
*   [[ArpSpoofing|Empoisonnement ARP (ARP Spoofing)]] : L'attaquant envoie de fausses réponses ARP pour associer son adresse MAC à l'adresse IP d'une [[Gateway|passerelle]] ou d'un autre hôte, interceptant ainsi le trafic.
*   Évasion de filtres réseau basés sur les adresses MAC.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkAccessControl|Contrôle d'accès réseau]] (NAC) : Authentifie les appareils avant de leur permettre l'accès au réseau, rendant plus difficile l'utilisation d'adresses MAC falsifiées.
*   [[PortSecurity|Sécurité des ports]] (Port Security) sur les commutateurs : Limite le nombre d'adresses MAC qui peuvent apprendre sur un port spécifique et peut associer statiquement une adresse MAC à un port.
*   Surveillance du réseau pour détecter les adresses MAC inhabituelles ou multiples sur un même port.
*   Utilisation de [[VirtualLocalAreaNetwork|VLANs]] pour segmenter les réseaux et limiter la portée des attaques basées sur les adresses MAC.

## 🔗 Notes Connexes
*   [[AddressResolutionProtocol|Protocole de Résolution d'Adresses (ARP)]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[NetworkInterfaceCard|Carte d'Interface Réseau (NIC)]]
*   [[InternetProtocolAddress|Adresse IP]]