---
tags:
  - cidr
  - adresses-ip-publices
  - adresses-ip-privées
  - ipv4
  - ipv6
  - networksegmentation
aliases:
  - Blocs d'adresses IP
  - Plages d'adresses IP
  - IP Address Blocks
source:
  - null
cssclasses:
  - max
---

# Blocs d'Adresses IP (Internet Protocol Address Blocks)

## 📥 Définition en une phrase
> Les [[InternetProtocolAddress|blocs d'adresses IP]] sont des plages contiguës d'[[InternetProtocolAddress|adresses IP]] allouées et gérées par des autorités spécifiques pour faciliter l'[[IPAddressing|adressage]] et le [[RoutingTable|routage]] sur [[Internet|Internet]] et les [[Network|réseaux]] privés.

## 🧠 Concepts Clés / Fonctionnement
*   **Attribution Hiérarchique**: Les blocs sont attribués hiérarchiquement par l'[[InternetAssignedNumbersAuthority|IANA]] aux [[RegionalInternetRegistry|Régistres Internet Régionaux (RIRs)]], qui les délèguent ensuite aux [[InternetServiceProvider|Fournisseurs d'Accès Internet (FAI)]] et aux grandes [[Enterprise|organisations]].
*   **[[ClasslessInterDomainRouting|CIDR]] (Classless Inter-Domain Routing)**: La méthode moderne de gestion des blocs d'[[InternetProtocolAddress|adresses IP]] qui a remplacé l'ancien [[ClassfulAddressing|adressage classique]]. Elle permet une allocation plus flexible et efficace des [[InternetProtocolAddress|adresses IP]] en utilisant des préfixes de longueur variable pour définir la taille du bloc (ex: 192.168.1.0/24).
*   **[[NetworkAddress|Adresse réseau]] et [[BroadcastAddress|Adresse de diffusion]]**: Chaque bloc [[InternetProtocolAddress|d'adresses IP]] (ou [[NetworkSegment|segment réseau]]) contient une [[NetworkAddress|adresse réseau]] qui identifie le [[Network|réseau]] lui-même et une [[BroadcastAddress|adresse de diffusion]] pour envoyer des [[Message|messages]] à tous les [[Host|hôtes]] du [[NetworkSegment|segment]].
*   **Adresses Publiques vs. Privées**: Distinction entre les [[PublicIPAddress|adresses IP publiques]], routables sur [[Internet|Internet]], et les [[PrivateIPAddress|adresses IP privées]], utilisées au sein des [[LocalAreaNetwork|LAN]] et nécessitant une [[NetworkAddressTranslation|NAT]] pour communiquer avec [[Internet|Internet]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[IPAddressing|Adressage IP]]
*   [[ClasslessInterDomainRouting|Routage Inter-Domaine Sans Classe (CIDR)]]
*   [[InternetAssignedNumbersAuthority|IANA]]
*   [[RegionalInternetRegistry|Régistre Internet Régional (RIR)]]
---