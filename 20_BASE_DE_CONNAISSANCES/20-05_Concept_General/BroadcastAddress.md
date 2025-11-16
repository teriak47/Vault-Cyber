---
tags:
aliases:
  - Adresse de Diffusion
  - Broadcast Address
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Adresse de Diffusion (Broadcast Address)

## 📥 Définition en une phrase
> Une [[BroadcastAddress|adresse de diffusion]] est une [[InternetProtocol|adresse IP]] spéciale utilisée pour envoyer des [[Data|données]] à tous les [[Host|hôtes]] d'un [[LocalAreaNetwork|réseau local]] ou d'un [[Subnet|sous-réseau]] spécifique simultanément.

## 🧠 Concepts Clés / Piliers
*   **Identification Ciblée**: L'[[BroadcastAddress|adresse de diffusion]] identifie tous les [[NetworkDevice|périphériques]] au sein d'un [[BroadcastDomain|domaine de diffusion]] donné, permettant une communication "un à plusieurs".
*   **Format [[InternetProtocolVersion4|IPv4]]**: Pour l'[[InternetProtocolVersion4|IPv4]], une [[BroadcastAddress|adresse de diffusion]] est caractérisée par la [[HostPortion|partie hôte]] de l'[[InternetProtocol|adresse IP]] où tous les bits sont définis à '1'.
*   **Rôle dans la Découverte**: Elle est cruciale pour des opérations de [[Host|découverte d'hôtes]] et de services, notamment pour les requêtes [[DynamicHostConfigurationProtocol|DHCP]] (obtention d'une [[InternetProtocol|adresse IP]]) et [[AddressResolutionProtocol|ARP]] (résolution d'[[MediaAccessControlAddress|adresses MAC]]).
*   **Types**: On distingue la [[LimitedBroadcast|diffusion limitée]] (255.255.255.255, locale au [[LocalAreaNetwork|LAN]]) et la [[DirectedBroadcast|diffusion dirigée]] (par exemple, 192.168.1.255, vers un [[RemoteNetwork|réseau distant]] spécifique).

## 💡 Importance en Cybersécurité
> La [[BroadcastAddress|diffusion]] est un mécanisme fondamental pour la [[NetworkCommunication|communication réseau]] et la [[Host|découverte d'hôtes]] dans un [[NetworkSegment|segment réseau]], facilitant des services essentiels comme l'attribution automatique d'[[InternetProtocol|adresses IP]]. Cependant, sa nature "un à plusieurs" en fait une cible privilégiée pour les [[ThreatActor|acteurs de menace]]. L'exploitation abusive des [[BroadcastAddress|adresses de diffusion]] peut entraîner des [[DenialOfService|attaques par déni de service]] (via des tempêtes de [[NetworkCongestion|congestion réseau]] ou des [[SmurfAttack|attaques Smurf]]) ou servir à la [[Reconnaissance|reconnaissance]] de la [[AttackSurface|surface d'attaque]]. La [[Security|sécurité]] de l'usage des [[BroadcastAddress|adresses de diffusion]] est donc vitale et passe par la [[NetworkSegmentation|segmentation réseau]], des [[Firewall|règles de pare-feu]] strictes, et la [[PortSecurity|sécurité des ports]] des [[NetworkSwitch|commutateurs]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[Unicast|Unicast]]
*   [[Multicast|Multicast]]
*   [[BroadcastDomain|Domaine de Diffusion]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DirectedBroadcast|Diffusion Dirigée]]
*   [[LimitedBroadcast|Diffusion Limitée]]
*   [[AddressResolutionProtocol|Protocole de résolution d'adresse (ARP)]]
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[NetworkCongestion|Congestion Réseau]]
*   [[SmurfAttack|Attaque Smurf]]