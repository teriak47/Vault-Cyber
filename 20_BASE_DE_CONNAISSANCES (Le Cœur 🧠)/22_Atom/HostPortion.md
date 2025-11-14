---
tags:
  - host-portion
  - subnet-mask
  - ip-address-conflict
  - DHCPServer
  - NetworkSegmentation
  - VirtualLocalAreaNetwork
aliases:
  - Partie hôte
  - Host Portion
source:
  - null
cssclasses:
  - max
---

# Partie Hôte

## 📥 Définition en une phrase
> La partie hôte d'une [[InternetProtocolAddress|adresse IP]] est la partie de l'adresse qui identifie un [[Host|hôte]] spécifique au sein d'un [[Network|réseau]] local.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification Locale**: Elle est utilisée pour identifier de manière unique un [[Computer|ordinateur]], un [[Server|serveur]], un [[NetworkPrinter|imprimante réseau]] ou tout autre [[NetworkDevice|périphérique réseau]] au sein du [[LocalAreaNetwork|LAN]].
*   **Détermination par le [[SubnetMask|Masque de sous-réseau]]**: La [[SubnetMask|masque de sous-réseau]] est un nombre de 32 [[BinaryDigit|bits]] qui permet de séparer la [[NetworkPortion|partie réseau]] de la [[HostPortion|partie hôte]] d'une [[InternetProtocolAddress|adresse IP]]. Les [[BinaryDigit|bits]] mis à 0 dans le [[SubnetMask|masque]] désignent la [[HostPortion|partie hôte]].
*   **Unicité**: Chaque [[Host|hôte]] ou [[NetworkInterface|interface réseau]] sur un [[LogicalNetwork|réseau logique]] donné doit avoir une [[HostPortion|partie hôte]] unique pour assurer une [[NetworkCommunication|communication réseau]] correcte.
*   **Adresses Réservées**:
    *   Une [[HostPortion|partie hôte]] où tous les [[BinaryDigit|bits]] sont à 0 représente l'[[Network|adresse réseau]] elle-même et ne peut être attribuée à un [[Host|hôte]].
    *   Une [[HostPortion|partie hôte]] où tous les [[BinaryDigit|bits]] sont à 1 représente l'[[Broadcast|adresse de diffusion]] (broadcast) pour le [[Network|réseau]] et est utilisée pour envoyer des [[Message|messages]] à tous les [[Host|hôtes]] du [[Network|réseau]].

## 🛡️ Risques / Menaces Associés
*   **Conflits d'[[InternetProtocolAddress|adresses IP]]**: Une mauvaise [[NetworkConfiguration|configuration]] manuelle de la [[HostPortion|partie hôte]] peut entraîner des conflits d'[[InternetProtocolAddress|adresses IP]] et des [[InteroperabilityIssues|problèmes d'interopérabilité]] ou une [[ServiceDisruption|interruption de service]].
*   **[[Reconnaissance|Reconnaissance]]**: Un [[ThreatActor|acteur de menace]] peut utiliser la [[NetworkScanning|découverte de la partie hôte]] pour identifier les [[Host|hôtes]] actifs sur un [[Network|réseau]] et ainsi accroître sa [[AttackSurface|surface d'attaque]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[DynamicHostConfigurationProtocol|DHCP]]**: Utiliser un [[DHCPServer|serveur DHCP]] pour attribuer dynamiquement les [[InternetProtocolAddress|adresses IP]] et leurs [[HostPortion|parties hôtes]] afin d'éviter les erreurs et les conflits.
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Diviser un grand [[Network|réseau]] en [[VirtualLocalAreaNetwork|VLAN]] ou sous-réseaux plus petits pour limiter le nombre de [[Host|hôtes]] dans chaque [[NetworkPortion|partie réseau]] et réduire les [[Collision|collisions]] d'[[InternetProtocolAddress|adresses IP]].
*   **[[SecurityMonitoring|Surveillance de sécurité]]**: Surveiller les journaux [[Log|logs]] des [[NetworkDevice|équipements réseau]] pour détecter les conflits d'[[InternetProtocolAddress|adresses IP]] ou les activités de [[NetworkScanning|balayage réseau]] suspectes.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkPortion|Partie Réseau]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique]]
*   [[Network|Réseau]]
*   [[Host|Hôte]]
*   [[Broadcast|Diffusion]]