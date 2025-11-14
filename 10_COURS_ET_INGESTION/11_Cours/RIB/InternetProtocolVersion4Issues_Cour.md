---
cssclasses:
  - max
title: Problèmes liés au protocole IPv4
tags:
  - espace-adressage-ipv4
  - migration-dual-stack
  - traduction-nat64
  - InternetProtocolVersion4
  - InternetProtocolVersion6
  - NetworkAddressTranslation
module: RIB
---

# Problèmes liés au protocole IPv4

## Limitations de l'IPv4 et Avantages de l'IPv6

Le manque d'espace d'adressage [[InternetProtocolVersion4|IPv4]] a été le facteur le plus décisif pour la transition vers l'[[InternetProtocolVersion6|IPv6]]. 
L'[[InternetProtocolVersion6|IPv6]] dispose d'un espace d'adressage plus large de 128 bits, fournissant 340 undecillions d'adresses possibles.

Lorsque l'[[InternetEngineeringTaskForce|IETF]] a commencé à développer un successeur à l'[[InternetProtocolVersion4|IPv4]], l'organisme a utilisé cette opportunité pour corriger les limites de l'[[InternetProtocolVersion4|IPv4]] et améliorer ce protocole. 
Un exemple est [[ICMPv6|ICMPv6]], qui inclut la [[AddressResolutionProtocol|résolution d'adresse]] et l'autoconfiguration d'adresse que l'on ne trouve pas dans [[InternetControlMessageProtocol|ICMPv4]].

## Coexistence et Transition

Les deux protocoles [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]] coexistent, et la transition vers le seul protocole [[InternetProtocolVersion6|IPv6]] prendra plusieurs années. 
L'[[InternetEngineeringTaskForce|IETF]] a créé divers protocoles et outils pour aider les administrateurs réseau à migrer leurs réseaux vers l'[[InternetProtocolVersion6|IPv6]].

## Techniques de Migration

Les techniques de migration peuvent être divisées en trois catégories principales :

### Dual Stack
*   Les périphériques *[[DualStack|Dual Stack]]* (double pile) exécutent les [[ProtocolStack|piles de protocoles]] [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]] simultanément.

### Tunneling
*   Le [[Tunneling|Tunneling]] est une méthode qui consiste à transporter un [[Packet|paquet]] [[InternetProtocolVersion6|IPv6]] sur un [[Network|réseau]] [[InternetProtocolVersion4|IPv4]].
*   Les [[Packet|paquets]] [[InternetProtocolVersion6|IPv6]] sont [[Encapsulation|encapsulés]] dans des [[Packet|paquets]] [[InternetProtocolVersion4|IPv4]], de la même manière que d'autres types de [[Data|données]].

### Translation
*   **NAT64** permet aux appareils compatibles [[InternetProtocolVersion6|IPv6]] de communiquer avec les appareils compatibles [[InternetProtocolVersion4|IPv4]] en utilisant une technique de traduction similaire à la [[NetworkAddressTranslation|NAT pour IPv4]].
*   Un [[Packet|paquet]] [[InternetProtocolVersion6|IPv6]] est traduit en un [[Packet|paquet]] [[InternetProtocolVersion4|IPv4]], et inversement.