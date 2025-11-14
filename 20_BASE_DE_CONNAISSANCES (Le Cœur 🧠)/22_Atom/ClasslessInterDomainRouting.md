---
tags:
  - notation-cidr
  - adressage-ip-classless
  - segmentation-reseau-flexible
  - InternetProtocolAddress
  - RoutingTable
  - NetworkPrefix
aliases:
  - CIDR
  - Classless Inter-Domain Routing
  - Routage inter-domaines sans classes
cssclasses:
  - max
---

# Routage Inter-Domaines Sans Classes (CIDR)

## 📥 Définition en une phrase
> Le [[ClasslessInterDomainRouting|Routage Inter-Domaines Sans Classes]] (CIDR) est une méthode d'[[IPAddressing|adressage IP]] et de [[RoutingTable|routage]] qui permet une utilisation plus flexible et efficace des [[InternetProtocolAddress|adresses IP]] en remplaçant le système d'[[ClassfulAddressing|adressage classique]] par un mécanisme basé sur un [[NetworkPrefix|préfixe de réseau]].

## 🧠 Concepts Clés / Fonctionnement
*   Le [[ClasslessInterDomainRouting|CIDR]] a été introduit pour pallier les limitations de l'[[ClassfulAddressing|adressage IP par classes]], notamment le gaspillage d'[[InternetProtocolAddress|adresses IP]] et l'augmentation rapide de la taille des [[RoutingTable|tables de routage]] sur l'[[Internet|Internet]].
*   Il utilise une notation de [[NetworkPrefix|préfixe de réseau]], généralement écrite comme une [[InternetProtocolAddress|adresse IP]] suivie d'une barre oblique et d'un nombre (ex: 192.168.1.0/24), où le nombre indique la longueur du [[NetworkPrefix|préfixe réseau]] en bits.
*   Ce [[NetworkPrefix|préfixe]] détermine la partie [[NetworkPortion|réseau]] de l'[[InternetProtocolAddress|adresse IP]], tandis que les bits restants définissent la [[HostPortion|partie hôte]]. Cela remplace le concept fixe de [[SubnetMask|masque de sous-réseau]] par classe.
*   Permet l'agrégation de multiples [[NetworkAddress|adresses réseau]] en une seule entrée dans la [[RoutingTable|table de routage]], réduisant ainsi la taille de la table et améliorant l'efficacité du [[Router|routage]].
*   Facilite la [[NetworkSegmentation|segmentation de réseau]] flexible, offrant aux [[InternetServiceProvider|FAI]] et aux organisations plus de granularité dans l'allocation des [[InternetProtocolAddressBlocks|blocs d'adresses IP]].

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[SubnetMask|Masque de Sous-réseau]]
*   [[ClassfulAddressing|Adressage Classique]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Router|Routeur]]
*   [[RoutingTable|Table de Routage]]
*   [[InternetProtocolAddressBlocks|Blocs d'adresses IP]]
*   [[NetworkPrefix|Préfixe Réseau]]