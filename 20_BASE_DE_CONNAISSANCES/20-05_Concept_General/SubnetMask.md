---
tags:
  - concept/general
  - reseau/segmentation
  - reseau
  - calcul/reseau
  - adressage
aliases:
  - Masque de sous-réseau
  - Subnet Mask
  - Subnetmask
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Masque de Sous-réseau

## 📥 Définition en une phrase
> Le masque de sous-réseau est un nombre binaire de 32 bits (pour IPv4) utilisé pour séparer la portion réseau de la portion hôte d'une adresse IP, facilitant ainsi la segmentation réseau en sous-réseaux.

## 🧠 Concepts Clés / Piliers
*   **Identification des Composants d'une Adresse IP**: Il permet à un appareil de déterminer si une autre adresse IP se trouve sur le même réseau local ou sur un réseau distant, en différenciant les identifiants de réseau et d'hôte.
*   **Format et Notation**: Représenté par une suite de bits à 1 pour la partie réseau et de bits à 0 pour la partie hôte (par exemple, `255.255.255.0` en décimal). Il est souvent exprimé via la notation Classless Inter-Domain Routing (CIDR) (ex: `/24`) qui indique le nombre de bits alloués à la portion réseau.
*   **Calcul de Routage**: Un appareil utilise le masque de sous-réseau pour effectuer une opération AND logique entre sa propre adresse IP et le masque, afin d'obtenir l'adresse réseau à laquelle il appartient. Cette information est cruciale pour le routage correct des paquets de données.
*   **Optimisation et Segmentation**: L'utilisation du masque de sous-réseau est fondamentale pour le sous-réseautage, permettant de diviser un grand réseau en plusieurs sous-réseaux plus petits. Ceci optimise l'utilisation des adresses IP et améliore la segmentation réseau pour des raisons de performance, de scalabilité et de sécurité.

## 💡 Importance en Cybersécurité
> Le masque de sous-réseau est un contrôle de sécurité fondamental en cybersécurité réseau car il permet une segmentation réseau efficace. Cette segmentation est essentielle pour isoler les systèmes critiques, contenir la propagation d'logiciels malveillants ou d'attaques, et réduire la surface d'attaque. Une configuration appropriée des masques de sous-réseau, dans le cadre d'une politique de sécurité robuste, facilite la mise en œuvre du principe du moindre privilège en limitant la communication réseau entre les sous-réseaux, et améliore la capacité de surveillance et d'intervention en cas d'incident.

## 🔗 Notes Connexes
*   Adresse IP
*   IPv4
*   Sous-réseautage
*   Segmentation Réseau
*   Classless Inter-Domain Routing (CIDR)
*   Adresse Réseau
*   Adresse d'Hôte
*   Adresse de Diffusion