---
tags:
  - usurpation-ip
  - adressage-ipv6
  - gestion-ipam
  - auto-configuration-reseau
  - segmentation-reseau
  - controle-acces/liste-acl
aliases:
  - Adressage IP
  - IP Addressing
source:
  - null
cssclasses:
  - max
---

# Adressage IP

## 📥 Définition en une phrase
> Le processus d'attribution et de gestion des adresses IP ([[InternetProtocol]]) aux appareils connectés à un réseau, permettant leur identification unique et leur communication.

## 🧠 Concepts Clés / Fonctionnement
* Les adresses IP sont des identifiants numériques logiques qui désignent un appareil sur un réseau [[InternetProtocol|IP]].
* Il existe deux versions principales : [[InternetProtocolVersion4]] (32 bits, ex: 192.168.1.1) et [[InternetProtocolVersion6]] (128 bits, ex: 2001:0db8::1).
* Chaque adresse est associée à un [[NetworkMask|masque de sous-réseau]] qui définit la partie réseau et la partie hôte de l'adresse, essentielle pour le [[Subnetting|sous-réseautage]].
* Les adresses peuvent être attribuées statiquement (manuellement) ou dynamiquement via un serveur [[DynamicHostConfigurationProtocol|DHCP]].
* L'adressage IP permet le routage des paquets de données entre différents réseaux via des [[Router|routeurs]] et [[Gateway|passerelles]].

## 🛡️ Risques / Menaces Associés
* [[IPSpoofing|Usurpation d'adresse IP]] : Utilisation d'une fausse adresse IP source pour masquer l'identité d'un attaquant ou contourner les contrôles de sécurité.
* [[DenialOfService|Attaques par déni de service]] (DoS/DDoS) : Ciblent ou utilisent les adresses IP pour surcharger des ressources réseau, les rendant indisponibles.
* [[NetworkScanning|Scans de réseau]] et [[PortScanning|scans de ports]] : Les attaquants utilisent des plages d'adresses IP pour découvrir des hôtes actifs et des services vulnérables.
* [[ManInTheMiddle|Attaques de l'homme du milieu]] (MITM) : L'adressage IP peut être manipulé pour intercepter ou modifier le trafic entre deux parties.

## 💎 Mesures de Protection / Bonnes Pratiques
* [[NetworkSegmentation|Segmentation réseau]] : Diviser le réseau en sous-réseaux plus petits (VLANs) pour isoler le trafic et limiter la portée des attaques.
* [[AccessControlList|Listes de contrôle d'accès]] (ACLs) sur les [[Router|routeurs]] et [[Firewall|pare-feu]] : Filtrer le trafic en fonction des adresses IP sources et destinations autorisées.
* [[DynamicHostConfigurationProtocol|DHCP Snooping]] : Sécuriser les communications DHCP en filtrant les messages DHCP non fiables et en construisant une table de liaison DHCP.
* Utilisation d'[[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]] : Détecter et bloquer les activités suspectes ou les tentatives d'[[IPSpoofing|usurpation d'IP]].
* Gestion rigoureuse des adresses IP (IPAM) : Suivre l'attribution et l'utilisation des adresses pour faciliter l'[[IncidentResponse|investigation des incidents]].

## 🔗 Notes Connexes
* [[InternetProtocol|Protocole Internet]]
* [[InternetProtocolVersion4]]
* [[InternetProtocolVersion6]]
* [[Subnetting|Sous-réseautage]]
* [[DynamicHostConfigurationProtocol|DHCP]]
* [[DomainNameSystem|Système de Noms de Domaine]]
* [[NetworkMask|Masque de sous-réseau]]