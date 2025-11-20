---
tags:
aliases:
  - Multidiffusion
  - Multicast
  - Multicast Communication
archetype: protocole
rfc:
cssclasses:
  - max
---

# Multidiffusion (Multicast)

## 🎯 Rôle et Couche OSI
> La multidiffusion est une méthode de communication réseau un à plusieurs où un émetteur envoie des paquets à un groupe spécifique de récepteurs simultanément, sans avoir à les envoyer individuellement à chaque destinataire. Elle permet une distribution efficace d'un seul flux de données à de multiples destinataires abonnés à un groupe.
>
> Ce mécanisme opère principalement à la couche réseau du modèle OSI (pour l'adressage IP et le routage) et, en support, à la couche liaison de données (pour les adresses MAC de multidiffusion).

## ⚙️ Fonctionnement
1.  **Modèle de Communication**: Un seul flux de données est distribué efficacement à plusieurs destinataires qui se sont abonnés à un groupe de multidiffusion.
2.  **Adresses IP de Multidiffusion**: Utilise une plage spécifique d'adresses IP de classe D (224.0.0.0 à 239.255.255.255 pour IPv4) pour identifier les groupes de multidiffusion plutôt que des hôtes individuels.
3.  **Gestion des Groupes**: Le Internet Group Management Protocol (IGMP) est utilisé par les hôtes pour s'abonner (joindre) ou se désabonner (quitter) des groupes de multidiffusion.
4.  **Routage Multicast**: Les routeurs utilisent des protocoles comme le Protocol Independent Multicast (PIM) pour acheminer efficacement le trafic multicast à travers les réseaux vers les sous-réseaux où des membres du groupe sont présents.
*   **Ports par défaut**: La multidiffusion n'utilise pas de ports TCP ou UDP dédiés au sens traditionnel. Elle s'appuie sur des adresses IP de multidiffusion spécifiques pour identifier les groupes de destinataires.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Déni de Service (DoS) : Une mauvaise configuration ou une exploitation peut entraîner une inondation du réseau (flooding) si le trafic multicast n'est pas correctement contenu, surchargeant les commutateurs ou les hôtes.
    *   Divulgation d'informations : Des groupes de multidiffusion non sécurisés peuvent exposer des données sensibles à des entités non autorisées qui se joignent au groupe.
    *   Reconnaissance : Peut être utilisé par des attaquants pour découvrir des services ou des hôtes actifs sur le réseau qui participent à des groupes de multidiffusion.
*   **Mesures de protection**:
    *   Segmentation Réseau : Utiliser des VLANs pour isoler le trafic multicast à des segments de réseau spécifiques, limitant ainsi sa portée.
    *   Listes de Contrôle d'Accès (ACLs) : Configurer des ACLs sur les routeurs et les commutateurs pour contrôler qui peut joindre des groupes de multidiffusion et quel trafic multicast est autorisé à transiter.
    *   IGMP Snooping : Activer l'IGMP Snooping sur les commutateurs pour s'assurer que le trafic multicast est uniquement forwardé vers les ports où des membres du groupe sont réellement présents, évitant ainsi le flooding et améliorant la performance réseau.
    *   Authentification et Autorisation : Si possible, implémenter des mécanismes pour authentifier les membres avant qu'ils ne puissent joindre des groupes de multidiffusion sensibles.

## 🔗 Notes Connexes
*   Unicast
*   Broadcast
*   IGMP
*   PIM
*   Adresse Multicast
*   Couche Réseau
*   Wireshark
*   IPv4