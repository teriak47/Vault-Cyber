---
tags:
  - transmission/multidiffusion
  - protocole/gestion-groupe
  - reseau/adressage
aliases:
  - Multidiffusion
  - Multicast
source:
  - 
cssclasses:
  - max
---

# Multidiffusion (Multicast)

## 📥 Définition en une phrase
> La multidiffusion est une méthode de communication réseau "un à plusieurs" où un émetteur envoie des paquets à un groupe spécifique de récepteurs simultanément, sans avoir à les envoyer individuellement à chaque destinataire.

## 🧠 Concepts Clés / Fonctionnement
*   **Modèle de Communication :** Permet à un seul flux de données d'être distribué efficacement à plusieurs destinataires qui se sont abonnés à un groupe de multidiffusion.
*   **Adresses IP de Multidiffusion :** Utilise une plage spécifique d'[[InternetProtocolAddress|adresses IP]] de classe D (224.0.0.0 à 239.255.255.255) pour identifier les groupes de multidiffusion plutôt que des hôtes individuels.
*   **Gestion des Groupes :** Le [[InternetGroupManagementProtocol|IGMP]] (Internet Group Management Protocol) est utilisé par les hôtes pour s'abonner (joindre) ou se désabonner (quitter) des groupes de multidiffusion.
*   **Routage Multicast :** Les routeurs utilisent des protocoles comme le [[ProtocolIndependentMulticast|PIM]] (Protocol Independent Multicast) pour acheminer efficacement le trafic multicast à travers les réseaux vers les sous-réseaux où des membres du groupe sont présents.
*   **Efficacité :** Réduit la charge réseau sur l'émetteur et le réseau en général, car le même paquet est envoyé une seule fois sur un segment de réseau, même s'il est destiné à plusieurs récepteurs sur ce segment.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service (DoS)]] : Une mauvaise configuration ou une exploitation peut entraîner une inondation du réseau (flooding) si le trafic multicast n'est pas correctement contenu, surchargeant les commutateurs ou les hôtes.
*   [[InformationDisclosure|Divulgation d'informations]] : Des groupes de multidiffusion non sécurisés peuvent exposer des [[SensitiveData|données sensibles]] à des entités non autorisées qui se joignent au groupe.
*   Reconnaissance : Peut être utilisé par des attaquants pour découvrir des services ou des hôtes actifs sur le réseau qui participent à des groupes de multidiffusion.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSegmentation|Segmentation Réseau]] :** Utiliser des [[VirtualLAN|VLANs]] pour isoler le trafic multicast à des segments de réseau spécifiques, limitant ainsi sa portée.
*   **[[AccessControlList|Listes de Contrôle d'Accès (ACLs)]] :** Configurer des ACLs sur les routeurs et les commutateurs pour contrôler qui peut joindre des groupes de multidiffusion et quel trafic multicast est autorisé à transiter.
*   **[[IGMPSnooping|IGMP Snooping]] :** Activer l'IGMP Snooping sur les commutateurs pour s'assurer que le trafic multicast est uniquement forwardé vers les ports où des membres du groupe sont réellement présents, évitant ainsi le flooding.
*   **Authentification et Autorisation :** Si possible, implémenter des mécanismes pour authentifier les membres avant qu'ils ne puissent joindre des groupes de multidiffusion sensibles.

## 🔗 Notes Connexes
*   [[Unicast|Unicast]]
*   [[Broadcast|Broadcast]]
*   [[InternetGroupManagementProtocol|IGMP]]
*   [[ProtocolIndependentMulticast|PIM]]
*   [[MulticastAddress|Adresse Multicast]]