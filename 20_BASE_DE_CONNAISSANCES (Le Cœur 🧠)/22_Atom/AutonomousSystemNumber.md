---
tags:
  - numero-asn
  - detournement-bgp
  - securite-routage
  - BorderGatewayProtocol
  - RoutingSecurity
  - InternetAssignedNumbersAuthority
aliases:
  - Numéro de Système Autonome
  - AS Number
  - ASN
  - Autonomous System Number
source:
  - null
cssclasses:
  - max
---

# Numéro de Système Autonome (ASN)

## 📥 Définition en une phrase
> Un [[AutonomousSystem|Système Autonome]] (AS) est un groupe de réseaux [[InternetProtocol|IP]] gérés par une ou plusieurs entités, et un numéro de système autonome (ASN) est un identifiant numérique unique attribué à chaque AS pour faciliter le [[Routing|routage]] sur l'[[Internet|Internet]].

## 🧠 Concepts Clés / Fonctionnement
*   Un ASN est un identifiant globalement unique utilisé par le [[BorderGatewayProtocol|Protocole BGP]] (Border Gateway Protocol) pour échanger des informations de routage entre différents [[AutonomousSystem|Systèmes Autonomes]].
*   Les ASN sont attribués par l'[[InternetAssignedNumbersAuthority|IANA]] (Internet Assigned Numbers Authority) et ses registres Internet régionaux (RIRs) pour garantir leur unicité.
*   Il existe deux types principaux d'ASN : les ASN publics, utilisés pour le routage de trafic sur l'[[Internet|Internet]], et les ASN privés, utilisés uniquement au sein d'un réseau interne sans routage externe.
*   Chaque [[AutonomousSystem|Système Autonome]] prend des décisions de routage indépendantes basées sur ses [[RoutingPolicy|politiques de routage]] et les informations BGP reçues d'autres ASNs.

## 🛡️ Risques / Menaces Associés
*   [[BorderGatewayProtocolHijacking|Détournement BGP]] : Un acteur malveillant peut annoncer de manière frauduleuse des préfixes IP qui ne lui appartiennent pas, redirigeant ainsi le trafic.
*   Mauvaise configuration : Des erreurs de configuration des ASN ou des [[BorderGatewayProtocol|routes BGP]] peuvent entraîner une [[ServiceDisruption|interruption de service]] généralisée ou une [[DataCorruption|corruption de données]] par un routage incorrect.
*   [[DenialOfService|Attaques par déni de service]] (DoS/DDoS) : Un ASN peut être ciblé ou utilisé involontairement dans des attaques par amplification de trafic si ses [[RoutingPolicy|politiques de routage]] sont faibles.
*   [[InadvertentExposure|Exposition involontaire]] : Des annonces BGP incorrectes peuvent exposer des parties internes d'un [[EnterpriseNetwork|réseau d'entreprise]] à l'[[Internet|Internet]] public.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mise en œuvre de [[SecureRoutingProtocols|protocoles de routage sécurisés]] et de [[RoutingPolicy|politiques de routage]] strictes pour valider les préfixes IP annoncés.
*   Utilisation du filtrage des routes et de la validation des chemins BGP pour prévenir le [[BorderGatewayProtocolHijacking|détournement BGP]].
*   Surveillance continue des annonces BGP et du trafic pour détecter toute anomalie ou tentative de [[BorderGatewayProtocolHijacking|détournement]].
*   Participation à des initiatives de [[RoutingSecurity|sécurité du routage]] telles que RPKI (Resource Public Key Infrastructure) pour authentifier les propriétaires d'adresses IP.

## 🔗 Notes Connexes
*   [[AutonomousSystem|Système Autonome]]
*   [[BorderGatewayProtocol|Protocole BGP]]
*   [[Internet|Internet]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Router|Routeur]]
*   [[InternetAssignedNumbersAuthority|IANA]]
*   [[RoutingSecurity|Sécurité du Routage]]