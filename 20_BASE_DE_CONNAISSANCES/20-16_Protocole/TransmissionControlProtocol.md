---
tags:
  - protocole
  - protocole/tcp
aliases:
  - Protocole de Contrôle de Transmission
  - TCP
  - Transmission Control Protocol
  - protocole TCP
archetype: protocole
rfc: RFC 793
cssclasses:
  - max
---

# Protocole de Contrôle de Transmission (TCP)

## 🎯 Rôle et Couche OSI
Le [[TransmissionControlProtocol|Protocole de Contrôle de Transmission (TCP)]] est un [[NetworkProtocol|protocole]] de communication fiable, orienté connexion, qui opère au niveau de la [[TransportLayer|couche Transport]] du [[InternetProtocolSuite|modèle TCP/IP]]. Son rôle principal est d'assurer la livraison ordonnée et sans erreur des [[Data|données]] entre les [[SoftwareApplication|applications]] sur un [[Network|réseau]].

## ⚙️ Fonctionnement
1.  **Établissement de Connexion (Three-Way Handshake)**: Avant tout [[DataTransmission|transfert de données]], le [[TransmissionControlProtocol|TCP]] utilise une [[ThreeWayHandshake|poignée de main en trois étapes]] (SYN, SYN-ACK, ACK) pour établir une connexion logique fiable entre deux [[Host|hôtes]].
2.  **Fiabilité et Ordre**: Il assure la livraison complète et dans le bon ordre des [[Data|données]] en attribuant un [[Sequencing|numéro de séquence]] à chaque segment et en nécessitant un [[Acknowledgement|acquittement (ACK)]] pour la réception réussie. Si un acquittement n'est pas reçu, le segment est [[Retransmission|retransmis]].
3.  **Contrôle de Flux (Flow Control)**: Le [[TransmissionControlProtocol|TCP]] empêche un expéditeur d'envoyer des [[Data|données]] plus rapidement que le récepteur ne peut les traiter en utilisant des [[FlowControl|fenêtres glissantes]], évitant ainsi la saturation du [[Buffer|tampon]] du récepteur.
4.  **Contrôle de Congestion (Congestion Control)**: Ajuste dynamiquement le [[Throughput|débit]] de [[DataTransmission|transmission]] des [[Data|données]] pour éviter la [[NetworkCongestion|congestion du réseau]], en utilisant des algorithmes tels que [[CongestionControl|Slow Start]] et [[CongestionControl|Congestion Avoidance]].
5.  **Gestion des Segments**: Les [[Data|données]] d'[[SoftwareApplication|application]] sont divisées en [[Packet|segments TCP]], qui sont ensuite [[Encapsulation|encapsulés]] dans des [[InternetProtocol|paquets IP]] pour le [[Routing|routage]] à travers le [[Network|réseau]].
* **Ports par défaut**:
  *   TCP/20, TCP/21 ([[FileTransferProtocol|FTP]])
  *   TCP/23 (Telnet)
  *   TCP/25 (SMTP)
  *   TCP/80 ([[HypertextTransferProtocol|HTTP]])
  *   TCP/443 ([[HypertextTransferProtocolSecure|HTTPS]])

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  *   [[DenialOfService|Attaques par Déni de Service]] (ex: SYN Flood, qui épuise les ressources du [[Server|serveur]] en maintenant des connexions semi-ouvertes).
  *   [[ManInTheMiddle|Attaques de l'Homme du Milieu]] (MITM), en particulier lorsque le [[Data|trafic]] n'est pas chiffré.
  *   [[SessionHijacking|Détournement de session]] ([[SessionHijacking|Session Hijacking]]) via la prédiction ou l'interception des numéros de [[Sequencing|séquence]].
* **Versions sécurisées**:
  *   La [[Security|sécurité]] du [[TransmissionControlProtocol|TCP]] est principalement renforcée par des [[NetworkProtocol|protocoles]] de couches supérieures, notamment [[TransportLayerSecurity|Transport Layer Security (TLS)]] et son prédécesseur [[SecureSocketLayer|Secure Socket Layer (SSL)]]. Ces [[Protocol|protocoles]] sont utilisés par des services comme [[HypertextTransferProtocolSecure|HTTPS]], [[FileTransferProtocolSecure|FTPS]] et [[SecureShell|SSH]] pour le [[Encryption|chiffrement]] et l'[[Authentication|authentification]].

## 🔗 Notes Connexes
*   [[InternetProtocol|Protocole Internet (IP)]]
*   [[UserDatagramProtocol|Protocole de Datagrammes Utilisateur (UDP)]]
*   [[InternetProtocolSuite|Suite de Protocoles Internet (TCP/IP)]]
*   [[ThreeWayHandshake|Poignée de main en trois étapes]]
*   [[Wireshark|Wireshark]]
