---
tags:
  - protocole
  - protocole/ssl
  - cryptographie/chiffrement
aliases:
  - SSL
  - Secure Socket Layer
archetype: protocole
port_defaut: 443
couche_osi:
  - Présentation (Couche 6)
rfc:
  - RFC 6101 (SSL 3.0)
  - RFC 2246 (TLS 1.0, successeur de SSL)
cssclasses:
  - max
---

# Secure Socket Layer

> [!info] Carte d'Identité
> *   **Couche OSI** : Présentation (Couche 6). SSL/TLS opère entre la [[TransportLayer|couche Transport]] et la [[ApplicationLayer|couche Application]].
> *   **Port par défaut** : `TCP 443` (pour HTTPS)
> *   **Transport** : [[TransmissionControlProtocol|TCP]]

## ⚙️ Fonctionnement (Handshake)
Le [[Protocol|protocole]] Secure Socket Layer (SSL) établit une session sécurisée entre un [[Client]] et un [[Server]] en utilisant un processus de négociation appelé "handshake" afin d'échanger des clés de [[Encryption|chiffrement]] et d'authentifier les parties.

## 📦 Structure du Paquet (Record Protocol Header)
Le [[Protocol|protocole]] SSL/TLS est une suite de protocoles. Le protocole d'enregistrement (Record Protocol) est la couche inférieure qui transporte les [[Data|données]] d'application et les messages des autres protocoles SSL/TLS (Handshake, Change Cipher Spec, Alert).

| Champ | Taille | Description |
|---|---|---|
| **Type de Contenu** | 1 octet | Indique le type de message contenu dans l'enregistrement (par exemple, handshake, alerte, données d'application). |
| **Version** | 2 octets | Spécifie la version du protocole SSL ou TLS utilisé (par exemple, SSL 3.0, TLS 1.2). |
| **Longueur** | 2 octets | La longueur en octets des données chiffrées (ou non chiffrées avant chiffrement) qui suivent cet en-tête. |

## 🦈 Analyse Wireshark
> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole SSL/TLS
> ssl
> tls
>
> # Filtrer les messages d'alerte TLS
> tls.alert_message
>
> # Filtrer le handshake TLS
> tls.handshake
> ```

## 🛡️ Sécurité
Le [[Protocol|protocole]] SSL, en particulier les versions antérieures (SSL 2.0 et SSL 3.0), présente plusieurs [[Vulnerability|vulnérabilités]] connues et est aujourd'hui considéré comme obsolète et non sécurisé. Il a été remplacé par le [[Protocol|protocole]] [[TransportLayerSecurity|TLS]] (Transport Layer Security), qui offre des fonctionnalités de [[Security|sécurité]] améliorées et une meilleure performance.

> [!danger] Vulnérabilités Connues
> *   **Sniffing** : Bien que SSL vise à chiffrer les communications, des failles dans les anciennes versions (comme SSL 3.0 avec l'attaque POODLE) peuvent permettre à un [[ThreatActor|attaquant]] d'accéder au [[Cleartext|texte clair]] dans certaines conditions.
> *   **Spoofing** : Une authentification serveur via [[DigitalCertificate|certificat numérique]] est standard, mais la falsification de certificats (par exemple, par le biais d'une autorité de certification compromise) ou des attaques [[ManInTheMiddle|Homme du Milieu]] peuvent permettre l'usurpation d'identité.
> *   **Attaques par "Padding Oracle"** : Des faiblesses dans les modes de [[Encryption|chiffrement]] (comme CBC) peuvent être exploitées (par exemple, BEAST, Lucky 13, CRIME).
> *   **Vulnérabilité Heartbleed** : Une [[Vulnerability|faille]] grave dans la bibliothèque OpenSSL a permis aux [[ThreatActor|attaquants]] de lire des [[SensitiveData|données sensibles]] de la mémoire des [[Server|serveurs]] exécutant des versions [[Vulnerability|vulnérables]] d'OpenSSL, incluant les clés de [[Encryption|chiffrement]] et les [[Credential|identifiants]].
> *   **Versions obsolètes** : L'utilisation de protocoles SSL 2.0 et SSL 3.0 est fortement déconseillée en raison de leurs nombreuses faiblesses de [[Security|sécurité]].

## 🔗 Notes Connexes
*   **Version Sécurisée** : [[TransportLayerSecurity|TLS]] (Transport Layer Security)
*   **Implémentation** : [[HypertextTransferProtocolSecure]], [[FileTransferProtocolSecure]]
