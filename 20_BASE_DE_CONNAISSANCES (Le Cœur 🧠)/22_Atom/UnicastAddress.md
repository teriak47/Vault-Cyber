---
tags:
  - unicast-address
  - point-to-point-communication
  - denial-of-service-targeting
  - firewall
  - intrusion-detection-system
  - network-segmentation
aliases:
  - Adresse Unicast
  - Unicast Address
  - Unidiffusion
source:
  - null
cssclasses:
  - max
---

# Adresse Unicast

## 📥 Définition en une phrase
> Une adresse unicast est un identifiant unique qui désigne une seule [[NetworkInterface|interface réseau]] spécifique sur un [[Network|réseau]], permettant une [[OneToOneCommunications|communication un à un]] directe entre un expéditeur et un récepteur.

## 🧠 Concepts Clés / Fonctionnement
*   **Communication Point-à-Point**: Contrairement à la [[Multicast|multidiffusion]] ou à la [[Broadcast|diffusion]], une adresse unicast est conçue pour qu'un paquet soit envoyé d'un point source à un unique point de destination.
*   **Identifiant Unique**: Chaque [[EndDevices|dispositif terminal]] ou [[NetworkDevice|périphérique réseau]] peut avoir une ou plusieurs adresses unicast pour ses interfaces.
*   **Types d'Adresses**: Les adresses unicast existent à différentes [[OpenSystemsInterconnectionModel|couches du modèle OSI]], notamment :
    *   [[MediaAccessControlAddress|Adresses MAC]] (couche 2 [[DataLinkLayer|Liaison de Données]]) : Identifient un adaptateur réseau physique.
    *   [[InternetProtocolAddress|Adresses IP]] (couche 3 [[NetworkLayer|Réseau]]) : Identifient logiquement un appareil sur un [[Network|réseau]] [[InternetProtocolSuite|IP]].

## 🛡️ Risques / Menaces Associés
*   Bien que les communications unicast soient plus ciblées, elles peuvent être la cible d'[[Attack|attaques]] spécifiques si la [[Security|sécurité]] du destinataire n'est pas adéquate.
*   Les attaques de [[DenialOfService|déni de service (DoS)]] ou de [[DistributedDenialOfService|DDoS]] peuvent cibler des adresses unicast spécifiques pour saturer un hôte ou un service.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Firewall|Pare-feu]]**: Utiliser des [[Firewall|pare-feu]] pour contrôler le trafic entrant et sortant vers et depuis des adresses unicast spécifiques.
*   **[[IntrusionPreventionSystem|IPS]] / [[IntrusionDetectionSystem|IDS]]**: Déployer des systèmes pour détecter et prévenir les [[Attack|attaques]] ciblant des hôtes unicast.
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Isoler les systèmes critiques sur des [[VirtualLocalAreaNetwork|VLAN]] ou sous-réseaux distincts pour limiter la propagation d'[[Attack|attaques]].
*   **[[AccessControl|Contrôles d'Accès]]**: Implémenter des [[AccessControl|contrôles d'accès]] stricts pour s'assurer que seuls les [[Client|clients]] autorisés peuvent communiquer avec certaines adresses unicast.

## 🔗 Notes Connexes
*   [[Unicast|Unidiffusion]]
*   [[OneToOneCommunications|Communication un à un]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[Multicast|Multidiffusion]]
*   [[Broadcast|Diffusion]]
*   [[NetworkLayer|Couche Réseau]]
*   [[DataLinkLayer|Couche Liaison de Données]]