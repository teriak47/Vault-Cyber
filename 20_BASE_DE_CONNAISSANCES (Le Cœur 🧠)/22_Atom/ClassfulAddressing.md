---
tags:
  - adressage-classique
  - classes-ipv4
  - masque-sous-reseau-fixe
  - adressage
  - adressage-ipv4
  - adressage-ipv6
aliases:
  - Adressage Classique
  - Classful IP Addressing
cssclasses:
  - max
---

# Adressage Classique (Classful Addressing)

## 📥 Définition en une phrase
> L'[[ClassfulAddressing|adressage classique]] est une ancienne méthode de division de l'espace d'[[InternetProtocolAddress|adresses IP]] en différentes classes (A, B, C, D, E), où la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]] d'une [[InternetProtocolAddress|adresse IP]] sont définies par une [[SubnetMask|masque de sous-réseau]] fixe, sans tenir compte des besoins réels de l'organisation.

## 🧠 Concepts Clés / Fonctionnement
*   **Classes Prédéfinies** : L'[[InternetProtocolVersion4|IPv4]] était divisé en cinq classes (A, B, C, D, E), les classes A, B et C étant utilisées pour l'[[IPAddressing|adressage]] des [[Host|hôtes]].
    *   **Classe A** : Le premier octet définit la [[NetworkPortion|partie réseau]]. Destinée aux très grands [[Enterprise|réseaux]] avec un grand nombre d'[[Host|hôtes]]. Le [[SubnetMask|masque de sous-réseau]] par défaut est 255.0.0.0.
    *   **Classe B** : Les deux premiers octets définissent la [[NetworkPortion|partie réseau]]. Destinée aux [[Enterprise|réseaux]] de taille moyenne à grande. Le [[SubnetMask|masque de sous-réseau]] par défaut est 255.255.0.0.
    *   **Classe C** : Les trois premiers octets définissent la [[NetworkPortion|partie réseau]]. Destinée aux petits [[Network|réseaux]]. Le [[SubnetMask|masque de sous-réseau]] par défaut est 255.255.255.0.
    *   **Classes D et E** : La Classe D est réservée pour le [[Multicast|multidiffusion]], et la Classe E est réservée pour la recherche et le développement.
*   **Division Fixe** : La distinction entre la [[NetworkPortion|partie réseau]] et la [[HostPortion|partie hôte]] était fixe et déterminée uniquement par le premier octet de l'[[InternetProtocolAddress|adresse IP]].
*   **Inefficacité** : Cette méthode entraînait un gaspillage considérable d'[[InternetProtocolAddress|adresses IP]], car des blocs entiers d'adresses étaient attribués même si une organisation n'utilisait qu'une petite fraction des [[Host|hôtes]] disponibles dans sa classe.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Transition vers l'[[ClasslessInterDomainRouting|adressage sans classes (CIDR)]]** : La principale "bonne pratique" fut la migration vers le [[ClasslessInterDomainRouting|CIDR]] qui permet une attribution d'[[InternetProtocolAddress|adresses IP]] plus flexible et efficace, optimisant l'utilisation de l'espace [[InternetProtocolVersion4|IPv4]].
*   **Adoption de l'[[InternetProtocolVersion6|IPv6]]** : Pour les nouveaux déploiements et à long terme, l'adoption de l'[[InternetProtocolVersion6|IPv6]] élimine complètement les contraintes de l'[[ClassfulAddressing|adressage classique]] et du [[ClasslessInterDomainRouting|CIDR]] en offrant un espace d'adressage quasi illimité.


---