---
tags:
  - protocole
aliases:
  - Neighbor Discovery Protocol
  - NDP
  - Protocole de Découverte de Voisins
archetype: protocole
rfc: RFC 4861
cssclasses:
  - max
---

# Protocole de Découverte de Voisins (NDP)

## 🎯 Rôle et Couche OSI
Le Protocole de Découverte de Voisins (NDP) est un protocole essentiel pour IPv6, qui remplace et combine les fonctionnalités d'ARP et d'ICMP Router Discovery pour la découverte de voisins, la résolution d'adresses, et la gestion des routeurs sur un segment de réseau local. Il opère principalement à la couche Réseau du modèle TCP/IP et à la couche Internet pour la gestion des interactions entre hôtes sur le même lien. Il utilise les messages ICMPv6.

## ⚙️ Fonctionnement
1.  **Résolution d'Adresse**: Un nœud détermine l'adresse MAC (couche liaison de données) d'un autre nœud IPv6 sur le même lien, en utilisant les messages ICMPv6 `Neighbor Solicitation` et `Neighbor Advertisement`.
2.  **Découverte de Routeur**: Les hôtes identifient les routeurs disponibles sur le lien local et découvrent leurs préfixes réseau via les messages ICMPv6 `Router Solicitation` et `Router Advertisement`. Cela facilite l'auto-configuration sans état (SLAAC) des adresses IPv6.
3.  **Détection d'Adresses Dupliquées (DAD)**: Un nœud utilise le NDP pour s'assurer qu'une adresse IPv6 qu'il souhaite utiliser n'est pas déjà assignée à un autre nœud sur le même lien.
4.  **Découverte de Préfixe**: Les routeurs annoncent les préfixes IPv6 disponibles, permettant aux hôtes de configurer automatiquement leurs adresses IPv6 et d'identifier les passerelles par défaut.
5.  **Redirection**: Un routeur peut informer un hôte qu'un meilleur chemin existe pour atteindre une destination spécifique via un autre routeur sur le même lien.
*   **Ports par défaut**: N/A (opère au niveau de la couche Réseau via ICMPv6, non basé sur des ports TCP/UDP).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Attaques de l'homme du milieu (MitM): L'attaquant peut intercepter et modifier le trafic en usurpant des identités via de fausses annonces NDP.
    *   Déni de Service (DoS): L'attaquant sature le réseau avec des messages NDP falsifiés, surchargeant les hôtes et les routeurs, perturbant ainsi la communication IPv6.
    *   Usurpation d'adresses: Falsification des messages NDP pour associer une adresse IPv6 légitime à l'adresse MAC de l'attaquant.
    *   Usurpation d'Annonce de Routeur: L'attaquant se fait passer pour un routeur légitime, distribue de fausses informations de routage ou de préfixes, et détourne le trafic.
*   **Mesures de protection**:
    *   Sécurité du Premier Saut (FHS): Inclut `RA-Guard` (protection contre les fausses annonces de routeur) et `NDP Snooping` sur les commutateurs réseau pour valider et bloquer les messages NDP non autorisés.
    *   SEND (Secure Neighbor Discovery): Une extension de NDP utilisant la cryptographie (certificats X.509 et signatures numériques) pour authentifier les messages. Son adoption reste limitée.
    *   Segmentation Réseau: Isoler les systèmes critiques sur des segments de réseau distincts pour limiter l'surface d'attaque.
    *   Contrôle d'Accès Réseau (NAC): Restreindre l'accès au réseau aux appareils autorisés et surveiller leur comportement.
    *   Surveillance de sécurité et détection d'intrusion: Mettre en place des systèmes pour identifier les anomalies dans le trafic NDP.

## 🔗 Notes Connexes
*   IPv6
*   ARP
*   ICMPv6
*   Usurpation d'Annonce de Routeur
*   Sécurité du Premier Saut
*   Wireshark (Outil d'analyse)
*   Auto-configuration sans état (SLAAC)