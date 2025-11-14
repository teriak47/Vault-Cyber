---
tags:
  - protocole/trame-ethernet
  - attaque/inondation-mac
  - norme/ieee-802-3
  - ethernet
  - couche/liaison-donnees
  - reseau/reseau-local
aliases:
  - Protocole Ethernet
  - IEEE 802.3
source:
  - null
cssclasses:
  - max
---

# Protocole Ethernet (IEEE 802.3)

## 📥 Définition en une phrase
> Ethernet est une famille de technologies de mise en réseau informatique standardisée (IEEE 802.3) qui définit la manière dont les données sont transmises et reçues sur un réseau local (LAN) filaire.

## 🧠 Concepts Clés / Fonctionnement
*   **Standard de Fait** : C'est la technologie la plus répandue pour les réseaux locaux (LAN) et souvent utilisée pour les réseaux métropolitains (MAN) et étendus (WAN).
*   **Couches Opérationnelles** : Opère principalement au niveau de la couche liaison de données ([[OpenSystemsInterconnectionModel|couche 2 du modèle OSI]]) pour l'adressage logique (adresses MAC) et au niveau de la couche physique ([[OpenSystemsInterconnectionModel|couche 1]]) pour la transmission des [[ElectricalSignals|signaux électriques]] ou optiques.
*   **Trames Ethernet** : Les données sont encapsulées dans des "trames" (frames) qui contiennent les adresses MAC source et destination, le type de [[Protocols|protocole]] et les données utiles.
*   **Adresses MAC** : Utilise des adresses MAC ([[MediaAccessControlAddress|Media Access Control]]) uniques sur 48 bits pour identifier chaque interface réseau au sein d'un segment de réseau local.
*   **Gestion des Accès** : Historiquement, le [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]] était utilisé pour gérer l'accès au médium partagé. Les réseaux Ethernet modernes, basés sur des [[NetworkSwitch|commutateurs]], fonctionnent généralement en full-duplex, éliminant ainsi les collisions.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] (en particulier sur les réseaux non commutés ou via l'[[ARPPoisoning|empoisonnement ARP]]).
*   [[MACFlooding|MAC Flooding]] : Attaque qui sature la table d'adresses MAC d'un [[NetworkSwitch|commutateur]], le forçant à se comporter comme un hub.
*   [[ARPPoisoning|Empoisonnement ARP]] : Manipulation de la table ARP des hôtes pour intercepter le trafic.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Commutateurs Réseau** : Utilisation de [[NetworkSwitch|commutateurs réseau]] plutôt que de hubs pour segmenter le trafic et isoler les collisions.
*   **[[VirtualLocalAreaNetwork|VLANs]]** : Implémentation de réseaux locaux virtuels (VLAN) pour isoler logiquement le trafic et renforcer la sécurité.
*   **[[PortSecurity|Sécurité des Ports]]** : Configuration de la sécurité des ports sur les [[NetworkSwitch|commutateurs]] pour limiter les adresses MAC autorisées.
*   **Authentification 802.1X** : Contrôle de l'accès au réseau basé sur les utilisateurs et les appareils.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkSwitch|Commutateur Réseau]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[CarrierSenseMultipleAccessWithCollisionDetection|CSMA/CD]]