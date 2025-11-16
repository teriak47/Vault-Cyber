---
tags:
aliases:
  - Partie hôte
  - Host Portion
  - Host part
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Partie Hôte

## 📥 Définition en une phrase
> La partie hôte d'une [[InternetProtocol|adresse IP]] est le segment de l'adresse qui identifie de manière unique un [[Host|hôte]] ou un [[NetworkDevice|périphérique réseau]] au sein d'un [[Network|réseau]] spécifique.

## 🧠 Concepts Clés / Piliers
*   **Identification Locale Unique**: Elle permet d'identifier précisément un [[Computer|ordinateur]], un [[Server|serveur]], une [[NetworkPrinter|imprimante réseau]] ou toute [[NetworkInterface|interface réseau]] sur un [[LogicalNetwork|réseau logique]], assurant une [[OneToOneCommunications|communication point à point]] au sein du [[LocalAreaNetwork|LAN]].
*   **Détermination par le [[SubnetMask|Masque de sous-réseau]]**: La frontière entre la [[NetworkPortion|partie réseau]] et la partie hôte est définie par le [[SubnetMask|masque de sous-réseau]]. Les [[BinaryDigit|bits]] mis à 0 dans le [[SubnetMask|masque]] correspondent à la partie hôte de l'[[InternetProtocol|adresse IP]].
*   **Unicité Nécessaire**: Pour que la [[NetworkCommunication|communication réseau]] fonctionne correctement, chaque [[Host|hôte]] actif sur un même [[NetworkSegment|segment réseau]] doit posséder une partie hôte unique.
*   **Adresses Réservées Spécifiques**:
    *   Une partie hôte composée uniquement de [[BinaryDigit|zéros]] est réservée pour l'[[NetworkAddress|adresse réseau]] elle-même et ne peut être attribuée à un [[Host|hôte]] individuel.
    *   Une partie hôte composée uniquement de [[BinaryDigit|uns]] est l'[[BroadcastAddress|adresse de diffusion]] du [[Network|réseau]], utilisée pour envoyer des [[Message|messages]] à tous les [[Host|hôtes]] du [[Subnet|sous-réseau]].

## 💡 Importance en Cybersécurité
> La gestion et la compréhension de la partie hôte sont fondamentales pour la [[NetworkSecurity|sécurité réseau]] et la [[Availability|disponibilité]] des services. Une [[NetworkConfiguration|configuration]] incorrecte peut mener à des [[InternetProtocol|conflits d'adresses IP]] et des [[ServiceDisruption|interruptions de service]], compromettant l'[[Availability|disponibilité]]. Pour les [[ThreatActor|acteurs de menace]], l'analyse des parties hôtes actives via la [[Reconnaissance|reconnaissance]] et le [[PortScanning|balayage de ports]] est une étape clé pour identifier les cibles potentielles et accroître la [[AttackSurface|surface d'attaque]]. L'adoption de pratiques comme le [[DynamicHostConfigurationProtocol|DHCP]] pour une attribution automatisée, la [[NetworkSegmentation|segmentation réseau]] (par exemple via des [[VirtualLocalAreaNetwork|VLAN]]) pour réduire la taille des domaines de diffusion, et la [[SecurityMonitoring|surveillance de sécurité]] des [[Log|journaux]] sont des mesures essentielles pour prévenir les risques liés à la mauvaise gestion des parties hôtes et renforcer la [[Défense en Profondeur|défense en profondeur]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[NetworkPortion|Partie Réseau]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique]]
*   [[Network|Réseau]]
*   [[Host|Hôte]]
*   [[Broadcast|Diffusion]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Reconnaissance|Reconnaissance]]