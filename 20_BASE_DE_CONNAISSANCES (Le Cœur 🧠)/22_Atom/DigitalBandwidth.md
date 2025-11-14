---
tags:
  - vol/bande-passante
  - gestion-trafic/mise-en-forme
  - reseau/cdn
  - reseau/bande-passante
  - cyberattaque/deni-service
  - gestion-trafic/qualite-service
aliases:
  - Bande passante numérique
  - Digital Bandwidth
source:
  - null
cssclasses:
  - max
---

# Bande Passante Numérique

## 📥 Définition en une phrase
> La bande passante numérique est la quantité maximale de données qui peut être transférée sur une connexion réseau ou un support de communication pendant une période donnée, généralement mesurée en bits par seconde (bps).

## 🧠 Concepts Clés / Fonctionnement
*   **Capacité Maximale :** Représente le débit théorique maximal d'une connexion, et non le débit réel qui peut être influencé par divers facteurs (latence, congestion, équipement).
*   **Unités de Mesure :** Fréquemment exprimée en kilobits par seconde (Kbps), mégabits par seconde (Mbps) ou gigabits par seconde (Gbps), indiquant le volume de données par unité de temps.
*   **Facteurs Influents :** La qualité du support physique (câble, fibre optique), les équipements réseau (routeurs, commutateurs), la congestion du réseau et les protocoles de transmission peuvent limiter le débit effectif.
*   **Différence avec la Latence :** La bande passante est le "volume" de données qui peut passer, tandis que la [[Latency|latence]] est le "délai" avant que les données n'atteignent leur destination.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaque par déni de service (DoS)]] ou [[DistributedDenialOfService|DDoS]] : Des attaques visant à saturer la bande passante d'une cible, rendant les services inaccessibles aux utilisateurs légitimes.
*   [[NetworkCongestion|Congestion réseau]] : Une bande passante insuffisante pour la demande peut entraîner des ralentissements, des pertes de paquets et une dégradation de la performance.
*   [[BandwidthTheft|Vol de bande passante]] : L'utilisation non autorisée de la bande passante d'un réseau par des tiers malveillants, souvent à des fins illégales ou pour des opérations clandestines.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[TrafficShaping|Mise en forme du trafic (Traffic Shaping)]] et [[QualityOfService|Qualité de Service (QoS)]] : Techniques pour prioriser ou limiter certains types de trafic, garantissant que les applications critiques disposent de la bande passante nécessaire.
*   [[IntrusionPreventionSystem|Systèmes de prévention d'intrusion (IPS)]] et [[Firewall|Pare-feux]] : Détectent et bloquent les trafics malveillants ou anormaux qui pourraient tenter de saturer la bande passante.
*   [[ContentDeliveryNetwork|Réseaux de diffusion de contenu (CDN)]] : Distribuent le contenu sur des serveurs géographiquement proches des utilisateurs, réduisant la charge sur la bande passante du serveur d'origine.
*   [[NetworkMonitoring|Surveillance réseau]] : Surveiller en continu l'utilisation de la bande passante pour détecter les anomalies et prévenir les problèmes de performance ou les attaques.

## 🔗 Notes Connexes
*   [[Throughput|Débit]]
*   [[Latency|Latence]]
*   [[NetworkPerformance|Performance Réseau]]
*   [[NetworkCapacity|Capacité Réseau]]