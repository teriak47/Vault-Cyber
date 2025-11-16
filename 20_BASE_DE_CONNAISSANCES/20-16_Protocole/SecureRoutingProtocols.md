---
tags:
  - protocole
  - protocole/routage
aliases:
  - Protocoles de Routage Sécurisés
  - Secure Routing Protocols
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocoles de Routage Sécurisés

## 🎯 Rôle et Couche OSI
> Les [[SecureRoutingProtocols|protocoles de routage sécurisés]] sont des extensions ou des implémentations renforcées des [[NetworkProtocol|protocoles réseau]] standards. Leur rôle principal est de protéger les informations de [[Routing|routage]] contre les [[Attack|attaques]], en garantissant l'[[Integrity|intégrité]] et l'[[Authentication|authentification]] des mises à jour de routage. Ils opèrent principalement au niveau de la [[NetworkLayer|couche réseau]] du [[OSIModel|modèle OSI]] et du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
1.  **[[Authentication|Authentification]] des Mises à Jour**: Ces protocoles intègrent des mécanismes cryptographiques pour vérifier l'origine et l'authenticité des messages de [[Routing|routage]]. Cela empêche les entités non autorisées ([[ThreatActor|acteurs de menace]]) d'injecter ou de modifier des informations de routage, évitant ainsi les [[Spoofing|usurpations]] et les fausses annonces.
2.  **[[Integrity|Intégrité]] des Données**: Ils utilisent des [[Hashing|fonctions de hachage]] et des [[DigitalSignature|signatures numériques]] pour s'assurer que les informations de routage n'ont pas été altérées ([[Tampering|altérées]]) pendant la [[SignalTransmission|transmission]]. Tout changement non autorisé rendrait l'information invalide et serait rejeté.
3.  **Prévention des [[RoutingAnomaly|Anomalies de Routage]]**: L'objectif est de contrer des problèmes graves qui peuvent perturber la [[Network|connectivité réseau]], tels que les [[RoutingLoop|boucles de routage]] persistantes, les [[BlackholeRouting|trous noirs de routage]] (où le trafic est dirigé vers une destination inexistante) et les annonces de routes non valides.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités atténuées**:
    *   [[RoutingAttack|Attaques de routage]] (y compris [[ManInTheMiddle|attaques de l'homme du milieu]] sur les informations de routage)
    *   [[RouteHijacking|Détournement de routes]] (où un [[ThreatActor|attaquant]] annonce des routes qu'il ne possède pas)
    *   Injection de routes malveillantes
    *   Altération des messages de routage
*   **Implémentations et versions sécurisées**:
    *   **BGPsec**: Une extension du [[BorderGatewayProtocol|Border Gateway Protocol]] qui utilise la [[Cryptography|cryptographie]] pour authentifier l'ensemble du chemin d'une route, renforçant la confiance dans les annonces de routes entre [[AutonomousSystemNumber|systèmes autonomes]].
    *   **OSPFv3 avec [[InternetProtocolSecurity|IPsec]]**: Le protocole [[OpenShortestPathFirst|Open Shortest Path First]] pour [[InternetProtocolVersion6|IPv6]] peut être sécurisé en utilisant [[InternetProtocolSecurity|IPsec]] pour chiffrer et authentifier l'échange de ses messages, garantissant la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]].
    *   **[[PublicKeyInfrastructure|RPKI]] (Resource Public Key Infrastructure)**: Un système de [[PublicKeyInfrastructure|PKI]] qui authentifie la propriété des [[InternetProtocolAddressBlocks|blocs d'adresses IP]] et des [[AutonomousSystemNumber|numéros de système autonome (ASN)]]. Il permet aux opérateurs de réseau de vérifier que les annonces de routes sont légitimes, prévenant ainsi les [[RouteHijacking|détournements de routes]].

## 🔗 Notes Connexes
*   [[Routing|Routage]]
*   [[NetworkLayer|Couche Réseau]]
*   [[InternetProtocol|Internet Protocol]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[InternetProtocolSecurity|IPsec]]
*   [[DigitalSignature|Signature Numérique]]
*   [[ThreatActor|Acteur de Menace]]