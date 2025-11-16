---
tags:
  - attaque
aliases:
  - Déni de Service
  - DoS
  - Denial of Service
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Déni de Service (DoS)

## 📥 Définition
> Une [[DenialOfService|attaque par déni de service (DoS)]] est une [[Attack|tentative malveillante]] de rendre une [[Resource|ressource]] ou un service réseau indisponible pour ses [[User|utilisateurs légitimes]] en submergeant le [[System|système]] de requêtes ou en exploitant une [[Vulnerability|vulnérabilité]]. L'objectif est d'empêcher l'[[Availability|accès normal]] aux services.

## 🎯 Vecteurs d'Attaque
*   **Surcharge Volumétrique** : Saturation de la [[NetworkBandwidth|bande passante]] du réseau avec un trafic massivement élevé (ex: [[UDPFlood|UDP Flood]], [[ICMPFlood|ICMP Flood]]).
*   **Exploitation de Vulnérabilités de [[NetworkProtocol|Protocoles]]** : Cible les faiblesses de la pile de [[Protocol|protocoles]] de communication pour consommer les [[Server|ressources]] du [[Server|serveur]] (ex: [[SYNFlood|SYN Flood]]).
*   **Attaques de la [[ApplicationLayer|Couche Application]]** : Concentrent l'[[Attack|attaque]] sur des [[SoftwareApplication|applications]] web spécifiques, envoyant des requêtes légitimes mais coûteuses à traiter pour épuiser les ressources applicatives.

## 💥 Impacts Potentiels
*   [[Availability|Perte de disponibilité]] des services critiques.
*   [[ReputationalDamage|Dommage à la réputation]] et perte de confiance des clients.
*   [[FinancialLoss|Pertes financières]] dues à l'indisponibilité des opérations et des [[OnlineServices|services en ligne]].
*   Peut servir de diversion pour d'autres [[DigitalAttack|attaques numériques]] plus discrètes, masquant une [[DataTheft|exfiltration de données]] ou une [[SystemCompromise|compromission de système]].

## 📝 Exemple concret
> Imaginez un concert où la salle est conçue pour accueillir 1000 personnes. Une [[DenialOfService|attaque DoS]] serait l'équivalent de 10 000 personnes essayant d'entrer en même temps par une seule porte. Même si 9 000 d'entre elles sont des imposteurs et que les 1 000 légitimes ont des billets, la porte ne peut pas gérer l'afflux, et personne ne peut entrer. Dans le monde numérique, c'est un [[Server|serveur]] ou un [[Network|réseau]] submergé par un volume anormalement élevé de [[Packet|paquets]] de données, le rendant incapable de répondre aux [[Request|requêtes]] des [[User|utilisateurs]] légitimes.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[RateLimiting|Limitation de débit]] : Restreindre le nombre de requêtes ou de connexions qu'un [[Client|client]] ou une [[InternetProtocol|adresse IP]] peut initier dans un intervalle de temps donné.
    *   [[Firewall|Pare-feux]] et [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] : Configurer des règles strictes pour filtrer le [[NetworkTrafficAnalysis|trafic]] et bloquer les [[Packet|paquets]] suspects ou les [[MessagePattern|modèles d'attaque]] connus.
    *   [[ContentDeliveryNetwork|Réseaux de Diffusion de Contenu (CDN)]] : Utiliser des services CDN pour distribuer le [[NetworkTrafficAnalysis|trafic]] et absorber les pics d'[[Attack|attaques volumétriques]].
*   **Détection** :
    *   [[NetworkMonitoring|Surveillance réseau]] et [[SecurityInformationAndEventManagement|SIEM]] : Mettre en place une surveillance continue du [[NetworkTrafficAnalysis|trafic réseau]] pour identifier les anomalies, les hausses soudaines de [[NetworkTrafficAnalysis|trafic]] ou les [[MessagePattern|modèles de requêtes]] inhabituels.
    *   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] : Détecter les signatures d'[[Attack|attaques]] et les comportements anormaux.
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : Définir et tester des procédures claires pour réagir rapidement, minimiser l'impact et rétablir les services en cas d'[[Attack|attaque DoS]].

## 🔗 Notes Connexes
*   [[DistributedDenialOfService|Déni de Service Distribué (DDoS)]]
*   [[Attack|Attaque]]
*   [[Availability|Disponibilité]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]
*   [[Payload|Charge utile]]