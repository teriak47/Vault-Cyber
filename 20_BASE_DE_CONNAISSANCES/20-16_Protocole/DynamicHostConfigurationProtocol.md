---
tags:
  - protocole
aliases:
  - Protocole de Configuration d'Hôte Dynamique
  - DHCP
  - Dynamic Host Configuration Protocol
archetype: protocole
rfc: RFC 2131
cssclasses:
  - max
---

# Protocole de Configuration d'Hôte Dynamique (DHCP)

## 🎯 Rôle et Couche OSI
> Le DHCP est un protocole réseau qui permet à un serveur DHCP de distribuer automatiquement des adresses IP et d'autres paramètres de configuration réseau (comme le masque de sous-réseau, la passerelle par défaut et les serveurs DNS) aux clients DHCP sur un réseau IP. Il opère principalement à la couche Application du modèle TCP/IP.

## ⚙️ Fonctionnement
Le DHCP utilise un processus en quatre étapes, souvent désigné par l'acronyme DORA :
1.  **Découverte (Discovery)** : Un client DHCP non configuré envoie un paquet de diffusion (`DHCPDISCOVER`) sur le segment réseau local pour localiser les serveurs DHCP disponibles. Ce paquet utilise l'UDP sur le port 68.
2.  **Offre (Offer)** : Un ou plusieurs serveurs DHCP reçoivent le message de découverte et répondent avec un paquet d'offre (`DHCPOFFER`), contenant une adresse IP proposée, un bail, un masque de sous-réseau, et l'adresse de la passerelle par défaut. Ce paquet est envoyé en unidiffusion ou diffusion sur le port 67.
3.  **Requête (Request)** : Le client DHCP reçoit les offres et sélectionne généralement la première offre reçue. Il envoie ensuite un paquet de requête (`DHCPREQUEST`) en diffusion pour accepter l'offre spécifique et informer les autres serveurs DHCP que leur offre n'a pas été retenue.
4.  **Accusé de Réception (Acknowledgement)** : Le serveur DHCP sélectionné confirme l'attribution de l'adresse IP et des paramètres via un paquet d'accusé de réception (`DHCPACK`). Ce message est envoyé en unidiffusion ou diffusion et marque la fin du processus d'attribution.

*   **Ports par défaut**: Le DHCP utilise les ports UDP :
    *   **UDP/67** pour les serveurs DHCP.
    *   **UDP/68** pour les clients DHCP.
*   **Concepts clés**:
    *   **Bail** : Durée pendant laquelle une adresse IP est attribuée à un client. Le client doit renouveler son bail avant son expiration.
    *   **Pool d'adresses** : Plage d'adresses IP configurée sur le serveur DHCP et disponible pour la distribution.
    *   **Options DHCP** : Paramètres réseau supplémentaires qui peuvent être distribués, tels que les serveurs DNS, les serveurs WINS, le nom de domaine, etc.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   DHCP starvation : Une acteur de menace envoie un grand nombre de requêtes DHCP pour épuiser le pool d'adresses IP disponibles, empêchant les clients légitimes d'obtenir une adresse et provoquant un déni de service.
    *   DHCP spoofing : Une acteur de menace déploie un serveur DHCP malveillant sur le réseau. Ce serveur distribue de fausses configurations IP (par exemple, une passerelle par défaut ou des serveurs DNS frauduleux), redirigeant le trafic client vers l'attaquant pour l'interception ou l'exfiltration de données.
    *   Divulgation d'informations : Un serveur DHCP mal configuré peut involontairement révéler des informations sensibles sur la structure du réseau aux attaquants lors de la phase de reconnaissance.
*   **Mesures de protection**:
    *   DHCP Snooping : Une fonctionnalité de sécurité implémentée sur les commutateurs réseau qui valide les messages DHCP et bloque ceux provenant de serveurs DHCP malveillants. Elle aide à prévenir les attaques de DHCP spoofing et starvation.
    *   Segmentation réseau : L'utilisation de VLAN pour isoler différents segments du réseau peut limiter la portée et l'impact des attaques DHCP.
    *   Sécurité physique : Protéger l'accès physique aux serveurs DHCP et aux équipements réseau pour empêcher l'installation de serveurs DHCP malveillants.
    *   Contrôle d'accès basé sur les ports (ex: IEEE 802.1X) : Authentifie les terminaux avant de leur accorder l'accès au réseau, rendant plus difficile pour les attaquants d'introduire des serveurs DHCP malveillants.
    *   Configuration statique pour les serveurs critiques : Attribuer manuellement des adresses IP statiques aux serveurs critiques et aux équipements réseau plutôt que de dépendre de DHCP.

## 🔗 Notes Connexes
*   Adressage IP
*   Protocoles Réseau
*   Modèle TCP/IP
*   Serveur DHCP
*   Client DHCP
*   UDP
*   Diffusion
*   Adressage IP Statique
*   Commutateur réseau
*   Vulnérabilités de sécurité