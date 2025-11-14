---
tags:
  - standardisation
  - regles-communication
  - architecture/protocolaire
  - protocole
  - modele/osi
  - securite/protocoles-reseau
aliases:
  - Protocole Réseau
  - Network Protocol
source:
  - null
cssclasses:
  - max
---

# Protocole Réseau

## 📥 Définition en une phrase
> Un protocole réseau est un ensemble de règles et de conventions standardisées qui régissent la manière dont les données sont formatées, transmises, reçues et interprétées entre différents appareils sur un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Standardisation:** Les protocoles assurent l'interopérabilité et la communication cohérente entre des systèmes hétérogènes.
*   **Modèles en Couches:** Ils sont souvent organisés en couches, comme illustré par le [[OpenSystemsInterconnectionModel|Modèle OSI]] (7 couches) ou le [[TcpIpModel|Modèle TCP/IP]] (4/5 couches), où chaque couche gère des aspects spécifiques de la communication.
*   **Fonctionnalités:** Incluent l'adressage (ex: [[InternetProtocol|IP]]), le routage, le contrôle de flux, la détection et la correction d'erreurs, l'établissement de sessions et la fragmentation/réassemblage des données.
*   **Types Communs:** On distingue les protocoles de transport (ex: [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]]), de réseau (ex: [[InternetProtocol|IP]], [[InternetControlMessageProtocol|ICMP]]), et d'application (ex: [[HypertextTransferProtocol|HTTP]], [[FileTransferProtocol|FTP]], [[DomainNameSystem|DNS]]).

## 🛡️ Risques / Menaces Associés
*   [[ProtocolVulnerability|Vulnérabilités de protocole]]: Des failles dans la conception ou l'implémentation des protocoles peuvent être exploitées pour des attaques.
*   [[ManInTheMiddle|Attaque de l'homme du milieu (MitM)]]: Interception et modification du trafic réseau en se plaçant entre deux interlocuteurs.
*   [[DenialOfService|Attaque par déni de service (DoS)]]: Exploitation des protocoles pour surcharger les ressources d'un système et le rendre indisponible.
*   [[PacketSniffing|Reniflage de paquets]]: Capture de données non chiffrées échangées via certains protocoles pour en extraire des [[SensitiveData|informations sensibles]].
*   [[IP_Spoofing|Usurpation d'IP]]: Falsification de l'adresse IP source pour masquer l'identité de l'attaquant ou contourner des contrôles d'accès.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]]: Utiliser des protocoles sécurisés (ex: [[TransportLayerSecurity|TLS]], [[SecureShell|SSH]], [[IPsec]]) pour protéger la confidentialité et l'intégrité des données en transit.
*   [[Firewall|Pare-feu]]: Configurer des règles de filtrage strictes pour contrôler le trafic protocolaire autorisé et bloquer les communications suspectes.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]]: Surveiller le trafic réseau pour détecter et potentiellement prévenir les activités protocolaires malveillantes ou anormales.
*   [[PatchManagement|Gestion des correctifs]]: Appliquer régulièrement les mises à jour et correctifs de sécurité pour les systèmes d'exploitation et les applications afin de corriger les vulnérabilités connues dans les implémentations de protocoles.
*   [[NetworkSegmentation|Segmentation réseau]]: Isoler les différents segments du réseau pour limiter la propagation d'une attaque en cas de compromission d'un [[Protocols|protocole]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[TcpIpModel|Modèle TCP/IP]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetProtocol|IP]]
*   [[HypertextTransferProtocol|HTTP]]
*   [[DomainNameSystem|DNS]]