---
tags:
  - concept/general
aliases:
  - Unidiffusion
  - Unicast
  - Unidiffusion (réseau)
  - Communication un-à-un
  - One-to-One Communication
  - Point-to-Point Communication
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Unicast (Unidiffusion)

## 📥 Définition en une phrase
> L'Unicast est un mode de communication réseau où un seul émetteur envoie des données à un seul récepteur spécifique.

## 🧠 Concepts Clés / Piliers
*   **Communication Point-à-Point**: C'est le mode de communication le plus fondamental, où un appareil cible établit une connexion directe avec un autre appareil cible, sans interférence avec d'autres hôtes sur le réseau. Cela est également appelé communication un à un.
*   **Adressage Unique**: La livraison des paquets en unicast est rendue possible par l'utilisation d'adresses IP et/ou d'adresses MAC uniques pour chaque périphérique réseau. Chaque paquet contient l'adresse source et l'adresse de destination spécifiques, garantissant un routage précis.
*   **Fiabilité et Contrôle**: Les protocoles de la couche Transport tels que TCP s'appuient fortement sur l'unicast pour établir des connexions fiables. Ils incluent des mécanismes de retransmission, de contrôle de flux et d'accusés de réception pour s'assurer que les données arrivent intactes et dans le bon ordre, contrairement au UDP qui est également unicast mais sans garantie de livraison.

## 💡 Importance en Cybersécurité
> L'unicast est le pilier de la plupart des communications réseau modernes, incluant les transactions en ligne, la navigation Web, et l'échange d'e-mails. Sa nature ciblée est essentielle pour établir des canaux de communication confidentiels et intègres (par exemple via TLS ou SSH). Pour la cybersécurité, il permet la surveillance et l'analyse ciblée du trafic vers et depuis des hôtes spécifiques, aidant à détecter les attaques ciblées et les exfiltrations de données. Cependant, les attaquants exploitent également la nature unicast pour les attaques ciblées de hameçonnage, les exécutions de code à distance et les compromissions de système individuels. Une mauvaise configuration des pare-feu ou des routeurs peut exposer des hôtes unicast à des attaques externes.

## 🔗 Notes Connexes
*   Multicast
*   Broadcast
*   Internet Protocol
*   Adresse MAC
*   Transmission Control Protocol (TCP)
*   User Datagram Protocol (UDP)
*   Communication réseau
*   Architecture Client-Serveur
*   Passerelle par défaut