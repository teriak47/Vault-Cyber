---
tags:
aliases:
  - Pile de Protocoles
  - Protocol Stack
  - Protocol stack
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Pile de Protocoles (Protocol Stack)

## 📥 Définition en une phrase
> Une [[ProtocolStack|pile de protocoles]] est un ensemble de [[NetworkProtocol|protocoles réseau]] fonctionnant ensemble de manière hiérarchique, chaque [[Protocol|protocole]] à une [[NetworkLayer|couche]] spécifique offrant des services à la couche supérieure et utilisant ceux de la couche inférieure pour assurer une [[NetworkCommunication|communication réseau]] complète.

## 🧠 Concepts Clés / Piliers
*   **Organisation en Couches**: La [[ProtocolStack|pile de protocoles]] est structurée en couches distinctes, comme illustré par les [[ReferenceModel|modèles de référence]] tels que le [[OpenSystemsInterconnectionModel|Modèle OSI]] (7 couches) et le [[InternetProtocolSuite|Modèle TCP/IP]] (4 ou 5 couches). Chaque [[NetworkLayer|couche]] a des responsabilités bien définies dans le processus de [[DataTransmission|transmission de données]].
*   **Responsabilités Spécifiques**: Chaque [[NetworkLayer|couche]] gère une fonction particulière de la [[NetworkCommunication|communication]]. Par exemple, la [[PhysicalLayer|couche physique]] s'occupe de la transmission des [[Bit|bits]], la [[DataLinkLayer|couche liaison de données]] de l'accès au [[NetworkMedia|support réseau]], la [[NetworkLayer|couche réseau]] du [[Routing|routage]] des [[Packet|paquets]], la [[TransportLayer|couche transport]] de la fiabilité de la [[Delivery|livraison]], et la [[ApplicationLayer|couche application]] des services aux [[User|utilisateurs]].
*   **[[Encapsulation|Encapsulation]] et [[Decapsulation|Décapsulation]]**: Lors de l'envoi de [[Data|données]], chaque [[NetworkLayer|couche]] ajoute son propre [[Header|en-tête]] (et parfois un pied de page) aux [[Data|données]] reçues de la couche supérieure. Ce processus est appelé [[Encapsulation|encapsulation]]. À la [[Acknowledgement|réception]], les [[Header|en-têtes]] sont retirés séquentiellement par chaque couche lors de la [[Decapsulation|désencapsulation]], jusqu'à l'extraction de la [[Payload|charge utile]] originale.
*   **Communication Inter-Couches**: Les [[NetworkLayer|couches]] adjacentes interagissent via des interfaces de services définies, permettant à un [[NetworkProtocol|protocole]] d'utiliser les services de la couche inférieure sans nécessiter de connaissance approfondie de son implémentation. Cela favorise l'[[Interoperability|interopérabilité]] et la modularité.
*   **Exemples Concrets**: La [[InternetProtocolSuite|pile de protocoles Internet (TCP/IP)]] est l'exemple le plus répandu, intégrant des [[NetworkProtocol|protocoles]] tels que [[Ethernet|Ethernet]] (couche liaison de données), [[InternetProtocol|IP]] (couche réseau), [[TransmissionControlProtocol|TCP]] ou [[UserDatagramProtocol|UDP]] (couche transport), et [[HypertextTransferProtocol|HTTP]] ou [[DomainNameSystem|DNS]] (couche application).

## 💡 Importance en Cybersécurité
> La [[ProtocolStack|pile de protocoles]] est au cœur de la [[NetworkSecurity|sécurité réseau]]. Toute [[Vulnerability|vulnérabilité]] ou mauvaise [[NetworkConfiguration|configuration]] à n'importe quelle [[NetworkLayer|couche]] peut servir de [[AttackVector|vecteur d'attaque]] pour des [[DigitalAttack|attaques numériques]]. Une compréhension approfondie de son fonctionnement est essentielle pour la [[DefenseInDepth|défense en profondeur]]. Par exemple, des [[Attack|attaques]] comme le [[DenialOfService|déni de service]] peuvent cibler les faiblesses des [[NetworkProtocol|protocoles]] de [[TransportLayer|transport]], tandis que les [[ManInTheMiddle|attaques de l'homme du milieu]] peuvent exploiter des vulnérabilités dans les [[NetworkProtocol|protocoles]] de bas niveau comme [[AddressResolutionProtocol|ARP]]. La [[Security|sécurité]] d'une [[ProtocolStack|pile de protocoles]] repose sur la [[PatchManagement|gestion des correctifs]], des [[Firewall|pare-feux]] efficaces et des [[SecureConfiguration|configurations sécurisées]] pour protéger chaque [[NetworkLayer|couche]] contre l'[[Exploitation|exploitation]]. Le [[Encryption|chiffrement]] (ex: [[TransportLayerSecurity|TLS]], IPsec) est également vital pour la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[DataTransmission|transmissions]].

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[Encapsulation|Encapsulation]]
*   [[Decapsulation|Décapsulation]]
*   [[InternetProtocolSuite|Suite de Protocoles Internet (TCP/IP)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DefenseInDepth|Défense en Profondeur]]
*   [[ProtocolVulnerability|Vulnérabilité de Protocole]]
*   [[SecureConfiguration|Configuration Sécurisée]]