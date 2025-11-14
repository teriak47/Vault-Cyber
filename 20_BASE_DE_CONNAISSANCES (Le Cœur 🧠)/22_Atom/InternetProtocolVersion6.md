---
tags:
  - adressage/128-bits
  - auto-configuration-reseau
  - protocole
  - reseau/ip
aliases:
  - Protocole Internet version 6
  - IPv6
  - Internet Protocol Version 6
cssclasses:
  - max
---

# Protocole Internet version 6 (IPv6)

## 📥 Définition en une phrase
> IPv6 est la version la plus récente du protocole de couche réseau fondamental pour l'interconnexion des réseaux, conçu pour remplacer [[InternetProtocolVersion4|IPv4]] en offrant un espace d'adressage considérablement élargi et des améliorations de performances et de sécurité.

## 🧠 Concepts Clés / Fonctionnement
*   **Espace d'adressage étendu**: Utilise des adresses de 128 bits, offrant $2^{128}$ adresses uniques, contre 32 bits pour [[InternetProtocolVersion4|IPv4]], résolvant ainsi la pénurie d'adresses IPv4.
*   **Format d'en-tête simplifié**: L'en-tête IPv6 est plus simple et plus efficace que celui d'IPv4, ce qui permet un traitement plus rapide par les routeurs.
*   **Auto-configuration sans état (SLAAC)**: Permet aux hôtes de générer automatiquement leurs propres adresses IPv6 sans avoir besoin d'un serveur [[DynamicHostConfigurationProtocol|DHCP]] (bien que [[DynamicHostConfigurationProtocol|DHCPv6]] existe).
*   **Pas de NAT (Network Address Translation)**: Avec un espace d'adressage suffisant, le [[NetworkAddressTranslation|NAT]] n'est plus nécessaire pour pallier la pénurie d'adresses, ce qui simplifie la connectivité de bout en bout.
*   **Qualité de Service (QoS) intégrée**: Inclut des champs d'en-tête (Traffic Class, Flow Label) pour faciliter l'implémentation de la QoS.
*   **Sécurité intégrée (IPsec)**: La prise en charge d'[[IPsec|IPsec]] est une exigence fondamentale dans IPv6, facilitant le chiffrement et l'authentification des paquets IP.
*   **Multicast et Anycast**: Remplace les diffusions (broadcast) d'IPv4, permettant une livraison plus efficace des paquets à des groupes d'hôtes ou à l'hôte le plus proche d'un groupe.

## 🛡️ Risques / Menaces Associés
*   [[ShadowIT|Visibilité réduite]]: La complexité de la transition ou la méconnaissance d'IPv6 peut entraîner un "ombre IT" où des services IPv6 sont actifs sans être sécurisés ou monitorés.
*   [[Bypass|Contournement des contrôles]]: Des pare-feux ou [[IntrusionPreventionSystem|IPS]] mal configurés pour IPv6 peuvent être contournés, permettant à des [[Malware|logiciels malveillants]] ou des [[AdvancedPersistentThreat|APT]] de s'infiltrer.
*   [[NeighborDiscoveryProtocol|Attaques NDP]]: Vulnérabilités similaires à [[AddressResolutionProtocol|ARP]] spoofing dans IPv4 (ex: [[NeighborDiscoveryProtocol|cache poisoning]]).
*   [[RouterAdvertisement|Falsification de RA]]: Un routeur malveillant peut annoncer de fausses informations de routage, redirigeant le trafic.
*   [[DenialOfService|Attaques DoS]]: L'utilisation de fragments IPv6 ou de paquets malformés peut être exploitée pour des attaques par déni de service.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[VulnerabilityManagement|Gestion des vulnérabilités]]: Effectuer des audits réguliers des configurations IPv6 pour identifier et corriger les faiblesses.
*   [[NetworkAccessControl|Contrôle d'accès réseau (NAC)]]: Mettre en œuvre des politiques pour contrôler les périphériques se connectant via IPv6.
*   [[Firewall|Configuration des pare-feux]]: S'assurer que les règles de pare-feu sont correctement appliquées au trafic IPv6, idéalement en mode "deny by default".
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]]: Déployer des systèmes capables de surveiller et de bloquer les attaques spécifiques à IPv6.
*   [[NetworkSegmentation|Segmentation réseau]]: Isoler les systèmes critiques et limiter la propagation des menaces en cas de compromission.
*   [[IPsec|Déploiement d'IPsec]]: Utiliser [[IPsec|IPsec]] pour sécuriser les communications de bout en bout, notamment pour le trafic sensible.
*   [[SecurityAwareness|Sensibilisation]]: Former les équipes techniques aux spécificités et aux risques de sécurité d'IPv6.

## 🔗 Notes Connexes
*   [[InternetProtocolVersion4|IPv4]]
*   [[NeighborDiscoveryProtocol|Neighbor Discovery Protocol (NDP)]]
*   [[IPsec|IPsec]]
*   [[NetworkAddressTranslation|NAT]]
*   [[DualStack|Dual-Stack]]
*   [[DynamicHostConfigurationProtocol|DHCPv6]]