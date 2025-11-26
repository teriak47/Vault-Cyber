---
aliases:
  - Protocole IPsec
  - IPsec Protocol
  - IP Security
  - AH
  - ESP
  - IKE
  - Authentication Header
  - Encapsulating Security Payload
  - Internet Key Exchange
  - IKEv1
  - IKEv2
archetype: protocole
port_defaut: UDP 500, UDP 4500
couche_osi:
  - "Couche 3 - Réseau"
rfc:
  - RFC 2401
  - RFC 2402
  - RFC 2406
  - RFC 2409
  - RFC 4301
  - RFC 4302
  - RFC 4303
  - RFC 4309
  - RFC 6071
cssclasses:
  - max
tags:
  - protocole/vpn/ipsec
  - protocole/ike
  - protocole/ah
  - protocole/esp
  - protocole/ipsec/security-association
  - protocole/ipsec/anti-relecture
  - modele-osi/couche-3
  - reseau
  - authentification
  - integrite
  - confidentialite
  - cryptographie
---

# IPsec Protocol

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 3 - Réseau
> * **Port par défaut** : `UDP 500` (IKE), `UDP 4500` (IKE NAT-T)
> * **Transport** : Directement sur IP (IP Protocol 50 for ESP, 51 for AH)

L'**IPsec** (Internet Protocol Security) est une suite de protocoles et d'extensions qui fournit une sécurité cryptographique pour les communications IP au niveau de la couche réseau. IPsec est conçu pour offrir des services de sécurité robustes pour IPv4 et IPv6.

Les objectifs de sécurité principaux d'IPsec sont :
*   **Authentification** : Vérifier l'identité de l'expéditeur du paquet.
*   **Intégrité** : Garantir que les données n'ont pas été modifiées pendant le transit.
*   **Confidentialité** : Chiffrer les données pour empêcher l'écoute clandestine (uniquement avec ESP).
*   **Protection contre les relectures (Anti-replay)** : Empêcher les attaquants de renvoyer des paquets capturés.

## ⚙️ Fonctionnement (Handshake)

Le fonctionnement d'IPsec repose sur plusieurs composants principaux, dont le protocole **IKE** (Internet Key Exchange) pour l'établissement et la gestion des associations de sécurité (SA - Security Associations). IKE utilise généralement les ports UDP 500 et 4500 (pour NAT-T) pour ses négociations.

Le processus IKE se déroule en deux phases principales :

**Phase 1 : Établissement d'une SA IKE (Main Mode ou Aggressive Mode)**
Cette phase établit un canal de communication sécurisé et authentifié entre les deux pairs IPsec.
1.  **Négociation des politiques IKE** : Les pairs s'accordent sur les algorithmes de chiffrement, de hachage, le groupe Diffie-Hellman et la durée de vie de la SA IKE.
2.  **Échange de clés Diffie-Hellman** : Les pairs échangent des informations pour générer une clé secrète partagée de manière sécurisée.
3.  **Authentification des pairs** : Les pairs s'authentifient mutuellement à l'aide de clés pré-partagées (PSK), de certificats RSA ou de signatures numériques.

**Phase 2 : Établissement des SA IPsec (Quick Mode)**
Une fois le canal sécurisé de la Phase 1 établi, la Phase 2 négocie les SA pour les données réelles.
1.  **Négociation des politiques IPsec** : Les pairs s'accordent sur les algorithmes de chiffrement (pour ESP), d'authentification (pour AH ou ESP) et les modes (tunnel ou transport).
2.  **Échange de clés de session** : De nouvelles clés sont générées pour les SA IPsec à l'aide du canal sécurisé de la Phase 1.
3.  **Échange d'identifiants de trafic** : Les pairs définissent quels flux de trafic seront protégés par les SA nouvellement établies.

```mermaid
sequenceDiagram
    participant Initiator
    participant Responder

    box IKE Phase 1 (SA IKE Establishment - UDP 500)
        Initiator->>Responder: Main Mode Msg 1 (SA Proposal)
        Responder->>Initiator: Main Mode Msg 2 (SA Acceptance + DH Public Value)
        Initiator->>Responder: Main Mode Msg 3 (DH Public Value)
        Responder->>Initiator: Main Mode Msg 4 (ID + Auth)
        Initiator->>Responder: Main Mode Msg 5 (ID + Auth)
        Note right of Responder: Secure IKE Tunnel Established
    end

    box IKE Phase 2 (SA IPsec Establishment - UDP 500 within IKE tunnel)
        Initiator->>Responder: Quick Mode Msg 1 (SA IPsec Proposal + Nonce + Traffic Selectors)
        Responder->>Initiator: Quick Mode Msg 2 (SA IPsec Acceptance + Nonce + Traffic Selectors)
        Initiator->>Responder: Quick Mode Msg 3 (ACK)
        Note right of Responder: IPsec SA for Data Established
    end

    box Data Transfer (AH or ESP)
        Initiator->>Responder: Encapsulated Data (e.g., ESP)
        Responder->>Initiator: Encapsulated Data (e.g., ESP)
    end
```

## 📦 Structure du Paquet (Header)

IPsec utilise deux protocoles principaux pour fournir les services de sécurité : **AH** (Authentication Header) et **ESP** (Encapsulating Security Payload).

### Authentication Header (AH)

Le protocole AH (IP Protocol 51) fournit l'intégrité des données, l'authentification de l'origine des données et la protection anti-relecture. Il ne fournit pas de confidentialité (chiffrement). AH protège la majeure partie du paquet IP, y compris certaines parties de l'en-tête IP qui ne changent pas en transit.

| Champ               | Taille    | Description                                                                                                                                                                                                                                                                 |
| :------------------ | :-------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Next Header**     | 8 bits    | Identifie le protocole suivant dans la charge utile (ex: TCP, UDP).                                                                                                                                                                                           |
| **Payload Length**  | 8 bits    | Longueur de l'en-tête AH en mots de 32 bits, moins 2.                                                                                                                                                                                                             |
| **Reserved**        | 16 bits   | Réservé pour une utilisation future.                                                                                                                                                                                                                             |
| **Security Parameter Index (SPI)** | 32 bits   | Identifie l'Association de Sécurité (SA) spécifique à laquelle ce paquet appartient, permettant au récepteur de trouver les paramètres de sécurité appropriés.                                                                                              |
| **Sequence Number** | 32 bits   | Un compteur qui augmente de manière monotone pour chaque paquet envoyé dans une SA. Utilisé pour la protection anti-relecture. Le premier paquet a un numéro de séquence de 1. |
| **Authentication Data** | Variable | Contient la valeur d'intégrité cryptographique (ICV - Integrity Check Value), calculée sur des champs sélectionnés du paquet IP et de l'en-tête AH. Généralement un HMAC.                                                                                   |

### Encapsulating Security Payload (ESP)

Le protocole ESP (IP Protocol 50) fournit la confidentialité (chiffrement), l'intégrité des données, l'authentification de l'origine des données et la protection anti-relecture. ESP est généralement le protocole préféré car il offre plus de services de sécurité qu'AH.

| Champ                     | Taille     | Description                                                                                                                                                                                                                                                        |
| :------------------------ | :--------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Security Parameter Index (SPI)** | 32 bits    | Identifie l'Association de Sécurité (SA) spécifique.                                                                                                                                                                                            |
| **Sequence Number**       | 32 bits    | Un compteur croissant utilisé pour la protection anti-relecture.                                                                                                                                                                                      |
| **Payload Data**          | Variable   | Les données chiffrées (l'en-tête de la couche supérieure et les données originales du paquet IP).                                                                                                                                                       |
| **Padding**               | 0-255 bytes | Données de remplissage pour se conformer aux exigences des algorithmes de chiffrement par bloc et/ou pour masquer la longueur réelle du message.                                                                                                   |
| **Pad Length**            | 8 bits     | Longueur du champ de remplissage.                                                                                                                                                                                                                       |
| **Next Header**           | 8 bits     | Identifie le type de données chiffrées (ex: TCP, UDP, ICMP).                                                                                                                                                                                              |
| **Authentication Data**   | Variable   | Contient la valeur d'intégrité (ICV) si l'authentification est activée pour ESP.                                                                                                                                                                  |

### Modes de fonctionnement

IPsec peut fonctionner en deux modes :

*   **Mode Transport** : Protège la charge utile du paquet IP. L'en-tête IP original reste intact. Il est généralement utilisé pour la communication de bout en bout entre hôtes.
    *   *AH en mode Transport* : L'en-tête AH est inséré entre l'en-tête IP et l'en-tête de la couche supérieure (TCP/UDP).
    *   *ESP en mode Transport* : L'en-tête ESP est inséré après l'en-tête IP et avant la charge utile de la couche supérieure, qui est chiffrée. L'en-tête IP original n'est pas chiffré.
*   **Mode Tunnel** : Chiffre et/ou authentifie le paquet IP *entier* (en-tête et charge utile) et l'encapsule dans un nouveau paquet IP avec un nouvel en-tête IP. Ce mode est couramment utilisé entre des passerelles de sécurité (ex: pour les VPN site-à-site) ou entre un hôte et une passerelle.
    *   *AH en mode Tunnel* : Le paquet IP original est encapsulé, et le nouvel en-tête IP suivi de l'en-tête AH protège l'ensemble du paquet original.
    *   *ESP en mode Tunnel* : Le paquet IP original est encapsulé et chiffré, puis un nouvel en-tête IP est ajouté.

## 🦈 Analyse Wireshark

> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole IPsec
> ip.proto == 50 or ip.proto == 51
>
> # Filtrer le trafic IKE (Internet Key Exchange)
> isakmp or udp.port == 500 or udp.port == 4500
>
> # Filtrer les paquets ESP (Encapsulating Security Payload)
> esp
>
> # Filtrer les paquets AH (Authentication Header)
> ah
> ```

## 🛡️ Sécurité

IPsec est une pierre angulaire de la sécurité réseau, notamment pour les **VPN** (Virtual Private Networks), car il fournit un cadre robuste pour la sécurisation des communications.

> [!danger] Vulnérabilités Connues
> *   **Sniffing** : Est-ce chiffré ?
>     *   **Non** avec AH seul, car AH ne fournit pas de confidentialité. Les données peuvent être lues.
>     *   **Oui** avec ESP, car ESP chiffre la charge utile, protégeant ainsi la confidentialité des données.
> *   **Spoofing** : L'**authentification** forte (via IKE et AH/ESP) protège contre l'usurpation d'identité et garantit l'origine des données.
> *   **Attaques par relecture** : La protection par numéro de séquence dans AH et ESP est conçue pour atténuer les attaques par relecture en rejetant les paquets dupliqués ou hors séquence.
> *   **Complexité de configuration** : La complexité de la configuration d'IPsec peut introduire des vulnérabilités si elle n'est pas correctement gérée.
> *   **Vulnérabilités dans les algorithmes cryptographiques** : Comme toute solution cryptographique, la sécurité d'IPsec dépend de la force des algorithmes de chiffrement et de hachage utilisés. Des faiblesses découvertes dans ces algorithmes peuvent compromettre la sécurité d'IPsec.
> *   **Attaques par déni de service (DoS)** : Les phases d'échange de clés IKE peuvent être ciblées par des attaques DoS, bien que des mécanismes de protection existent.