---
tags:
aliases:
  - Dual Stack
  - Double Pile
  - IPv4/IPv6 Dual Stack
source:
  - 
cssclasses:
  - max
---

# Dual Stack (IPv4/IPv6)

## 📥 Définition en une phrase
> Le [[DualStack|Dual Stack]] est un mécanisme permettant aux [[NetworkDevice|équipements réseau]] et aux [[Host|hôtes]] d'opérer simultanément avec les [[InternetProtocolVersion4|protocoles Internet version 4]] et [[InternetProtocolVersion6|Internet Protocol version 6]].

## 🧠 Concepts Clés / Fonctionnement
*   **Nécessité de la Transition**: La coexistence des deux versions de l'[[InternetProtocol|IP]] est cruciale en raison de l'épuisement progressif des [[InternetProtocolAddress|adresses IPv4]] et de la migration vers [[InternetProtocolVersion6|IPv6]]. Le [[DualStack|Dual Stack]] facilite cette transition en assurant une [[Interoperability|interopérabilité]] continue.
*   **Implémentation**: Un même [[Host|hôte]] ou [[NetworkDevice|équipement réseau]] maintient deux piles de [[NetworkProtocol|protocoles]] indépendantes, une pour [[InternetProtocolVersion4|IPv4]] et une pour [[InternetProtocolVersion6|IPv6]], sur la même [[NetworkInterfaceCard|carte d'interface réseau]]. Cela signifie que la carte peut recevoir et envoyer des [[Packet|paquets]] [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]] simultanément.
*   **Flexibilité**: Permet à un dispositif de communiquer avec d'autres dispositifs qui utilisent soit [[InternetProtocolVersion4|IPv4]], soit [[InternetProtocolVersion6|IPv6]], sans nécessiter de [[Tunneling|tunnelisation]] ou de [[NetworkAddressTranslation|traduction]] de protocole pour les communications directes.
*   **Comparaison**: Il se distingue d'autres [[TransitionMechanism|mécanismes de transition IPv6]] comme la [[Tunneling|tunnelisation]] (qui encapsule un protocole dans l'autre) ou la [[NetworkAddressTranslation|traduction]] (qui convertit les [[InternetProtocolAddress|adresses]] entre les deux versions).

## 🛡️ Risques / Menaces Associés
*   **Élargissement de la [[AttackSurface|Surface d'attaque]]**: La gestion de deux piles de [[NetworkProtocol|protocoles]] distinctes peut introduire de nouvelles [[SecurityVulnerabilities|vulnérabilités]] si les deux ne sont pas correctement sécurisées, doublant potentiellement les points d'entrée pour les [[ThreatActor|attaquants]].
*   **Complexité des [[SecurityPolicy|politiques de sécurité]]**: Les règles de [[Firewall|pare-feu]] et les [[AccessControl|contrôles d'accès]] doivent être configurés pour les deux versions de l'[[InternetProtocol|IP]], augmentant le risque d'erreurs de [[NetworkConfiguration|configuration]] ou d'omissions.
*   **[[RoutingAttack|Attaques de routage]]**: Des [[ThreatActor|acteurs malveillants]] pourraient exploiter les différences ou les faiblesses de routage entre [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]] pour intercepter ou rediriger le [[NetworkTrafficAnalysis|trafic réseau]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[SecurityByDesign|Sécurité dès la conception]]**: Intégrer la [[Security|sécurité]] pour les deux piles ([[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]]) dès la planification et la [[NetworkConfiguration|configuration]] des systèmes et des [[Network|réseaux]].
*   **[[Firewall|Configuration des pare-feu]] Rigoureuse**: Appliquer des règles de [[Firewall|pare-feu]] robustes et cohérentes pour le [[NetworkTrafficAnalysis|trafic]] [[InternetProtocolVersion4|IPv4]] et [[InternetProtocolVersion6|IPv6]], en s'assurant qu'aucune faille n'existe.
*   **[[SecurityAudit|Audits de sécurité]] Réguliers**: Effectuer des [[PenetrationTesting|tests d'intrusion]] et des audits pour identifier et corriger les [[SecurityVulnerabilities|vulnérabilités]] spécifiques au [[DualStack|Dual Stack]], y compris les erreurs de [[NetworkConfiguration|configuration]].
*   **[[SecurityAwareness|Sensibilisation]] et Formation**: S'assurer que les équipes [[Cybersecurity|cybersécurité]] et [[Network|réseau]] sont formées aux spécificités de la [[Security|sécurité]] [[InternetProtocolVersion6|IPv6]] et aux défis posés par le [[DualStack|Dual Stack]].

## 🔗 Notes Connexes
*   [[InternetProtocolVersion4|Internet Protocol version 4]]
*   [[InternetProtocolVersion6|Internet Protocol version 6]]
*   [[NetworkProtocol|Protocoles Réseau]]
*   [[TransitionMechanism|Mécanismes de Transition IPv6]]
*   [[NetworkLayer|Couche Réseau]]