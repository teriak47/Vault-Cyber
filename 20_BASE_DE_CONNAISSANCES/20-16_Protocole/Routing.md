---
tags:
  - protocole
  - protocole/reseau
  - reseau/table-de-routage
  - routage/statique
  - routage/dynamique
aliases:
  - Routage
  - Network Routing
archetype: protocole
rfc:
cssclasses:
  - max
---

# Routage

## 🎯 Rôle et Couche OSI
> Le routage est le processus fondamental de sélection du meilleur chemin pour le [[NetworkTrafficAnalysis|trafic réseau]] à travers un ou plusieurs [[Network|réseaux]] interconnectés. Il permet aux [[Packet|paquets]] de [[Data|données]] d'atteindre leur [[DestinationInternetProtocolVersion4Address|destination]] de manière efficace. Le routage opère principalement au niveau de la [[NetworkLayer|Couche Réseau]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et de la [[InternetLayer|Couche Internet]] du [[InternetProtocolSuite|modèle TCP/IP]], s'appuyant sur le [[InternetProtocol|Protocole Internet (IP)]].

## ⚙️ Fonctionnement
1.  **Décision du chemin**: Les [[Router|routeurs]] reçoivent des [[Packet|paquets]] et examinent leur [[DestinationInternetProtocolVersion4Address|adresse de destination]] pour déterminer où les envoyer ensuite.
2.  **Consultation de la [[RoutingTable|Table de Routage]]**: Le [[Router|routeur]] compare l'[[DestinationInternetProtocolVersion4Address|adresse de destination]] du [[Packet|paquet]] avec les entrées de sa [[RoutingTable|table de routage]]. Cette table contient des informations sur les chemins connus vers différentes [[NetworkAddress|adresses réseau]], y compris l'[[IntermediateDevice|interface de sortie]] ou la [[Gateway|passerelle]] à utiliser.
3.  **Redirection du [[Packet|Paquet]]**: Le [[Router|routeur]] transfère le [[Packet|paquet]] vers l'[[IntermediateDevice|interface de sortie]] ou la [[Gateway|passerelle]] qui mène à la [[DestinationInternetProtocolVersion4Address|destination]] finale ou au [[Router|routeur]] suivant sur le chemin.
* **Types de Routage**:
    *   [[StaticConfiguration|Routage Statique]]: Les chemins sont configurés manuellement par un administrateur. Simple pour les petits réseaux, mais nécessite des mises à jour manuelles en cas de changement de [[NetworkTopology|topologie]].
    *   [[DynamicRouting|Routage Dynamique]]: Les [[Router|routeurs]] échangent automatiquement des informations de routage via des [[NetworkProtocol|protocoles de routage]] (ex: OSPF, BGP) pour découvrir les chemins et s'adapter dynamiquement aux changements.
* **Ports par défaut**: N/A pour le concept général de routage, mais les [[NetworkProtocol|protocoles de routage]] utilisent des ports ou protocoles spécifiques (ex: [[TransmissionControlProtocol|TCP]]/179 pour BGP, [[UserDatagramProtocol|UDP]]/520 pour RIP, [[InternetProtocol|IP]] protocole 89 pour OSPF).

## 🛡️ Sécurité du Routage
* **Vulnérabilités connues**:
  * [[RoutingAttack|Attaques de Routage]]: Ciblant les [[RoutingTable|tables de routage]] pour rediriger le [[NetworkTrafficAnalysis|trafic]].
  * [[ManInTheMiddle|Attaque de l'homme du milieu]]: Peut intercepter ou modifier le [[NetworkTrafficAnalysis|trafic]] en manipulant les informations de routage.
  * [[Spoofing|Usurpation]] d'[[InternetProtocol|adresses IP]] ou de messages de [[NetworkProtocol|protocoles de routage]].
* **Mesures de sécurité / Protocoles sécurisés**:
  * [[SecureRoutingProtocols|Protocoles de Routage Sécurisés]]: Utilisation de mécanismes d'[[Authentication|authentification]] et de chiffrement pour les échanges de routage.
  * [[AccessControl|Contrôle d'accès]] strict sur les [[Router|routeurs]] et leurs configurations.
  * [[SecurityMonitoring|Surveillance de sécurité]] du [[NetworkTrafficAnalysis|trafic réseau]] et des [[Log|journaux]] de [[Router|routeur]].

## 🔗 Notes Connexes
* [[Router|Routeur]]
* [[RoutingTable|Table de Routage]]
* [[InternetProtocol|Protocole Internet (IP)]]
* [[StaticConfiguration|Routage Statique]]
* [[DynamicRouting|Routage Dynamique]]
* [[RoutingAttack|Attaque de Routage]]
* [[SecureRoutingProtocols|Protocoles de Routage Sécurisés]]
* [[Wireshark|Wireshark]] (pour l'analyse des [[NetworkProtocol|protocoles de routage]])
* [[Subnetting|Subdivision de réseau]]