---
tags:
  - adresse-de-diffusion
  - contrôle-des-tempêtes-de-diffusion
  - BroadcastDomain
  - NetworkSegmentation
  - VirtualLocalAreaNetwork
aliases:
  - Adresse de Diffusion
  - Broadcast Address
source:
  - null
cssclasses:
  - max
---

# Adresse de Diffusion (Broadcast Address)

## 📥 Définition en une phrase
> Une [[BroadcastAddress|adresse de diffusion]] est une [[InternetProtocolAddress|adresse IP]] spéciale utilisée pour envoyer des [[Data|données]] à tous les [[Host|hôtes]] d'un [[LocalAreaNetwork|réseau local]] ou d'un [[SubnetMask|sous-réseau]] spécifique simultanément.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification Globale :** L'[[BroadcastAddress|adresse de diffusion]] identifie tous les [[NetworkDevice|périphériques]] au sein d'un [[BroadcastDomain|domaine de diffusion]] donné, permettant une [[OneToOneCommunications|communication un à plusieurs]].
*   **Format [[InternetProtocolVersion4|IPv4]] :** Pour [[InternetProtocolVersion4|IPv4]], une [[BroadcastAddress|adresse de diffusion]] est caractérisée par la partie [[HostPortion|hôte]] de l'[[InternetProtocolAddress|adresse IP]] où tous les bits sont définis à '1'.
*   **Cas d'Usage :** Elle est principalement utilisée pour des opérations de découverte de [[Host|hôtes]] et de services sur le [[Network|réseau]], comme les requêtes [[DynamicHostConfigurationProtocol|DHCP]] (pour obtenir une [[InternetProtocolAddress|adresse IP]]) ou [[AddressResolutionProtocol|ARP]] (pour résoudre des [[MediaAccessControlAddress|adresses MAC]]).
*   **Types de Diffusion :** Il existe la diffusion limitée (255.255.255.255), qui envoie un [[Packet|paquet]] à tous les [[Host|hôtes]] sur le [[LocalAreaNetwork|LAN]] local, et la [[DirectedBroadcast|diffusion dirigée]] (par exemple, 192.168.1.255), qui s'adresse à tous les [[Host|hôtes]] d'un [[RemoteNetwork|réseau distant]] spécifique.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service (DoS)]] : Un [[ThreatActor|attaquant]] peut générer un volume excessif de trafic de [[Broadcast|diffusion]] (tempête de diffusion), ce qui sature le [[Network|réseau]] et entraîne un [[ServiceDisruption|déni de service]] pour les [[UserAwarenessTraining|utilisateurs]] légitimes.
*   [[Reconnaissance|Reconnaissance]] : Les [[ThreatActor|attaquants]] peuvent envoyer des requêtes de [[Broadcast|diffusion]] pour identifier les [[Host|hôtes]] actifs, les [[NetworkDevice|périphériques réseau]] et les services disponibles sur un [[Network|réseau]] cible, aidant ainsi à la cartographie de l'[[AttackSurface|attaque]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation Réseau]] : Utiliser des [[VirtualLocalAreaNetwork|VLAN]] pour diviser les [[BroadcastDomain|domaines de diffusion]] en segments plus petits, limitant ainsi la portée d'une éventuelle tempête de [[Broadcast|diffusion]] ou d'une [[Reconnaissance|reconnaissance]] par [[Broadcast|diffusion]].
*   [[Firewall|Règles de Pare-feu]] : Configurer des [[Firewall|pare-feux]] pour filtrer et bloquer le trafic de [[Broadcast|diffusion]] inutile ou malveillant, en particulier aux points d'interconnexion entre [[Network|réseaux]] ou sous-réseaux.
*   Configuration des [[NetworkSwitch|Commutateurs]] : Configurer les [[NetworkSwitch|commutateurs]] pour limiter la propagation des tempêtes de [[Broadcast|diffusion]] (broadcast storm control) et mettre en œuvre des fonctionnalités de [[PortSecurity|sécurité des ports]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[Unicast|Unicast]]
*   [[Multicast|Multicast]]
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DirectedBroadcast|Diffusion Dirigée]]
*   [[AddressResolutionProtocol|Protocole de résolution d'adresse (ARP)]]
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]