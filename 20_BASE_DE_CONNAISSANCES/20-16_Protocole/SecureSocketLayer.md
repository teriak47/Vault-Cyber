---
tags:
  - protocole
  - protocole/ssl
  - securite/chiffrement
  - securite/certificat-numerique
  - securite/reseau
  - securite/connexion-securisee
  - securite/cryptographie
  - securite/authentification
aliases:
  - SSL
  - Secure Socket Layer
  - Couche de Sockets Sécurisée
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Couche de Sockets Sécurisée (SSL)

## 🎯 Rôle et Couche OSI
> Le [[SecureSocketLayer|protocole Secure Socket Layer]] (SSL) est un [[Protocol|protocole]] de [[Security|sécurité]] déprécié qui établissait un [[CommunicationChannel|canal chiffré]] entre un [[Client|client]] et un [[Server|serveur]] pour sécuriser les [[NetworkCommunication|communications]] sur un [[Network|réseau informatique]], notamment sur le [[WorldWideWeb|web]]. Il opérait principalement entre la [[TransportLayer|couche de transport]] ([[TransmissionControlProtocol|TCP]]) et la [[ApplicationLayer|couche application]] du [[InternetProtocolSuite|modèle TCP/IP]], et correspondait aux couches [[PresentationLayer|Présentation]] et [[SessionLayer|Session]] du [[OpenSystemsInterconnectionModel|modèle OSI]].

## ⚙️ Fonctionnement
1.  **Établissement de la poignée de main (Handshake)**: Le [[SecureSocketLayer|SSL]] utilisait un [[HandshakeProtocol|protocole de poignée de main]] pour initier une [[SecureConnection|connexion sécurisée]]. Durant cette phase, le [[Client|client]] et le [[Server|serveur]] négociaient les paramètres de [[Encryption|chiffrement]], les algorithmes à utiliser et échangeaient les clés de [[Session|session]].
2.  **Authentification et intégrité**: Il s'appuyait sur des [[DigitalCertificate|certificats numériques]] (X.509) pour l'[[Authentication|authentification]] du [[Server|serveur]] et, parfois, du [[Client|client]], garantissant l'[[Integrity|intégrité]] des [[Data|données]] échangées.
3.  **Chiffrement des données**: L'[[Encryption|échange initial de clés]] était réalisé via le [[AsymmetricEncryption|chiffrement asymétrique]]. Une fois la [[Session|session]] établie, le [[DataTransmission|transfert de données]] était sécurisé par le [[SymmetricEncryption|chiffrement symétrique]], plus rapide et efficace pour de grands volumes de [[Data|données]].
* **Ports par défaut**: [[TransmissionControlProtocol|TCP]]/443 (pour [[HypertextTransferProtocolSecure|HTTPS]])

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * Le [[SecureSocketLayer|SSL]] a été sujet à de nombreuses [[Vulnerability|vulnérabilités critiques]] au fil de ses versions, le rendant obsolète. Parmi elles, on compte des faiblesses permettant des [[ManInTheMiddle|attaques de l'homme du milieu]], des attaques par [[PaddingOracleAttack|oracle de padding]] (comme [[POODLEAttack|POODLE]]), et des fuites d'informations via des attaques comme [[CRIMEAttack|CRIME]] et [[BEASTAttack|BEAST]].
* **Versions sécurisées**:
  * Le protocole [[TransportLayerSecurity|Transport Layer Security]] (TLS) est le successeur direct du [[SecureSocketLayer|SSL]], apportant des améliorations significatives en matière de [[Security|sécurité]] et de robustesse. Toutes les versions de SSL sont aujourd'hui considérées comme obsolètes et dangereuses.

## 🔗 Notes Connexes
* [[TransportLayerSecurity|Transport Layer Security (TLS)]]
* [[DigitalCertificate|Certificat Numérique]]
* [[Encryption|Chiffrement]]
* [[Cryptography|Cryptographie]]
* [[AsymmetricEncryption|Chiffrement Asymétrique]]
* [[SymmetricEncryption|Chiffrement Symétrique]]
* [[Authentication|Authentification]]
* [[HypertextTransferProtocolSecure|HTTPS]]
* [[Wireshark|Wireshark]]
* [[ManInTheMiddle|Man-in-the-Middle (MITM)]]
* [[PaddingOracleAttack|Attaque par Oracle de Padding]]