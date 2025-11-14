---
tags:
  - protocole/ipx
  - reseau/netware
  - gestion-risques/obsolescence-technologique
  - modele/osi
  - protocole/sans-connexion
  - modele/couche-reseau
aliases:
  - Échange de Paquets Inter-Réseaux
  - IPX
  - Internetwork Packet Exchange
source:
  - null
cssclasses:
  - max
---

# Internetwork Packet Exchange (IPX)

## 📥 Définition en une phrase
> L'Internetwork Packet Exchange (IPX) est un protocole de couche réseau obsolète développé par Novell, principalement utilisé dans les réseaux Novell NetWare des années 1980 et 1990, servant à acheminer des paquets de données entre hôtes sur des réseaux locaux et étendus.

## 🧠 Concepts Clés / Fonctionnement
*   **Protocole sans connexion (datagramme)** : Similaire à [[UserDatagramProtocol|UDP]], IPX ne garantit pas la livraison ni l'ordre des paquets.
*   **Couche Réseau (OSI L3)** : Opère au niveau de la couche réseau du [[OpenSystemsInterconnectionModel|modèle OSI]], gérant l'adressage et le routage des paquets entre différents segments de réseau.
*   **Adressage IPX** : Utilise une adresse réseau de 32 bits et une adresse de nœud de 48 bits (généralement l'[[MediaAccessControlAddress|adresse MAC]] de la carte réseau).
*   **[[SequencedPacketExchange|SPX]]** : Souvent associé au protocole [[SequencedPacketExchange|SPX]] (Sequenced Packet Exchange) qui fournit un service de transport fiable et orienté connexion au-dessus d'IPX, similaire au rôle de [[TransmissionControlProtocol|TCP]] pour [[InternetProtocol|IP]].
*   **Routage** : IPX inclut des capacités de routage pour acheminer les paquets à travers des routeurs vers des réseaux distants.
*   **Obsolescence** : Largement remplacé par la suite de protocoles [[TransmissionControlProtocolInternetProtocol|TCP/IP]] à la fin des années 1990 et au début des années 2000 en raison de l'essor d'Internet.

## 🛡️ Risques / Menaces Associés
*   [[ObsoleteTechnology|Technologie Obsolète]] : Les systèmes utilisant IPX sont souvent des systèmes hérités non patchés et non maintenus, présentant de graves [[Vulnerability|vulnérabilités]].
*   [[LackOfSupport|Manque de Support]] : Absence de mises à jour de sécurité ou de correctifs pour d'éventuelles failles découvertes.
*   [[CompatibilityIssue|Problèmes de compatibilité]] : Les équipements et logiciels modernes ne prennent plus en charge IPX nativement, rendant son intégration complexe et potentiellement risquée.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Migration|Migration]] : Prioriser la migration de tous les services et systèmes utilisant IPX vers [[TransmissionControlProtocolInternetProtocol|TCP/IP]].
*   [[NetworkSegmentation|Segmentation Réseau]] : Isoler les systèmes hérités qui *doivent* encore utiliser IPX dans des segments de réseau dédiés et hautement sécurisés, avec des règles de [[Firewall|pare-feu]] strictes.
*   [[Decommissioning|Mise hors service]] : Retirer les composants IPX ou les systèmes qui en dépendent dès que possible.
*   [[SecurityAudit|Audit de Sécurité]] : Effectuer des audits réguliers pour s'assurer qu'aucun trafic IPX inattendu ne circule sur le réseau.

## 🔗 Notes Connexes
*   [[SequencedPacketExchange|SPX]]
*   [[TransmissionControlProtocolInternetProtocol|TCP/IP]]
*   [[InternetProtocol|IP]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[NetworkBasicInputOutputSystem|NetBIOS]]