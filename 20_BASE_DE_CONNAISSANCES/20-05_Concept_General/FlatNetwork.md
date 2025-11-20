---
tags:
aliases:
  - Réseau Plat
  - Single Local Network Segment
  - Réseau sans segmentation
  - Flat Network
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Réseau Plat

## 📥 Définition en une phrase
> Une topologie de réseau plat est une architecture où tous les hôtes se trouvent sur un seul domaine de diffusion et partagent le même segment de réseau local, ce qui simplifie la communication directe mais peut entraîner des défis de performance et de sécurité.

## 🧠 Concepts Clés / Piliers
*   **Simplicité Structurelle**: Tous les hôtes sont sur un unique LAN et un seul domaine de diffusion, ce qui simplifie la configuration initiale et peut réduire les coûts d'infrastructure.
*   **Communication Directe**: Les hôtes utilisent le protocole ARP pour se découvrir mutuellement et communiquer directement, sans nécessiter de routeur intermédiaire pour les communications au sein du segment.
*   **Visibilité Élevée**: Tous les équipements connectés sur le segment sont mutuellement visibles, facilitant les interactions au sein du groupe mais augmentant également la surface d'exposition.

## 💡 Importance en Cybersécurité
> Bien que les réseaux plats soient faciles à mettre en place pour les petits réseaux domestiques ou les petits bureaux, ils présentent des vulnérabilités de sécurité significatives. L'absence de segmentation réseau signifie qu'une seule vulnérabilité sur un hôte peut potentiellement exposer l'ensemble du réseau à des menaces, favorisant la propagation de malwares et facilitant les attaques de l'homme du milieu. La gestion de la qualité de service (QoS) et la surveillance réseau sont également plus complexes, rendant la réponse aux incidents plus ardue. Comprendre cette topologie est crucial pour évaluer et atténuer l'étendue de l'attaque dans un tel environnement.

## 🔗 Notes Connexes
*   Domaine de Diffusion
*   ARP
*   Segmentation Réseau
*   VLAN
*   Qualité de Service (QoS)
*   Réseau Local (LAN)
*   Sécurité Réseau
*   Routeur
*   Surface d'Attaque