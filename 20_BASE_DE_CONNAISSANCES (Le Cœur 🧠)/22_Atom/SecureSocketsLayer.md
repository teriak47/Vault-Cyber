---
tags:
  - obsolescence/protocole-securite
  - cryptographie/poignee-main
  - securite/infrastructure-cles-publiques
  - chiffrement
  - protocole/tls
  - cyberattaque/retrogradation
aliases:
  - SSL
  - Secure Sockets Layer
  - Couche de Sockets Sécurisée
source:
  - null
cssclasses:
  - max
---

# Secure Sockets Layer (SSL)

## 📥 Définition en une phrase
> Le Secure Sockets Layer (SSL) est un [[Protocols|protocole]] de cryptographie obsolète qui fournissait un canal de communication sécurisé sur un réseau informatique, principalement utilisé pour sécuriser les communications [[HyperTextTransferProtocolSecure|HTTPs]] sur Internet, et est le prédécesseur de [[TransportLayerSecurity|TLS]].

## 🧠 Concepts Clés / Fonctionnement
*   **Chiffrement de Données**: SSL utilise la [[Cryptography|cryptographie]] pour chiffrer les données transmises entre un client (ex: navigateur web) et un serveur, garantissant ainsi la confidentialité.
*   **Authentification**: Il permet d'authentifier les parties communicantes (généralement le serveur au client) à l'aide de [[X.509Certificate|certificats numériques X.509]] émis par des [[CertificateAuthority|autorités de certification]] (CA).
*   **Intégrité des Données**: SSL vérifie l'intégrité des données pour s'assurer qu'elles n'ont pas été altérées pendant le transit.
*   **Handshake SSL**: Un processus initial de "poignée de main" est effectué pour établir la connexion sécurisée, négocier les paramètres cryptographiques et échanger les clés de session.
*   **Obsolescence**: Toutes les versions de SSL (SSLv2 et SSLv3) sont considérées comme obsolètes et insécurisées en raison de nombreuses vulnérabilités découvertes. Elles ont été remplacées par [[TransportLayerSecurity|TLS]].

## 🛡️ Risques / Menaces Associés
*   **[[Vulnerability|Vulnérabilités]] Connues**: SSLv2 et SSLv3 sont affectés par des failles majeures comme [[POODLEAttack|POODLE]] (Padding Oracle On Downgraded Legacy Encryption) qui permettent des attaques de type [[ManInTheMiddle|Homme du Milieu]].
*   **Attaques par Rétrogradation (Downgrade Attacks)**: Des attaquants peuvent forcer les connexions à utiliser des versions obsolètes et vulnérables de SSL.
*   **Divulgation d'Informations**: Exploitation des faiblesses cryptographiques pour déchiffrer des communications confidentielles.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Migration vers [[TransportLayerSecurity|TLS]]**: La mesure la plus cruciale est de désactiver toutes les versions de SSL et de migrer vers des versions récentes et sécurisées de [[TransportLayerSecurity|TLS]] (actuellement TLS 1.2 ou TLS 1.3).
*   **Configuration Serveur Robuste**: S'assurer que les serveurs web et autres services sont configurés pour n'accepter que les protocoles TLS modernes et les suites de chiffrement fortes.
*   **Mise à Jour des Logiciels**: Maintenir à jour les systèmes d'exploitation, les serveurs web et les bibliothèques cryptographiques pour bénéficier des correctifs de sécurité.
*   **Utilisation de Certificats Valides**: Déployer des [[X.509Certificate|certificats SSL/TLS]] émis par des [[CertificateAuthority|CA]] de confiance et les renouveler avant leur expiration.

## 🔗 Notes Connexes
*   [[TransportLayerSecurity|TLS]]
*   [[HyperTextTransferProtocolSecure|HTTPS]]
*   [[Cryptography|Cryptographie]]
*   [[X.509Certificate|Certificat X.509]]
*   [[CertificateAuthority|Autorité de Certification]]
*   [[PublicKeyInfrastructure|Infrastructure à Clé Publique (PKI)]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[POODLEAttack|Attaque POODLE]]