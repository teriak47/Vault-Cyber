---
tags:
  - protocole/sans-connexion
  - securite/ipsec
  - ip
  - modele/couche-reseau
aliases:
  - Protocole Internet
  - IP
  - Internet Protocol
cssclasses:
  - max
---

# Protocole Internet (IP)

## 📥 Définition en une phrase
> L'Internet Protocol (IP) est le principal protocole de la couche réseau de la suite de protocoles Internet, responsable de l'adressage et du routage des paquets de données entre les hôtes sur un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Adresses IP**: Chaque appareil connecté à un réseau IP reçoit une adresse unique (par exemple, [[InternetProtocolVersion4|IPv4]] ou [[InternetProtocolVersion6|IPv6]]) qui sert d'identifiant pour la communication.
*   **Routage**: Les paquets de données sont acheminés à travers le réseau via des routeurs qui examinent l'adresse IP de destination et transfèrent le paquet vers le chemin le plus approprié.
*   **Encapsulation**: Les données sont encapsulées dans des paquets IP, incluant un en-tête IP contenant des informations telles que les adresses source et destination, la version du protocole, et le type de service.
*   **Sans connexion (Stateless)**: IP est un [[Protocols|protocole]] sans connexion, ce qui signifie qu'il ne maintient pas d'état sur les communications précédentes ou futures entre les hôtes. Chaque paquet est traité indépendamment.
*   **Fragmentations**: Les paquets IP peuvent être fragmentés en unités plus petites (fragments) s'ils sont trop grands pour être transmis sur un segment de réseau donné, puis réassemblés à destination.

## 🛡️ Risques / Menaces Associés
*   [[IPSpoofing|Usurpation d'IP]]: Un attaquant falsifie l'adresse IP source d'un paquet pour se faire passer pour un autre hôte.
*   [[DenialOfService|Attaques par déni de service (DoS)]]: L'utilisation abusive de paquets IP pour saturer une cible et rendre ses services inaccessibles.
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]]: Peut intercepter et modifier des paquets IP en transit, souvent via des techniques d'usurpation d'identité.
*   [[InformationDisclosure|Fuite d'informations]]: Les en-têtes IP peuvent révéler des informations sur la topologie du réseau ou les systèmes d'exploitation.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Filtrage par [[Firewall|Pare-feu]]**: Configurer des règles de pare-feu pour autoriser ou bloquer le trafic IP basé sur les adresses source/destination, les ports et les protocoles.
*   **[[NetworkSegmentation|Segmentation réseau]]**: Isoler les différentes parties d'un réseau pour limiter la propagation des attaques et réduire la surface d'attaque.
*   **Utilisation d'[[InternetProtocolSecurity|IPsec]]**: Protocole de sécurité qui offre l'authentification et le chiffrement des paquets IP, protégeant ainsi l'intégrité et la confidentialité des communications.
*   **Détection d'[[IntrusionDetectionSystem|Intrusion (IDS)]] / [[IntrusionPreventionSystem|Prévention (IPS)]]**: Surveiller le trafic IP pour détecter et potentiellement bloquer les activités malveillantes ou suspectes.
*   **Validation des paquets**: Mettre en œuvre des mécanismes pour vérifier la validité des adresses IP source des paquets entrants afin de contrer l'usurpation d'IP.

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[NetworkLayer|Couche Réseau]]