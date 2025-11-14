---
tags:
  - reseau/vlan
  - securite/vlan-hopping
  - reseau/reseau-local
  - reseau/segmentation
aliases:
  - Réseau Local Virtuel
  - VLAN
  - Virtual Local Area Network
source:
  - 
cssclasses:
  - max
---

# Réseau Local Virtuel (VLAN)

## 📥 Définition en une phrase
> Un [[VirtualLocalAreaNetwork|VLAN]] est une méthode de [[NetworkSegmentation|segmentation réseau]] logique qui permet de diviser un [[LocalAreaNetwork|LAN]] physique en plusieurs réseaux virtuels distincts, isolant le trafic entre eux.

## 🧠 Concepts Clés / Fonctionnement
*   **Segmentation Logique** : Contrairement aux réseaux physiques, les VLANs regroupent des hôtes indépendamment de leur localisation physique, en se basant sur la configuration logicielle des commutateurs.
*   **Domaines de Broadcast Réduits** : Chaque VLAN crée son propre [[BroadcastDomain|domaine de broadcast]], ce qui améliore les performances du réseau en limitant la propagation des diffusions et renforce la sécurité.
*   **Marquage (Tagging)** : Le standard [[IEEE8021Q|IEEE 802.1Q]] est couramment utilisé pour ajouter une étiquette (tag) aux trames Ethernet, identifiant le VLAN auquel elles appartiennent lors de leur transit sur les liens "trunk" entre les commutateurs.
*   **Isolation du Trafic** : Les hôtes appartenant à différents VLANs ne peuvent pas communiquer directement au niveau de la couche 2 ; ils nécessitent un routeur ou un commutateur de couche 3 pour acheminer le trafic entre eux.
*   **Avantages** : Améliore la [[NetworkSecurity|sécurité réseau]], la flexibilité de la gestion des utilisateurs et des ressources, et optimise l'utilisation des équipements réseau.

## 🛡️ Risques / Menaces Associés
*   [[VLANHopping|VLAN Hopping]] : Une [[Threat|menace]] où un attaquant tente d'accéder à un VLAN différent de celui auquel son port est assigné.
*   [[Misconfiguration|Mauvaise configuration]] : Une [[Vulnerability|vulnérabilité]] courante qui peut entraîner des fuites d'informations ou un accès non autorisé entre VLANs.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[PortSecurity|Sécurité des Ports]]** : Configurer la [[PortSecurity|sécurité des ports]] pour limiter le nombre d'adresses MAC autorisées et pour désactiver les ports inutilisés.
*   **Séparation des Rôles** : Isoler les VLANs critiques (ex: gestion, serveurs) du reste du réseau.
*   **Désactiver DTP (Dynamic Trunking Protocol)** : Empêcher la négociation automatique des trunks sur les ports non destinés à cela.
*   **VLAN natif non utilisé** : Utiliser un VLAN inutilisé et non routé comme VLAN natif sur les liens trunk pour atténuer les attaques de VLAN hopping.
*   **[[AccessControlList|Listes de Contrôle d'Accès (ACLs)]]** : Utiliser des ACLs sur les routeurs ou les commutateurs de couche 3 pour filtrer le trafic inter-VLAN.

## 🔗 Notes Connexes
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[LocalAreaNetwork|LAN]]
*   [[BroadcastDomain|Domaine de Broadcast]]
*   [[IEEE8021Q|IEEE 802.1Q]]
*   [[Trunking|Trunking]]
*   [[Subnetting|Subnetting]]