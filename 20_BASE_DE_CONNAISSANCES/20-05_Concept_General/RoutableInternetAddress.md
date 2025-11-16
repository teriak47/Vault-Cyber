---
tags:
  - routage
  - reseau
  - internet
aliases:
  - Adresse Internet Routable
  - Routable IP Address
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Adresse Internet Routable

## 🎯 Rôle et Contexte Réseau
> Une [[RoutableInternetAddress|adresse Internet routable]] est une [[InternetProtocol|adresse IP]] unique et globalement accessible sur l'[[Internet|Internet]], permettant aux [[Router|routeurs]] de la localiser et d'y acheminer le [[Packet|trafic]]. Ces adresses, qu'il s'agisse d'[[InternetProtocolVersion4|IPv4]] ou d'[[InternetProtocolVersion6|IPv6]], opèrent à la [[NetworkLayer|couche réseau]] (Couche 3 du [[OpenSystemsInterconnectionModel|modèle OSI]]) pour l'adressage logique des [[Host|hôtes]].

## ⚙️ Caractéristiques et Attribution
1.  **Accessibilité Globale**: Contrairement aux [[PrivateIPAddress|adresses IP privées]], une [[RoutableInternetAddress|adresse routable]] est directement visible et accessible depuis n'importe quel point de l'[[Internet|Internet]].
2.  **Unicité Mondiale**: Chaque [[RoutableInternetAddress|adresse routable]] est unique à l'échelle mondiale, garantissant qu'un [[Packet|paquet]] destiné à cette adresse atteint toujours le bon [[Host|hôte]].
3.  **[[Routing|Routage]] Global**: Les [[Router|routeurs]] sur l'[[Internet|Internet]] utilisent ces adresses pour diriger le [[NetworkTrafficAnalysis|trafic]] entre les différents [[InterconnectedNetworks|réseaux interconnectés]] et [[AutonomousSystemNumber|systèmes autonomes]].
4.  **Attribution**: Elles sont attribuées par les [[InternetServiceProvider|FAI]] et gérées par les [[RegionalInternetRegistry|RIRs]] sous l'égide de l'[[InternetAssignedNumbersAuthority|IANA]], puis allouées aux [[Enterprise|entreprises]] et [[Client|clients]].

## 🛡️ Implications de Sécurité
*   **Vulnérabilités / Risques**:
    *   [[AttackSurface|Surface d'attaque]] accrue: Une [[RoutableInternetAddress|adresse routable]] expose directement un [[Host|hôte]] ou un [[Network|réseau]] à des [[DigitalAttack|attaques numériques]] provenant de l'[[Internet|Internet]].
    *   [[PortScanning|Balayage de ports]] et [[Reconnaissance|reconnaissance]]: Les [[ThreatActor|acteurs de menace]] peuvent facilement identifier les [[OnlineServices|services en ligne]] exposés sur une [[RoutableInternetAddress|adresse routable]].
    *   Ciblage direct pour des [[DistributedDenialOfService|attaques par déni de service distribué]] (DDoS), [[Spoofing|usurpations]] ou autres [[Attack|attaques]].
*   **Mesures de protection**:
    *   L'utilisation de [[Firewall|pare-feu]] est essentielle pour filtrer le [[NetworkTrafficAnalysis|trafic]] et bloquer les [[UnauthorizedAccess|accès non autorisés]].
    *   La [[NetworkAddressTranslation|Traduction d'Adresses Réseau (NAT)]] est couramment employée pour masquer les [[PrivateIPAddress|adresses IP privées]] du [[InternalNetwork|réseau interne]] derrière une seule [[RoutableInternetAddress|adresse routable]].
    *   La mise en œuvre de [[SecurityPolicy|politiques de sécurité]] robustes et une [[DefenseInDepth|défense en profondeur]] sont cruciales pour protéger les [[Resource|ressources]] exposées.

## 🔗 Notes Connexes
*   [[InternetProtocol|Protocole Internet]]
*   [[PublicIPAddress|Adresse IP Publique]]
*   [[PrivateIPAddress|Adresse IP Privée]]
*   [[NetworkAddressTranslation|NAT]]
*   [[Routing|Routage]]
*   [[InternetAssignedNumbersAuthority|IANA]]
*   [[RegionalInternetRegistry|RIR]]