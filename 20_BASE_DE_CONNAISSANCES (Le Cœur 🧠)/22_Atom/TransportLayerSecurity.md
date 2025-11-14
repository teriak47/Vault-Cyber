---
tags:
  - protocole/tls
  - cyberattaque/retrogradation
  - securite/configuration-tls
  - protocole
  - chiffrement
  - cyberattaque/homme-du-milieu
aliases:
  - Sécurité de la Couche de Transport
  - TLS
  - Transport Layer Security
source:
  - null
cssclasses:
  - max
---

# Transport Layer Security (TLS)

## 📥 Définition en une phrase
> Le Transport Layer Security (TLS) est un [[Protocols|protocole]] cryptographique conçu pour assurer la sécurité des communications sur un réseau informatique en fournissant la confidentialité, l'intégrité des données et l'authentification des entités communicantes.

## 🧠 Concepts Clés / Fonctionnement
*   **Chiffrement de bout en bout**: TLS établit un canal de communication chiffré entre le client (ex: navigateur web) et le serveur, protégeant les données des écoutes indésirables.
*   **Authentification**: Utilise des [[DigitalCertificate|certificats numériques]] (basés sur l'infrastructure à [[PublicKeyInfrastructure|clés publiques (PKI)]]) pour vérifier l'identité du serveur (et optionnellement du client), empêchant l'[[ManInTheMiddle|usurpation d'identité]].
*   **Intégrité des données**: Garantit que les données échangées n'ont pas été altérées ou falsifiées pendant le transit grâce à des codes d'authentification de message (MAC).
*   **Négociation de la suite de chiffrement**: Lors de la poignée de main ([[TLSHandshake|TLS Handshake]]), le client et le serveur s'accordent sur les algorithmes cryptographiques et les clés à utiliser pour la session sécurisée.
*   **Évolution de [[SecureSocketsLayer|SSL]]**: TLS est la norme successeur du protocole Secure Sockets Layer (SSL), apportant des améliorations de sécurité significatives.

## 🛡️ Risques / Menaces Associés
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MITM)]]: Si l'authentification échoue ou est compromise, un attaquant peut intercepter et potentiellement modifier la communication.
*   **Vulnérabilités dans les implémentations TLS**: Des failles logicielles dans les bibliothèques ou serveurs TLS peuvent être exploitées (ex: Heartbleed, FREAK).
*   [[DowngradeAttack|Attaques de rétrogradation]]: Un attaquant force l'utilisation de versions plus anciennes et moins sécurisées de TLS/SSL.
*   **Certificats faibles ou compromis**: L'utilisation de [[SelfSignedCertificate|certificats auto-signés]] non vérifiés ou la compromission d'une [[CertificateAuthority|Autorité de Certification (CA)]] peut miner la confiance.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Utilisation de TLS 1.2 ou supérieur**: Toujours privilégier les versions récentes de TLS (actuellement TLS 1.2 ou [[TLS13|TLS 1.3]]) et désactiver les versions obsolètes comme SSLv3 ou TLS 1.0/1.1.
*   **Configuration de suites de chiffrement robustes**: Choisir des algorithmes de chiffrement forts, de grandes tailles de clés et un échange de clés [[PerfectForwardSecrecy|PFS (Perfect Forward Secrecy)]].
*   **Gestion rigoureuse des certificats**: Utiliser des certificats émis par des CA de confiance, les renouveler à temps et protéger les clés privées.
*   **Implémentation HSTS ([[HTTPStrictTransportSecurity|HTTP Strict Transport Security]])**: Force les navigateurs à utiliser TLS pour toutes les connexions au domaine.
*   [[SecurityAudit|Audits de sécurité]] réguliers: Vérifier la configuration TLS des serveurs et applications.

## 🔗 Notes Connexes
*   [[SecureSocketsLayer|Secure Sockets Layer (SSL)]]
*   [[Cryptography|Cryptographie]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[PublicKeyInfrastructure|Infrastructure à Clés Publiques (PKI)]]
*   [[TLSHandshake|Poignée de main TLS]]