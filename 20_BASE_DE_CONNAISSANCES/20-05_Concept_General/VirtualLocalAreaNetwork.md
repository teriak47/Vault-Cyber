---
tags:
  - concept/general
  - reseau
  - reseau/virtuel
  - reseau/segmentation
aliases:
  - Réseau Local Virtuel
  - VLAN
  - Virtual Local Area Network
  - Réseaux Locaux Virtuels
  - Virtual LAN
archetype: concept-general
source:
cssclasses:
  - max
---

# Réseau Local Virtuel (VLAN)

## 📥 Définition en une phrase
> Un VLAN est une méthode de segmentation réseau logique qui permet de diviser un LAN physique en plusieurs réseaux virtuels distincts, isolant le trafic entre eux.

## 🧠 Concepts Clés / Piliers
*   **Segmentation Logique**: Un VLAN opère au niveau de la couche liaison de données (couche 2 du modèle OSI), permettant de regrouper des hôtes sans tenir compte de leur localisation physique sur un commutateur réseau. Cela crée des segments réseau logiques distincts.
*   **Isolation de Trafic**: Chaque VLAN est un domaine de diffusion indépendant. Le trafic au sein d'un VLAN n'est pas vu par les autres VLANs. Pour que deux VLANs puissent communiquer, le trafic doit être acheminé via un routeur ou un commutateur de couche 3.
*   **Flexibilité et Gestion**: Les VLANs offrent une grande flexibilité en matière de configuration réseau. Ils permettent de déplacer facilement des utilisateurs ou des ressources d'un segment réseau à un autre sans nécessiter de recâblage physique, simplifiant ainsi l'gestion réseau.
*   **Sécurité des Ports**: Les commutateurs réseau peuvent être configurés pour assigner des ports Ethernet spécifiques à des VLANs donnés, empêchant ainsi l'accès non autorisé à certains segments réseau, même si l'appareil est physiquement connecté.

## 💡 Importance en Cybersécurité
> Les VLANs sont un composant essentiel de la sécurité réseau moderne. Ils permettent de contenir la portée d'une attaque en isolant les systèmes critiques ou sensibles dans des segments distincts, ce qui réduit considérablement la surface d'attaque et limite le mouvement latéral des attaquants. En séparant les données et les applications par fonction, département ou niveau de sécurité, les VLANs facilitent l'implémentation du principe du moindre privilège et des contrôles d'accès granulaires. Ils jouent un rôle clé dans une stratégie de défense en profondeur, en ajoutant une couche d'isolation logique qui complète les mesures de sécurité physique.

## 🔗 Notes Connexes
*   Segmentation réseau
*   Réseau Local
*   Domaine de Diffusion
*   Sécurité Réseau
*   Contrôle d'Accès
*   Routeur
*   Commutateur Réseau
*   Défense en Profondeur
*   Politique de Sécurité
*   Ethernet

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   La note pourrait bénéficier d'exemples concrets de scénarios d'utilisation des VLANs pour des cas spécifiques de sécurité (ex: réseau invité, IoT, serveurs critiques).
*   Des détails techniques supplémentaires sur les modes de VLAN (port-based, MAC-based, protocol-based) et le VLAN tagging (ex: 802.1Q) pourraient enrichir la compréhension.
*   Aborder les vulnérabilités de sécurité spécifiques aux VLANs (ex: VLAN Hopping, double tagging) et les contremesures associées.