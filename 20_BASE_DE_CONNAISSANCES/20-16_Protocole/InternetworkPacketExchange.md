---
tags:
  - protocole
aliases:
  - Échange de Paquets Inter-Réseaux
  - IPX
  - Internetwork Packet Exchange
  - InternetworkPacketExchange
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Internetwork Packet Exchange (IPX)

## 🎯 Rôle et Couche OSI
> Le protocole [[InternetworkPacketExchange|Internetwork Packet Exchange]] (IPX) est un [[Protocol|protocole]] de [[NetworkLayer|couche réseau]] (Couche 3 du [[OpenSystemsInterconnectionModel|modèle OSI]]) obsolète, développé par Novell. Il était principalement utilisé dans les réseaux Novell NetWare des années 1980 et 1990 pour acheminer des [[Packet|paquets]] de [[Data|données]] entre [[Host|hôtes]] sur des [[LocalAreaNetwork|réseaux locaux]] et [[WideAreaNetwork|étendus]].

## ⚙️ Fonctionnement
1.  **Protocole sans connexion**: Similaire à [[UserDatagramProtocol|UDP]], [[InternetworkPacketExchange|IPX]] est un [[Protocol|protocole]] de type datagramme, ce qui signifie qu'il n'établit pas de connexion préalable et ne garantit ni la livraison, ni l'ordre des [[Packet|paquets]].
2.  **Adressage IPX**: Utilise une [[NetworkAddress|adresse réseau]] de 32 bits pour identifier le [[NetworkSegment|segment réseau]] et une [[HostAddress|adresse de nœud]] de 48 bits (généralement l'[[MediaAccessControlAddress|adresse MAC]] du [[NetworkInterfaceCard|NIC]]) pour identifier le [[Host|hôte]] spécifique.
3.  **Routage**: Incluait des capacités de [[Routing|routage]] pour acheminer les [[Packet|paquets]] à travers des [[Router|routeurs]] vers des [[RemoteNetwork|réseaux distants]].
4.  **Association avec SPX**: Souvent associé au [[SequencedPacketExchange|Sequenced Packet Exchange]] (SPX), un [[Protocol|protocole]] de [[TransportLayer|couche de transport]] qui fournissait un service fiable et orienté connexion par-dessus [[InternetworkPacketExchange|IPX]], de manière analogue au rôle du [[TransmissionControlProtocol|TCP]] pour l'[[InternetProtocol|IP]].
*   **Ports par défaut**: Non pertinent pour [[InternetworkPacketExchange|IPX]] car il ne fonctionne pas avec le concept de ports comme dans [[TransmissionControlProtocol|TCP/IP]].

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[ObsoleteTechnology|Technologie Obsolète]] : Les systèmes basés sur [[InternetworkPacketExchange|IPX]] sont considérés comme des [[System|systèmes]] [[ObsoleteTechnology|hérités]], présentant des [[SecurityVulnerabilities|vulnérabilités de sécurité]] importantes dues à l'absence de [[PatchManagement|mises à jour]] et de support.
    *   [[LackOfSupport|Manque de Support]] : L'absence de [[Software|logiciels]] et de [[Hardware|matériels]] modernes prenant en charge [[InternetworkPacketExchange|IPX]] signifie qu'aucune nouvelle faille de [[Security|sécurité]] ne sera corrigée.
    *   [[CompatibilityIssue|Problèmes de compatibilité]] : L'intégration de [[System|systèmes]] [[InternetworkPacketExchange|IPX]] dans un [[CorporateNetwork|réseau d'entreprise]] moderne est complexe et peut introduire des [[AttackSurface|surfaces d'attaque]] inattendues.
*   **Alternatives ou Mesures de Protection (migration recommandée)**:
    *   [[Migration|Migration]] : La stratégie principale est la [[Migration|migration]] de tous les [[System|systèmes]] et [[OnlineServices|services]] utilisant [[InternetworkPacketExchange|IPX]] vers la [[TransmissionControlProtocol|suite de protocoles TCP/IP]].
    *   [[NetworkSegmentation|Segmentation Réseau]] : Pour les [[System|systèmes]] [[ObsoleteTechnology|hérités]] qui ne peuvent pas être migrés immédiatement, une [[NetworkSegmentation|segmentation réseau]] rigoureuse est essentielle, les isolant dans des [[VirtualLocalAreaNetwork|VLAN]] dédiés et appliquant des [[Firewall|règles de pare-feu]] strictes.
    *   [[Decommissioning|Mise hors service]] : Planifier le [[Decommissioning|retrait]] progressif et définitif de tous les composants [[InternetworkPacketExchange|IPX]] dès que possible.
    *   [[SecurityAudit|Audit de Sécurité]] : Réaliser des [[SecurityAudit|audits de sécurité]] réguliers pour détecter toute présence ou [[NetworkCommunication|communication]] [[InternetworkPacketExchange|IPX]] non autorisée.

## 🔗 Notes Connexes
*   [[SequencedPacketExchange|SPX]]
*   [[TransmissionControlProtocol|TCP/IP]]
*   [[InternetProtocol|IP]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[UserDatagramProtocol|UDP]]
*   [[ObsoleteTechnology|Technologie Obsolète]]
*   [[Vulnerability|Vulnérabilité]]
*   [[LackOfSupport|Manque de Support]]
*   [[CompatibilityIssue|Problème de compatibilité]]
*   [[Migration|Migration]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[Firewall|Pare-feu]]
*   [[Decommissioning|Mise hors service]]
*   [[SecurityAudit|Audit de Sécurité]]