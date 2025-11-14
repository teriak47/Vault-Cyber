---
tags:
  - reseau/reseau-etendu
  - infrastructure/telecoms
  - reseau
  - cybersécurité
aliases:
  - Réseau Étendu
  - WAN
  - Wide Area Network
source:
  - 
cssclasses:
  - max
---

# Réseau Étendu (WAN)

## 📥 Définition en une phrase
> Un réseau étendu (WAN) est un réseau de télécommunications qui s'étend sur une vaste zone géographique, comme des villes, des pays ou même des continents, pour connecter des réseaux locaux (LANs) et d'autres types de réseaux entre eux.

## 🧠 Concepts Clés / Fonctionnement
*   Un WAN est utilisé pour connecter des [[LocalAreaNetwork|Réseaux Locaux (LAN)]] situés dans des emplacements géographiquement dispersés, permettant la communication et le partage de ressources sur de grandes distances.
*   Il utilise des technologies de transmission diverses telles que les lignes louées, le [[MultiprotocolLabelSwitching|MPLS]], le [[VirtualPrivateNetwork|VPN]], et plus récemment le [[SoftwareDefinedWideAreaNetwork|SD-WAN]].
*   Les infrastructures WAN sont souvent gérées par des fournisseurs de services de télécommunications qui offrent la connectivité via des fibres optiques, des liaisons satellites ou d'autres médias à large bande passante.
*   Il sert de colonne vertébrale pour relier des succursales d'une entreprise, des campus universitaires ou des utilisateurs distants à des ressources centrales.

## 🛡️ Risques / Menaces Associés
*   [[Eavesdropping|Écoute clandestine]] sur les lignes de communication si le trafic n'est pas chiffré.
*   [[DenialOfService|Attaques par déni de service]] (DoS/DDoS) visant à perturber la connectivité et la disponibilité du réseau.
*   [[UnauthorizedAccess|Accès non autorisé]] aux ressources du réseau via des points d'entrée mal sécurisés.
*   [[DataBreach|Fuites de données]] ou compromission de l'intégrité des données en transit.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémenter des [[VirtualPrivateNetwork|VPN]] pour chiffrer et sécuriser les communications sur le WAN.
*   Utiliser des [[Firewall|Pare-feu]] robustes aux points d'interconnexion pour filtrer le trafic et contrôler les accès.
*   Mettre en place des [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et des [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion (IPS)]] pour surveiller et réagir aux activités suspectes.
*   Appliquer des politiques de [[NetworkSegmentation|segmentation réseau]] pour isoler les différentes parties du WAN et limiter la propagation des menaces.
*   Effectuer des audits de sécurité réguliers et des tests de pénétration.

## 🔗 Notes Connexes
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[MetropolitanAreaNetwork|Réseau Métropolitain (MAN)]]
*   [[VirtualPrivateNetwork|Réseau Privé Virtuel (VPN)]]
*   [[MultiprotocolLabelSwitching|MPLS]]
*   [[SoftwareDefinedWideAreaNetwork|SD-WAN]]
*   [[NetworkSecurity|Sécurité Réseau]]