---
tags:
  - protocole
  - protocole/tls
  - cryptographie
  - securite/communication
  - securite/donnees
  - chiffrement
  - certificat-numerique
  - confidentialite
  - integrite
  - a-completer
aliases:
  - Sécurité de la Couche de Transport
  - TLS
  - Transport Layer Security
archetype: protocole
rfc:
cssclasses:
  - max
---

# Transport Layer Security (TLS)

## 🎯 Rôle et Couche OSI
> Le [[TransportLayerSecurity|Transport Layer Security (TLS)]] est un [[NetworkProtocol|protocole réseau]] cryptographique essentiel conçu pour sécuriser les [[NetworkCommunication|communications réseau]] sur [[Internet|Internet]]. Il établit un canal de communication sécurisé qui garantit la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] des [[Data|données]] et l'[[Authentication|authentification]] des entités communicantes. Il opère principalement au-dessus de la [[TransportLayer|couche Transport]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et de la [[InternetProtocolSuite|suite TCP/IP]], agissant comme une surcouche de sécurité pour des [[ApplicationLayer|protocoles de la couche Application]] tels que [[HypertextTransferProtocol|HTTP]].

## ⚙️ Fonctionnement
Le fonctionnement du [[TransportLayerSecurity|TLS]] repose sur une série d'étapes, notamment la poignée de main [[TLSHandshake|TLS Handshake]], pour établir une session sécurisée :

1.  **Négociation du Handshake**: Le [[Client|client]] et le [[Server|serveur]] échangent des messages (ClientHello, ServerHello) pour négocier les paramètres de la connexion sécurisée, incluant la version de [[TransportLayerSecurity|TLS]] à utiliser, les [[CipherSuite|suites de chiffrement]] supportées, et des nombres aléatoires.
2.  **Authentification du Serveur**: Le [[Server|serveur]] envoie son [[DigitalCertificate|certificat numérique]] (contenant sa [[PublicKey|clé publique]]) au [[Client|client]]. Le [[Client|client]] vérifie la validité de ce [[DigitalCertificate|certificat]] auprès d'une [[CertificateAuthority|autorité de certification]] de confiance afin d'authentifier le [[Server|serveur]] et de prévenir les [[ManInTheMiddle|attaques de l'homme du milieu]]. L'authentification mutuelle du [[Client|client]] est optionnelle et moins fréquente.
3.  **Échange de Clés**: Les parties utilisent un [[KeyExchangeAlgorithm|algorithme d'échange de clés]] (ex: Diffie-Hellman) pour établir une clé de session symétrique unique et secrète, qui sera utilisée pour le [[DataEncryption|chiffrement]] des [[Data|données]] de la session. Cet échange se fait de manière sécurisée grâce à la [[Cryptography|cryptographie]] asymétrique.
4.  **Chiffrement des Données**: Une fois la clé de session établie, toutes les [[DataTransmission|données échangées]] entre le [[Client|client]] et le [[Server|serveur]] sont [[DataEncryption|chiffrées]] symétriquement et accompagnées d'un [[MessageAuthenticationCode|code d'authentification de message (MAC)]] pour garantir leur [[Confidentiality|confidentialité]] et leur [[Integrity|intégrité]] durant le [[DataTransmission|transit]].

*   **Ports par défaut**: [[TransmissionControlProtocol|TCP]]/443 (pour [[HypertextTransferProtocolSecure|HTTPS]])

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   [[ManInTheMiddle|Attaques de l'homme du milieu]] (lorsque l'[[DigitalCertificate|authentification]] est contournée ou le [[DigitalCertificate|certificat]] compromis)
    *   [[ProtocolDowngradeAttacks|Attaques par rétrogradation de protocole]] (forcer la connexion à utiliser des versions de [[TransportLayerSecurity|TLS]] ou [[SecureSocketLayer|SSL]] plus anciennes et moins sécurisées)
    *   [[WeakCipherSuites|Utilisation de suites de chiffrement faibles]] ou obsolètes
    *   [[SoftwareVulnerability|Vulnérabilités logicielles]] dans les implémentations de [[TransportLayerSecurity|TLS]] (ex: Heartbleed pour OpenSSL dans le passé, [[ZeroDay|zero-days]])
*   **Versions sécurisées**:
    *   [[TransportLayerSecurity|TLS]] est le successeur de [[SecureSocketLayer|SSL]] (versions 1.0, 2.0, 3.0), toutes les versions de [[SecureSocketLayer|SSL]] étant considérées comme obsolètes et insécurisées.
    *   [[TransportLayerSecurity|TLS]] 1.2 et [[TransportLayerSecurity|TLS]] 1.3 sont les versions actuellement recommandées. [[TransportLayerSecurity|TLS]] 1.3, en particulier, apporte des améliorations significatives en termes de performance et de sécurité en simplifiant le processus de [[TLSHandshake|handshake]] et en éliminant les fonctionnalités cryptographiques obsolètes.

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|TCP]]
*   [[HypertextTransferProtocolSecure|HTTPS]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[Cryptography|Cryptographie]]
*   [[Authentication|Authentification]]
*   [[Integrity|Intégrité]]
*   [[Confidentiality|Confidentialité]]
*   [[Wireshark|Wireshark]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[SecureSocketLayer|SSL]]
*   [[TLSHandshake|TLS Handshake]]
*   [[ApplicationLayer|Couche Application]]
*   [[TransportLayer|Couche de Transport]]
*   [[CipherSuite|Suite de Chiffrement]]
*   [[KeyExchangeAlgorithm|Algorithme d'Échange de Clés]]
*   [[CertificateAuthority|Autorité de Certification]]

## 🤔 Pistes d'Amélioration (Auto-Évaluation IA)
*   Le concept de [[TLSHandshake|Handshake TLS]] mériterait un développement plus détaillé, incluant les différentes phases (ClientHello, ServerHello, Certificate, ServerKeyExchange, ClientKeyExchange, ChangeCipherSpec, Finished).
*   Il serait également pertinent de détailler les différences clés et les améliorations de sécurité entre les versions de [[TransportLayerSecurity|TLS]] (1.2 et 1.3).
*   Une section sur les [[CipherSuite|suites de chiffrement]] et leur importance pour la sécurité pourrait être ajoutée.