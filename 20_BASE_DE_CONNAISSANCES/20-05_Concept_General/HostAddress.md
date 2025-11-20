---
tags:
aliases:
  - Adresse d'Hôte
  - Host Address
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse d'Hôte (Host Address)

## 📥 Définition en une phrase
> Une adresse d'hôte est un identifiant unique attribué à un hôte (un ordinateur, un serveur, un smartphone, etc.) sur un réseau informatique, lui permettant d'être localisé et de communiquer efficacement.

## 🧠 Concepts Clés / Piliers
*   **Identification Unique**: L'adresse d'hôte est l'identifiant numérique ou physique qui distingue un hôte spécifique au sein d'un réseau, essentiel pour son adressage et sa localisation précise.
*   **Double Nature (Logique vs. Physique)**: Elle se manifeste sous deux formes principales : l'adresse IP (logique, attribuée dynamiquement par DHCP ou statiquement, et gérée par la couche réseau) et l'adresse MAC (physique, encodée dans la carte d'interface réseau et utilisée par la couche liaison de données).
*   **Rôle dans la Communication**: Ces adresses sont cruciales pour l'encapsulation et la décapsulation des paquets de données, assurant qu'ils parviennent au bon dispositif terminal sur le réseau local et, via le routage, vers des réseaux distants. Le Protocole ARP est souvent utilisé pour résoudre une adresse IP en une adresse MAC correspondante.
*   **Structure et Organisation**: Pour les adresses IP, elles sont divisées en une partie réseau qui identifie le segment réseau, et une partie hôte qui identifie spécifiquement le hôte au sein de ce segment, suivant un adressage hiérarchique.

## 💡 Importance en Cybersécurité
> La gestion rigoureuse des adresses d'hôte est essentielle pour la sécurité réseau. Toute vulnérabilité ou attaque ciblant ces adresses (comme le MAC Spoofing, l'empoisonnement ARP, ou l'utilisation de serveurs DHCP malveillants) peut mener à l'accès non autorisé, à la fuite de données, ou à la perturbation de service. Des contrôles de sécurité comme la sécurité des ports ou la segmentation réseau sont vitaux pour protéger l'intégrité et la disponibilité des communications réseau.

## 🔗 Notes Connexes
*   Adresse IP
*   Adresse MAC
*   Adressage IP
*   Partie hôte
*   Carte d'Interface Réseau
*   ARP
*   Sécurité Réseau
*   MAC Spoofing
*   Attaque de l'Homme du Milieu