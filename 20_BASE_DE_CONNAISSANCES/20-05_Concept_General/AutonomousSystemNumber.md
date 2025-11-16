---
tags:
aliases:
  - Numéro de Système Autonome
  - AS Number
  - ASN
  - Autonomous System Number
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Numéro de Système Autonome (ASN)

## 📥 Définition en une phrase
> Un [[AutonomousSystem|Système Autonome]] (AS) est un groupe de réseaux [[InternetProtocol|IP]] gérés par une ou plusieurs entités, et un numéro de système autonome ([[AutonomousSystemNumber|ASN]]) est un identifiant numérique unique attribué à chaque AS pour faciliter le [[Routing|routage]] sur l'[[Internet|Internet]].

## 🧠 Concepts Clés / Piliers
*   **Identifiant Unique**: L'[[AutonomousSystemNumber|ASN]] est un identifiant globalement unique essentiel pour distinguer un [[AutonomousSystem|Système Autonome]] sur l'[[Internet|Internet]] et pour l'échange d'informations de [[Routing|routage]] entre eux.
*   **[[BorderGatewayProtocol|Routage BGP]]**: L'[[AutonomousSystemNumber|ASN]] est le pilier du [[BorderGatewayProtocol|Protocole BGP]] (Border Gateway Protocol), permettant aux [[AutonomousSystem|Systèmes Autonomes]] d'annoncer leurs préfixes [[InternetProtocol|IP]] et de déterminer les chemins optimaux pour le trafic réseau global.
*   **Attribution et Gestion**: Les [[AutonomousSystemNumber|ASN]] sont attribués et gérés par l'[[InternetAssignedNumbersAuthority|IANA]] et ses [[RegionalInternetRegistry|Registres Internet Régionaux]] (RIRs) pour garantir leur unicité et une distribution ordonnée à l'échelle mondiale.
*   **Types d'ASN**: On distingue les [[AutonomousSystemNumber|ASN]] publics, utilisés pour le [[Routing|routage]] sur l'[[Internet|Internet]] global, et les [[AutonomousSystemNumber|ASN]] privés, réservés au [[Routing|routage]] interne au sein d'un [[EnterpriseNetwork|réseau d'entreprise]] sans interaction directe avec l'[[Internet|Internet]] public.
*   **[[RoutingPolicy|Politiques de Routage]]**: Chaque [[AutonomousSystem|Système Autonome]] définit ses propres [[RoutingPolicy|politiques de routage]] en fonction de son [[AutonomousSystemNumber|ASN]] et des informations BGP reçues, influençant ainsi la manière dont le trafic est acheminé.

## 💡 Importance en Cybersécurité
> La gestion sécurisée des [[AutonomousSystemNumber|Numéros de Système Autonome]] est fondamentale pour la [[Cybersecurity|cybersécurité]] et la résilience de l'[[Internet|Internet]]. Des [[SecurityVulnerabilities|vulnérabilités]] ou des erreurs de configuration liées aux [[AutonomousSystemNumber|ASN]] peuvent être exploitées par des [[ThreatActor|acteurs de menace]] pour réaliser des [[BorderGatewayProtocolHijacking|détournements BGP]], entraînant la redirection de trafic, des [[ServiceDisruption|interruptions de service]] massives, ou la [[DataExfiltration|fuite de données]]. Une [[SecurityPolicy|politique de sécurité]] stricte pour le [[Routing|routage]], incluant l'utilisation de [[SecureRoutingProtocols|protocoles de routage sécurisés]], la validation cryptographique des routes via des technologies comme le [[ResourcePublickeyInfrastructure|RPKI]], et une [[NetworkMonitoring|surveillance réseau]] constante, est cruciale pour préserver l'[[Integrity|intégrité]] des chemins de [[DataTransmission|transmission de données]] et la [[Availability|disponibilité]] des [[OnlineServices|services en ligne]] sur l'[[Internet|Internet]].

## 🔗 Notes Connexes
*   [[AutonomousSystem|Système Autonome]]
*   [[BorderGatewayProtocol|Protocole BGP]]
*   [[Internet|Internet]]
*   [[InternetProtocol|Adresse IP]]
*   [[NetworkLayer|Couche Réseau]]
*   [[Router|Routeur]]
*   [[InternetAssignedNumbersAuthority|IANA]]
*   [[RoutingSecurity|Sécurité du Routage]]
*   [[RegionalInternetRegistry|Registre Internet Régional]]
*   [[ResourcePublickeyInfrastructure|Resource Public Key Infrastructure]]