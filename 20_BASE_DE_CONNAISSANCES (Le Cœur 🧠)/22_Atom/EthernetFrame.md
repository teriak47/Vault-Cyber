---
tags:
  - trame/ethertype
  - trame/verification-erreur
  - securite/port-reseau
  - ethernet
  - couche/liaison-donnees
  - protocole/format-trame
aliases:
  - Trame Ethernet
  - Ethernet Frame
source:
  - null
cssclasses:
  - max
---

# Trame Ethernet

## 📥 Définition en une phrase
> Une trame Ethernet est l'unité de données fondamentale encapsulée et transmise sur un réseau [[Ethernet|Ethernet]], opérant au niveau de la [[DataLinkLayer|couche liaison de données]] (couche 2 du modèle OSI).

## 🧠 Concepts Clés / Fonctionnement
*   **Structure Standard**: Une trame Ethernet typique inclut un préambule, un délimiteur de début de trame (SFD), les adresses [[MediaAccessControlAddress|MAC]] de destination et de source, un champ EtherType ou Longueur, le champ de données (payload) et une séquence de vérification de trame (FCS).
*   **Adresses MAC**: Les champs d'adresse MAC de destination et de source identifient de manière unique les interfaces réseau impliquées dans la communication locale, permettant la livraison de la trame au bon appareil sur le même segment réseau.
*   **EtherType**: Ce champ de 2 octets indique le protocole de couche supérieure encapsulé dans le champ de données de la trame (par exemple, [[InternetProtocol|IP]], [[AddressResolutionProtocol|ARP]], [[InternetworkPacketExchange|IPX]]).
*   **Charge Utile (Payload)**: Contient les données réelles des protocoles de couche supérieure, comme un paquet [[InternetProtocol|IP]] ou un segment [[TransmissionControlProtocol|TCP]], avec une taille variable (généralement entre 46 et 1500 octets pour Ethernet II).
*   **Séquence de Vérification de Trame (FCS)**: Un code de vérification d'erreur (CRC) de 32 bits utilisé par les récepteurs pour détecter les erreurs de transmission dans la trame.

---

## 💾 Structure de la Trame Ethernet : L'Essentiel

La trame Ethernet est l'unité de données de base qui circule sur un réseau. Elle s'organise en plusieurs champs essentiels pour l'acheminement et l'intégrité des données :
![[Pasted image 20251112223838.png|1000]]
### 1. En-tête de Démarrage (Délimitation)
- **Preamble (7 bytes) & SFD (1 byte) :** Servent à la **synchronisation** des horloges entre les équipements et marquent le **début effectif** de la trame.
### 2. Adressage
- **Destination MAC Address (6 bytes) :** Adresse physique du **destinataire**.
- **Source MAC Address (6 bytes) :** Adresse physique de l'**émetteur**.
### 3. Contrôle
- **Type/Length (2 bytes) :** Indique soit la **longueur** des données, soit le **protocole de couche supérieure** encapsulé (l'**EtherType**, ex. : IP, ARP).
### 4. Charge Utile
- **IP Packet Data or Data :** Contient les **données utiles** (paquet IP, ARP, etc.).
### 5. Vérification d'Erreur
- **FCS (Frame Check Sequence) - 4 bytes :** Contient le code **CRC-32**, utilisé par le récepteur pour **vérifier l'intégrité** de la trame.

**Contraintes de Taille :** La taille totale de la trame (adresses jusqu'au FCS) est comprise entre **64 bytes (Minimum)** et **1518 bytes (Maximum)**.

---
## 🛡️ Risques / Menaces Associés
*   [[PacketSniffing|Reniflage de paquets]] : Les trames peuvent être interceptées et analysées, exposant des données non chiffrées.
*   [[MACSpoofing|Usurpation d'adresse MAC]] : Un attaquant peut modifier l'adresse MAC de sa carte réseau pour se faire passer pour un autre appareil.
*   [[ManInTheMiddle|Man-in-the-Middle]] (MITM) : Des techniques comme le [[AddressResolutionProtocolPoisoning|empoisonnement ARP]] manipulent les adresses MAC pour rediriger le trafic.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation réseau]] : Limite la portée de la diffusion des trames et des attaques potentielles.
*   [[PortSecurity|Sécurité des ports]] : Configure les commutateurs pour restreindre les adresses MAC autorisées sur chaque port, empêchant l'usurpation.
*   [[DataEncryption|Chiffrement des données]] : Utiliser des protocoles de chiffrement pour protéger le contenu de la charge utile de la trame (par exemple, HTTPS, VPNs).
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) : Surveiller le trafic de trames pour détecter des anomalies ou des activités malveillantes.

## 🔗 Notes Connexes
*   [[Ethernet|Ethernet]]
*   [[MediaAccessControlAddress|Adresse MAC]]
*   [[DataLinkLayer|Couche Liaison de Données]]
*   [[AddressResolutionProtocol|ARP]]
*   [[InternetProtocol|IP]]
*   [[TransmissionControlProtocol|TCP]]