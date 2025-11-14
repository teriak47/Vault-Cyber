---
tags:
  - adresses-expérimentales
  - plage-ip-reservée
  - environnement-test
  - networksegmentation
  - firewall
  - networkmonitoring
aliases:
  - Adresses expérimentales
  - Experimental IP Addresses
source:
  - null
cssclasses:
  - max
---

# Adresses Expérimentales

## 📥 Définition en une phrase
> Les [[ExperimentalAddresses|adresses expérimentales]] sont des plages d'[[InternetProtocolAddress|adresses IP]] spécifiquement réservées par l'[[InternetEngineeringTaskForce|IETF]] pour la recherche, le développement et l'expérimentation de nouvelles technologies ou [[NetworkProtocol|protocoles réseau]], et ne sont pas destinées à être utilisées sur l'[[Internet|Internet]] public.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif:** Ces adresses permettent aux chercheurs et développeurs de tester de nouveaux concepts d'[[IPAddressing|adressage IP]] et de [[NetworkProtocol|protocoles]] dans des environnements contrôlés sans risquer de conflits ou d'interférences avec les [[LiveNetwork|réseaux en production]].
*   **Utilisation Typique:** Elles sont principalement déployées dans des environnements de laboratoire, des bancs d'essai (testbeds) et pour des fins de [[NetworkDocumentation|documentation réseau]] et d'exemples.
*   **Plages Spécifiques:**
    *   **[[InternetProtocolVersion4|IPv4]]**: La plage `240.0.0.0/4`, souvent appelée "Class E", est réservée et n'est pas allouée pour une utilisation publique. Bien que techniquement "Reserved", elle est souvent assimilée à un usage expérimental dans le contexte des discussions sur l'[[InternetProtocolVersion4|IPv4]].
    *   **[[InternetProtocolVersion6|IPv6]]**: La plage `2001:0DB8::/32`, connue sous le nom de [[DocumentationPrefix|préfixe de documentation]], est spécifiquement définie pour être utilisée dans la littérature et les exemples, à l'instar des plages d'exemples pour [[InternetProtocolVersion4|IPv4]] (par exemple, 192.0.2.0/24). La plage `FC00::/7` pour les [[UniqueLocalAddress|adresses locales uniques]] sert aussi un objectif similaire pour les communications privées.
*   **Non Routables Publiquement:** Par conception, le [[Router|routage]] de ces [[ExperimentalAddresses|adresses expérimentales]] est bloqué par les [[Router|routeurs]] sur la [[InternetBackbone|dorsale d'Internet]] afin d'assurer leur isolation et de prévenir les [[InteroperabilityIssues|problèmes d'interopérabilité]].

## 🛡️ Risques / Menaces Associés
*   [[InadvertentExposure|Exposition involontaire]]: L'utilisation accidentelle d'[[ExperimentalAddresses|adresses expérimentales]] dans un [[PublicNetwork|réseau public]] peut entraîner des [[NetworkConnectivityIssues|problèmes de connectivité réseau]], des erreurs de [[RoutingTable|routage]], ou des [[NetworkCongestion|congestions réseau]] inattendues.
*   [[SecurityVulnerabilities|Vulnérabilités de sécurité]]: Si elles sont mal configurées ou non isolées, l'utilisation de ces adresses dans un environnement de test pourrait involontairement exposer le [[System|système]] ou le [[Network|réseau]] à des [[Threat|menaces]] si l'environnement de test est compromis.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[NetworkSegmentation|Segmentation réseau]]: Isoler strictement les environnements de test utilisant des [[ExperimentalAddresses|adresses expérimentales]] des [[CorporateNetwork|réseaux d'entreprise]] et de production via des [[VLAN|VLAN]] ou des [[PhysicalSecurity|séparations physiques]].
*   [[Firewall|Pare-feu]]: Mettre en place des [[Firewall|pare-feu]] pour bloquer tout trafic entrant ou sortant entre les réseaux utilisant ces adresses et les réseaux externes ou de production.
*   [[NetworkMonitoring|Surveillance réseau]]: Utiliser la [[NetworkMonitoring|surveillance réseau]] et la [[NetworkTrafficAnalysis|analyse du trafic réseau]] pour détecter toute tentative de routage ou d'utilisation inappropriée de ces adresses en dehors des zones désignées.

## 🔗 Notes Connexes
*   [[InternetProtocolAddress|Adresse IP]]
*   [[PrivateIPAddress|Adresse IP Privée]]
*   [[PublicIPAddress|Adresse IP Publique]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[NetworkSegmentation|Segmentation Réseau]]
*   [[InternetEngineeringTaskForce|IETF]]
*   [[DocumentationPrefix|Préfixe de Documentation]]
*   [[UniqueLocalAddress|Adresses Locales Uniques]]