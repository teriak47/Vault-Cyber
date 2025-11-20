---
tags:
  - protocole
  - reseau
  - adressage
aliases:
  - Protocole Internet
  - IP
  - Internet Protocol
  - Protocole IP
archetype: protocole
rfc:
cssclasses:
  - max
---

# Protocole Internet (IP)

## 🎯 Rôle et Couche OSI
> Le Protocole Internet (IP) est le principal protocole de la couche réseau (couche 3 du modèle OSI et couche Internet du modèle TCP/IP) au sein de la suite de protocoles Internet. Il est responsable de l'adressage logique et du routage des paquets de données entre les hôtes et les réseaux interconnectés.

## ⚙️ Fonctionnement
1.  **Adressage IP**: Chaque appareil connecté à un réseau IP se voit attribuer une adresse IPunique (IPv4 ou IPv6). Cette adresse IPsert d'identifiant logique pour la communication au sein du réseau et au-delà.
2.  **Routage**: Les paquets de données sont acheminés à travers le réseau grâce à des routeurs. Les routeurs examinent l'adresse IP de destination contenue dans l'en-tête IP du paquet et utilisent leurs tables de routage pour déterminer le chemin le plus efficace vers la destination.
3.  **Encapsulation**: Les données des couches supérieures sont encapsulées dans des paquets IP. Chaque paquet IP comprend un en-tête qui contient des informations essentielles telles que les adresses IP source et destination, la version du protocole (IPv4 ou IPv6), le temps de vie (TTL) et le type de service.
4.  **Sans connexion (Stateless)**: IP est un protocole "sans connexion" (stateless). Cela signifie qu'il ne maintient pas d'état ni de connexion continue entre l'émetteur et le récepteur. Chaque paquet est traité indépendamment, ce qui rend le réseau flexible mais nécessite des protocoles de couches supérieures (comme TCP) pour la fiabilité.
5.  **Fragmentation**: Si un paquet IP est trop grand pour être transmis sur un segment de réseau spécifique (dépassant le MTU - Maximum Transmission Unit), il peut être fragmenté en unités plus petites. Ces fragments sont ensuite réassemblés à la destination.
* **Ports par défaut**: Le Protocole Internet (IP) n'utilise pas de ports dans le sens des protocoles de transport comme TCP ou UDP. Son rôle est de fournir l'adressage logique et le routage entre les hôtes.

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * Usurpation d'IP: Un attaquant falsifie l'adresse IP source d'un paquet pour masquer son identité ou se faire passer pour un autre hôte.
  * Attaques par déni de service (DoS) / DDoS: Utilisation abusive de paquets IP pour submerger une cible, rendant ses services inaccessibles.
  * Attaques de l'homme du milieu (MitM): Bien que non directement une vulnérabilité IP, de nombreuses attaques MitM manipulent le routage ou l'adressage IP (ex: ARP Poisoning) pour intercepter et potentiellement modifier les paquets IP en transit.
  * Fuite d'informations: Les en-têtes IP peuvent révéler des informations sur la topologie du réseau ou les systèmes d'exploitation utilisés.
* **Mesures de protection**:
  * Filtrage par pare-feu: Configuration de pare-feu pour contrôler le trafic IP en fonction des adresses IPsource/destination, des ports et des protocoles de couche supérieure.
  * Segmentation réseau: Isolation des différentes parties d'un réseau pour limiter la propagation d'attaques et réduire la surface d'attaque.
  * IPsec: Une suite de protocoles qui offre l'authentification et le chiffrement des paquets IP, protégeant l'intégrité et la confidentialité des communications.
  * Systèmes de détection d'intrusion (IDS) / Prévention d'intrusion (IPS): Surveillance continue du trafic IP pour détecter et potentiellement bloquer les activités malveillantes ou suspectes.
  * **Validation des paquets**: Implémentation de mécanismes pour vérifier la validité des adresses IP source des paquets entrants, afin de contrer l'usurpation d'IP.

## 🔗 Notes Connexes
* TCP
* UDP
* IPv4
* IPv6
* Couche Réseau
* Outil d'analyse de protocoles comme Wireshark