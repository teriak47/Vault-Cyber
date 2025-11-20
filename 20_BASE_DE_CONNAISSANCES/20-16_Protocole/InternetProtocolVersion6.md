---
tags:
  - protocole
aliases:
  - Protocole Internet version 6
  - IPv6
  - Internet Protocol Version 6
  - IP version 6
archetype: protocole
rfc: RFC 8200
cssclasses:
  - max
---

# Protocole Internet version 6 (IPv6)

## 🎯 Rôle et Couche OSI
> IPv6 est la version la plus récente du protocole de couche réseau fondamental pour l'interconnexion des réseaux. Il opère à la couche réseau (Couche 3) du modèle OSI et du modèle TCP/IP. Son rôle principal est d'identifier de manière unique les dispositifs sur un réseau et de router les paquets de données entre les réseaux, succédant à IPv4 pour pallier la pénurie d'adresses IP et offrir des améliorations de performances et de sécurité.

## ⚙️ Fonctionnement
1.  **Gestion des adresses IP**: IPv6 utilise des adresses de 128 bits, offrant un espace d'adressage considérablement élargi ($2^{128}$ adresses uniques) par rapport aux 32 bits d'IPv4. Ces adresses sont représentées par huit groupes de quatre valeurs hexadécimales séparées par des deux-points (par exemple, `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
2.  **Encapsulation et Routage**: Il encapsule les données en paquets et les route d'une source à une destination à travers des réseaux interconnectés. L'en-tête IPv6 est simplifié pour un traitement plus efficace par les routeurs, avec des champs comme la classe de trafic (Traffic Class) et l'étiquette de flux (Flow Label) pour le QoS.
3.  **Auto-configuration sans état (SLAAC)**: Permet aux hôtes de générer automatiquement leurs propres adresses IPv6 link-local et globales sans nécessiter de serveur DHCP. Ils peuvent former une adresse link-local en combinant un préfixe réseau avec leur adresse MAC ou un identifiant aléatoire, et peuvent ensuite obtenir une adresse globale via des messages de publicité de routeur (RA).
4.  **Absence de NAT pour la pénurie d'adresses**: Grâce à l'énorme espace d'adressage, le NAT (Traduction d'Adresses Réseau), souvent utilisé en IPv4 pour pallier la pénurie d'adresses, n'est plus nécessaire à cette fin, simplifiant la connectivité de bout en bout et les applications client-serveur.
5.  **Prise en charge de Multicast et Anycast**: IPv6 remplace les diffusions d'IPv4 par le multicast (envoi à un groupe spécifique) et l'anycast (envoi à l'hôte le plus proche d'un groupe), permettant une livraison plus efficace des paquets.
* **Ports par défaut**: Le Protocole Internet version 6 opère à la couche réseau (couche 3) et n'utilise pas de ports au sens des protocoles de transport comme TCP ou UDP.

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * **Visibilité réduite / Dérive de configuration**: La complexité de la transition ou la méconnaissance d'IPv6 peut entraîner des services IPv6 actifs mais non sécurisés ou monitorés, créant des failles de sécurité.
  * **Contournement des contrôles**: Des pare-feux ou IPS mal configurés pour IPv6 peuvent être contournés, permettant à des logiciels malveillants ou des APT de s'infiltrer.
  * **Attaques NDP**: Des vulnérabilités similaires au spoofing ARP d'IPv4 existent pour le NDP (par exemple, empoisonnement du cache NDP), permettant des attaques de l'homme du milieu.
  * **Falsification de RA**: Un acteur de menace peut annoncer de fausses informations de routage pour rediriger le trafic.
  * **Attaques DoS**: L'exploitation de fragments IPv6 ou de paquets malformés peut être utilisée pour des attaques par déni de service.
* **Sécurité intégrée**:
  * IPsec est une exigence fondamentale dans IPv6, facilitant le chiffrement de bout en bout et l'authentification des paquets IP, offrant une base sécurisée pour les communications.
  * **Gestion des vulnérabilités**: Audits réguliers des configurations IPv6 pour identifier et corriger les faiblesses.
  * **Contrôle d'accès**: Mettre en œuvre des politiques NAC pour contrôler les périphériques connectés via IPv6.
  * **Configuration des pare-feux**: Assurer que les règles de pare-feu sont correctement appliquées au trafic IPv6, idéalement en mode "deny by default".
  * **Systèmes de détection d'intrusion (IDS) / IPS**: Déployer des systèmes capables de surveiller et de bloquer les attaques spécifiques à IPv6.
  * **Segmentation réseau**: Isoler les systèmes critiques et limiter la propagation des menaces.
  * **Sensibilisation**: Former les équipes techniques aux spécificités et aux risques de sécurité d'IPv6.

## 🔗 Notes Connexes
*   IPv4
*   Neighbor Discovery Protocol (NDP)
*   IPsec
*   NAT
*   Dual-Stack
*   DHCPv6
*   Couche réseau
*   Modèle TCP/IP
*   Modèle OSI
*   Paquet
*   Routage
*   IETF
*   IANA
*   Adresses Unicast
*   Multicast
*   Anycast
*   Mécanismes de transition IPv4 vers IPv6
*   Wireshark