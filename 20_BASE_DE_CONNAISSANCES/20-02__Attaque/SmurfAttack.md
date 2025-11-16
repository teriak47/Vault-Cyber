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
> L'[[SmurfAttack|attaque Smurf]] est une forme d'[[DenialOfService|attaque par déni de service]] qui exploite des [[Network|réseaux]] de [[Computer|ordinateurs]] pour surcharger un [[System|système victime]] en utilisant des [[InternetControlMessageProtocol|requêtes ICMP]] de [[Broadcast|diffusion]] avec une [[Spoofing|adresse IP source usurpée]].

## 🎯 Vecteurs d'Attaque
*   **[[InternetControlMessageProtocol|Requêtes ICMP]] de [[Broadcast|diffusion]]**: L'[[ThreatActor|attaquant]] envoie un grand nombre de [[InternetControlMessageProtocol|requêtes ICMP]] (ping) à l'[[BroadcastAddress|adresse de diffusion]] d'un [[Network|réseau]] tiers. Chaque [[Host|hôte]] de ce [[BroadcastDomain|domaine de diffusion]] répondra à la [[System|cible]].
*   **[[Spoofing|Usurpation d'adresse IP]]**: Les [[InternetControlMessageProtocol|paquets ICMP]] envoyés par l'[[ThreatActor|attaquant]] ont une [[SourceInternetProtocolVersion4Address|adresse IP source]] falsifiée, qui est en réalité l'[[InternetProtocol|adresse IP]] de la [[System|victime]].

## 💥 Impacts Potentiels
*   [[DenialOfService|Indisponibilité de service]]
*   [[NetworkCongestion|Congestion du réseau]]
*   [[SystemCompromise|Compromission du système]] (indirectement par la surcharge)
*   [[FinancialLoss|Perte financière]] due à l'interruption des [[OnlineServices|services en ligne]]

## 🗣️ Exemple concret
> Un [[ThreatActor|attaquant]] envoie de nombreux [[InternetControlMessageProtocol|paquets ICMP]] à l'[[BroadcastAddress|adresse de diffusion]] d'un [[NetworkMisconfiguration|réseau mal configuré]]. Chaque paquet a l'[[SourceInternetProtocolVersion4Address|adresse IP source]] de la [[System|cible]] (la [[System|victime]]). Tous les [[Host|hôtes]] sur ce [[BroadcastDomain|domaine de diffusion]] reçoivent le paquet et répondent à la [[System|cible]]. Si le [[Network|réseau]] de diffusion compte des centaines d'[[Host|hôtes]], la [[System|victime]] est bombardée par des centaines de réponses pour chaque paquet initial envoyé par l'[[ThreatActor|attaquant]], provoquant une [[DenialOfService|surcharge]] et rendant ses [[OnlineServices|services en ligne]] inaccessibles pour les [[User|utilisateurs légitimes]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Désactiver les [[Broadcast|réponses ICMP de diffusion]] sur les [[Router|routeurs]] et [[IntermediateDevice|dispositifs intermédiaires]] (conformément à la RFC 2644).
    *   Mettre en œuvre le [[IngressFiltering|filtrage d'entrée]] pour empêcher les paquets avec des [[Spoofing|adresses IP sources usurpées]] de quitter le [[Network|réseau]] interne.
    *   Utiliser des [[Firewall|pare-feu]] pour filtrer les [[InternetControlMessageProtocol|requêtes ICMP]] entrantes et sortantes anormales.
    *   [[NetworkSegmentation|Segmenter le réseau]] pour limiter les [[BroadcastDomain|domaines de diffusion]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] pour surveiller le [[NetworkTraffic|trafic réseau]] à la recherche d'anomalies.
    *   [[NetworkMonitoring|Outils de surveillance réseau]] pour identifier les pics de [[NetworkTraffic|trafic ICMP]].
*   **Réponse** :
    *   Mettre en œuvre un [[IncidentResponse|plan de réponse à incident]] pour réagir rapidement aux [[DenialOfService|attaques par déni de service]].
    *   Appliquer la [[RateLimiting|limitation de débit]] sur les [[Router|routeurs]] ou [[Firewall|pare-feu]] pour le [[NetworkTraffic|trafic ICMP]].

## 🔗 Notes Connexes
*   [[DenialOfService|Déni de Service]]
*   [[DistributedDenialOfService|DDoS]]
*   [[Spoofing|Usurpation d'adresse IP]]
*   [[InternetControlMessageProtocol|ICMP]]
*   [[BroadcastAddress|Adresse de Diffusion]]
*   [[AmplificationAttack|Attaque par amplification]]
*   [[NetworkConfiguration|Configuration réseau]]