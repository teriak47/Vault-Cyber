---
tags:
  - securite/securite-port
  - cybersécurité/empoisonnement-arp
  - materiel/commutateur
  - couche-liaison
aliases:
  - Commutateur réseau
  - Switch
  - Network Switch
source:
  - Base de connaissances
cssclasses:
  - max
---

# Commutateur Réseau (Switch)

## 📥 Définition en une phrase
> Un commutateur réseau (switch) est un équipement de niveau 2 (couche liaison de données) du modèle OSI qui connecte des appareils au sein d'un [[LocalAreaNetwork|réseau local (LAN)]] en transmettant le trafic de manière intelligente et efficace en fonction des [[MediaAccessControlAddress|adresses MAC]].

## 🧠 Concepts Clés / Fonctionnement
*   **Fonctionnement de Couche 2** : Opère sur la [[DataLinkLayer|couche liaison de données]] (OSI), utilisant les [[MediaAccessControlAddress|adresses MAC]] pour prendre des décisions de transfert.
*   **Table d'Adresses MAC** : Apprend et maintient une table des adresses MAC des périphériques connectés à chaque port pour diriger les trames vers leur destination spécifique.
*   **Micro-segmentation** : Crée un [[CollisionDomain|domaine de collision]] distinct pour chaque port, ce qui réduit les collisions et améliore les performances par rapport à un [[Hub|concentrateur (hub)]].
*   **Full-Duplex** : Permet la transmission et la réception simultanées de données sur chaque port.
*   **[[VirtualLocalAreaNetwork|VLANs]]** : Prend en charge la segmentation logique du réseau en créant des [[VirtualLocalAreaNetwork|réseaux locaux virtuels]] (VLANs) pour isoler le trafic entre différents groupes d'utilisateurs ou de périphériques.

## 🛡️ Risques / Menaces Associés
*   [[MACFlooding|Attaques de flooding MAC]] : Saturation de la table MAC du commutateur, le forçant à se comporter comme un hub.
*   [[ARPPoisoning|Empoisonnement ARP]] : Peut être utilisé pour rediriger le trafic à travers un attaquant, même si le commutateur est configuré pour la sécurité.
*   [[PhysicalSecurity|Accès physique non autorisé]] : L'accès direct à un commutateur peut permettre la manipulation des configurations ou l'interception du trafic.
*   [[DenialOfService|Attaques par déni de service (DoS)]] : Ciblent les ressources du commutateur pour perturber la connectivité réseau.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des ports]] : Limiter le nombre d'adresses MAC par port, lier des adresses MAC spécifiques à des ports, ou désactiver les ports inutilisés.
*   [[VirtualLocalAreaNetwork|Segmentation du réseau avec des VLANs]] : Isoler le trafic sensible et restreindre la communication entre différents segments.
*   [[AccessControl|Contrôles d'accès]] : Mettre en place des mécanismes d'authentification (ex: [[8021x|802.1X]]) pour autoriser uniquement les périphériques légitimes à se connecter.
*   [[NetworkMonitoring|Surveillance du réseau]] : Utiliser des outils de surveillance pour détecter les comportements anormaux ou les tentatives d'attaque.
*   [[FirmwareUpdate|Mises à jour régulières du firmware]] : Appliquer les patchs de sécurité pour corriger les vulnérabilités connues.

## 🔗 Notes Connexes
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[Router|Routeur]]
*   [[Hub|Concentrateur (Hub)]]
*   [[DataLinkLayer|Couche Liaison de Données (OSI)]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[VirtualLocalAreaNetwork|Réseau Local Virtuel (VLAN)]]
*   [[SpanningTreeProtocol|Protocole Spanning Tree (STP)]]