---
tags:
  - concept/general
  - reseau
  - reseau/segmentation
aliases:
  - Sub-network
  - Sous-réseau
  - Subnet
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Sous-réseau (Subnet)

## 📥 Définition en une phrase
> Une subdivision logique d'un espace d'adressage IP au sein d'un réseau plus vaste, optimisant l'organisation, la sécurité et la performance réseau.

## 🧠 Concepts Clés / Piliers
*   **Segmentation**: Un sous-réseau divise un grand réseau en plusieurs segments plus petits, logiquement distincts et gérables, limitant ainsi la taille des domaines de diffusion.
*   **Identification**: Il est défini par une adresse IP et un masque de sous-réseau qui identifie la partie réseau et la partie hôte de l'adresse.
*   **Contrôle du Trafic**: La pratique du subnetting permet de contrôler le trafic réseau, de réduire la taille des domaines de diffusion et d'améliorer l'efficacité du routage.
*   **Routage**: Les dispositifs réseau tels que les routeurs utilisent le masque de sous-réseau pour déterminer si un paquet est destiné à un hôte sur le même sous-réseau ou s'il doit être routé vers un autre réseau distant.

## 💡 Importance en Cybersécurité
> La création de sous-réseaux est une mesure de sécurité essentielle. Elle permet une segmentation réseau qui isole les systèmes critiques ou les données sensibles, réduisant ainsi la surface d'attaque. En cas de compromission d'un segment, l'attaquant est confiné à ce sous-réseau, limitant la propagation latérale et les pertes financières. Elle facilite également la surveillance réseau et l'application de politiques de sécurité granulaires.

## 🔗 Notes Connexes
*   Subnetting
*   Masque de Sous-réseau
*   CIDR
*   Segmentation Réseau
*   Protocole Internet (IP)
*   Routage
*   Couche Réseau