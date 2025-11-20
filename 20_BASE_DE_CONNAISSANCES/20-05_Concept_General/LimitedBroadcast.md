---
tags:
  - reseau
  - ipv4
aliases:
  - Limited Broadcast
  - Diffusion limitée
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Diffusion Limitée (Limited Broadcast)

## 🎯 Rôle et Couche OSI

> La diffusion limitée est un mécanisme de communication spécifique à IPv4 qui permet à un hôte d'envoyer un paquet de données à tous les autres hôtes présents sur le même segment réseau local. Elle opère principalement au niveau de la couche Réseau du modèle TCP/IP.

## ⚙️ Fonctionnement

1.  **Adresse de Destination**: Le paquet est adressé à l'adresse IP de diffusion spécifique à un segment local, qui est 255.255.255.255.
2.  **Portée Locale**: Les routeurs sont configurés par défaut pour ne pas retransmettre les paquets envoyés à l'adresse `255.255.255.255`, confinant ainsi la diffusion au domaine de diffusion d'origine.
3.  **Réception Universelle Locale**: Tous les dispositifs terminaux et intermédiaires connectés au segment réseau local reçoivent et traitent ce paquet.
4.  **Cas d'Usage**: Elle est couramment utilisée par des protocoles comme DHCP pour la découverte initiale de serveurs ou de services sur un réseau local lorsque l'adresse IP de destination n'est pas encore connue.

- **Ports par défaut**: N/A (ce n'est pas un protocole de transport, mais une méthode d'adressage IP)

## 🛡️ Sécurité du Protocole

- **Vulnérabilités connues**:
  - Déni de Service (DoS): Un volume excessif de diffusions peut saturer le réseau local, provoquant une congestion réseau et potentiellement un déni de service pour les hôtes du segment.
  - Attaques Smurf: Bien que les routeurs modernes bloquent généralement les diffusions dirigées vers des réseaux distants, une configuration laxiste ou une exploitation locale des diffusions limitées peut toujours contribuer à une attaque par surcharge.
  - Interception de Paquets: Étant donné que tous les hôtes du segment réseau reçoivent le paquet, il est plus facile pour un acteur de menace d'intercepter les données si elles ne sont pas chiffrées.
- **Versions sécurisées**:
  - Pas de "versions" sécurisées au sens protocolaire, mais des mesures de contrôle de sécurité sont cruciales:
    - Segmentation Réseau: L'utilisation de VLANs pour réduire la taille des domaines de diffusion.
    - Filtrage par Pare-feu: Configuration rigoureuse des pare-feu pour bloquer les diffusions inutiles ou suspectes.
    - Surveillance Réseau: Détection d'activités de diffusion anormales via des outils de surveillance du trafic réseau.

## 🔗 Notes Connexes

- Diffusion
- Adresse de Diffusion
- Diffusion Dirigée
- Internet Protocol version 4 (InternetProtocolVersion4)
- Réseau Local (LocalAreaNetwork)
- Couche Réseau
- Congestion Réseau
- Attaque Smurf
- Protocole de Configuration d'Hôte Dynamique (DynamicHostConfigurationProtocol)
- Segmentation Réseau
