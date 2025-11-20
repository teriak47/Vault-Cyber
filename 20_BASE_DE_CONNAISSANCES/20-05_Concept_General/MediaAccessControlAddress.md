---
tags:
  - reseau
  - identification
  - couche/liaison/donnees
  - securite
aliases:
  - Adresse MAC
  - MAC
  - Media Access Control Address
  - MAC address
archetype: concept-general
source:
cssclasses:
  - max
---

# Adresse MAC (Media Access Control)

## 🎯 Rôle et Couche OSI
> L'adresse MAC est un identifiant unique attribué de manière permanente à une interface réseau pour les communications au sein d'un segment de réseau local. Elle opère au niveau de la couche liaison de données (couche 2 du modèle OSI).

## ⚙️ Caractéristiques et Fonctionnement
1.  **Identifiant Unique Permanent**: Chaque carte réseau (NIC) se voit attribuer une adresse MAC unique par le fabricant, souvent gravée dans le micrologiciel de l'appareil.
2.  **Format**: Il s'agit d'une adresse de 48 bits (6 octets), généralement représentée sous forme hexadécimale, séparée par des deux-points ou des tirets (ex: `00:1A:2B:3C:4D:5E`).
3.  **Organisation Unique Identifier (OUI)**: Les trois premiers octets de l'adresse MAC identifient le fabricant de la carte réseau (l'OUI), tandis que les trois derniers sont un numéro de série unique attribué par ce fabricant.
4.  **Non Routable**: Contrairement aux adresses IP, les adresses MAC ne sont pas utilisées pour le routage entre différents réseaux distants. Elles servent uniquement à identifier les hôtes sur un même segment de réseau local.
5.  **Interaction avec ARP**: Le protocole de résolution d'adresse (ARP) est fondamental pour l'utilisation des adresses MAC. Il permet de résoudre une adresse IP logique en une adresse MAC physique correspondante sur un réseau local.

## 🛡️ Sécurité et Menaces
*   **Usurpation d'Adresse MAC (MAC Spoofing)**: Un acteur de menace modifie son adresse MAC pour se faire passer pour un autre appareil. Cela peut être utilisé pour contourner les contrôles d'accès (ex: filtrage d'adresses MAC) ou masquer l'identité de l'attaquant.
*   **Empoisonnement ARP (ARP Poisoning)**: L'attaquant envoie de fausses réponses ARP pour associer son adresse MAC à l'adresse IP d'une passerelle par défaut ou d'un autre hôte. Cette attaque de l'homme du milieu permet d'intercepter et potentiellement de modifier le trafic réseau.
*   **Évasion de filtres réseau**: Le MAC spoofing peut être utilisé pour contourner les filtres basés sur les adresses MAC, permettant un accès non autorisé à un réseau ou à des ressources.

## ✅ Mesures de Protection
*   **Contrôle d'Accès Réseau (NAC)**: Authentifie les appareils avant de leur permettre l'accès au réseau. Cela rend l'utilisation d'adresses MAC falsifiées plus difficile, car l'appareil doit également passer d'autres vérifications (ex: authentification de l'utilisateur ou de l'appareil).
*   **Sécurité des Ports**: Sur les commutateurs réseau, cette fonctionnalité permet de limiter le nombre d'adresses MAC qui peuvent être apprises sur un port spécifique. Elle peut également associer statiquement une adresse MAC à un port, bloquant ainsi toute autre adresse MAC.
*   **Surveillance réseau et Analyse du Trafic**: Des outils de surveillance peuvent détecter les adresses MAC inhabituelles ou multiples sur un même port, signalant une potentielle attaque de MAC spoofing ou d'empoisonnement ARP.
*   **VLANs**: L'utilisation de réseaux locaux virtuels permet la segmentation des réseaux, ce qui limite la portée des attaques basées sur les adresses MAC à un seul VLAN plutôt qu'à l'ensemble du réseau local.

## 🔗 Notes Connexes
*   Protocole de Résolution d'Adresses (ARP)
*   Modèle OSI
*   Couche Liaison de Données
*   Réseau Local (LAN)
*   Carte d'Interface Réseau (NIC)
*   Adresse IP
*   Usurpation d'Adresse MAC (MAC Spoofing)
*   Empoisonnement ARP (ARP Poisoning)
*   Contrôle d'Accès Réseau (NAC)