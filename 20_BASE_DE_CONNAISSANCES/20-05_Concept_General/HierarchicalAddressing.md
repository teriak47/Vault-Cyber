---
tags:
aliases:
  - Adressage Hiérarchique
  - Hierarchical Addressing
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adressage Hiérarchique

## 📥 Définition en une phrase
> L'adressage hiérarchique est une méthode structurée d'affectation des adresses IP qui divise logiquement un réseau en sous-réseaux plus petits, facilitant un routage efficace et une gestion simplifiée de l'adressage IP à grande échelle.

## 🧠 Concepts Clés / Piliers
*   **Division Logique: Une adresse IP est logiquement séparée en une partie réseau et une partie hôte. La partie réseau identifie le réseau (souvent un LAN ou WAN), et la partie hôte désigne l'hôte unique au sein de ce réseau.
*   **Routage Efficace**: Les routeurs exploitent principalement la partie réseau pour diriger les paquets vers le réseau de destination approprié. Cette approche réduit significativement la taille et la complexité des tables de routage, car il n'est pas nécessaire de stocker des entrées pour chaque hôte individuel.
*   **Subdivision de Réseau**: L'utilisation du masque de sous-réseau permet de définir la partie réseau et la partie hôte d'une adresse IP, facilitant la création de segments réseau plus petits, appelés sous-réseaux.
*   **Évolutivité et Gestion**: Ce modèle d'adressage améliore l'évolutivité des réseaux. Les entreprises et les FAI peuvent ajouter de nouveaux sous-réseaux ou réseaux distants sans avoir à réaffecter l'ensemble de l'adressage IP.
*   **Indépendance Logique**: L'adressage IP représente une adresse logique de la couche réseau (Modèle TCP/IP), qui est distincte de l'adresse MAC physique de la carte d'interface réseau.

## 💡 Importance en Cybersécurité
> L'adressage hiérarchique est fondamental pour la cybersécurité car il permet une segmentation réseau efficace, un contrôle de sécurité essentiel pour isoler les systèmes et limiter la propagation des logiciels malveillants et des attaques. Une bonne conception facilite l'application de contrôles d'accès granulaires et du principe du moindre privilège, réduisant ainsi l'surface d'attaque. Inversement, une mauvaise configuration réseau peut introduire des vulnérabilités de sécurité significatives, conduisant à des accès non autorisés et à une compromission de système. Une politique de sécurité rigoureuse et l'utilisation de protocoles de routage sécurisés sont indispensables pour maintenir l'intégrité et la confidentialité des données au sein d'une architecture hiérarchique.

## 🔗 Notes Connexes
*   Adressage IP
*   Couche Réseau
*   Protocole Internet
*   Masque de Sous-réseau
*   Table de Routage
*   Segmentation Réseau
*   Routage
*   Subdivision de réseau
*   Conception de Réseau Hiérarchique
*   Contrôle de Sécurité