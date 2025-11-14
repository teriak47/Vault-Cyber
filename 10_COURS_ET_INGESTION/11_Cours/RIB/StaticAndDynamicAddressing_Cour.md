---
cssclasses:
  - max
title: Adressage Statique et Dynamique
tags:
  - adressage-dynamique
  - pool-adresse-ipv4
  - reseau-domestique
  - DHCPServer
  - DynamicHostConfigurationProtocol
  - InternetProtocolAddress
module: RIB
---

# Adressage Statique et Dynamique

## Adressage Statique

Avec une attribution statique, l'administrateur réseau doit configurer manuellement les informations réseau relatives à un [[Host|hôte]]. 
Ces informations comprennent au minimum :

*   L'[[InternetProtocolVersion4|adresse IPv4]] de l'hôte
*   Le [[SubnetMask|masque de sous-réseau]]
*   La [[Gateway|passerelle]] par défaut

L'attribution statique d'informations d'adressage peut permettre de mieux contrôler les ressources réseau, mais la saisie d'informations pour chaque [[Host|hôte]] peut prendre beaucoup de temps. 
Lorsque vous utilisez l'adressage [[InternetProtocolVersion4|IPv4]] statique, il est important de tenir à jour une liste qui permet de savoir précisément quelles [[InternetProtocolAddress|adresses IPv4]] ont été attribuées à quels appareils.

## Adressage Dynamique (DHCP)

Les [[InternetProtocolAddress|adresses IPv4]] peuvent être attribuées automatiquement à l'aide d'un [[Protocols|protocole]] appelé [[DynamicHostConfigurationProtocol|DHCP]] (Protocole de Configuration d'Hôte Dynamique). 
Le [[DynamicHostConfigurationProtocol|protocole DHCP]] est généralement la méthode d'attribution d'[[InternetProtocolAddress|adresses IPv4]] privilégiée pour les réseaux de grande taille, car il dégage le personnel de support de cette tâche et le risque d'erreur de saisie est presque éliminé.

Un autre avantage du [[DynamicHostConfigurationProtocol|protocole DHCP]] réside dans le fait qu'une adresse n'est pas attribuée à un [[Host|hôte]] de manière permanente ; elle est seulement **louée** pour une période donnée. 
Si l'[[Host|hôte]] est mis hors tension ou retiré du [[Network|réseau]], l'adresse est retournée au pool pour être réutilisée.

### Exemple de fonctionnement

Lorsque vous entrez dans une zone de couverture, le [[Client|client]] [[DynamicHostConfigurationProtocol|DHCP]] de votre ordinateur portable contacte le [[DHCPServer|serveur DHCP]] local via une connexion sans fil. 
Le [[DHCPServer|serveur DHCP]] attribue une [[InternetProtocolVersion4|adresse IPv4]] à votre ordinateur portable.

*   **Réseaux domestiques** : Dans le cas des [[HomeNetwork|réseaux domestiques]], la configuration [[InternetProtocolVersion4|IPv4]] est souvent reçue directement du [[InternetServiceProvider|fournisseur d'accès à Internet]] ([[InternetServiceProvider|FAI]]).
*   **Équipement SOHO** : Bon nombre de [[HomeNetwork|réseaux domestiques]] et de petites entreprises utilisent un [[WirelessRouter|routeur sans fil]] et un modem. Dans ce cas, le [[WirelessRouter|routeur sans fil]] est à la fois un [[Client|client]] et un [[Server|serveur]] [[DynamicHostConfigurationProtocol|DHCP]].