---
tags:
  - materiel
  - materiel/routeur
  - reseau/lan
  - reseau/internet
  - reseau/nat
  - protocole/ip
  - protocole/osi
aliases:
  - Routeur
  - Network Router
archetype: materiel
source:
  -
cssclasses:
  - max
---

# Routeur

## 🎯 Rôle et Fonction
> Un routeur est un équipement réseau crucial qui opère à la couche réseau (Couche 3) du Modèle OSI. Son rôle principal est de transmettre les paquets de données entre différents réseaux informatiques, comme un LAN et l'Internet, en déterminant le chemin le plus efficace pour atteindre leur destination. Il utilise les adresses IP pour faciliter ce routage intelligent.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Dispositif réseau d'interconnexion de réseaux, peut être physique ou virtuel (logiciel).
*   **Connectique**: Généralement plusieurs ports Ethernet (ex: RJ45), et parfois des interfaces Wi-Fi ou pour fibre optique.
*   **Performances**: Débit de traitement des paquets (en Mbps ou Gbps), nombre de routes gérées, capacité de NAT.
*   **Normes associées**:
    *   Suite de protocoles TCP/IP (incluant IP, TCP, UDP).
    *   IEEE (pour les interfaces Ethernet ou Wi-Fi).
    *   IETF (pour les protocoles de routage).
*   **Fonctionnalités Clés**:
    *   Maintien de tables de routage pour stocker les informations de chemin.
    *   Supporte les protocoles de routage dynamiques (tels qu'OSPF, BGP) et le routage statique.
    *   Effectue souvent la Traduction d'Adresses Réseau (NAT).
    *   Peut servir de passerelle par défaut pour un réseau local.

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Interconnexion et Segmentation**: Permet la connexion de multiples segments de réseau et leur segmentation, améliorant la performance et la sécurité.
    *   **Optimisation du Trafic**: Sélectionne le meilleur chemin pour les paquets, réduisant la latence et améliorant l'efficacité du réseau.
    *   **NAT et Sécurité**: Offre des fonctions de NAT pour économiser les adresses IP publiques et masquer la structure du réseau interne, agissant comme une première ligne de défense.
    *   **Évolutivité**: Facilite l'expansion du réseau en ajoutant de nouveaux sous-réseaux.
*   **Inconvénients**:
    *   **Coût**: Peut être coûteux, surtout pour les modèles haute performance d'entreprise.
    *   **Complexité de Configuration**: Nécessite une expertise pour une configuration et une sécurité optimales.
    *   **Point de Défaillance Unique**: Une panne peut interrompre la communication entre réseaux.
    *   **Surface d'attaque**: Cible potentielle pour les attaques s'il n'est pas correctement sécurisé.

## 🔒 Considérations de Sécurité Physique
*   Protection contre l'accès non autorisé via des verrous ou des zones sécurisées.
*   Contrôles environnementaux pour prévenir la surchauffe, l'humidité excessive ou d'autres risques physiques.
*   Mise à jour régulière du micrologiciel pour corriger les vulnérabilités connues.
*   Implémentation de contrôles d'accès administratifs robustes.

## 🔗 Notes Connexes
*   Couche Réseau : Le routeur opère principalement à cette couche OSI.
*   Protocole Internet (IP) : Le routeur utilise les adresses IP pour le routage.
*   Table de Routage : Une base de données essentielle maintenue par le routeur.
*   Traduction d'Adresses Réseau (NAT) : Une fonction courante des routeurs.
*   Passerelle par défaut : Le point de sortie par défaut pour le trafic réseau sortant d'un sous-réseau.
*   Commutateur réseau : Un autre dispositif réseau souvent utilisé en conjonction avec un routeur pour la segmentation au niveau 2.
*   Routeur sans fil : Une variante intégrant des fonctionnalités Wi-Fi pour l'accès sans fil.
*   Protocoles de Routage : Mécanismes utilisés pour échanger des informations de routage entre routeurs.