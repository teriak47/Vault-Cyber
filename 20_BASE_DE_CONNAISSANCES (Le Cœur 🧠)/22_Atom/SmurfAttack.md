---
tags:
  - smurf-attaque
  - broadcast-ping
  - DenialOfService
  - InternetControlMessageProtocol
  - Firewall
aliases:
  - Attaque Smurf
  - Smurf Attack
source:
  - null
cssclasses:
  - max
---

# Attaque Smurf (Smurf Attack)

## 📥 Définition en une phrase
> L'[[SmurfAttack|attaque Smurf]] est une forme d'[[DenialOfService|attaque par déni de service]] qui exploite des [[Network|réseaux]] de [[Computer|ordinateurs]] pour surcharger un [[Victim|système victime]] en utilisant des [[InternetControlMessageProtocol|requêtes ICMP]] de [[Broadcast|diffusion]] avec une [[SpoofingAttack|adresse IP source usurpée]].

## 🧠 Concepts Clés / Fonctionnement
*   L'attaquant envoie un grand nombre de [[InternetControlMessageProtocol|requêtes ICMP]] (ping) à l'[[BroadcastAddress|adresse de diffusion]] d'un [[InterconnectedNetworks|réseau interconnecté]].
*   Les paquets [[InternetControlMessageProtocol|ICMP]] ont une [[SourceInternetProtocolVersion4Address|adresse IP source]] usurpée, qui est celle de la [[Victim|cible]].
*   Tous les [[Host|hôtes]] du [[Network|réseau]] de [[BroadcastDomain|diffusion]] répondent à ces requêtes, inondant la [[Victim|victime]] d'une quantité massive de [[NetworkTraffic|trafic réseau]].
*   Cela entraîne une [[DenialOfService|surcharge du serveur cible]], le rendant inaccessible pour les [[Client|utilisateurs légitimes]].

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service]] : Interruption complète ou partielle de la disponibilité des [[OnlineServices|services]] de la [[Victim|cible]].
*   [[ServiceDisruption|Interruption de Service]] : Les ressources de la [[Victim|victime]] sont entièrement consommées par les réponses [[InternetControlMessageProtocol|ICMP]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Désactiver la [[DirectedBroadcast|diffusion dirigée]] sur les [[Router|routeurs]]** : Empêcher les [[Router|routeurs]] de transférer des paquets de [[Broadcast|diffusion]] provenant de l'extérieur vers le [[LocalAreaNetwork|LAN]].
*   **[[Firewall|Filtrage par pare-feu]]** : Configurer les [[Firewall|pare-feu]] pour bloquer les [[InternetControlMessageProtocol|requêtes ICMP]] avec une [[SourceInternetProtocolVersion4Address|adresse IP source]] usurpée ou pour limiter le [[NetworkTraffic|trafic ICMP]].
*   **[[IngressFiltering|Filtrage d'entrée]]** : Mettre en œuvre le filtrage des paquets entrants pour bloquer ceux dont l'[[SourceInternetProtocolVersion4Address|adresse IP source]] n'est pas censée se trouver sur ce [[Network|réseau]].
*   **[[EgressFiltering|Filtrage de sortie]]** : Mettre en œuvre le filtrage des paquets sortants pour empêcher qu'un [[Network|réseau]] interne ne soit utilisé comme [[AttackVector|vecteur d'attaque]] pour d'autres [[SmurfAttack|attaques Smurf]].

## 🔗 Notes Connexes
*   [[DenialOfService|Déni de Service]]
*   [[InternetControlMessageProtocol|Protocole de Message de Contrôle Internet]]
*   [[BroadcastAddress|Adresse de Diffusion]]
*   [[SpoofingAttack|Attaque par Usurpation]]
*   [[NetworkTraffic|Trafic Réseau]]
*   [[Firewall|Pare-feu]]