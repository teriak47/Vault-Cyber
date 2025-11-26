---
aliases:
  - "Data Over Cable Service Interface Specification"
  - "EuroDOCSIS"
  - "DOCSIS 1.0"
  - "DOCSIS 1.1"
  - "DOCSIS 2.0"
  - "DOCSIS 3.0"
  - "DOCSIS 3.1"
  - "DOCSIS 4.0"
archetype: protocole
port_defaut: N/A
couche_osi:
  - "Couche 1 - Physique"
  - "Couche 2 - Liaison"
rfc:
  - "RFC 4036"
  - "RFC 3256"
  - "RFC 4323"
  - "RFC 4131"
cssclasses:
  - max
tags:
  - norme/docsis
  - telecommunications
  - reseau/cable
  - reseau/infrastructure/fibre-optique
  - internet/acces
  - debit
  - materiel/reseau/modem
  - modele-osi/couche-1
  - modele-osi/couche-2
  - protocole/dhcp
  - protocole/tftp
  - securite
  - chiffrement
  - authentification
  - qos
  - protocole/ip/ipv6
  - protocole/ethernet
  - application/voip
  - tdma
  - s-cdma
  - ofdma
  - ofdm
  - docsis/channel-bonding
  - docsis/full-duplex
  - docsis/extended-spectrum
---

# DOCSIS

> [!info] Carte d'Identité
> * **Couche OSI** : Couche 1 - Physique, Couche 2 - Liaison
> * **Port par défaut** : `N/A`
> * **Transport** : N/A (Opère aux couches inférieures)

Le standard **DOCSIS** (Data Over Cable Service Interface Specification) est une norme de télécommunication internationale qui permet l'ajout de transfert de données à haut débit aux systèmes de télévision par câble (CATV) existants. Développé par CableLabs en 1997, il est utilisé par les opérateurs de télévision par câble pour fournir un accès Internet haut débit via leur infrastructure hybride fibre-coaxiale (HFC) existante.

## ⚙️ Fonctionnement

Le fonctionnement de DOCSIS repose sur l'interaction entre deux composants principaux : le **modem câble (CM)**, situé chez l'abonné, et le **système de terminaison de modem câble (CMTS)**, situé au niveau de la tête de réseau de l'opérateur. DOCSIS gère la manière dont les données sont transmises sur le réseau HFC, supportant un flux bidirectionnel de données IP (paquets Internet Protocol) entre le CM et le CMTS.

Le processus d'initialisation et de fonctionnement d'un modem câble est une séquence d'événements coordonnée par la couche MAC du CMTS :

1.  **Balayage et Acquisition de Canal Downstream** : Le modem câble recherche un canal descendant (du CMTS vers le CM) valide pour établir la communication. Ce canal transporte des données, de la vidéo, et des informations de contrôle.
2.  **Ranging (Étalonnage)** : Le CMTS mesure le délai de propagation des signaux entre le modem câble et lui-même. Cela permet de synchroniser les modems sur le canal montant (du CM vers le CMTS) partagé, en allouant des mini-slots de temps de transmission à chaque modem pour éviter les collisions.
3.  **Attribution d'Adresse IP (DHCP)** : Une fois le modem en ligne, il obtient une adresse IP via DHCP, ainsi que l'adresse du serveur TFTP et le nom du fichier de configuration DOCSIS.
4.  **Téléchargement du Fichier de Configuration (TFTP)** : Le modem télécharge un fichier de configuration spécifique depuis le serveur TFTP de l'opérateur. Ce fichier contient des paramètres essentiels comme la vitesse de liaison montante et descendante, les services activés (QoS), et les informations de sécurité.
5.  **Authentification et Sécurité (BPI/SEC)** : Le modem s'authentifie auprès du CMTS et établit des clés de chiffrement pour sécuriser les communications (voir section "Sécurité").
6.  **Enregistrement** : Le modem s'enregistre auprès du CMTS pour indiquer qu'il est pleinement opérationnel.

Le standard DOCSIS emploie des méthodes d'accès déterministes pour les transmissions montantes, comme le **TDMA** (Time-Division Multiple Access) pour les premières versions, et le **S-CDMA** (Synchronous Code-Division Multiple Access) pour DOCSIS 2.0 et 3.0, avec une utilisation limitée de la contention pour les requêtes de réservation de bande passante.

Les **versions majeures** de DOCSIS et leurs évolutions clés incluent :
*   **DOCSIS 1.0 (1997)** : Version initiale, bande passante de 40 Mbps en descendant et 10 Mbps en montant.
*   **DOCSIS 1.1 (1999)** : Standardisation des mécanismes de qualité de service (**QoS**) et ajout des capacités VoIP.
*   **DOCSIS 2.0 (2001)** : Amélioration significative des débits de données en amont (jusqu'à 30 Mbps) pour supporter des services plus symétriques.
*   **DOCSIS 3.0 (2006)** : Introduction du **channel bonding** (agrégation de canaux) pour des débits de plusieurs centaines de Mbps à 1 Gbps, support d'IPv6 et chiffrement AES.
*   **DOCSIS 3.1 (2013)** : Utilisation de l'**OFDM** (Orthogonal Frequency-Division Multiplexing) et **OFDMA** pour les débits montants, permettant jusqu'à 10 Gbit/s en descendant et 1 Gbit/s en montant, avec une efficacité spectrale accrue.
*   **DOCSIS 4.0 (2020)** : Introduit le **Full Duplex DOCSIS (FDX)** et l'**Extended Spectrum DOCSIS (ESD)** pour des services multi-gigabit symétriques (jusqu'à 10 Gbit/s en descendant et 6 Gbit/s en montant) sur l'intégralité du spectre du réseau câblé.

```mermaid
graph TD
    CM[Cable Modem] -->|1. Recherche Downstream| CMTS[CMTS (Tête de réseau)]
    CMTS -->|2. Ranging/Attribution de temps Upstream| CM
    CM -->|3. Requête DHCP| CMTS
    CMTS -->|4. Réponse DHCP (IP, TFTP server, config file)| CM
    CM -->|5. Téléchargement Config (TFTP)| CMTS
    CM -->|6. Authentification & Clés de Chiffrement| CMTS
    CM -->|7. Enregistrement| CMTS
    CM -- Trafic de données --> CMTS
```

## 📦 Structure du Paquet (Header)

La structure des paquets DOCSIS n'est pas comparable à un en-tête de protocole de couche 3 ou 4 tel que TCP ou IP. DOCSIS définit les spécifications des couches physique et liaison de données pour le transfert de données sur le réseau câblé.

*   **Encapsulation**: DOCSIS encapsule des trames Ethernet (contenant généralement des paquets IP) pour les transporter sur le réseau HFC.
*   **Flux Downstream (Descendant)**: Les données sont transportées dans un flux continu de paquets de transport MPEG-2. Pour distinguer les données DOCSIS de la vidéo, les trames DOCSIS utilisent une valeur spécifique dans l'en-tête MPEG (par exemple, un PID de `0x1FFE`). Ces trames MPEG ont une taille fixe (généralement 188 octets).
*   **Flux Upstream (Montant)**: Les données sont organisées en "mini-slots". Le CMTS alloue ces mini-slots aux modems câbles pour leurs transmissions, gérant ainsi l'accès partagé au canal montant. La couche MAC est cruciale pour allouer la bande passante et gérer les demandes de transmission.

En essence, le protocole DOCSIS se situe principalement aux couches 1 et 2 du modèle OSI, agissant comme un pont de couche 2 entre le réseau local du client et le réseau HFC, et il définit des mécanismes d'accès au support physique plutôt que des en-têtes de paquets classiques de couche réseau ou transport.

## 🦈 Analyse Wireshark
L'analyse des flux DOCSIS avec Wireshark peut être complexe en raison de l'encapsulation spécifique et du chiffrement.

> [!tip] Filtres Utiles
> ```
> # Filtrer par protocole DOCSIS (si les décodeurs Wireshark sont présents)
> docsis
>
> # Filtrer le trafic DHCP (souvent visible pendant l'initialisation du modem)
> bootp
>
> # Filtrer le trafic TFTP (pour les fichiers de configuration)
> tftp
> ```
Il est important de noter que le trafic entre le modem câble et le CMTS est généralement chiffré, rendant le "sniffing" passif de données utilisateur difficile sans accès aux clés de chiffrement.

## 🛡️ Sécurité

DOCSIS intègre des services de sécurité au niveau de la couche MAC pour protéger la vie privée des utilisateurs et l'intégrité du réseau.

> [!danger] Vulnérabilités Connues
> *   **Sniffing** : Le réseau câblé étant un support partagé, il existe un risque inhérent d'interception de données. Pour y remédier, DOCSIS utilise le **Baseline Privacy Interface (BPI)** et sa version améliorée, **BPI+**, qui a ensuite évolué vers la spécification **"Security" (SEC)** dans DOCSIS 3.0. Ces spécifications décrivent les services de sécurité de la couche MAC, y compris le chiffrement des données entre le CMTS et le modem câble, utilisant DES 56 bits dans les premières versions, puis AES. Donc, le trafic est chiffré : **Oui**.
> *   **Spoofing / Vol de service** : Une authentification faible ou la manipulation des fichiers de configuration DOCSIS (téléchargés via TFTP) pourrait permettre à un utilisateur malveillant de se provisionner avec plus de bande passante ou d'accéder illégitimement au réseau. Les opérateurs mettent en œuvre des contrôles d'accès sur les CMTS pour restreindre l'accès aux serveurs TFTP et valider les configurations.
> *   **Attaques par déni de service (DoS)** : Les réseaux DOCSIS sont vulnérables aux attaques DoS, qui peuvent perturber la disponibilité du service.
> *   **Vulnérabilités logicielles (ex: Cable Haunt)** : Des vulnérabilités spécifiques aux implémentations logicielles des modems peuvent exister. Par exemple, la vulnérabilité "Cable Haunt" (découverte en 2020) a exploité une faille de dépassement de tampon (buffer overflow) dans les chipsets Broadcom de certains modems DOCSIS, permettant potentiellement des attaques de type "man-in-the-middle", le changement de DNS, ou la modification du firmware. Ces vulnérabilités nécessitent des mises à jour de firmware.