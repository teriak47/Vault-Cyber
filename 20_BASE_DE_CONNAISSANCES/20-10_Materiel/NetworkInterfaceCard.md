---
tags:
  - materiel
aliases:
  - Carte d'Interface Réseau
  - NIC
  - Network Interface Card
archetype: materiel
source:
  - 
cssclasses:
  - max
---

# Carte d'Interface Réseau (NIC)

## 🎯 Rôle et Fonction
> La Carte d'Interface Réseau est un composant matériel essentiel qui permet à un ordinateur ou à tout autre périphérique réseau de se connecter à un réseau et d'établir des communications avec d'autres appareils. Elle sert de pont entre le système interne et le support réseau.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**:
    *   Intégrées à la carte mère (onboard) ou cartes d'extension.
    *   Filaire (par exemple, pour Ethernet) ou sans fil (pour Wi-Fi, Bluetooth).
*   **Connectique**:
    *   Connecteur RJ45 pour les connexions Ethernet filaires.
    *   Antennes intégrées ou externes pour les connexions sans fil.
*   **Performances**: Les capacités varient en fonction du modèle, supportant des débits de Mbps à plusieurs Gbps.
*   **Normes associées**:
    *   IEEE 802.3 pour les réseaux Ethernet filaires.
    *   IEEE 802.11 pour les réseaux Wi-Fi sans fil.

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   Permet la communication réseau fondamentale pour les ordinateurs et périphériques.
    *   Offre une flexibilité pour se connecter à différents supports réseau (filaire ou sans fil).
    *   Supporte des vitesses de transmission de données élevées.
*   **Inconvénients**:
    *   Peut représenter une surface d'attaque pour certaines menaces spécifiques au réseau.
    *   La configuration incorrecte peut introduire des vulnérabilités de sécurité.

## 🔒 Considérations de Sécurité Physique
*   Protection contre l'accès non autorisé: En tant que composant matériel, elle est sujette aux risques physiques classiques, nécessitant des mesures de sécurité physique pour protéger l'ordinateur hôte.
*   Contrôles environnementaux (température, humidité): Les mêmes considérations que pour tout autre matériel informatique s'appliquent pour assurer la longévité et le bon fonctionnement.

## 🛡️ Considérations de Cybersécurité
*   **Vulnérabilités et Risques**:
    *   Usurpation d'adresse MAC: Les attaquants peuvent modifier l'adresse MAC de leur NIC pour contourner les contrôles d'accès ou se faire passer pour un autre appareil sur le LAN.
    *   Capture de Paquets: Une NIC peut être configurée en mode promiscuité pour intercepter et analyser tout le trafic réseau passant sur un segment réseau, y compris les données non destinées à l'appareil.
*   **Mesures de Protection**:
    *   Sécurité des Ports: Configurer les commutateurs réseau pour limiter les adresses MAC autorisées sur un port spécifique afin d'empêcher les appareils non autorisés.
    *   Segmentation Réseau: Utiliser des VLAN ou d'autres techniques de segmentation réseau pour isoler les systèmes et limiter la portée des attaques.
    *   Contrôle d'accès: Implémenter des politiques de contrôle d'accès strictes au niveau du périphérique réseau pour s'assurer que seuls les appareils légitimes peuvent se connecter.

## 🔗 Notes Connexes
*   Modèle OSI
*   Couche Physique
*   Couche Liaison de Données
*   Adresse MAC
*   Ethernet
*   Wi-Fi
*   Périphérique Réseau
*   Ordinateur
*   Réseau
*   Interface Réseau
---