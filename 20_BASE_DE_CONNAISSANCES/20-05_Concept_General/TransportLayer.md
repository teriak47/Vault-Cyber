---
tags:
  - concept
  - concept/general
  - couche/transport
  - modele/osi
  - modele/tcp-ip
aliases:
  - Couche de Transport
  - Transport Layer
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Couche de Transport

## 📥 Définition en une phrase
> La [[TransportLayer|Couche de Transport]], quatrième couche du [[OpenSystemsInterconnectionModel|modèle OSI]] et deuxième du [[InternetProtocolSuite|modèle TCP/IP]], est responsable d'établir et de maintenir la communication logique de bout en bout entre les [[SoftwareApplication|applications]] exécutées sur différents [[Host|hôtes]], garantissant la [[DataTransmission|transmission de données]] fiable ou rapide.

## 🧠 Concepts Clés / Piliers
*   **[[DataSegmentation|Segmentation]] et [[DataReassembly|Réassemblage]]**: Division des [[Data|données]] de l'[[ApplicationLayer|application]] en [[Segment|segments]] de taille gérable pour la [[DataTransmission|transmission]], et leur reconstitution à la réception.
*   **[[Multiplexing|Multiplexage]] et [[Demultiplexing|Démultiplexage]]**: Permet à plusieurs [[SoftwareApplication|applications]] d'utiliser simultanément une même [[Network|connexion réseau]] grâce à l'attribution de [[PortNumber|numéros de port]] uniques.
*   **[[FlowControl|Contrôle de Flux]]**: Mécanisme pour gérer le débit de [[Data|données]] entre émetteur et récepteur, empêchant l'émetteur de submerger le récepteur. Cela contribue à la [[Availability|disponibilité]] du [[System|système]].
*   **[[ErrorControl|Contrôle d'Erreur]]**: Fonctionnalité (principalement dans [[TransmissionControlProtocol|TCP]]) qui assure l'[[Integrity|intégrité]] des [[Data|données]] en détectant et en corrigeant les [[SoftwareBugs|erreurs]] de [[SignalTransmission|transmission de signal]] ou les pertes de [[Segment|segments]].
*   **Protocoles Majeurs**:
    *   [[TransmissionControlProtocol|TCP]]: [[Protocol|Protocole]] orienté connexion, offrant une [[DataTransmission|transmission fiable]] grâce à des [[Acknowledgement|accusés de réception]], le [[FlowControl|contrôle de flux]] et le [[CongestionControl|contrôle de congestion]].
    *   [[UserDatagramProtocol|UDP]]: [[Protocol|Protocole]] sans connexion, plus rapide car sans surcharge de fiabilité, utilisé pour les applications sensibles à la [[Latency|latence]] (ex: streaming, jeux en ligne).

## 💡 Importance en Cybersécurité
> La [[TransportLayer|Couche de Transport]] est cruciale pour la [[Cybersecurity|cybersécurité]] car elle détermine la fiabilité et la confidentialité des [[NetworkCommunication|communications réseau]]. Les [[NetworkProtocol|protocoles réseau]] comme [[TransmissionControlProtocol|TCP]] et [[UserDatagramProtocol|UDP]] influencent directement la [[Availability|disponibilité]] et l'[[Integrity|intégrité]] des [[OnlineServices|services en ligne]]. Des [[SecurityVulnerabilities|vulnérabilités]] au niveau de cette couche peuvent mener à des [[DenialOfService|attaques par déni de service]], des [[Eavesdropping|écoutes clandestines]] (si non protégée par [[TransportLayerSecurity|TLS]] ou [[SecureSocketLayer|SSL]]) ou des problèmes d'[[Integrity|intégrité]] des [[Data|données]]. La bonne configuration des [[PortNumber|numéros de port]] et l'utilisation de [[SecureRoutingProtocols|protocoles sécurisés]] sont essentielles pour prévenir les [[DigitalAttack|attaques numériques]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[ApplicationLayer|Couche Application]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[PortNumber|Numéro de Port]]
*   [[NetworkCommunication|Communication réseau]]
*   [[DataTransmission|Transmission de données]]
*   [[Integrity|Intégrité]]
*   [[Availability|Disponibilité]]
*   [[DenialOfService|Déni de Service]]
*   [[TransportLayerSecurity|TLS]]