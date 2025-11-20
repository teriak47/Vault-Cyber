---
aliases:
  - Protocole de résolution d'adresse
  - ARP
  - Address Resolution Protocol
  - ARP Protocol
source:
  - 
rfc:
  - RFC 826
cssclasses:
  - max
archetype: protocole
---

# Protocole de Résolution d'Adresse (ARP)

## 🎯 Rôle et Couche OSI
> L'ARP est un protocole de communication essentiel qui établit la correspondance entre une adresse IP logique (IPv4) et l'adresse MAC physique correspondante d'un hôte. Cette traduction est nécessaire pour la communication réseau au sein d'un réseau local.
> Il opère principalement à la couche Liaison de Données (couche 2 du modèle OSI) pour la résolution de l'adresse MAC, tout en manipulant des informations de la couche Réseau (couche 3) pour l'adresse IP. Pour le modèle TCP/IP, il est souvent considéré comme faisant partie de la couche d'accès réseau.

## ⚙️ Fonctionnement
1.  **Recherche dans le cache ARP**: Avant d'envoyer une requête ARP, un hôte vérifie son cache ARP local pour voir s'il possède déjà la correspondance IP-MAC de la destination.
2.  **Requête ARP (Broadcast)**: Si la correspondance n'est pas trouvée, l'hôte émet une requête ARP en diffusion (domaine de diffusion) sur le LAN. Cette requête contient l'adresse IP de la machine cible et demande son adresse MAC.
3.  **Réponse ARP (Unicast)**: Le hôte dont l'adresse IP correspond à celle de la requête répond avec une réponse ARP. Cette réponse contient sa propre adresse MAC et est envoyée directement en unicast à l'expéditeur de la requête.
4.  **Mise à jour du cache ARP**: L'hôte demandeur reçoit la réponse ARP et stocke la nouvelle correspondance IP-MAC dans son cache ARP pour une durée limitée.

*   **Ports par défaut**: L'ARP n'utilise pas de numéros de port TCP ou UDP car il opère directement à un niveau inférieur (couche 2/3) de la pile de protocoles.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Usurpation d'ARP (ARP Spoofing): Un attaquant peut envoyer de fausses réponses ARP pour associer son adresse MAC à l'adresse IP d'un autre dispositif légitime (comme une passerelle par défaut ou un serveur). Cela permet au malveillant d'intercepter, modifier ou rediriger le trafic (une forme d'attaque de l'homme du milieu).
    *   Déni de Service (DoS): Des réponses ARP malveillantes massives peuvent inonder le cache ARP d'un hôte avec des entrées incorrectes, le rendant incapable de communiquer avec d'autres dispositifs sur le segment réseau.
*   **Mesures de protection**:
    *   Inspection ARP Dynamique (DAI - Dynamic ARP Inspection): Les commutateurs réseau peuvent valider les paquets ARP entrants en les comparant aux informations stockées dans les tables DHCP snooping, rejetant les paquets ARP non valides ou usurpés.
    *   Entrées ARP statiques: Pour les dispositifs critiques comme les routeurs ou les serveurs de fichiers, il est possible de configurer manuellement des entrées ARP statiques dans leur cache ARP afin d'empêcher toute modification dynamique malveillante.
    *   Sécurité des ports: Configurer la sécurité des ports sur les commutateurs permet de limiter le nombre d'adresses MAC autorisées sur un port, aidant à prévenir les attaques d'usurpation d'adresse MAC et par extension les attaques ARP spoofing.
    *   Contrôle d'accès réseau (NAC): Les solutions de NAC peuvent aider à garantir que seuls les appareils autorisés sont capables de se connecter au réseau et d'utiliser l'ARP.

## 🔗 Notes Connexes
*   Adresse IP
*   Adresse MAC
*   Ethernet
*   Neighbor Discovery Protocol (l'équivalent de l'ARP pour IPv6)
*   Couche Liaison de Données
*   Couche Réseau
*   Modèle OSI
*   Modèle TCP/IP
*   Empoisonnement du protocole de résolution d'adresses
*   Attaque de l'Homme du Milieu
*   Wireshark (Outil pour analyser le trafic réseau incluant les paquets ARP)