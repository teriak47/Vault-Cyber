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
> L'[[ClassfulAddressing|adressage classique]] est une ancienne méthode de division de l'espace d'[[InternetProtocol|adresses IP]] en différentes classes (A, B, C, D, E), où la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]] d'une [[InternetProtocol|adresse IP]] sont définies par une [[SubnetMask|masque de sous-réseau]] fixe, sans tenir compte des besoins réels de l'organisation.

## 🧠 Concepts Clés / Piliers
*   **Classes d'[[InternetProtocolVersion4|IPv4]]**: L'[[InternetProtocolVersion4|IPv4]] était initialement structuré en cinq classes principales, chacune avec une allocation prédéfinie de bits pour la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]].
    *   **Classe A**: Conçue pour de très grands [[Network|réseaux]] (potentiellement des millions d'[[Host|hôtes]]), où le premier octet (8 bits) identifie le [[Network|réseau]] et les trois octets suivants (24 bits) les [[Host|hôtes]]. Le [[SubnetMask|masque de sous-réseau]] par défaut est 255.0.0.0.
    *   **Classe B**: Destinée aux [[Network|réseaux]] de taille moyenne à grande (jusqu'à 65 534 [[Host|hôtes]]), utilisant les deux premiers octets (16 bits) pour le [[Network|réseau]] et les deux derniers (16 bits) pour les [[Host|hôtes]]. Le [[SubnetMask|masque de sous-réseau]] par défaut est 255.255.0.0.
    *   **Classe C**: Idéale pour les petits [[Network|réseaux]] (jusqu'à 254 [[Host|hôtes]]), avec les trois premiers octets (24 bits) dédiés au [[Network|réseau]] et le dernier octet (8 bits) aux [[Host|hôtes]]. Le [[SubnetMask|masque de sous-réseau]] par défaut est 255.255.255.0.
    *   **Classes D et E**: La Classe D est réservée pour le [[Multicast|multidiffusion]], tandis que la Classe E est mise de côté pour des [[ExperimentalAddresses|adresses expérimentales]] et des recherches futures.
*   **Division Inflexible**: La caractéristique principale de l'[[ClassfulAddressing|adressage classique]] est la [[HierarchicalAddressing|division hiérarchique]] et fixe de l'[[InternetProtocol|adresse IP]] en [[NetworkPortion|partie réseau]] et [[HostPortion|partie hôte]], déterminée uniquement par le premier octet de l'adresse et non par les besoins réels du [[Network|réseau]]. Cette rigidité est à l'origine de son inefficacité.
*   **Gaspillage des [[InternetProtocol|Adresses IP]]**: En raison de sa structure fixe, l'[[ClassfulAddressing|adressage classique]] entraînait un gaspillage considérable de l'espace d'[[InternetProtocolVersion4|IPv4]]. De grands blocs d'adresses étaient alloués à des organisations qui n'en utilisaient qu'une petite fraction, contribuant à l'épuisement précoce des [[InternetProtocol|adresses IP]] disponibles.

## 💡 Importance en Cybersécurité
> Bien que l'[[ClassfulAddressing|adressage classique]] soit largement obsolète, sa compréhension est cruciale pour saisir l'évolution des [[IPAddressing|méthodes d'adressage IP]] et les raisons de la transition vers des approches plus efficaces comme le [[ClasslessInterDomainRouting|CIDR]] et l'[[InternetProtocolVersion6|IPv6]]. Historiquement, l'inefficacité de l'allocation des [[InternetProtocol|adresses IP]] pouvait, à long terme, freiner l'expansion des [[Network|réseaux]] et la capacité à isoler ou segmenter les [[NetworkSegment|segments réseau]] de manière granulaire, ce qui a des implications indirectes sur la [[NetworkSecurity|sécurité réseau]] et la gestion des [[AttackSurface|surfaces d'attaque]]. Les techniques modernes d'[[IPAddressing|adressage]] offrent une meilleure flexibilité pour la [[NetworkSegmentation|segmentation réseau]] et la gestion des [[Resource|ressources]], contribuant à une posture de [[Cybersecurity|cybersécurité]] plus robuste.

## 🔗 Notes Connexes
*   [[IPAddressing|Adressage IP]]
*   [[InternetProtocolVersion4|Internet Protocol version 4 (IPv4)]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[ClasslessInterDomainRouting|Classless Inter-Domain Routing (CIDR)]]
*   [[InternetProtocolVersion6|Internet Protocol version 6 (IPv6)]]
*   [[NetworkPortion|Partie Réseau]]
*   [[HostPortion|Partie Hôte]]
*   [[Routing|Routage]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[InternetAssignedNumbersAuthority|Internet Assigned Numbers Authority (IANA)]]