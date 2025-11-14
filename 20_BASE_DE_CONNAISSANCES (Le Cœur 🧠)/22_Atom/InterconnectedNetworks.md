---
tags:
  - network-interconnexion
  - segmentation-reseau
  - surveillance-securite
  - reseau
  - reseau/segmentation
  - pare-feu
  - IntrusionPreventionSystem
aliases:
  - Réseaux interconnectés
  - Interconnected Networks
source:
  - null
cssclasses:
  - max
---

# Réseaux Interconnectés

## 📥 Définition en une phrase
> Un réseau interconnecté est un ensemble de plusieurs [[Network|réseaux]] informatiques individuels connectés entre eux, permettant la communication et le partage de ressources entre des périphériques situés dans des segments de réseaux différents.

## 🧠 Concepts Clés / Fonctionnement
*   **Agrégation de Réseaux** : Il combine des [[LocalAreaNetwork|LAN]], des [[MetropolitanAreaNetwork|MAN]] et des [[WideAreaNetwork|WAN]] (si elle n'existe pas, il faut la créer) pour former un ensemble plus vaste.
*   **[[Router|Routeurs]] et [[NetworkSwitch|Commutateurs]]** : Des [[Router|routeurs]] sont utilisés pour transférer les [[Packet|paquets]] de données entre différents réseaux, tandis que les [[NetworkSwitch|commutateurs]] gèrent le trafic au sein d'un même réseau local.
*   **[[NetworkProtocol|Protocoles réseau]]** : La communication entre les réseaux est rendue possible par l'utilisation de [[NetworkProtocol|protocoles]] standards comme la [[InternetProtocolSuite|suite de protocoles Internet]] ([[InternetProtocol|IP]] étant central), qui définissent les règles d'échange de données.
*   **[[Internet|Internet]]** : L'exemple le plus vaste et le plus connu de réseau interconnecté, reliant des milliards d'appareils à l'échelle mondiale.

## 🛡️ Risques / Menaces Associés
*   **[[AttackVector|Augmentation des vecteurs d'attaque]]** : Chaque connexion entre réseaux peut introduire de nouvelles portes d'entrée pour les attaquants.
*   **Propagation rapide des menaces** : Une [[Malware|malware]] ou une [[SoftwareVulnerability|vulnérabilité]] exploitée sur un segment peut rapidement se propager à l'ensemble du réseau interconnecté.
*   **[[DenialOfService|Déni de Service]] (DoS/[[DistributedDenialOfService|DDoS]])** : Des attaques peuvent viser à saturer les interconnexions, rendant les ressources inaccessibles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSegmentation|Segmentation Réseau]]** : Diviser le réseau en segments isolés pour limiter la propagation des attaques et appliquer des politiques de [[AccessControl|contrôle d'accès]] granulaires.
*   **[[Firewall|Pare-feu]] et [[IntrusionPreventionSystem|IPS]]** : Déployer des [[Firewall|pare-feu]] et des [[IntrusionPreventionSystem|systèmes de prévention d'intrusion]] aux points d'interconnexion pour filtrer le trafic et bloquer les activités malveillantes.
*   **Politiques de [[NetworkSecurity|sécurité réseau]] robustes** : Mettre en œuvre des politiques de [[SecurityControl|sécurité]] strictes pour la configuration des [[Router|routeurs]], des [[NetworkSwitch|commutateurs]] et des autres dispositifs d'interconnexion.
*   **[[SecurityMonitoring|Surveillance de la sécurité]]** : Surveiller en permanence le trafic réseau pour détecter les comportements anormaux et les tentatives d'intrusion.

## 🔗 Notes Connexes
*   [[Network|Réseau]]
*   [[Internet|Internet]]
*   [[Router|Routeur]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[MetropolitanAreaNetwork|Réseau Métropolitain (MAN)]]
*   [[WideAreaNetwork|Réseau Étendu (WAN)]]
*   [[NetworkSegmentation|Segmentation Réseau]]