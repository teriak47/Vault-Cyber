---
cssclasses:
  - max
title: Objectif Adresse IPv4
module: RIB
---
# Objectif Adresse IPv4

## Définition

L'[[InternetProtocolVersion4|adresse IPv4]] est une adresse de [[LogicalNetwork|réseau logique]] qui identifie un [[Host|hôte]] donné. Elle doit être unique et correctement configurée pour permettre les communications.

*   **Sur le LAN :** Elle doit être unique sur le [[LocalAreaNetwork|LAN]] pour permettre les communications locales.
*   **Sur le réseau mondial :** Elle doit être unique sur Internet pour permettre les communications distantes.

## Attribution

Une [[InternetProtocolVersion4|adresse IPv4]] est attribuée à la connexion de l'[[NetworkInterface|interface réseau]] d'un [[Host|hôte]]. Cette connexion est généralement une [[NetworkInterfaceCard|carte réseau]] (NIC) installée dans l'appareil.

## Rôle dans les Paquets

Chaque [[Packet|paquet]] envoyé via Internet dispose d'une [[SourceInternetProtocolVersion4Address|adresse IPv4 source]] et d'une [[DestinationInternetProtocolVersion4Address|adresse IPv4 de destination]]. Les appareils réseau utilisent ces informations pour s'assurer que les données arrivent à la bonne destination et que toutes les réponses sont renvoyées à la source d'origine.