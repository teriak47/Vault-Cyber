---
tags:
  - reseau
  - ip
aliases:
  - Adresse Link-Local
  - Adresse Lien Local
  - Link-Local Address
  - LinkLocalAddress
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse Link-Local

## 📥 Définition en une phrase
> Une adresse Link-Local est une adresse IP auto-configurée qui permet aux hôtes d'un même segment de réseau local de communiquer directement, sans dépendre d'un serveur DHCP ni d'un routeur.

## 🧠 Concepts Clés / Piliers
*   **Auto-configuration**: Les systèmes d'exploitation attribuent automatiquement une adresse Link-Local lorsqu'aucune autre adresse IP n'est disponible via DHCP ou configuration statique. Ce processus garantit une connectivité de base sur le lien.
*   **Non routable**: Ces adresses IP sont intrinsèquement conçues pour la communication intra-LAN et ne doivent pas être acheminées au-delà du segment local par un routeur.
*   **Spécificités IPv4 (APIPA)**: Pour IPv4, la plage dédiée est `169.254.0.0/16` (connu sous le nom d'APIPA - Automatic Private IP Addressing). Le système attribue une adresse et vérifie son unicité sur le lien.
*   **Spécificités IPv6**: En IPv6, chaque interface réseau se voit attribuer une adresse Link-Local avec le préfixe `fe80::/10`. Elles sont fondamentales pour des protocoles essentiels comme le Neighbor Discovery Protocol (NDP) sur le lien local.
*   **Rôles principaux**: Elles sont utilisées pour la découverte de voisins, la résolution d'adresses MAC (similaire à l'ARP en IPv4) et pour établir une communication de base en l'absence de toute autre configuration réseau.

## 💡 Importance en Cybersécurité
> Les adresses Link-Local sont cruciales pour la connectivité réseau de base, permettant aux dispositifs de communiquer sur un même segment même sans serveur DHCP ou configuration statique. Cependant, leur nature auto-configurée et non routable présente des vulnérabilités de sécurité significatives. Un acteur de menace présent sur le même réseau local peut exploiter ces adresses pour la reconnaissance des hôtes et des dispositifs, potentiellement menant à des attaques de l'homme du milieu ou à des tentatives d'accès non autorisé si la segmentation réseau est faible. Une gestion et une surveillance réseau rigoureuses sont donc essentielles pour prévenir l'exposition involontaire et limiter la surface d'attaque potentielle, même si les hôtes ne sont pas configurés avec des adresses IP routables.

## 🔗 Notes Connexes
*   Adresse IP
*   Segment de Réseau
*   Serveur DHCP
*   Routeur
*   Neighbor Discovery Protocol
*   ARP
*   APIPA
*   IPv4
*   IPv6
*   Sécurité Réseau
*   Segmentation Réseau
*   Surveillance Réseau
*   Surface d'attaque
*   Attaque de l'Homme du Milieu
*   Reconnaissance