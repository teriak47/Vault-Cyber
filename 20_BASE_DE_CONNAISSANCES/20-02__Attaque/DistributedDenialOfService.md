---
tags:
  - attaque
aliases:
  - Attaque par Déni de Service Distribué
  - DDoS
  - Distributed Denial of Service
  - Déni de Service Distribué
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque par Déni de Service Distribué (DDoS)

## 📥 Définition
> Une attaque par déni de service distribué (DDoS) vise à rendre un service ou une ressource indisponible en la submergeant d'un flot de trafic malveillant provenant de multiples hôtes distribués, souvent orchestrés via un botnet. L'objectif est d'épuiser les ressources de la cible, la rendant inaccessible aux utilisateurs légitimes.

## 🎯 Vecteurs d'Attaque
*   **Attaques de volume** : Saturant la bande passante du réseau ou du serveur cible. Elles opèrent généralement aux couches réseau et de transport du modèle OSI (par exemple, UDP ou ICMP floods).
*   **Attaques protocolaires** : Ciblant des vulnérabilités au niveau des protocoles, épuisant les ressources de connexion du serveur (par exemple, SYN Flood) ou des équipements réseau.
*   **Attaques de la couche applicative** : Exploitant des vulnérabilités au niveau de la couche applicative (couche 7 du modèle OSI) avec des requêtes complexes et coûteuses en ressources (par exemple, requêtes HTTP malformées ou excessives).

## 💥 Impacts Potentiels
*   Interruption de service
*   Pertes financières
*   Atteinte à la réputation
*   Exfiltration de données (parfois comme diversion pour masquer d'autres attaques)

##  concret
> Imaginez un magasin populaire qui reçoit soudainement des milliers de personnes qui bloquent l'entrée et les allées, non pas pour acheter, mais pour empêcher les clients légitimes d'accéder aux produits et services. Le magasin n'est pas physiquement endommagé, mais il est totalement paralysé. Dans le monde numérique, une attaque DDoS est similaire : un site web, une application en ligne ou un serveur est inondé de requêtes inutiles par un réseau de bots, le rendant inaccessible pour ses utilisateurs habituels.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Sensibilisation des utilisateurs aux risques d'infection des ordinateurs pour prévenir la formation de botnets.
    *   Implémentation de pare-feu et de filtrage de trafic en périphérie du réseau.
    *   Utilisation de services de mitigation DDoS spécialisés (CDN, WAF cloud) capables d'absorber et de filtrer le trafic malveillant.
    *   Mise en place de limitation de débit sur les serveurs et équipements réseau.
*   **Détection** :
    *   Systèmes de détection d'intrusion (IDS) et IPS pour identifier et bloquer le trafic suspect.
    *   Surveillance réseau et analyse du trafic réseau pour détecter les anomalies de comportement.
*   **Réponse** :
    *   Plan de réponse à incident clair pour détecter, contenir et récupérer rapidement d'une attaque DDoS.
    *   Coopération avec les FAI et les fournisseurs de services anti-DDoS.

## 🔗 Notes Connexes
*   Déni de Service (DoS)
*   Botnet
*   Cybersécurité
*   Disponibilité
*   SYN Flood
*   Congestion Réseau
---