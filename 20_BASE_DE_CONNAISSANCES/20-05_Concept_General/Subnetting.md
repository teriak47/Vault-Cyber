---
tags:
  - concept/general
  - reseau
  - reseau/segmentation
aliases:
  - Subdivision de réseau
  - Subnetting IP
  - Subnetting
  - IP Subnetting
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Subdivision de Réseau (Subnetting)

## 📥 Définition en une phrase
> Le Subnetting est le processus de division d'un réseau IP en plusieurs sous-réseaux plus petits et logiquement distincts, facilitée par l'utilisation d'un masque de sous-réseau étendu.

## 🧠 Concepts Clés / Piliers
*   **Création de Sous-Réseaux**: Implique l'"emprunt" de bits de la partie hôte d'une adresse IP pour les intégrer à la partie réseau, définissant ainsi des sous-réseaux uniques.
*   **Masque de Sous-Réseau**: Un masque de sous-réseau est utilisé pour déterminer la partie de l'adresse IP qui identifie le réseau et celle qui identifie l'hôte au sein de ce sous-réseau.
*   **Calcul Binaire**: La mise en œuvre du Subnetting repose sur des calculs binaires pour attribuer des plages d'adresses IP valides, l'adresse réseau et l'adresse de diffusion pour chaque sous-réseau.
*   **Domaines de Diffusion**: Chaque sous-réseau créé correspond à un domaine de diffusion distinct, réduisant la taille des domaines et le volume de trafic de diffusion.

## 💡 Importance en Cybersécurité
> Le Subnetting est fondamental pour la cybersécurité car il permet une segmentation réseau efficace. Cette segmentation isole les segments réseau, limitant la propagation des logiciels malveillants et des attaques, et facilitant la mise en œuvre de contrôles d'accès granulaires. En réduisant la taille des domaines de diffusion, il diminue également la surface d'attaque et améliore la performance réseau en réduisant la congestion. Il optimise l'utilisation des adresses IP et aide à l'organisation des réseaux d'entreprise.

## 🔗 Notes Connexes
*   Segmentation Réseau
*   Blocs d'adresses IP
*   Masque de Sous-Réseau
*   Domaine de Diffusion
*   Sécurité Réseau
*   Protocole Internet