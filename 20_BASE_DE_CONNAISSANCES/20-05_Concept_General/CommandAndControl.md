---
tags:
  - cybersecurite
  - attaque
  - reseau
aliases:
  - Commande et Contrôle
  - C2
  - Command and Control
  - C2 (Command and Control)
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Commandement et Contrôle (C2)

## 📥 Définition en une phrase
> Le Commandement et Contrôle (C2) est le mécanisme par lequel un attaquant maintient la communication et le contrôle sur des systèmes compromis (souvent appelés "bots" ou "agents") au sein d'un réseau cible, après une intrusion initiale.

## 🧠 Concepts Clés / Piliers
*   **Communication bidirectionnelle** : Établit un canal de communication secret entre l'attaquant et le système compromis pour envoyer des commandes et recevoir des données.
*   **Diversité des canaux** : Les communications C2 peuvent utiliser une multitude de protocoles (par exemple, HTTP/S, DNS, ICMP) pour se fondre dans le trafic légitime et éviter la détection.
*   **Fonctionnalités étendues** : Permet à l'attaquant d'exécuter des commandes à distance, d'exfiltrer des données sensibles, de télécharger des charges utiles supplémentaires, de propager le logiciel malveillant ou de coordonner des attaques plus complexes.
*   **Invisibilité et persistance** : Les infrastructures C2 sont souvent conçues pour être résilientes et difficiles à détecter et à démanteler, utilisant des techniques comme la dissimulation de domaine ou des serveurs proxy pour assurer la persistance.
*   **Phase de post-exploitation** : Constitue une étape cruciale de la Cyber Kill Chain, intervenant après l'accès initial et l'exécution du malware.

## 💡 Importance en Cybersécurité
> Le Commandement et Contrôle est la colonne vertébrale des cyberattaques post-intrusion, permettant aux acteurs de menace de maintenir une persistance et une communication avec les systèmes compromis. Il est essentiel pour la fuite de données, la distribution de logiciels malveillants (y compris ransomware et botnets) et la coordination d'attaques avancées. La détection et la rupture des canaux C2 sont donc une priorité absolue pour la réponse aux incidents et la sécurité réseau, car elles coupent le lien vital de l'attaquant et limitent l'étendue des dommages.

## 🔗 Notes Connexes
*   Malware
*   Botnet
*   Cyber Kill Chain
*   Renseignement sur les Menaces
*   Red Teaming
*   Exfiltration de Données
*   Segmentation Réseau
*   Système de Détection d'Intrusion (IDS)
*   Système de Prévention d'Intrusion (IPS)
*   SIEM
*   EDR
*   Pare-feu
*   Menaces Persistantes Avancées (APT)
*   Persistance
*   Dissimulation de domaine
*   Accès initial
*   Exécution