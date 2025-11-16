---
tags:
  - transition/ipv6
  - reseau
aliases:
  - Dual Stack
  - Double Pile
  - IPv4/IPv6 Dual Stack
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Dual Stack (IPv4/IPv6)

## 🎯 Rôle et Contexte
> Le [[DualStack|Dual Stack]] est un [[TransitionMechanism|mécanisme de transition]] permettant aux [[NetworkDevice|équipements réseau]] et aux [[Host|hôtes]] d'opérer simultanément avec les [[InternetProtocolVersion4|protocoles Internet version 4]] ([[IPv4]]) et [[InternetProtocolVersion6|Internet Protocol version 6]] ([[IPv6]]). Son rôle est d'assurer une [[Interoperability|interopérabilité]] continue pendant la migration progressive de l'[[Internet|Internet]] vers [[InternetProtocolVersion6|IPv6]], en gérant les deux piles de [[NetworkProtocol|protocoles]] au niveau de la [[NetworkLayer|couche réseau]].

## ⚙️ Fonctionnement
1.  **Nécessité de la Transition**: Crucial en raison de l'épuisement des [[InternetProtocol|adresses IPv4]] et de la nécessité de migrer vers [[InternetProtocolVersion6|IPv6]]. Il permet une coexistence transparente des deux versions.
2.  **Implémentation Indépendante**: Un même [[Host|hôte]] ou [[NetworkDevice|équipement réseau]] maintient deux piles de [[NetworkProtocol|protocoles]] (une pour [[InternetProtocolVersion4|IPv4]] et une pour [[InternetProtocolVersion6|IPv6]]) sur la même [[NetworkInterfaceCard|carte d'interface réseau]]. Cela permet à l'interface de recevoir et d'envoyer des [[Packet|paquets]] [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]] simultanément.
3.  **Flexibilité de Communication**: Grâce à cette double implémentation, un dispositif [[DualStack|Dual Stack]] peut communiquer directement avec des dispositifs utilisant soit [[InternetProtocolVersion4|IPv4]], soit [[InternetProtocolVersion6|IPv6]], sans recourir à des techniques intermédiaires comme la [[Tunneling|tunnelisation]] ou la [[NetworkAddressTranslation|traduction d'adresses]].
4.  **Différenciation avec Autres Mécanismes**: Le [[DualStack|Dual Stack]] se distingue de la [[Tunneling|tunnelisation]] (qui encapsule un protocole dans l'autre) et de la [[NetworkAddressTranslation|traduction]] (qui convertit les [[InternetProtocol|adresses]] entre les deux versions), offrant une gestion native des deux piles.
* **Ports par défaut**: Non applicable, car il ne s'agit pas d'un protocole d'application avec des ports dédiés, mais d'une capacité d'un système à gérer les [[InternetProtocol|protocoles IP]] aux niveaux inférieurs.

## 🛡️ Sécurité du Dual Stack
* **Vulnérabilités et défis connus**:
  *   **Élargissement de la [[AttackSurface|Surface d'attaque]]**: La gestion de deux piles de [[NetworkProtocol|protocoles]] distinctes peut introduire de nouvelles [[SecurityVulnerabilities|vulnérabilités]] si les deux ne sont pas correctement sécurisées, doublant potentiellement les points d'entrée pour les [[ThreatActor|attaquants]].
  *   **Complexité des [[SecurityPolicy|politiques de sécurité]]**: Les règles de [[Firewall|pare-feu]] et les [[AccessControl|contrôles d'accès]] doivent être configurés pour les deux versions de l'[[InternetProtocol|IP]], augmentant le risque d'erreurs de [[NetworkConfiguration|configuration]] ou d'omissions.
  *   **[[RoutingAttack|Attaques de routage]]**: Des [[ThreatActor|acteurs malveillants]] pourraient exploiter les différences ou les faiblesses de routage entre [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]] pour intercepter ou rediriger le [[NetworkTrafficAnalysis|trafic réseau]].
* **Mesures de protection et bonnes pratiques**:
  *   **[[SecurityByDesign|Sécurité dès la conception]]**: Intégrer la [[Security|sécurité]] pour les deux piles ([[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]]) dès la planification et la [[NetworkConfiguration|configuration]] des systèmes et des [[Network|réseaux]].
  *   **[[Firewall|Configuration des pare-feu]] Rigoureuse**: Appliquer des règles de [[Firewall|pare-feu]] robustes et cohérentes pour le [[NetworkTrafficAnalysis|trafic]] [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]], en s'assurant qu'aucune faille n'existe.
  *   **[[SecurityAudit|Audits de sécurité]] Réguliers**: Effectuer des [[PenetrationTesting|tests d'intrusion]] et des [[SecurityAudit|audits de sécurité]] pour identifier et corriger les [[SecurityVulnerabilities|vulnérabilités]] spécifiques au [[DualStack|Dual Stack]], y compris les erreurs de [[NetworkConfiguration|configuration]].
  *   **[[SecurityAwareness|Sensibilisation]] et Formation**: S'assurer que les équipes [[Cybersecurity|cybersécurité]] et [[Network|réseau]] sont formées aux spécificités de la [[Security|sécurité]] [[InternetProtocolVersion6|IPv6]] et aux défis posés par le [[DualStack|Dual Stack]].

## 🔗 Notes Connexes
*   [[InternetProtocolVersion4|Internet Protocol version 4]]
*   [[InternetProtocolVersion6|Internet Protocol version 6]]
*   [[NetworkProtocol|Protocoles Réseau]]
*   [[TransitionMechanism|Mécanismes de Transition IPv6]]
*   [[NetworkLayer|Couche Réseau]]
*   [[AttackSurface|Surface d'attaque]]
*   [[SecurityVulnerabilities|Vulnérabilités de sécurité]]
*   [[Firewall|Pare-feu]]
*   [[AccessControl|Contrôles d'accès]]
*   [[RoutingAttack|Attaques de routage]]