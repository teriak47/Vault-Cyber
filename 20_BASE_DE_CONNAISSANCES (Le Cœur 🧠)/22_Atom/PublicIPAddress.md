---
tags:
  - adresse-ip/publique
  - internet/routage
  - ip
  - reseau/adressage
aliases:
  - Adresse IP Publique
  - Public IP Address
source:
  - 
cssclasses:
  - max
---

# Adresse IP Publique

## 📥 Définition en une phrase
> Une adresse IP publique est une adresse IP globalement unique et routable sur Internet, utilisée pour identifier un appareil ou un réseau sur le réseau mondial, permettant la communication directe avec des services externes.

## 🧠 Concepts Clés / Fonctionnement
*   **Globalement Unique**: Chaque adresse IP publique est unique sur l'ensemble d'Internet à un instant donné.
*   **Attribution**: Généralement attribuée par les [[InternetServiceProvider|Fournisseurs d'Accès Internet]] (FAI) à un routeur ou un serveur.
*   **Accessibilité**: Permet à un appareil ou un réseau d'être directement accessible depuis n'importe quel point d'Internet.
*   **Contraste avec les adresses privées**: S'oppose aux [[PrivateIPAddress|adresses IP privées]] qui ne sont pas routables sur Internet et sont utilisées au sein de réseaux locaux.
*   **Types**: Peut être statique (fixe) ou dynamique (allouée temporairement et pouvant changer).

## 🛡️ Risques / Menaces Associés
*   [[DDoSAttack|Attaques par déni de service distribué]] (DDoS) ciblant l'accessibilité du service.
*   [[PortScanning|Scans de ports]] et tentatives d'intrusion via les services exposés.
*   [[InformationLeakage|Fuite d'informations]] sur l'infrastructure ou les services exposés.
*   [[Vulnerability|Vulnérabilités]] exploitables sur les services publics si non sécurisés ou non mis à jour.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Utiliser la [[NetworkAddressTranslation|Traduction d'Adresses Réseau]] (NAT) pour masquer les adresses IP privées et n'exposer que le strict nécessaire.
*   Mettre en place un [[Firewall|pare-feu]] robuste pour filtrer le trafic entrant et autoriser uniquement les connexions légitimes.
*   Utiliser un [[VirtualPrivateNetwork|VPN]] pour chiffrer et anonymiser le trafic sortant et sécuriser l'accès distant.
*   Maintenir tous les systèmes et services exposés publiquement à jour et patchés.
*   Désactiver les services réseau inutiles ou non essentiels qui pourraient être exposés publiquement.

## 🔗 Notes Connexes
*   [[PrivateIPAddress|Adresse IP Privée]]
*   [[NetworkAddressTranslation|NAT]]
*   [[InternetProtocol|Protocole Internet]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]