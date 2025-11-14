---
tags:
  - ipv6/decouverte-voisins
  - securite/premier-saut
  - protocole
  - reseau/protocoles
aliases:
  - Neighbor Discovery Protocol
  - NDP
  - Protocole de Découverte de Voisins
cssclasses:
  - max
---

# Protocole de Découverte de Voisins (NDP)

## 📥 Définition en une phrase
> Le Protocole de Découverte de Voisins (NDP) est un [[Protocols|protocole]] fondamental pour [[InternetProtocolVersion6|IPv6]], remplaçant en grande partie les fonctionnalités d'[[AddressResolutionProtocol|ARP]] et d'[[InternetControlMessageProtocol|ICMP]] Router Discovery pour la découverte de voisins, la résolution d'adresses, et la gestion des routeurs sur un lien local.

## 🧠 Concepts Clés / Fonctionnement
*   **Résolution d'Adresse**: Permet à un nœud de déterminer l'adresse MAC (couche liaison de données) d'un autre nœud IPv6 sur le même lien à partir de son adresse IPv6, via des messages [[InternetControlMessageProtocolVersion6|ICMPv6]] de Sollicitation de Voisin (`Neighbor Solicitation`) et d'Annonce de Voisin (`Neighbor Advertisement`).
*   **Découverte de Routeur**: Aide les hôtes à trouver les routeurs sur le lien et à déterminer leur préfixe, via des messages [[InternetControlMessageProtocolVersion6|ICMPv6]] de Sollicitation de Routeur (`Router Solicitation`) et d'Annonce de Routeur (`Router Advertisement`).
*   **Détection d'Adresses Dupliquées (DAD)**: Un nœud utilise NDP pour vérifier qu'une adresse IPv6 qu'il souhaite utiliser n'est pas déjà en usage par un autre nœud avant de l'assigner.
*   **Découverte de Préfixe**: Les routeurs annoncent les préfixes IPv6 disponibles sur le lien, permettant aux hôtes de configurer automatiquement leurs adresses (auto-configuration sans état, SLAAC).
*   **Redirection**: Un routeur peut informer un hôte d'un meilleur chemin pour atteindre une destination via un autre routeur sur le même lien.
*   **Messages ICMPv6 Clés**: NDP s'appuie sur cinq types de messages [[InternetControlMessageProtocolVersion6|ICMPv6]]: `Router Solicitation`, `Router Advertisement`, `Neighbor Solicitation`, `Neighbor Advertisement`, et `Redirect`.

## 🛡️ Risques / Menaces Associés
*   [[ManInTheMiddle|Attaques de l'Homme du Milieu (MitM)]]: Un attaquant peut usurper des identités en envoyant de fausses annonces de voisin ou de routeur, redirigeant le trafic vers lui.
*   [[DenialOfService|Déni de Service (DoS)]]: En inondant le réseau de messages NDP frauduleux, un attaquant peut surcharger les hôtes et les routeurs, empêchant le bon fonctionnement de la communication IPv6.
*   [[AddressSpoofing|Usurpation d'Adresses (IP ou MAC)]]: Les messages NDP peuvent être falsifiés pour associer une adresse IPv6 légitime à l'adresse MAC d'un attaquant.
*   [[RouterAdvertisementSpoofing|Usurpation d'Annonce de Routeur]]: Un attaquant peut se faire passer pour un routeur légitime, distribuer de fausses informations de routage ou de préfixe, et prendre le contrôle du trafic.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[FirstHopSecurity|Sécurité du Premier Saut (FHS)]]: Utilisation de fonctionnalités comme `RA-Guard` (Router Advertisement Guard) et `NDP Snooping` sur les commutateurs réseau pour valider les messages NDP et bloquer les messages non autorisés ou malveillants.
*   [[SecureNeighborDiscovery|SEND (Secure Neighbor Discovery)]]: Une extension de NDP qui utilise la cryptographie (certificats X.509 et signatures numériques) pour authentifier les messages NDP. Cependant, son adoption reste limitée.
*   [[NetworkSegmentation|Segmentation Réseau]]: Isoler les systèmes critiques sur des segments réseau distincts pour limiter la portée potentielle d'une attaque NDP.
*   [[NetworkAccessControl|Contrôle d'Accès Réseau (NAC)]]: Restreindre l'accès au réseau aux appareils autorisés et surveiller leur comportement.
*   **Surveillance et Détection d'Intrusion**: Mettre en place des systèmes pour détecter les anomalies dans le trafic NDP.

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|IPv6]]
*   [[AddressResolutionProtocol|ARP]]
*   [[InternetControlMessageProtocolVersion6|ICMPv6]]
*   [[RouterAdvertisementSpoofing|Usurpation d'Annonce de Routeur]]
*   [[FirstHopSecurity|Sécurité du Premier Saut]]