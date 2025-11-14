---
tags:
  - routage-statique
  - protocole-routage-dynamique
  - segmentation-reseau-vlan
  - routing
  - network-routing
aliases:
  - Routage
  - Network Routing
source:
  - null
cssclasses:
  - max
---

# Routage

## 📥 Définition en une phrase
> Le routage est le processus de sélection du meilleur chemin pour le [[NetworkTrafficAnalysis|trafic réseau]] à travers un ou plusieurs [[Network|réseaux]], permettant ainsi aux [[Packet|paquets]] de données d'atteindre leur [[DestinationInternetProtocolVersion4Address|destination]].

## 🧠 Concepts Clés / Fonctionnement
*   **Fonction des [[Router|Routeurs]]**: Les routeurs sont les dispositifs clés qui réalisent le routage, en transférant les paquets entre différents [[Network|réseaux]] interconnectés.
*   **[[RoutingTable|Tables de Routage]]**: Chaque [[Router|routeur]] maintient une table de routage qui contient des informations sur les chemins connus vers diverses [[NetworkAddress|adresses réseau]], y compris la [[Gateway|passerelle]] ou l'interface de sortie à utiliser.
*   **Couches du Modèle OSI/TCP-IP**: Le routage opère principalement au niveau de la [[NetworkLayer|Couche Réseau]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et de la [[InternetLayer|Couche Internet]] du [[TcpIpModel|modèle TCP/IP]], utilisant le [[InternetProtocol|Protocole Internet (IP)]].
*   **Types de Routage**:
    *   **[[StaticConfiguration|Routage Statique]]**: Les chemins sont configurés manuellement par un administrateur. Simple pour les petits réseaux, mais peu flexible.
    *   **Routage Dynamique**: Les [[Router|routeurs]] échangent des informations de routage via des [[NetworkProtocol|protocoles de routage]] (ex: OSPF, BGP) pour découvrir automatiquement les chemins et s'adapter aux changements de topologie.
*   **Objectif**: Assurer la [[DataTransmission|transmission des données]] de manière efficace et fiable, en minimisant la [[Latency|latence]] et en optimisant le [[Throughput|débit]].

## 🛡️ Risques / Menaces Associés
*   [[RoutingAttack|Attaques de routage]]: Des acteurs malveillants peuvent manipuler les tables de routage ou les protocoles pour rediriger le trafic vers des serveurs contrôlés par l'attaquant (ex: [[ManInTheMiddle|attaques de l'homme du milieu]]) ou des destinations non autorisées.
*   [[DenialOfService|Déni de service (DoS)]]: Une mauvaise configuration ou une [[Attack|attaque]] ciblée sur les [[Router|routeurs]] peut entraîner une [[ServiceDisruption|interruption de service]] en saturant les liens ou les ressources des routeurs, ou en créant des boucles de routage.
*   [[InadvertentExposure|Exposition involontaire]] de [[PrivateIPAddress|réseaux privés]]: Des erreurs de configuration de routage peuvent exposer des segments de [[CorporateNetwork|réseau d'entreprise]] qui devraient rester isolés.
*   [[NetworkCongestion|Congestion réseau]]: Un routage inefficace peut entraîner une accumulation de trafic sur certains chemins, diminuant les [[NetworkPerformance|performances réseau]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utilisation de [[SecureRoutingProtocols|Protocoles de Routage Sécurisés]]**: Mettre en œuvre des protocoles offrant des mécanismes d'[[Authentication|authentification]] et d'[[Encryption|chiffrement]] pour les échanges d'informations de routage.
*   **[[AccessControl|Contrôle d'Accès]] aux Routeurs**: Implémenter des [[SecurityControl|contrôles de sécurité]] stricts pour l'accès physique et logique aux [[Router|routeurs]] et à leur configuration.
*   **[[NetworkSegmentation|Segmentation Réseau]] et [[Firewall|Pare-feu]]**: Utiliser des VLAN et des pare-feu pour isoler les segments de réseau et contrôler les flux de trafic, empêchant ainsi la propagation d'anomalies de routage.
*   **[[NetworkMonitoring|Surveillance Réseau]]**: Mettre en place une [[SecurityMonitoring|surveillance continue]] des tables de routage et du [[NetworkTrafficAnalysis|trafic réseau]] pour détecter rapidement les modifications inattendues ou les signes d'[[AnomalyDetection|anomalies]].
*   **Filtre d'Entrée/Sortie**: Configurer des filtres sur les interfaces des [[Router|routeurs]] pour bloquer le trafic provenant ou se dirigeant vers des adresses IP invalides ou inattendues.

## 🔗 Notes Connexes
*   [[Router|Routeur]]
*   [[RoutingTable|Table de Routage]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocol|Protocole Internet]]
*   [[NetworkProtocol|Protocoles Réseau]]