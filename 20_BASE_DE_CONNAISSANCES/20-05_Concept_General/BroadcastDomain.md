---
tags:
aliases:
  - Domaine de Diffusion
  - Broadcast Domain
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Domaine de Diffusion (Broadcast Domain)

## 📥 Définition en une phrase
> Un domaine de diffusion est une section logique d'un réseau informatique dans laquelle toutes les stations de travail peuvent atteindre les autres par diffusion au niveau de la couche liaison de données.

## 🧠 Concepts Clés / Piliers
*   **Propagation de Diffusion**: Lorsqu'un appareil envoie un message de diffusion, tous les autres appareils au sein du même domaine de diffusion le reçoivent, y compris les serveurs, clients et imprimantes réseau.
*   **Limites du Domaine**: Les routeurs agissent comme des frontières et ne transmettent pas les messages de diffusion entre différents domaines de diffusion. En revanche, les commutateurs, par défaut, transmettent les diffusions à tous leurs ports au sein du même domaine.
*   **Impact de la Taille**: Un grand domaine de diffusion peut générer un volume élevé de trafic de diffusion, entraînant une congestion réseau, une dégradation de la performance et augmentant les vulnérabilités de sécurité.
*   **Segmentation Logique**: Les VLANs sont une technique couramment utilisée pour segmenter un commutateur en plusieurs domaines de diffusion logiques, permettant ainsi de mieux gérer le trafic et d'améliorer la sécurité.

## 💡 Importance en Cybersécurité
> Le contrôle et la segmentation des domaines de diffusion sont fondamentaux pour la cybersécurité et la performance réseau. Des domaines trop étendus augmentent l'surface d'attaque, rendant le réseau vulnérable aux attaques par déni de service via des tempêtes de diffusion et facilitant l'écoute clandestine, ce qui peut exposer des données sensibles. Une gestion adéquate des domaines de diffusion est essentielle pour limiter la portée des attaques et optimiser le trafic réseau.

## 🔗 Notes Connexes
*   Domaine de Collision
*   VLAN
*   Segmentation Réseau
*   Routeur
*   Commutateur
*   ARP
*   NDP
*   Déni de Service
*   Écoute clandestine
*   Performance réseau
*   Sécurité Réseau
*   Surface d'attaque
*   Congestion Réseau
*   Tempête de Diffusion