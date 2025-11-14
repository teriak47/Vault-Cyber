---
tags:
  - adressage/adresses-privees
  - adressage/attribution-dynamique
  - ip
  - reseau/adressage
aliases:
  - Adresse IP
  - IP
  - Internet Protocol Address
  - IP Address
  - Internet Address
source:
  - 
cssclasses:
  - max
---

# Adresse IP (IP)

## 📥 Définition en une phrase
> Un identifiant numérique unique attribué à chaque appareil connecté à un réseau informatique utilisant l'[[InternetProtocol|Internet Protocol]] pour sa communication et son routage.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification et Routage** : Sert à identifier de manière unique un appareil sur un réseau et permet le routage des paquets de données à travers les réseaux, de la source à la destination.
*   **Versions** : Il existe deux versions principales :
    *   [[InternetProtocolVersion4]] : Utilise 32 bits, généralement représentée par quatre nombres décimaux séparés par des points (ex: `192.168.1.1`).
    *   [[InternetProtocolVersion6]] : Utilise 128 bits, représentée par des blocs hexadécimaux séparés par des deux-points (ex: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
*   **Types d'Adresses** :
    *   **Publiques** : Adresses uniques globalement visibles sur Internet.
    *   **Privées** : Utilisées au sein d'un réseau local (LAN), non routables directement sur Internet. La [[NetworkAddressTranslation|NAT]] est utilisée pour permettre la communication des adresses privées avec l'extérieur.
*   **Attribution** :
    *   **Statique** : Assignée manuellement par un administrateur.
    *   **Dynamique** : Attribuée automatiquement par un serveur [[DynamicHostConfigurationProtocol|DHCP]].

## 🛡️ Risques / Menaces Associés
*   [[DistributedDenialOfService|Attaques par déni de service distribué]] : Si l'adresse IP est publique et exposée, elle peut être la cible d'attaques visant à la saturer.
*   [[IPSpoofing|Usurpation d'adresse IP]] : Falsification de l'adresse IP source d'un paquet pour masquer l'identité ou contourner des contrôles d'accès.
*   [[NetworkScanning|Balayage de réseau]] : Utilisation d'outils pour découvrir les adresses IP actives sur un réseau, en vue d'identifier des services ou des vulnérabilités.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Pare-feu]] : Configuration de règles de pare-feu pour filtrer le trafic basé sur les adresses IP sources et de destination.
*   [[NetworkAddressTranslation|NAT]] : Utilisation de la traduction d'adresses réseau pour masquer les adresses IP privées derrière une ou plusieurs adresses IP publiques, ajoutant une couche de sécurité.
*   [[VirtualPrivateNetwork|VPN]] : Utilisation de VPN pour chiffrer et encapsuler le trafic, masquant l'adresse IP réelle de l'utilisateur sur Internet.
*   Gestion rigoureuse des listes de contrôle d'accès (ACL) sur les routeurs et les commutateurs.

## 🔗 Notes Connexes
*   [[InternetProtocol]]
*   [[InternetProtocolVersion4]]
*   [[InternetProtocolVersion6]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[NetworkAddressTranslation|NAT]]
*   [[Subnetting|Sous-réseautage]]