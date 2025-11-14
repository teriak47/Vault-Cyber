---
tags:
  - infrastructure-reseau-backbone
  - bgp-security
  - redondance-connexion
  - cybersecurite/attaque-injection
  - cybersecurite/attaque-rejeu
aliases:
  - Dorsale d'Internet
  - Internet Backbone
  - réseau fédérateur Internet
source:
  - null
cssclasses:
  - max
---

# Dorsale d'Internet

## 📥 Définition en une phrase
> La Dorsale d'Internet (Internet Backbone) est l'infrastructure principale du réseau mondial, composée de lignes de données à haute capacité et de routeurs puissants, qui transporte le trafic intercontinental et inter-régional entre les principaux [[InternetExchangePoint|points d'échange Internet]] et les [[InternetServiceProvider|Fournisseurs d'Accès Internet (FAI)]] de niveau 1.

## 🧠 Concepts Clés / Fonctionnement
*   **Infrastructure Fondamentale** : Représente la couche la plus élevée et la plus vaste de la [[NetworkTopology|topologie réseau]] d'Internet, sur laquelle toutes les autres couches sont construites.
*   **Haute Capacité** : Constitué principalement de câbles à fibres optiques sous-marins et terrestres avec des débits de données extrêmement élevés (terabits par seconde).
*   **Propriété et Gestion** : Généralement détenue et exploitée par de grandes entreprises de télécommunications ou des opérateurs de réseaux de "Tier 1", qui ont des accords de peering (interconnexion directe) entre eux.
*   **Routage Global** : Utilise des protocoles de routage comme [[BorderGatewayProtocol|BGP]] pour échanger des informations de routage et diriger efficacement le trafic de données à travers le monde.
*   **Redondance et Résilience** : Conçue avec une grande [[Redundancy|redondance]] et de multiples chemins pour le trafic afin de garantir la continuité du service en cas de panne d'un segment.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service Distribué (DDoS)]] ciblant des nœuds de routage ou des segments clés.
*   [[PhysicalSecurityThreat|Menaces physiques]] (coupures de câbles sous-marins ou terrestres, sabotage d'infrastructures critiques).
*   [[SupplyChainAttack|Attaques de la chaîne d'approvisionnement]] sur les équipements réseau stratégiques.
*   [[Espionage|Espionnage]] ou surveillance à grande échelle du trafic de données transitant.
*   [[BorderGatewayProtocolHijacking|Détournement de BGP]] affectant le routage global.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Redundancy|Mise en œuvre d'une redondance]] et de chemins de routage multiples pour le trafic.
*   [[PhysicalSecurity|Sécurité physique]] renforcée des centres de données et des stations d'atterrissage des câbles.
*   [[NetworkMonitoring|Surveillance réseau]] avancée et [[IntrusionDetectionSystem|systèmes de détection d'intrusion (IDS)]] sur les points critiques.
*   [[IncidentResponse|Plans de réponse aux incidents]] robustes pour gérer les pannes ou les attaques.
*   [[BorderGatewayProtocolSecurity|Renforcement de la sécurité du BGP]] (validation de l'origine de routage (ROV) avec RPKI).

## 🔗 Notes Connexes
*   [[InternetServiceProvider|Fournisseur d'Accès Internet (FAI)]]
*   [[InternetExchangePoint|Point d'Échange Internet (IXP)]]
*   [[BorderGatewayProtocol|BGP]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[DataCenter|Centre de Données]]