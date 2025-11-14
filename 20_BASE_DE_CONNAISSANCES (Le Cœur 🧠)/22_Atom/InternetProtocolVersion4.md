---
tags:
  - adressage/cidr
  - paquets/fragmentation
  - ipv4
  - reseau/adressage
aliases:
  - IPv4
  - Internet Protocol version 4
  - Protocole Internet version 4
source:
  - 
cssclasses:
  - max
---

# Protocole Internet version 4 (IPv4)

## 📥 Définition en une phrase
> L'IPv4 est la quatrième version du [[InternetProtocol|Protocole Internet]], utilisée pour l'identification des appareils sur un réseau et le routage du trafic de données à travers Internet à l'aide d'adresses 32-bit.

## 🧠 Concepts Clés / Fonctionnement
*   **Adresses 32-bit** : Chaque appareil connecté à un réseau IPv4 possède une adresse unique de 32 bits, généralement représentée sous forme décimale pointée (ex: 192.168.1.1).
*   **Classes d'adresses** : Historiquement, les adresses IPv4 étaient divisées en classes (A, B, C, D, E) pour organiser les réseaux en fonction de leur taille.
*   **[[SubnetMask|Masque de sous-réseau]]** : Utilisé pour diviser une adresse IP en deux parties : l'ID réseau et l'ID hôte, permettant la segmentation des réseaux.
*   **[[Routing|Routage]]** : Les routeurs utilisent l'ID réseau pour déterminer la meilleure voie pour acheminer les paquets de données vers leur destination.
*   **Fragmentations des paquets** : L'IPv4 peut fragmenter les paquets de données trop grands pour être transmis sur un segment de réseau donné, puis les réassembler à destination.
*   **[[ClasslessInterDomainRouting|CIDR]]** : Introduit pour remplacer le système de classes et améliorer l'efficacité de l'allocation des adresses IP, en utilisant des préfixes de longueur variable.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS)]] : Des attaques comme les SYN floods ou les ICMP floods peuvent cibler des vulnérabilités dans le protocole IPv4 pour submerger un système ou un réseau.
*   [[IPSpoofing|Usurpation d'adresse IP]] : Des attaquants peuvent falsifier leur adresse IP source pour masquer leur identité ou contourner des contrôles d'accès basés sur l'IP.
*   [[ManInTheMiddle|Attaques de l'homme du milieu (MitM)]] : Bien que non directement liées à IPv4 lui-même, des vulnérabilités au niveau de l'[[AddressResolutionProtocol|ARP]] (comme l'ARP spoofing) peuvent être exploitées pour des attaques MitM dans les réseaux IPv4 locaux.
*   Pénurie d'adresses : Le nombre limité d'adresses 32-bit a conduit à la pénurie d'adresses IPv4 disponibles, poussant à l'adoption d'[[InternetProtocolVersion6|IPv6]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Pare-feu]] : Déployer des pare-feu pour filtrer le trafic, bloquer les adresses IP malveillantes et empêcher les attaques par déni de service.
*   [[NetworkAddressTranslation|NAT]] : Utiliser le NAT pour masquer les adresses IP internes d'un réseau derrière une seule adresse IP publique, économisant des adresses et ajoutant une couche de sécurité.
*   [[AccessControlList|Listes de contrôle d'accès (ACLs)]] : Configurer des ACLs sur les routeurs et les commutateurs pour restreindre le trafic basé sur les adresses IP sources et destinations.
*   Filtrage d'adresses IP : Mettre en œuvre des filtres pour bloquer le trafic provenant d'adresses IP suspectes ou malveillantes.
*   [[InternetProtocolSecurity|IPsec]] : Utiliser le protocole IPsec pour sécuriser les communications IP via le chiffrement et l'authentification, bien que plus courant avec IPv6, il peut être utilisé avec IPv4.

## 🔗 Notes Connexes
*   [[InternetProtocolVersion6|IPv6]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetControlMessageProtocol|ICMP]]
*   [[Subnetting|Sous-réseautage]]