---
tags:
  - protocole
  - couche/transport
  - non-fiable
  - sans-connexion
  - a-completer
rfc: RFC 768
aliases:
  - Protocole de Datagrammes Utilisateur
  - UDP
  - User Datagram Protocol
  - Protocole UDP
archetype: protocole
cssclasses:
  - max
---

# Protocole de Datagrammes Utilisateur (UDP)

## 🎯 Rôle et Couche OSI
> Le [[UserDatagramProtocol|Protocole de Datagrammes Utilisateur (UDP)]] est un [[NetworkProtocol|protocole]] de la [[TransportLayer|couche transport]] du [[InternetProtocolSuite|modèle TCP/IP]]. Son rôle est de fournir un service de communication de données minimaliste, rapide, sans connexion et non fiable, où la vitesse et la faible [[NetworkCongestion|surcharge]] sont préférées à la garantie de livraison.

## ⚙️ Fonctionnement
1.  **Communication Sans Connexion**: Contrairement à [[TransmissionControlProtocol|TCP]], l'[[UserDatagramProtocol|UDP]] n'établit pas de connexion préalable ("handshake") entre l'émetteur et le récepteur. Chaque [[Packet|paquet]] est envoyé indépendamment.
2.  **Transfert de Datagrammes Indépendants**: Les données sont encapsulées dans des [[Datagram|datagrammes]] [[UserDatagramProtocol|UDP]], qui sont des unités de données indépendantes et autonomes.
3.  **Non Fiabilité**: L'[[UserDatagramProtocol|UDP]] n'inclut pas de mécanismes intégrés pour garantir la livraison, l'ordre des [[Packet|paquets]], la détection des doublons ou la retransmission en cas de perte. Il n'y a pas d'[[Acknowledgement|accusés de réception]].
4.  **Faible Surcharge**: L'[[Header|en-tête]] [[UserDatagramProtocol|UDP]] est très petit (8 octets), ce qui réduit la [[NetworkCongestion|surcharge]] et permet un traitement rapide, le rendant idéal pour les applications sensibles à la [[Latency|latence]].
5.  **Multiplexage et Démultiplexage**: L'[[UserDatagramProtocol|UDP]] utilise des [[PortNumber|numéros de port]] pour permettre à plusieurs applications sur un même [[Host|hôte]] de partager le même [[CommunicationChannel|canal de communication]] et pour que les données soient acheminées vers la bonne [[SoftwareApplication|application]] de destination.
* **Ports par défaut**:
    *   **53/UDP**: [[DomainNameSystem|DNS]] (requêtes de résolution de noms)
    *   **67/UDP, 68/UDP**: [[DynamicHostConfigurationProtocol|DHCP]] (attribution d'adresses [[InternetProtocolAddressBlocks|IP]])
    *   **123/UDP**: Network Time Protocol (NTP)
    *   **161/UDP, 162/UDP**: Simple Network Management Protocol (SNMP)

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  *   [[DenialOfService|Attaques par déni de service (DoS)]] et [[DistributedDenialOfService|DDoS]]: La nature sans connexion de l'[[UserDatagramProtocol|UDP]] facilite l'[[MACSpoofing|usurpation]] de l'[[SourceInternetProtocolVersion4Address|adresse IP source]], permettant des attaques [[DistributedDenialOfService|DDoS]] par [[DDoSReflectionAmplification|amplification]] (ex: [[DomainNameSystem|DNS]] amplification).
  *   Absence inhérente de [[Confidentiality|confidentialité]], d'[[Integrity|intégrité]] et d'[[Authentication|authentification]] des données, ce qui rend les communications [[UserDatagramProtocol|UDP]] vulnérables à l'[[Eavesdropping|écoute clandestine]] et à l'[[Tampering|altération]].
  *   [[PacketSniffing|Capture de paquets]]: Les [[Datagram|datagrammes]] [[UserDatagramProtocol|UDP]] peuvent être facilement interceptés et lus si les données ne sont pas chiffrées à la [[ApplicationLayer|couche application]].
* **Mesures de Sécurité**:
  *   La [[Security|sécurité]] des communications [[UserDatagramProtocol|UDP]] dépend largement des mécanismes implémentés à la [[ApplicationLayer|couche application]].
  *   L'utilisation de [[VirtualPrivateNetwork|VPNs]] ou de [[TransportLayerSecurity|DTLS]] (Datagram Transport Layer Security, une version de [[TransportLayerSecurity|TLS]] adaptée à l'[[UserDatagramProtocol|UDP]]) peut ajouter la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Authentication|authentification]].
  *   Les [[Firewall|pare-feu]] et les [[IntrusionPreventionSystem|IPS]] peuvent aider à filtrer et à limiter les [[NetworkTrafficAnalysis|flux UDP]] malveillants.

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|Protocole de Contrôle de Transmission (TCP)]] (pour la comparaison des services fiables et sans connexion)
*   [[InternetProtocol|Protocole Internet (IP)]] (couche réseau sous-jacente)
*   [[DomainNameSystem|Système de Noms de Domaine (DNS)]] (service critique utilisant UDP)
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]] (service critique utilisant UDP)
*   [[NetworkMonitoring|Surveillance réseau]]
*   [[Wireshark|Wireshark]] (outil d'analyse de protocole)

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   [Raison 1 : La section "Sécurité du Protocole" pourrait bénéficier d'exemples plus spécifiques d'applications UDP et de leurs vulnérabilités intrinsèques, au-delà des attaques DDoS générales.]
*   [Raison 2 : Une comparaison plus directe et structurée avec TCP (points forts/faibles de chacun) serait utile pour renforcer la compréhension de la place d'UDP.]
*   [Raison 3 : Ajouter plus d'exemples d'applications ou de services qui tirent parti de la nature de l'UDP (streaming vidéo/audio, jeux en ligne, VoIP).]
---