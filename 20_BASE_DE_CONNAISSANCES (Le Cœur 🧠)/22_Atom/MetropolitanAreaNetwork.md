---
tags:
  - reseau/metropolitain
  - connectivite/haut-debit
  - reseau
  - infrastructure
aliases:
  - Réseau Métropolitain
  - MAN
  - Metropolitan Area Network
source:
  - 
cssclasses:
  - max
---

# Réseau Métropolitain (MAN)

## 📥 Définition en une phrase
> Un réseau informatique qui connecte des utilisateurs et des ressources informatiques dans une zone géographique plus grande qu'un [[LocalAreaNetwork|réseau local (LAN)]] mais plus petite qu'un [[WideAreaNetwork|réseau étendu (WAN)]], typiquement à l'échelle d'une ville ou d'une agglomération.

## 🧠 Concepts Clés / Fonctionnement
*   **Échelle Géographique** : Couvre une ville, une agglomération ou une région métropolitaine, reliant généralement plusieurs sites au sein de cette zone.
*   **Connectivité** : Permet de relier différents [[LocalAreaNetwork|LAN]] entre eux, facilitant la communication et le partage de ressources à l'échelle urbaine.
*   **Technologies** : S'appuie souvent sur des technologies à haut débit comme la fibre optique (ex: [[Ethernet|Ethernet]] métropolitain, [[SynchronousOpticalNetworking|SONET]]) ou des liaisons sans fil point-à-point.
*   **Objectif** : Offrir des services de communication rapides et fiables aux entreprises, institutions éducatives, entités gouvernementales et fournisseurs d'accès internet locaux.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS)]] : Peut cibler l'infrastructure centrale, perturbant la connectivité pour l'ensemble de la zone.
*   [[DataBreach|Fuites de données]] : Interception ou exfiltration de données transitant sur les liens partagés du MAN.
*   [[Eavesdropping|Écoute clandestine]] : Potentielle interception non autorisée du trafic réseau sur les segments physiques du MAN.
*   [[InfrastructureCompromise|Compromission d'infrastructure]] : Attaques visant les équipements réseau (routeurs, commutateurs) du MAN.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation Réseau]] : Isoler les différents segments du MAN pour limiter la propagation des menaces.
*   [[Encryption|Chiffrement]] du trafic : Utiliser des protocoles sécurisés comme [[VirtualPrivateNetwork|VPN]] ou [[InternetProtocolSecurity|IPsec]] pour protéger les données en transit.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]] : Déployer ces systèmes pour surveiller et bloquer les activités malveillantes.
*   [[AccessControl|Contrôles d'accès]] robustes : Appliquer des politiques strictes pour l'accès physique et logique aux équipements du MAN.

## 🔗 Notes Connexes
*   [[LocalAreaNetwork|Réseau Local (LAN)]]
*   [[WideAreaNetwork|Réseau Étendu (WAN)]]
*   [[NetworkTopology|Topologie Réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]