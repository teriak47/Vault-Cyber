---
tags:
aliases:
  - CIDR
  - Classless Inter-Domain Routing
  - Routage inter-domaines sans classes
  - ClasslessInterDomainRouting
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Routage Inter-Domaines Sans Classes (CIDR)

## 📥 Définition en une phrase
> Le [[ClasslessInterDomainRouting|Routage Inter-Domaines Sans Classes]] (CIDR) est une méthode d'[[IPAddressing|adressage IP]] et de [[Routing|routage]] qui permet une utilisation plus flexible et efficace des [[InternetProtocol|adresses IP]] en remplaçant l'[[ClassfulAddressing|adressage classique]] par un mécanisme basé sur un [[NetworkPrefix|préfixe de réseau]].

## 🧠 Concepts Clés / Piliers
*   **Adresses IP Flexibles**: Le [[ClasslessInterDomainRouting|CIDR]] utilise une notation de [[NetworkPrefix|préfixe de réseau]] (par exemple, 192.168.1.0/24), où le nombre après la barre oblique indique la longueur du [[NetworkPrefix|préfixe réseau]] en bits. Cela permet d'allouer des [[InternetProtocolAddressBlocks|blocs d'adresses IP]] de tailles arbitraires, s'affranchissant des classes A, B et C de l'[[ClassfulAddressing|adressage classique]].
*   **Agrégation de Routage**: Il permet l'agrégation de plusieurs [[NetworkAddress|réseaux]] plus petits en une seule entrée dans les [[RoutingTable|tables de routage]]. Cette technique, appelée supernetting, réduit la taille des [[RoutingTable|tables de routage]] des [[Router|routeurs]] et améliore l'efficacité du [[Routing|routage]] sur l'[[Internet|Internet]], limitant l'explosion des entrées de routage.
*   **Optimisation de l'Espace d'Adresses**: En offrant une allocation d'[[InternetProtocol|adresses IP]] plus granulaire et efficace, le [[ClasslessInterDomainRouting|CIDR]] a contribué à ralentir l'épuisement des [[InternetProtocol|adresses IPv4]] et à soutenir la croissance de l'[[Internet|Internet]] jusqu'à l'adoption plus large d'[[InternetProtocolVersion6|IPv6]].

## 💡 Importance en Cybersécurité
> En cybersécurité, le [[ClasslessInterDomainRouting|CIDR]] est fondamental car il permet une [[NetworkSegmentation|segmentation de réseau]] plus précise et granulaire, ce qui est crucial pour la mise en œuvre de [[SecurityControl|contrôles de sécurité]] tels que les règles de [[Firewall|pare-feu]] et le [[AccessControl|contrôle d'accès]]. Une allocation et une gestion efficaces des [[InternetProtocol|adresses IP]] via [[ClasslessInterDomainRouting|CIDR]] peuvent également réduire la [[AttackSurface|surface d'attaque]] et simplifier la [[NetworkSecurity|sécurité réseau]] en facilitant l'isolation des [[NetworkSegment|segments réseau]] critiques.

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[SubnetMask|Masque de sous-réseau]]
*   [[ClassfulAddressing|Adressage Classique]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Router|Routeur]]
*   [[RoutingTable|Table de Routage]]
*   [[InternetProtocolAddressBlocks|Blocs d'adresses IP]]
*   [[NetworkPrefix|Préfixe Réseau]]
*   [[IPAddressing|Adressage IP]]
*   [[Routing|Routage]]
*   [[Internet|Internet]]
*   [[NetworkPortion|Partie réseau]]
*   [[HostPortion|Partie hôte]]
*   [[NetworkAddress|Adresse réseau]]
*   [[NetworkSegmentation|Segmentation de réseau]]
*   [[InternetServiceProvider|Fournisseur d'Accès Internet]]
*   [[InternetProtocolVersion6|Internet Protocol version 6]]