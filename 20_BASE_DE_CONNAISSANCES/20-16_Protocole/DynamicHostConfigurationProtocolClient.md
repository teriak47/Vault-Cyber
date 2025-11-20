---
tags:
  - protocole
aliases:
  - Client DHCP
  - DHCP Client
  - Dynamic Host Configuration Protocol Client
  - Client du Protocole de Configuration d'Hôte Dynamique
archetype: protocole
rfc:
cssclasses:
  - max
---

# Client du Protocole de Configuration d'Hôte Dynamique (Client DHCP)

## 🎯 Rôle et Couche OSI
> Un client DHCP est un dispositif réseau (un hôte) configuré pour demander et recevoir automatiquement des informations de configuration réseau d'un serveur DHCP. Il joue un rôle essentiel dans la gestion dynamique des adresses IP et autres paramètres réseau pour les terminaux, opérant au niveau de l'couche Application du modèle TCP/IP pour l'échange de messages, mais ayant un impact direct sur la couche Réseau pour la connectivité.

## ⚙️ Fonctionnement
Le client DHCP initie un processus en quatre étapes, souvent appelé DORA (Discover, Offer, Request, Acknowledge), pour obtenir et gérer sa configuration réseau:

1.  **Discover (Découverte)**: Lorsqu'un ordinateur ou un autre périphérique réseau est configuré comme client DHCP, il envoie un message de découverte (DHCP Discover) en diffusion pour localiser les serveurs DHCP disponibles sur le segment réseau.
2.  **Offer (Offre)**: Les serveurs DHCP qui reçoivent la requête répondent avec des messages d'offre (DHCP Offer), proposant une adresse IP et d'autres paramètres de configuration réseau au client.
3.  **Request (Requête)**: Le client sélectionne l'une des offres reçues (généralement la première) et envoie un message de requête (DHCP Request) pour accepter l'adresse IP proposée et les autres paramètres. Ce message est également en diffusion pour informer les autres serveurs DHCP de son choix.
4.  **Acknowledge (Accusé de réception)**: Le serveur DHCP choisi envoie un message d'accusé de réception (DHCP Acknowledge ou DHCP ACK) confirmant l'attribution de l'adresse IP et des autres paramètres (comme le masque de sous-réseau, l'adresse de la passerelle par défaut, et les adresses des serveurs DNS).

*   **Informations Obtenues**: Outre l'adresse IP, le client reçoit le masque de sous-réseau, l'adresse de la passerelle par défaut, les adresses des serveurs DNS, et la durée du bail (lease time).
*   **Renouvellement de Bail**: Les adresses IP attribuées sont louées pour une période définie (le bail). Le client DHCP tente de renouveler son bail auprès du serveur DHCP avant son expiration pour conserver la même adresse IP et assurer une continuité de la communication.
*   **Ports par défaut**: Le client DHCP envoie des requêtes depuis le port UDP/68 vers le port UDP/67 du serveur DHCP et écoute les réponses sur le port UDP/68.

## 🛡️ Sécurité du Protocole
L'interaction entre un client DHCP et un serveur DHCP peut être la cible de diverses vulnérabilités et attaques:

*   **Serveur DHCP malveillant**: Un attaquant peut déployer un serveur DHCP non autorisé pour fournir aux clients des informations de configuration réseau incorrectes ou malveillantes. Cela peut entraîner une interruption de service, une exfiltration de données ou des attaques de l'homme du milieu en redirigeant le trafic vers des serveurs contrôlés par l'attaquant.
*   **Déni de Service (DoS)**: Un attaquant peut inonder le serveur DHCP de requêtes d'adresses IP légitimes ou falsifiées, épuisant ainsi son pool d'adresses IP disponibles. Cela empêche les nouveaux clients légitimes d'obtenir une configuration et de se connecter au réseau.
*   **Attaques Man-in-the-Middle**: En manipulant la configuration réseau via un serveur DHCP malveillant, un attaquant peut se positionner entre le client et le reste du réseau, interceptant et modifiant le trafic échangé.

**Mesures de Protection:**
*   **Sécurité des Ports et DHCP Snooping**: Implémenter des fonctionnalités de sécurité réseau sur les commutateurs réseau, comme le DHCP Snooping, qui permettent de valider les messages DHCP et d'empêcher les serveurs DHCP malveillants d'opérer sur le réseau.
*   **Contrôle d'accès Physique**: Restreindre l'accès physique à l'infrastructure réseau pour empêcher l'introduction de serveurs DHCP non autorisés.
*   **Politiques de sécurité Strictes**: Définir et appliquer des politiques de sécurité claires concernant la configuration réseau et la gestion des serveurs DHCP.
*   **Surveillance réseau et Vérification des Logs**: Surveiller activement les journaux du serveur DHCP et le trafic réseau pour détecter toute activité suspecte, comme des attributions d'adresses IP inhabituelles ou la présence de serveurs DHCP malveillants.

## 🔗 Notes Connexes
*   Protocole de Configuration d'Hôte Dynamique (DHCP)
*   Serveur DHCP
*   Adresse IP
*   Configuration réseau
*   Architecture Client-Serveur
*   Wireshark