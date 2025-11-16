---
tags:
aliases:
  - Traduction d'Adresses Réseau
  - NAT
  - Network Address Translation
  - NAPT
  - Overload NAT
cssclasses:
  - max
archetype: concept-general
source:
---

# Traduction d'Adresses Réseau (NAT)

## 📥 Définition en une phrase
> La [[NetworkAddressTranslation|Traduction d'Adresses Réseau]] (NAT) est une méthode utilisée pour remapper un [[InternetProtocolAddressBlocks|espace d'adressage IP]] à un autre en modifiant les informations d'[[InternetProtocol|adresse IP]] dans l'[[Header|en-tête]] des [[Packet|paquets]] lors de leur transit à travers un [[Router|dispositif de routage]] ou un [[Firewall|pare-feu]].

## 🧠 Concepts Clés / Piliers
*   **Masquage d'[[InternetProtocol|Adresses IP]]**: Permet à de multiples [[EndDevices|appareils]] sur un [[InternalNetwork|réseau privé]] d'utiliser une seule [[PublicIPAddress|adresse IP publique]] pour se connecter à l'[[Internet|Internet]], masquant ainsi leurs [[PrivateIPAddress|adresses IP privées]].
*   **Économie d'[[PublicIPAddress|Adresses IP Publiques]]**: Une fonction clé, particulièrement importante pour l'[[InternetProtocolVersion4|IPv4]] où les adresses publiques sont limitées. La NAT permet à un grand nombre d'appareils d'un [[LocalAreaNetwork|LAN]] de partager un nombre restreint d'[[PublicIPAddress|adresses IP publiques]].
*   **Types de NAT**:
    *   **NAT Statique**: Mappe une [[PrivateIPAddress|adresse IP privée]] spécifique à une [[PublicIPAddress|adresse IP publique]] dédiée. Souvent utilisée pour les [[Server|serveurs]] internes qui doivent être accessibles depuis l'[[Internet|extérieur]].
    *   **NAT Dynamique**: Mappe des [[PrivateIPAddress|adresses IP privées]] à un pool d'[[PublicIPAddress|adresses IP publiques]] disponibles, attribuées dynamiquement.
    *   **NAT de Port (PAT ou [[NetworkAddressTranslation|NAPT]])**: Le type le plus courant, également appelé "Overload NAT". Il permet à de multiples [[PrivateIPAddress|adresses IP privées]] de partager une seule [[PublicIPAddress|adresse IP publique]] en utilisant différents [[PortNumber|numéros de port]] pour distinguer les [[CommunicationChannel|communications]].
*   **Fonctionnement transparent**: La NAT est généralement transparente pour les [[Host|hôtes]] du [[InternalNetwork|réseau interne]] et pour les [[Server|serveurs]] externes, qui perçoivent l'adresse IP publique du [[NetworkAddressTranslation|dispositif NAT]].
*   **Implémentation**: La configuration de la NAT se fait généralement sur un [[Router|routeur]] ou un [[Firewall|pare-feu]] à la périphérie du [[Network|réseau]].

## 💡 Importance en Cybersécurité
> La [[NetworkAddressTranslation|NAT]] joue un rôle ambivalent en [[Cybersecurity|cybersécurité]]. D'une part, elle contribue à la [[Security|sécurité]] en cachant la [[NetworkTopology|topologie interne]] du [[InternalNetwork|réseau privé]] et les [[PrivateIPAddress|adresses IP privées]] des [[EndDevices|dispositifs]] internes, rendant plus difficile pour un [[ThreatActor|acteur de menace]] externe de cibler directement ces [[Host|hôtes]]. Cette capacité de masquage réduit la [[AttackSurface|surface d'attaque]] visible depuis l'[[Internet|Internet]].

> Cependant, la NAT introduit également des défis. Elle peut compliquer la [[TrafficManagement|gestion du trafic]] entrant et la mise en œuvre de [[SecurityControl|contrôles de sécurité]] pour des [[SoftwareApplication|applications]] spécifiques, nécessitant souvent des configurations complexes comme le [[PortForwarding|transfert de port]]. Le partage d'une même [[PublicIPAddress|adresse IP publique]] par plusieurs [[User|utilisateurs]] via [[NetworkAddressTranslation|PAT]] peut entraîner une [[LossOfTraceability|perte de traçabilité]] dans les [[Log|journaux]] externes, rendant l'[[IncidentResponse|analyse des incidents]] plus ardue. De plus, la [[NetworkAddressTranslation|NAT]] peut interférer avec certains [[SoftwareApplication|applications]] ou [[Protocol|protocoles]] (qui incluent des [[InternetProtocol|informations IP]] dans leur [[Payload|charge utile]]), nécessitant des [[ApplicationLayerGateway|passerelles de couche application]] (ALG) ou [[UniversalPlugAndPlay|UPnP]], ce dernier étant une [[SecurityVulnerabilities|vulnérabilité]] potentielle s'il n'est pas géré avec prudence. Les bonnes pratiques incluent un [[PortForwarding|transfert de port]] sélectif et la désactivation d'[[UniversalPlugAndPlay|UPnP]] pour renforcer la [[Security|sécurité]].

## 🔗 Notes Connexes
*   [[IPAddressing|Adressage IP]]
*   [[PrivateIPAddress|Adresses IP Privées]]
*   [[PublicIPAddress|Adresses IP Publiques]]
*   [[Firewall|Pare-feu]]
*   [[Router|Routeur]]
*   [[PortForwarding|Transfert de Port]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[UniversalPlugAndPlay|UPnP]]
*   [[SessionInitiationProtocol|SIP ALG]]
*   [[AttackSurface|Surface d'attaque]]
*   [[LossOfTraceability|Perte de Traçabilité]]
*   [[ApplicationLayerGateway|Passerelle de Couche Application]]