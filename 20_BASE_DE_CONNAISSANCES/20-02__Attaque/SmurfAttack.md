---
tags:
  - attaque
  - attaque/smurf
  - attaque/deni-de-service
  - usurpation/ip
aliases:
  - Attaque Smurf
  - Smurf Attack
archetype: attaque
source:
cssclasses:
  - max
---

# Attaque Smurf

## 📥 Définition
> L'attaque Smurf est une forme d'attaque par déni de service qui exploite des réseaux de ordinateurs pour surcharger un système victime en utilisant des requêtes ICMP de diffusion avec une adresse IP source usurpée.

## 🎯 Vecteurs d'Attaque
*   **Requêtes ICMP de diffusion**: L'attaquant envoie un grand nombre de requêtes ICMP (ping) à l'adresse de diffusion d'un réseau tiers. Chaque hôte de ce domaine de diffusion répondra à la cible.
*   **Usurpation d'adresse IP**: Les paquets ICMP envoyés par l'attaquant ont une adresse IP source falsifiée, qui est en réalité l'adresse IP de la victime.

## 💥 Impacts Potentiels
*   Indisponibilité de service
*   Congestion du réseau
*   Compromission du système (indirectement par la surcharge)
*   Perte financière due à l'interruption des services en ligne

## 🗣️ Exemple concret
> Un attaquant envoie de nombreux paquets ICMP à l'adresse de diffusion d'un réseau mal configuré. Chaque paquet a l'adresse IP source de la cible (la victime). Tous les hôtes sur ce domaine de diffusion reçoivent le paquet et répondent à la cible. Si le réseau de diffusion compte des centaines d'hôtes, la victime est bombardée par des centaines de réponses pour chaque paquet initial envoyé par l'attaquant, provoquant une surcharge et rendant ses services en ligne inaccessibles pour les utilisateurs légitimes.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Désactiver les réponses ICMP de diffusion sur les routeurs et dispositifs intermédiaires (conformément à la RFC 2644).
    *   Mettre en œuvre le filtrage d'entrée pour empêcher les paquets avec des adresses IP sources usurpées de quitter le réseau interne.
    *   Utiliser des pare-feu pour filtrer les requêtes ICMP entrantes et sortantes anormales.
    *   Segmenter le réseau pour limiter les domaines de diffusion.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) pour surveiller le trafic réseau à la recherche d'anomalies.
    *   Outils de surveillance réseau pour identifier les pics de trafic ICMP.
*   **Réponse** :
    *   Mettre en œuvre un plan de réponse à incident pour réagir rapidement aux attaques par déni de service.
    *   Appliquer la limitation de débit sur les routeurs ou pare-feu pour le trafic ICMP.

## 🔗 Notes Connexes
*   Déni de Service
*   DDoS
*   Usurpation d'adresse IP
*   ICMP
*   Adresse de Diffusion
*   Attaque par amplification
*   Configuration réseau