---
tags:
aliases:
  - IANA
  - Internet Assigned Numbers Authority
  - Autorité d'attribution des numéros d'Internet
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Autorité d'attribution des numéros d'Internet (IANA)

## 📥 Définition en une phrase
> L'[[InternetAssignedNumbersAuthority|IANA]] est l'entité responsable de la coordination mondiale des identificateurs uniques fondamentaux pour le fonctionnement d'[[Internet|Internet]], incluant les [[InternetProtocol|adresses IP]], les [[AutonomousSystemNumber|numéros de système autonome]] et le [[DomainNameSystem|système de noms de domaine (DNS)]].

## 🧠 Concepts Clés / Piliers
*   **Coordination Globale des Identificateurs**: L'[[InternetAssignedNumbersAuthority|IANA]] assure la gestion centrale et unique de registres critiques tels que les blocs d'[[InternetProtocol|adresses IP]] (pour [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]]), les [[AutonomousSystemNumber|numéros de système autonome]] (ASNs) qui sont essentiels pour le [[Routing|routage]] inter-réseaux, et les [[DomainNameSystem|noms de domaine]] de premier niveau. Cette fonction garantit l'unicité et la cohérence à l'échelle mondiale.
*   **Délégation Régionale**: Pour une gestion efficace, l'[[InternetAssignedNumbersAuthority|IANA]] délègue l'attribution des blocs d'[[InternetProtocol|adresses IP]] à cinq [[RegionalInternetRegistry|registres internet régionaux (RIRs)]] (AfriNIC, APNIC, ARIN, LACNIC et RIPE NCC). Ces [[RegionalInternetRegistry|RIRs]] allouent ensuite les adresses aux [[InternetServiceProvider|fournisseurs d'accès internet (FAI)]] et aux grandes [[Enterprise|organisations]] dans leurs régions respectives.
*   **Gestion de la Zone Racine [[DomainNameSystem|DNS]]**: L'[[InternetAssignedNumbersAuthority|IANA]] maintient la base de données centrale des [[DomainNameSystem|noms de domaine]] de premier niveau (TLD), appelée la zone racine du [[DomainNameSystem|DNS]]. Cette responsabilité est fondamentale pour la résolution des [[DomainNameSystem|noms de domaine]] en [[InternetProtocol|adresses IP]] et, par extension, pour la navigabilité de [[Internet|Internet]].
*   **Enregistrement des Paramètres de [[NetworkProtocol|Protocoles]]**: Au-delà des [[InternetProtocol|adresses IP]] et des [[DomainNameSystem|noms de domaine]], l'[[InternetAssignedNumbersAuthority|IANA]] est également le conservateur des enregistrements de nombreux paramètres de [[NetworkProtocol|protocoles réseau]], tels que les [[PortNumber|numéros de port]] et les types de médias, souvent définis dans les [[RequestForComments|RFC]] de l'[[InternetEngineeringTaskForce|IETF]].

## 💡 Importance en Cybersécurité
> L'[[InternetAssignedNumbersAuthority|IANA]] est un pilier de la [[Cybersecurity|cybersécurité]] car sa coordination centrale garantit l'intégrité et la stabilité des identificateurs réseau mondiaux. Sans cette gestion unifiée, des conflits d'[[InternetProtocol|adresses IP]] et des problèmes de [[DomainNameSystem|DNS]] rendraient [[Internet|Internet]] chaotique et vulnérable à des [[Attack|attaques]] suplantations ou de désorganisation massive. Sa fonction de délégation et de standardisation contribue à prévenir certaines [[SecurityVulnerabilities|vulnérabilités]] au niveau de l'[[NetworkInfrastructure|infrastructure réseau]] et facilite la [[ThreatIntelligence|renseignement sur les menaces]] en fournissant une source fiable pour l'identification des [[Network|réseaux]] et des [[System|systèmes]].

## 🔗 Notes Connexes
*   [[Internet|Internet]]
*   [[InternetProtocol|Adresse IP]]
*   [[DomainNameSystem|Système de Noms de Domaine]]
*   [[RequestForComments|Request For Comments (RFC)]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[AutonomousSystemNumber|Numéro de Système Autonome]]
*   [[RegionalInternetRegistry|Registre Internet Régional]]