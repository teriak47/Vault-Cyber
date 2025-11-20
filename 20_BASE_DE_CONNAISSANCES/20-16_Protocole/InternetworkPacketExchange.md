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
> Le protocole Internetwork Packet Exchange (IPX) est un protocole de couche réseau (Couche 3 du modèle OSI) obsolète, développé par Novell. Il était principalement utilisé dans les réseaux Novell NetWare des années 1980 et 1990 pour acheminer des paquets de données entre hôtes sur des réseaux locaux et étendus.

## ⚙️ Fonctionnement
1.  **Protocole sans connexion**: Similaire à UDP, IPX est un protocole de type datagramme, ce qui signifie qu'il n'établit pas de connexion préalable et ne garantit ni la livraison, ni l'ordre des paquets.
2.  **Adressage IPX**: Utilise une adresse réseau de 32 bits pour identifier le segment réseau et une adresse de nœud de 48 bits (généralement l'adresse MAC du NIC) pour identifier le hôte spécifique.
3.  **Routage**: Incluait des capacités de routage pour acheminer les paquets à travers des routeurs vers des réseaux distants.
4.  **Association avec SPX**: Souvent associé au Sequenced Packet Exchange (SPX), un protocole de couche de transport qui fournissait un service fiable et orienté connexion par-dessus IPX, de manière analogue au rôle du TCP pour l'IP.
*   **Ports par défaut**: Non pertinent pour IPX car il ne fonctionne pas avec le concept de ports comme dans TCP/IP.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Technologie Obsolète : Les systèmes basés sur IPX sont considérés comme des systèmes hérités, présentant des vulnérabilités de sécurité importantes dues à l'absence de mises à jour et de support.
    *   Manque de Support : L'absence de logiciels et de matériels modernes prenant en charge IPX signifie qu'aucune nouvelle faille de sécurité ne sera corrigée.
    *   Problèmes de compatibilité : L'intégration de systèmes IPX dans un réseau d'entreprise moderne est complexe et peut introduire des surfaces d'attaque inattendues.
*   **Alternatives ou Mesures de Protection (migration recommandée)**:
    *   Migration : La stratégie principale est la migration de tous les systèmes et services utilisant IPX vers la suite de protocoles TCP/IP.
    *   Segmentation Réseau : Pour les systèmes hérités qui ne peuvent pas être migrés immédiatement, une segmentation réseau rigoureuse est essentielle, les isolant dans des VLAN dédiés et appliquant des règles de pare-feu strictes.
    *   Mise hors service : Planifier le retrait progressif et définitif de tous les composants IPX dès que possible.
    *   Audit de Sécurité : Réaliser des audits de sécurité réguliers pour détecter toute présence ou communication IPX non autorisée.

## 🔗 Notes Connexes
*   SPX
*   TCP/IP
*   IP
*   Modèle OSI
*   UDP
*   Technologie Obsolète
*   Vulnérabilité
*   Manque de Support
*   Problème de compatibilité
*   Migration
*   Segmentation Réseau
*   Pare-feu
*   Mise hors service
*   Audit de Sécurité