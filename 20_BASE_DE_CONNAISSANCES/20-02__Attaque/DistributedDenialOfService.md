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
> Une [[DistributedDenialOfService|attaque par déni de service distribué (DDoS)]] vise à rendre un service ou une [[Resource|ressource]] indisponible en la submergeant d'un flot de [[NetworkTraffic|trafic malveillant]] provenant de multiples [[Host|hôtes]] distribués, souvent orchestrés via un [[Botnet|botnet]]. L'objectif est d'épuiser les ressources de la cible, la rendant inaccessible aux [[User|utilisateurs]] légitimes.

## 🎯 Vecteurs d'Attaque
*   **[[VolumeBasedAttack|Attaques de volume]]** : Saturant la [[Bandwidth|bande passante]] du réseau ou du [[Server|serveur]] cible. Elles opèrent généralement aux [[NetworkLayer|couches réseau]] et de [[TransportLayer|transport]] du [[OpenSystemsInterconnectionModel|modèle OSI]] (par exemple, [[UserDatagramProtocol|UDP]] ou [[InternetControlMessageProtocol|ICMP]] floods).
*   **[[ProtocolBasedAttack|Attaques protocolaires]]** : Ciblant des vulnérabilités au niveau des protocoles, épuisant les ressources de connexion du [[Server|serveur]] (par exemple, [[SYNFlood|SYN Flood]]) ou des [[NetworkDevice|équipements réseau]].
*   **[[ApplicationLayerAttack|Attaques de la couche applicative]]** : Exploitant des vulnérabilités au niveau de la [[ApplicationLayer|couche applicative]] (couche 7 du [[OpenSystemsInterconnectionModel|modèle OSI]]) avec des requêtes complexes et coûteuses en ressources (par exemple, requêtes [[HypertextTransferProtocol|HTTP]] malformées ou excessives).

## 💥 Impacts Potentiels
*   [[ServiceDisruption|Interruption de service]]
*   [[FinancialLoss|Pertes financières]]
*   [[ReputationalDamage|Atteinte à la réputation]]
*   [[DataExfiltration|Exfiltration de données]] (parfois comme diversion pour masquer d'autres [[Attack|attaques]])

##  concret
> Imaginez un magasin populaire qui reçoit soudainement des milliers de personnes qui bloquent l'entrée et les allées, non pas pour acheter, mais pour empêcher les clients légitimes d'accéder aux produits et services. Le magasin n'est pas physiquement endommagé, mais il est totalement paralysé. Dans le monde numérique, une [[DistributedDenialOfService|attaque DDoS]] est similaire : un site web, une [[OnlineServices|application en ligne]] ou un [[Server|serveur]] est inondé de requêtes inutiles par un [[Botnet|réseau de bots]], le rendant inaccessible pour ses [[User|utilisateurs]] habituels.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] aux risques d'[[Malware|infection]] des [[Computer|ordinateurs]] pour prévenir la formation de [[Botnet|botnets]].
    *   Implémentation de [[Firewall|pare-feu]] et de [[TrafficFiltering|filtrage de trafic]] en périphérie du [[Network|réseau]].
    *   Utilisation de [[DDoSMitigationService|services de mitigation DDoS]] spécialisés (CDN, WAF cloud) capables d'absorber et de filtrer le [[NetworkTraffic|trafic malveillant]].
    *   Mise en place de [[RateLimiting|limitation de débit]] sur les [[Server|serveurs]] et [[NetworkDevice|équipements réseau]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour identifier et bloquer le [[NetworkTraffic|trafic]] suspect.
    *   [[NetworkMonitoring|Surveillance réseau]] et [[NetworkTrafficAnalysis|analyse du trafic réseau]] pour détecter les anomalies de comportement.
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] clair pour détecter, contenir et récupérer rapidement d'une [[DistributedDenialOfService|attaque DDoS]].
    *   Coopération avec les [[InternetServiceProvider|FAI]] et les fournisseurs de [[DDoSMitigationService|services anti-DDoS]].

## 🔗 Notes Connexes
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[Botnet|Botnet]]
*   [[Cybersecurity|Cybersécurité]]
*   [[Availability|Disponibilité]]
*   [[SYNFlood|SYN Flood]]
*   [[NetworkCongestion|Congestion Réseau]]
---