---
tags:
  - non-routable
  - adressage/plages-reservees
  - ipv6/ula
  - adressage/adresses-privees
  - reseau/reseau-local
  - reseau/traduction-adresses
aliases:
  - Adresse IP Privée
  - Private IP Address
source:
  - null
cssclasses:
  - max
---

# Adresse IP Privée

## 📥 Définition en une phrase
> Une adresse IP privée est une adresse [[InternetProtocolAddress|IP]] réservée pour être utilisée au sein d'un [[LocalAreaNetwork|réseau local]] (LAN), non routable directement sur l'[[Internet|Internet]] public et distincte des [[PublicIPAddress|adresses IP publiques]].

## 🧠 Concepts Clés / Fonctionnement
*   **Non-Routable sur Internet** : Les paquets avec des adresses IP privées ne sont pas acheminés par les routeurs de l'Internet public, offrant ainsi une couche d'isolation.
*   **Réutilisation d'Adresses** : Les mêmes plages d'adresses IP privées peuvent être utilisées simultanément dans d'innombrables réseaux privés différents sans conflit global.
*   **Plages Réservées (IPv4)** :
    *   `10.0.0.0` à `10.255.255.255` (bloc /8) | 255.0.0.0
    *   `172.16.0.0` à `172.31.255.255` (bloc /12) | 255.255.0.0
    *   `192.168.0.0` à `192.168.255.255` (bloc /16) | 255.255.255.0
*   **Plages Réservées (IPv6)** : Principalement les [[UniqueLocalAddress|ULA]] (`fc00::/7`) et les [[LinkLocalAddress|adresses Link-Local]] (`fe80::/10`) pour la communication au sein du même segment de réseau.
*   **Communication Externe** : Pour qu'un appareil avec une adresse IP privée puisse communiquer avec l'[[Internet|Internet]], il doit passer par un processus de [[NetworkAddressTranslation|Traduction d'Adresses Réseau]] (NAT), généralement effectué par un routeur ou un [[Firewall|pare-feu]].

## 🛡️ Risques / Menaces Associés
*   **Menaces Internes** : Bien que non directement exposées aux [[ExternalThreat|attaques externes]], les adresses IP privées sont la cible de [[InsiderThreat|menaces internes]] ou d'attaques une fois le périmètre compromis.
*   **Mauvaise Configuration NAT** : Une configuration incorrecte du [[NetworkAddressTranslation|NAT]] peut exposer des services internes à l'Internet public, créant ainsi des [[Vulnerability|vulnérabilités]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkSegmentation|Segmentation Réseau]]** : Utiliser des [[VirtualLocalAreaNetwork|VLANs]] et des sous-réseaux pour isoler différents groupes d'appareils, même au sein du réseau privé.
*   **[[Firewall|Règles de Pare-feu]]** : Mettre en place des règles strictes sur le [[Firewall|pare-feu]] pour contrôler le trafic entre les segments privés et vers l'extérieur.
*   **[[NetworkConfigurationManagement|Audit de Configuration Réseau]]** : Examiner régulièrement les configurations réseau pour s'assurer qu'aucune [[InadvertentExposure|exposition involontaire]] n'existe et que les plages privées sont correctement utilisées.

## 🔗 Notes Connexes
*   [[PublicIPAddress|Adresse IP Publique]]
*   [[NetworkAddressTranslation|NAT]]
*   [[LocalAreaNetwork|Réseau Local]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[Subnetting|Sous-réseautage]]