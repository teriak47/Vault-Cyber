---
tags:
  - diffusion-limitée
  - risque-interception-paquets
  - segmentation-vlan
  - BroadcastDomain
  - DenialOfService
  - SmurfAttack
aliases:
  - Limited Broadcast
  - Diffusion limitée
source:
  - null
cssclasses:
  - max
---

# Diffusion Limitée

## 📥 Définition en une phrase
> Une diffusion limitée est un type de [[Broadcast|diffusion]] dans un réseau [[InternetProtocolVersion4|IPv4]] où le paquet est envoyé à l'adresse de diffusion spécifique à un [[LocalAreaNetwork|LAN]] (`255.255.255.255`), et est censé être reçu par tous les hôtes sur le même segment de [[LogicalNetwork|réseau logique]].

## 🧠 Concepts Clés / Fonctionnement
*   **Adresse Cible** : Utilise l'adresse [[BroadcastAddress|255.255.255.255]] comme adresse [[DestinationInternetProtocolVersion4Address|IP de destination IPv4]].
*   **Portée Locale** : Contrairement aux [[DirectedBroadcast|diffusions dirigées]], les diffusions limitées ne traversent pas les [[Router|routeurs]]. Elles sont strictement confinées au [[BroadcastDomain|domaine de diffusion]] local.
*   **Transmission à Tous** : Le paquet est traité et potentiellement accepté par tous les [[Host|hôtes]] qui sont connectés directement au même segment de [[PhysicalNetwork|réseau physique]].
*   **Utilité** : Souvent utilisée pour la découverte de services ou d'hôtes sur un segment de [[LocalAreaNetwork|réseau local]] sans avoir à connaître l'[[InternetProtocolAddress|adresse IP]] spécifique de chaque dispositif. Des protocoles comme [[DynamicHostConfigurationProtocol|DHCP]] peuvent l'utiliser lors de la phase initiale de découverte.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service (DoS)]] : Un volume excessif de diffusions limitées peut entraîner une [[NetworkCongestion|congestion réseau]] et potentiellement un [[DenialOfService|déni de service]] pour les hôtes sur le même segment.
*   [[SmurfAttack|Attaques Smurf]] : Bien que les routeurs modernes bloquent les diffusions dirigées, les diffusions limitées peuvent théoriquement être exploitées dans des scénarios spécifiques si les protections adéquates ne sont pas en place, en surchargeant les systèmes.
*   [[PacketSniffing|Interception de Paquets]] : Tous les hôtes sur le segment reçoivent le paquet, ce qui facilite l'[[PacketSniffing|écoute clandestine]] si le contenu n'est pas chiffré.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation Réseau]] : L'utilisation de [[VirtualLocalAreaNetwork|VLANs]] ou d'autres formes de [[NetworkSegmentation|segmentation réseau]] peut limiter l'étendue des diffusions, réduisant ainsi leur impact sur de larges portions du réseau.
*   [[Firewall|Pare-feu]] : Configurer les [[Firewall|pare-feu]] pour filtrer les paquets de diffusion indésirables ou suspects.
*   [[NetworkDevice|Équipements Réseau]] : S'assurer que les [[NetworkSwitch|commutateurs réseau]] et les [[Router|routeurs]] sont configurés pour gérer correctement et limiter la propagation des diffusions.
*   [[NetworkMonitoring|Surveillance Réseau]] : Mettre en place une [[SecurityMonitoring|surveillance de sécurité]] pour détecter les volumes anormaux de trafic de diffusion qui pourraient indiquer une activité malveillante ou une mauvaise configuration.

## 🔗 Notes Connexes
*   [[Broadcast|Diffusion]]
*   [[BroadcastAddress|Adresse de Diffusion]]
*   [[DirectedBroadcast|Diffusion Dirigée]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[NetworkLayer|Couche Réseau]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[SmurfAttack|Attaque Smurf]]