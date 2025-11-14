---
tags:
  - gestion-trafic/limitation-debit
  - vecteurs-attaque/saturation
  - cyberattaque/deni-service
  - cybersécurité
aliases:
  - Déni de Service
  - DoS
  - Denial of Service
source:
  - 
cssclasses:
  - max
---

# Déni de Service (DoS)

## 📥 Définition en une phrase
> Une attaque par déni de service (DoS) est une tentative malveillante de rendre une ressource ou un service réseau indisponible pour ses utilisateurs légitimes en submergeant le système de requêtes ou en exploitant une vulnérabilité.

## 🧠 Concepts Clés / Fonctionnement
*   **Principe d'Indisponibilité :** L'objectif principal est d'empêcher les utilisateurs légitimes d'accéder à un service, une ressource ou un site web.
*   **Types d'Attaques :** Les attaques DoS peuvent cibler différentes couches du modèle OSI :
    *   **Attaques par Volume :** Saturent la bande passante du réseau avec un trafic important (ex: [[UDPFlood|UDP Flood]], [[ICMPFlood|ICMP Flood]]).
    *   **Attaques par [[Protocols|Protocole]] :** Exploitent les faiblesses des protocoles de communication pour consommer des ressources serveur (ex: [[SYNFlood|SYN Flood]]).
    *   **Attaques de Couche Application :** Ciblent des applications web spécifiques pour les rendre inopérantes avec des requêtes coûteuses à traiter (ex: requêtes HTTP lentes).
*   **Vecteurs d'Attaque :** Utilise souvent une seule source ou un nombre limité de sources pour générer l'attaque.
*   **Consommation de Ressources :** Vise à épuiser les ressources du serveur (CPU, mémoire, bande passante) ou du réseau.

## 🛡️ Risques / Menaces Associés
*   [[AvailabilityLoss|Perte de disponibilité]] des services critiques.
*   [[ReputationDamage|Dommage à la réputation]] et perte de confiance des clients.
*   [[FinancialLoss|Pertes financières]] dues à l'indisponibilité des opérations.
*   Potentiel de servir de diversion pour d'autres [[Cyberattack|cyberattaques]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] :** Détectent et bloquent le trafic malveillant.
*   **[[Firewall|Pare-feux]] :** Configurer des règles pour filtrer le trafic et bloquer les paquets suspects.
*   **[[RateLimiting|Limitation de débit]] :** Restreindre le nombre de requêtes qu'un client ou une adresse IP peut faire dans un laps de temps donné.
*   **[[ContentDeliveryNetwork|Réseaux de Diffusion de Contenu (CDN)]] :** Aident à absorber le trafic excessif et à distribuer les requêtes.
*   **Plan de [[IncidentResponse|Réponse aux Incidents]] :** Mettre en place des procédures pour réagir rapidement à une attaque DoS.
*   **Surveillance Réseau :** Monitorer le trafic pour identifier les anomalies et les pics inhabituels.

## 🔗 Notes Connexes
*   [[DistributedDenialOfService|Déni de Service Distribué (DDoS)]]
*   [[Cyberattack|Cyberattaque]]
*   [[Availability|Disponibilité]]
*   [[NetworkSecurity|Sécurité Réseau]]