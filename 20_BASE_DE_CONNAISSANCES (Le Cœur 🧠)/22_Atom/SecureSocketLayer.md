---
tags:
aliases:
  - SSL
  - Secure Socket Layer
  - Couche de Sockets Sécurisée
source:
  - 
cssclasses:
  - max
---

# Couche de Sockets Sécurisée (SSL)

## 📥 Définition en une phrase
> Le protocole Secure Socket Layer (SSL) est un [[Protocols|protocole]] de sécurité déprécié qui établissait un canal chiffré entre un client et un serveur pour sécuriser les communications sur un réseau informatique, notamment sur le web.

## 🧠 Concepts Clés / Fonctionnement
*   Le [[SecureSocketLayer|SSL]] utilise un [[HandshakeProtocol|protocole de poignée de main]] pour établir une connexion sécurisée, au cours duquel le client et le serveur négocient les paramètres de chiffrement.
*   Il s'appuie sur des [[DigitalCertificate|certificats numériques]] (X.509) pour l'authentification du serveur et pour garantir l'intégrité des données échangées.
*   Emploie le [[Encryption|chiffrement]] asymétrique pour l'échange initial de clés et le chiffrement symétrique pour la communication des données une fois la session établie.
*   A été progressivement remplacé par le protocole [[TransportLayerSecurity|Transport Layer Security (TLS)]] en raison de nombreuses vulnérabilités découvertes dans les différentes versions de SSL.

## 🛡️ Risques / Menaces Associés
*   [[ProtocolVulnerability|Vulnérabilités de protocole]] inhérentes aux versions obsolètes de [[SecureSocketLayer|SSL]], telles que POODLE (Padding Oracle On Downgraded Legacy Encryption) et BEAST (Browser Exploit Against SSL/TLS).
*   Risque d'[[ManInTheMiddle|attaque de l'homme du milieu (MitM)]] si des versions non sécurisées de [[SecureSocketLayer|SSL]] sont utilisées ou si les [[DigitalCertificate|certificats]] ne sont pas correctement validés.
*   Déprécié par l'[[InternetEngineeringTaskForce|IETF]] et la plupart des navigateurs web et systèmes d'exploitation modernes, ce qui rend son utilisation risquée et non conforme aux bonnes pratiques de sécurité actuelles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Migrer impérativement vers [[TransportLayerSecurity|TLS]] (Transport Layer Security), en utilisant idéalement les versions 1.2 ou 1.3 qui sont considérées comme sécurisées.
*   Assurer la validité, la non-révocation et la bonne configuration des [[DigitalCertificate|certificats numériques]] sur les serveurs.
*   Appliquer des [[SecurityPatch|mises à jour de sécurité]] régulières aux serveurs et clients pour patcher les vulnérabilités connues.
*   Désactiver toutes les versions de [[SecureSocketLayer|SSL]] (SSLv2, SSLv3) et les versions obsolètes de [[TransportLayerSecurity|TLS]] sur les serveurs.
*   Utiliser des suites de chiffrement fortes et modernes.

## 🔗 Notes Connexes
*   [[TransportLayerSecurity|Transport Layer Security (TLS)]]
*   [[HypertextTransferProtocolSecure|HTTPS]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[PublicKeyPair|Paire de Clés Publique/Privée]]
*   [[Encryption|Chiffrement]]
