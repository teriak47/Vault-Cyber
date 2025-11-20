---
tags:
  - reseau
  - ipv4
aliases:
  - Adressage Classique
  - Classful IP Addressing
  - Adressage IP Classique
  - Classful Addressing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage Classique (Classful Addressing)

## 📥 Définition en une phrase
> L'adressage classique est une ancienne méthode de division de l'espace d'adresses IP en différentes classes (A, B, C, D, E), où la partie réseau et la partie hôte d'une adresse IP sont définies par une masque de sous-réseau fixe, sans tenir compte des besoins réels de l'organisation.

## 🧠 Concepts Clés / Piliers
*   **Classes d'IPv4**: L'IPv4 était initialement structuré en cinq classes principales, chacune avec une allocation prédéfinie de bits pour la partie réseau et la partie hôte.
    *   **Classe A**: Conçue pour de très grands réseaux (potentiellement des millions d'hôtes), où le premier octet (8 bits) identifie le réseau et les trois octets suivants (24 bits) les hôtes. Le masque de sous-réseau par défaut est 255.0.0.0.
    *   **Classe B**: Destinée aux réseaux de taille moyenne à grande (jusqu'à 65 534 hôtes), utilisant les deux premiers octets (16 bits) pour le réseau et les deux derniers (16 bits) pour les hôtes. Le masque de sous-réseau par défaut est 255.255.0.0.
    *   **Classe C**: Idéale pour les petits réseaux (jusqu'à 254 hôtes), avec les trois premiers octets (24 bits) dédiés au réseau et le dernier octet (8 bits) aux hôtes. Le masque de sous-réseau par défaut est 255.255.255.0.
    *   **Classes D et E**: La Classe D est réservée pour le multidiffusion, tandis que la Classe E est mise de côté pour des adresses expérimentales et des recherches futures.
*   **Division Inflexible**: La caractéristique principale de l'adressage classique est la division hiérarchique et fixe de l'adresse IP en partie réseau et partie hôte, déterminée uniquement par le premier octet de l'adresse et non par les besoins réels du réseau. Cette rigidité est à l'origine de son inefficacité.
*   **Gaspillage des Adresses IP**: En raison de sa structure fixe, l'adressage classique entraînait un gaspillage considérable de l'espace d'IPv4. De grands blocs d'adresses étaient alloués à des organisations qui n'en utilisaient qu'une petite fraction, contribuant à l'épuisement précoce des adresses IP disponibles.

## 💡 Importance en Cybersécurité
> Bien que l'adressage classique soit largement obsolète, sa compréhension est cruciale pour saisir l'évolution des méthodes d'adressage IP et les raisons de la transition vers des approches plus efficaces comme le CIDR et l'IPv6. Historiquement, l'inefficacité de l'allocation des adresses IP pouvait, à long terme, freiner l'expansion des réseaux et la capacité à isoler ou segmenter les segments réseau de manière granulaire, ce qui a des implications indirectes sur la sécurité réseau et la gestion des surfaces d'attaque. Les techniques modernes d'adressage offrent une meilleure flexibilité pour la segmentation réseau et la gestion des ressources, contribuant à une posture de cybersécurité plus robuste.

## 🔗 Notes Connexes
*   Adressage IP
*   Internet Protocol version 4 (IPv4)
*   Masque de sous-réseau
*   Classless Inter-Domain Routing (CIDR)
*   Internet Protocol version 6 (IPv6)
*   Partie Réseau
*   Partie Hôte
*   Routage
*   Segmentation Réseau
*   Internet Assigned Numbers Authority (IANA)