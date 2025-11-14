---
tags:
  - reseau/topologie-plate
  - securite/propagation-menaces
  - materiel/commutateur-gere
  - reseau/reseau-local
  - reseau/domaine-broadcast
  - reseau/collision
aliases:
  - Réseau Plat
  - Single Local Network Segment
  - Réseau sans segmentation
cssclasses:
  - max
---

# Réseau Plat (Flat Network)

## 📥 Définition en une phrase
> Une topologie de réseau où tous les hôtes se trouvent sur un seul [[BroadcastDomain|domaine de diffusion]] et partagent le même segment de réseau local, facilitant la communication directe mais pouvant entraîner des défis de performance et de sécurité.

## 🧠 Concepts Clés / Fonctionnement
*   Tous les hôtes résident sur un unique [[LocalAreaNetwork|LAN]] et un seul [[BroadcastDomain|domaine de diffusion]].
*   Les hôtes utilisent le [[AddressResolutionProtocol|protocole ARP]] pour se découvrir mutuellement et communiquer directement.
*   Simplicité de configuration et coûts d'infrastructure réduits, adaptés aux petits réseaux.
*   Transfert de données potentiellement plus rapide entre les appareils du même segment en l'absence de routeurs intermédiaires.
*   Visibilité mutuelle de tous les équipements connectés sur le segment.

## 🛡️ Risques / Menaces Associés
*   **Performances dégradées**: À mesure que le nombre d'hôtes augmente, le volume de [[BroadcastTraffic|trafic de diffusion]] et de collisions s'accroît, ralentissant les performances du réseau.
*   **Difficulté de [[QualityOfService|QoS]]**: La mise en œuvre de la [[QualityOfService|Qualité de Service (QoS)]] est plus complexe, rendant difficile la priorisation du trafic essentiel.
*   **Sécurité limitée**: Tous les hôtes sont visibles et accessibles les uns aux autres par défaut, augmentant le risque de propagation des [[Malware|malwares]] et rendant la segmentation de la [[NetworkSecurity|sécurité]] plus ardue.
*   **Faiblesse face aux attaques**: Une seule [[Vulnerability|vulnérabilité]] sur un hôte peut exposer l'ensemble du réseau à des [[Threat|menaces]] comme le [[ManInTheMiddle|Man-in-the-Middle]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre la [[NetworkSegmentation|segmentation réseau]] en utilisant des [[VirtualLocalAreaNetwork|VLANs]] ou des sous-réseaux pour diviser le réseau en domaines de diffusion plus petits.
*   Déployer des [[Firewall|pare-feu]] et des [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] pour surveiller et contrôler le trafic entre les segments.
*   Appliquer le principe du [[PrincipleOfLeastPrivilege|moindre privilège]] aux communications entre les hôtes.
*   Utiliser des commutateurs (switches) gérés pour contrôler et limiter le trafic de diffusion.

## 🔗 Notes Connexes
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[AddressResolutionProtocol|ARP]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[VirtualLocalAreaNetwork|VLAN]]
*   [[QualityOfService|Qualité de Service (QoS)]]
*   [[LocalAreaNetwork|Réseau Local (LAN)]]