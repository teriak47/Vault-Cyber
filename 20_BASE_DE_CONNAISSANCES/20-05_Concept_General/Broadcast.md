---
tags:
  - reseau
  - communication
aliases:
  - Diffusion
  - Broadcast (réseau)
  - Broadcasting
  - Diffusion réseau
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Diffusion (Broadcast)

## 📥 Définition en une phrase
> La diffusion est une méthode de communication réseau où un unique message est envoyé à tous les hôtes ou périphériques réseau situés au sein d'un même domaine de diffusion.

## 🧠 Concepts Clés / Piliers
*   **Mécanisme de Transmission**: Un paquet est expédié avec une adresse MAC de destination spéciale (généralement `FF:FF:FF:FF:FF:FF`) ou une adresse IP de diffusion, assurant que chaque hôte du domaine de diffusion le reçoive.
*   **Portée et Limites**: Le trafic de diffusion est intrinsèquement limité à son domaine de diffusion. Les routeurs agissent comme des frontières par défaut, empêchant la propagation des diffusions entre différents réseaux, tandis que les commutateurs réseau transmettent le trafic de diffusion au sein du LAN ou du VLAN auquel ils appartiennent.
*   **Utilisation Typique**: Essentielle pour des protocoles réseau fondamentaux tels que l'ARP (résolution d'adresses IP en adresses MAC) et le DHCP (attribution dynamique d'adresses IP).
*   **Contraste avec d'autres Communications**: La diffusion se distingue de l'unidiffusion (communication un-à-un) et de la multidiffusion (communication un-à-un-groupe).

## 💡 Importance en Cybersécurité
> La diffusion est un pilier fondamental du fonctionnement des réseaux locaux, facilitant la découverte et l'allocation des ressources. Cependant, sa nature "à tous" la rend intrinsèquement vulnérable. Un excès de trafic de diffusion peut entraîner une congestion réseau (potentiellement une tempête de diffusion) et des interruptions de service. De plus, l'interception des paquets de diffusion est triviale pour un attaquant au sein du même segment réseau, posant des risques d'écoute clandestine et d'attaques d'usurpation (comme l'empoisonnement ARP), particulièrement dans des réseaux plats. Une segmentation réseau adéquate, la sécurité des ports et des mécanismes de contrôle des tempêtes sont cruciaux pour atténuer ces risques.

## 🔗 Notes Connexes
*   Domaine de Diffusion
*   Communication réseau
*   Protocole de Résolution d'Adresses (ARP)
*   Protocole de Configuration d'Hôte Dynamique (DHCP)
*   Multidiffusion
*   Unidiffusion
*   Segmentation Réseau
*   Réseau Local Virtuel (VLAN)
*   Tempête de Diffusion
*   Contrôle des Tempêtes