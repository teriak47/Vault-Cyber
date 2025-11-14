---
tags:
  - securite/surveillance-dhcp
  - attaque/epuisement-dhcp
  - protocole/bail-adresse
  - adressage/attribution-dynamique
  - reseau/protocole
  - reseau/segmentation-vlan
aliases:
  - Protocole de Configuration d'Hôte Dynamique
  - DHCP
  - Dynamic Host Configuration Protocol
source:
  - null
cssclasses:
  - max
---

# Protocole de Configuration d'Hôte Dynamique (DHCP)

## 📥 Définition en une phrase
> Le [[DynamicHostConfigurationProtocol|DHCP]] est un protocole réseau qui permet à un serveur de distribuer automatiquement des adresses IP et d'autres paramètres de configuration réseau (masque de sous-réseau, passerelle par défaut, serveurs DNS) aux clients sur un réseau IP.

## 🧠 Concepts Clés / Fonctionnement
*   **Processus DORA (Discovery, Offer, Request, Acknowledgement)** : Le cycle standard d'attribution d'une adresse IP.
    *   **Découverte (Discovery)** : Le client envoie un paquet de diffusion (broadcast) pour localiser les serveurs DHCP.
    *   **Offre (Offer)** : Un serveur DHCP répond avec une offre d'adresse IP et d'autres paramètres.
    *   **Requête (Request)** : Le client demande formellement l'adresse IP et les paramètres proposés.
    *   **Accusé de Réception (Acknowledgement)** : Le serveur confirme l'attribution de l'adresse IP et des paramètres pour une durée de [[Lease|bail]] spécifiée.
*   **Bail (Lease)** : Une adresse IP est attribuée pour une période déterminée. Le client doit renouveler son bail avant son expiration pour conserver la même adresse.
*   **Pool d'adresses** : Une plage d'adresses IP que le serveur DHCP est configuré pour distribuer.
*   **Options DHCP** : Des paramètres supplémentaires qui peuvent être distribués par le serveur, comme les adresses des serveurs DNS, les serveurs WINS, le nom de domaine, etc.

## 🛡️ Risques / Menaces Associés
*   [[DhcpStarvation|DHCP starvation]] : Un attaquant consomme toutes les adresses IP disponibles dans le pool DHCP, empêchant les clients légitimes d'obtenir une adresse et provoquant un [[DenialOfService|déni de service]].
*   [[DhcpSpoofing|DHCP spoofing]] (serveur DHCP malveillant) : Un attaquant met en place un serveur DHCP non autorisé pour distribuer de fausses configurations IP, redirigeant le trafic client vers un [[ManInTheMiddle|attaquant (homme du milieu)]] ou un [[RogueAccessPoint|serveur DNS pirate]].
*   Divulgation d'informations (reconnaissance) : Un serveur DHCP peut involontairement divulguer des informations sur la structure du réseau.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[DhcpSnooping|DHCP Snooping]] : Une fonctionnalité de sécurité des commutateurs réseau qui permet de filtrer les messages DHCP non autorisés pour empêcher les serveurs DHCP pirates et les attaques de starvation.
*   [[NetworkSegmentation|Segmentation réseau]] : Isoler les réseaux par le biais de [[VirtualLocalAreaNetwork|VLAN]] pour limiter la portée des attaques DHCP.
*   [[PhysicalSecurity|Sécurité physique]] : Protéger l'accès physique aux serveurs DHCP et aux équipements réseau.
*   Authentification des ports : Utiliser des protocoles comme [[802.1x|IEEE 802.1X]] pour s'assurer que seuls les appareils autorisés peuvent se connecter au réseau.

## 🔗 Notes Connexes
*   [[IpAddressing|Adresses IP]]
*   [[NetworkProtocols|Protocoles Réseau]]
*   [[TcpIpStack|Pile TCP/IP]]
*   [[NetworkAccessControl|Contrôle d'Accès Réseau]]
*   [[StaticIpAddressing|Adresses IP Statiques]]