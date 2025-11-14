---
tags:
  - serveur-dhcp-rogue
  - snooping-dhcp
  - interception-mitm
  - DHCPServer
  - NetworkSegmentation
  - PortSecurity
aliases:
  - Serveur DHCP malveillant
  - Rogue DHCP
  - Serveur DHCP non autorisé
source:
  - null
cssclasses:
  - max
---

# Serveur DHCP Malveillant (Rogue DHCP)

## 📥 Définition en une phrase
> Un [[RogueDHCPServer|serveur DHCP malveillant]] est un [[DynamicHostConfigurationProtocol|serveur DHCP]] non autorisé sur un [[Network|réseau]] qui distribue des informations de configuration [[InternetProtocolAddress|IP]] incorrectes ou malveillantes aux [[Client|clients]], pouvant entraîner des [[ServiceDisruption|interruptions de service]], des [[ManInTheMiddle|attaques de l'homme du milieu]] ou de la [[DataTheft|fraude]].

## 🧠 Concepts Clés / Fonctionnement
*   **Opération [[DynamicHostConfigurationProtocol|DHCP]] légitime** : Un [[DHCPServer|serveur DHCP]] légitime est responsable d'attribuer dynamiquement des [[InternetProtocolAddress|adresses IP]], des [[SubnetMask|masques de sous-réseau]], des [[Gateway|passerelles]] par défaut et des [[DomainNameSystem|serveurs DNS]] aux [[Host|hôtes]] d'un [[Network|réseau]].
*   **Introduction du serveur malveillant** : Un attaquant peut introduire intentionnellement un [[RogueDHCPServer|serveur DHCP malveillant]] (via un [[WirelessAccessPoint|point d'accès]] compromis, un [[Computer|ordinateur]] infecté, etc.) ou il peut être installé par erreur.
*   **Distribution malveillante** : Le [[RogueDHCPServer|serveur malveillant]] répond aux requêtes [[DynamicHostConfigurationProtocol|DHCP]] des [[Client|clients]] plus rapidement que le [[DHCPServer|serveur DHCP]] légitime, ou sur un segment [[Network|réseau]] non surveillé, leur fournissant des configurations [[InternetProtocolAddress|IP]] fabriquées.
*   **Conséquences pour les [[Client|clients]]** : Les [[Client|clients]] qui acceptent les paramètres du [[RogueDHCPServer|serveur DHCP malveillant]] peuvent être redirigés vers des [[Server|serveurs]] malveillants, des [[DomainNameSystem|serveurs DNS]] compromis, subir une perte de connectivité [[Network|réseau]] (entraînant un [[DenialOfService|déni de service]]) ou voir leur [[Data|trafic]] intercepté.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Déni de Service (DoS)]] : Les [[Client|clients]] reçoivent des configurations [[InternetProtocolAddress|IP]] invalides (ex: [[Gateway|passerelles]] inexistantes, [[InternetProtocolAddress|adresses IP]] dupliquées), les empêchant d'accéder au [[Network|réseau]] ou à [[Internet|Internet]].
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]] : Le [[RogueDHCPServer|serveur malveillant]] peut fournir sa propre [[InternetProtocolAddress|adresse IP]] comme [[Gateway|passerelle]] par défaut ou comme [[DomainNameSystem|serveur DNS]], permettant à l'attaquant d'intercepter et de modifier le [[Data|trafic]] des [[Client|clients]].
*   [[DataTheft|Vol de Données]] / [[PrivacyInvasion|Invasion de la Vie Privée]] : Par la redirection, les [[Client|clients]] peuvent être envoyés vers des sites de [[Phishing|hameçonnage]] ou des [[Server|serveurs]] contrôlés par l'attaquant, facilitant la collecte de [[SensitiveData|données sensibles]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[PortSecurity|Sécurité des Ports]] : Configurer les [[NetworkSwitch|commutateurs]] pour n'autoriser les messages [[DynamicHostConfigurationProtocol|DHCP]] que depuis des [[PortNumber|ports]] spécifiques connectés aux [[DHCPServer|serveurs DHCP]] légitimes.
*   [[DHCPSnooping|DHCP Snooping]] : Activer cette fonctionnalité sur les [[NetworkSwitch|commutateurs]] de [[Network|réseau]] pour filtrer les messages [[DynamicHostConfigurationProtocol|DHCP]] non fiables et valider les informations de [[DynamicHostConfigurationProtocol|DHCP]].
*   [[NetworkSegmentation|Segmentation Réseau]] : Isoler les [[DHCPServer|serveurs DHCP]] légitimes dans des [[VirtualLocalAreaNetwork|VLAN]] ou des segments [[Network|réseau]] dédiés et appliquer des [[Firewall|règles de pare-feu]] strictes.
*   [[SecurityMonitoring|Surveillance de Sécurité]] : Mettre en place une [[SecurityInformationAndEventManagement|surveillance SIEM]] pour analyser les [[Log|journaux]] [[DynamicHostConfigurationProtocol|DHCP]] et le [[Network|trafic réseau]] afin de détecter l'activité de [[RogueDHCPServer|serveurs DHCP malveillants]].
*   [[Authentication|Authentification]] et [[AccessControl|Contrôle d'accès]] : S'assurer que seuls les administrateurs autorisés peuvent accéder et modifier la [[NetworkConfiguration|configuration réseau]] et les [[DHCPServer|serveurs DHCP]].

## 🔗 Notes Connexes
*   [[DynamicHostConfigurationProtocol|Protocole de Configuration d'Hôte Dynamique (DHCP)]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu (MITM)]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DenialOfService|Déni de Service (DoS)]]
*   [[DHCPServer|Serveur DHCP]]
*   [[NetworkConfiguration|Configuration Réseau]]
---