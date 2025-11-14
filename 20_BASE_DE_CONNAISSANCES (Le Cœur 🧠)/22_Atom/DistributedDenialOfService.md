---
tags:
  - protection/mitigation-ddos
  - reseau/epuisement-ressources
  - cyberattaque/deni-service
  - botnets
aliases:
  - Attaque par Déni de Service Distribué
  - DDoS
  - Distributed Denial of Service
source:
  - 
cssclasses:
  - max
---

# Attaque par Déni de Service Distribué (DDoS)

## 📥 Définition en une phrase
> Une attaque par déni de service distribué (DDoS) vise à rendre un service ou une ressource indisponible en le submergeant d'un flot de trafic malveillant provenant de multiples sources distribuées, souvent un [[Botnet|botnet]].

## 🧠 Concepts Clés / Fonctionnement
*   **Distribution des sources :** Contrairement à une attaque DoS classique, les attaques DDoS utilisent de multiples machines compromises (constituant un [[Botnet|botnet]]) pour générer le trafic malveillant, rendant la détection et la mitigation plus complexes.
*   **Ciblage de la disponibilité :** L'objectif principal est d'épuiser les ressources du serveur ciblé (bande passante, CPU, mémoire, connexions réseau) ou de l'application, l'empêchant de répondre aux requêtes légitimes et le rendant inaccessible aux utilisateurs.
*   **Vecteurs d'attaque variés :** Les attaques DDoS peuvent cibler différentes couches du [[OpenSystemsInterconnectionModel|modèle OSI]], allant des attaques de volume (couches 3/4, ex: UDP/ICMP floods) qui saturent la bande passante, aux attaques protocolaires (couche 4, ex: SYN floods) qui épuisent les ressources de connexion, et aux attaques de la [[ApplicationLayer|couche applicative]] (couche 7, ex: requêtes HTTP complexes) qui exploitent des vulnérabilités logicielles spécifiques.
*   **Impact :** Provoque des interruptions de service, des pertes financières (revenus, productivité), et des dommages à la réputation de l'organisation ciblée.

## 🛡️ Risques / Menaces Associés
*   [[ServiceDisruption|Interruption de service]]
*   [[FinancialLoss|Pertes financières]]
*   [[ReputationalDamage|Atteinte à la réputation]]
*   [[DataExfiltration|Exfiltration de données]] (parfois utilisée comme diversion)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DDoSMitigationService|Services de mitigation DDoS]] : Utilisation de fournisseurs spécialisés (CDN, WAF cloud) qui absorbent et filtrent le trafic malveillant avant qu'il n'atteigne l'infrastructure cible.
*   [[TrafficFiltering|Filtrage et analyse de trafic]] : Implémentation de pare-feu et de systèmes de détection/prévention d'intrusion (IDS/IPS) pour identifier et bloquer le trafic suspect.
*   [[RateLimiting|Limitation de débit]] : Configuration de mécanismes pour limiter le nombre de requêtes qu'une source unique ou un groupe de sources peut envoyer sur une période donnée.
*   [[NetworkSegmentation|Segmentation réseau]] : Séparer les services critiques pour minimiser l'impact d'une attaque sur l'ensemble de l'infrastructure.
*   [[IncidentResponsePlan|Plan de réponse aux incidents]] : Avoir un plan clair pour détecter, contenir et récupérer d'une attaque DDoS.

## 🔗 Notes Connexes
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[Botnet|Botnet]]
*   [[CyberAttack|Cyberattaque]]
*   [[Availability|Disponibilité]]
*   [[SYNFlood|SYN Flood]]