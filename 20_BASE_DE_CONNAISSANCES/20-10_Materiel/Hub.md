---
tags:
  - materiel
  - hub
  - reseau/appareil
  - couche/physique
  - ethernet
  - connectivite
archetype: materiel
aliases:
  - Concentrateur
  - Ethernet Hub
  - Hub
source:
  - 
cssclasses:
  - max
---

# Hub (Concentrateur)

## 🎯 Rôle et Fonction
Le [[Hub|hub]], ou concentrateur, est un [[NetworkDevice|dispositif réseau]] fondamental, bien que largement obsolète, utilisé pour connecter plusieurs [[Computer|ordinateurs]] ou autres [[EndDevices|dispositifs terminaux]] dans un [[LocalAreaNetwork|réseau local]] (LAN). Il opère au niveau de la [[PhysicalLayer|couche physique]] du [[OpenSystemsInterconnectionModel|modèle OSI]]. Son rôle principal est de régénérer et de diffuser les signaux électriques qu'il reçoit sur un port vers tous les autres ports connectés, agissant comme un répéteur multi-ports.

## 🛠️ Caractéristiques Techniques
*   **Type / Catégories**: Les hubs sont généralement classés comme des concentrateurs ou des répéteurs multi-ports. Ils peuvent être actifs (nécessitant une alimentation électrique pour amplifier les signaux) ou passifs (sans amplification).
*   **Connectique**: Principalement des ports [[RJ45Connector|RJ45]] pour les câbles [[TwistedPair|paires torsadées]] [[UnshieldedTwistedPair|UTP]].
*   **Performances**:
    *   **Débit**: Partage la [[Throughput|bande passante]] totale entre tous les ports. Par exemple, un hub 10 Mbps partagera ces 10 Mbps entre tous les appareils connectés.
    *   **Latence**: Introduit une latence minime due à la simple régénération et retransmission des signaux.
    *   **Méthode de transmission**: Utilise la [[HalfDuplexCommunication|communication half-duplex]], ce qui signifie que les appareils peuvent soit envoyer, soit recevoir des données, mais pas simultanément.
*   **Normes associées**: Conforme à la norme [[EthernetProtocol|IEEE 802.3]] pour les réseaux [[Ethernet]].

## ✅ Avantages et Inconvénients
*   **Avantages**:
    *   **Simplicité**: Facile à installer et à configurer, ne nécessitant aucune logique de routage ou d'adressage complexe.
    *   **Coût**: Historiquement très abordable, ce qui en faisait une solution économique pour les petits réseaux.
*   **Inconvénients**:
    *   **Collisions**: Crée un grand [[CollisionDomain|domaine de collision]] unique, ce qui signifie que si deux appareils transmettent en même temps, une collision se produit, nécessitant une [[Retransmission|retransmission]] des données et réduisant drastiquement les performances du [[NetworkTraffic|trafic réseau]].
    *   **Sécurité**: Ne filtre pas le [[Packet|trafic]]. Chaque paquet reçu est envoyé à tous les ports, ce qui facilite l'[[Eavesdropping|écoute clandestine]] et le [[PacketSniffing|sniffer]] de paquets par n'importe quel appareil connecté.
    *   **Efficacité**: Partage la [[Bandwidth|bande passante]] et n'est pas évolutif. Les performances du réseau diminuent rapidement à mesure que le nombre d'appareils ou le volume de données augmentent.

## 🔒 Considérations de Sécurité Physique
*   [[PhysicalSecurity|Protection contre l'accès non autorisé]]: Un hub étant un point central de connexion physique, son accès doit être restreint pour empêcher la connexion de dispositifs non autorisés ou la manipulation de câblage.
*   [[EnvironmentalControls|Contrôles environnementaux (température, humidité)]]: Comme tout [[Hardware|équipement matériel]], les hubs sont sensibles aux conditions environnementales. Une température ou humidité excessive peut entraîner des pannes ou des performances dégradées.

## 🔗 Notes Connexes
*   **Couche OSI**: [[PhysicalLayer|Couche Physique]]
*   **Protocole associé**: [[EthernetProtocol|Protocole Ethernet]]
*   **Alternative moderne**: [[NetworkSwitch|Commutateur réseau]]
*   **Concept de performance**: [[CollisionDomain|Domaine de Collision]]
*   **Concept de diffusion**: [[BroadcastDomain|Domaine de Diffusion]]