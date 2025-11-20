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
> Le Dual Stack est un mécanisme de transition permettant aux équipements réseau et aux hôtes d'opérer simultanément avec les protocoles Internet version 4 (InternetProtocolVersion4) et Internet Protocol version 6 (InternetProtocolVersion6). Son rôle est d'assurer une interopérabilité continue pendant la migration progressive de l'Internet vers IPv6, en gérant les deux piles de protocoles au niveau de la couche réseau.

## ⚙️ Fonctionnement
1.  **Nécessité de la Transition**: Crucial en raison de l'épuisement des adresses IPv4 et de la nécessité de migrer vers IPv6. Il permet une coexistence transparente des deux versions.
2.  **Implémentation Indépendante**: Un même hôte ou équipement réseau maintient deux piles de protocoles (une pour IPv4 et une pour IPv6) sur la même carte d'interface réseau. Cela permet à l'interface de recevoir et d'envoyer des paquets IPv4 et IPv6 simultanément.
3.  **Flexibilité de Communication**: Grâce à cette double implémentation, un dispositif Dual Stack peut communiquer directement avec des dispositifs utilisant soit IPv4, soit IPv6, sans recourir à des techniques intermédiaires comme la tunnelisation ou la traduction d'adresses.
4.  **Différenciation avec Autres Mécanismes**: Le Dual Stack se distingue de la tunnelisation (qui encapsule un protocole dans l'autre) et de la traduction (qui convertit les adresses entre les deux versions), offrant une gestion native des deux piles.
* **Ports par défaut**: Non applicable, car il ne s'agit pas d'un protocole d'application avec des ports dédiés, mais d'une capacité d'un système à gérer les protocoles IP aux niveaux inférieurs.

## 🛡️ Sécurité du Dual Stack
* **Vulnérabilités et défis connus**:
  *   **Élargissement de la Surface d'attaque**: La gestion de deux piles de protocoles distinctes peut introduire de nouvelles vulnérabilités si les deux ne sont pas correctement sécurisées, doublant potentiellement les points d'entrée pour les attaquants.
  *   **Complexité des politiques de sécurité**: Les règles de pare-feu et les contrôles d'accès doivent être configurés pour les deux versions de l'IP, augmentant le risque d'erreurs de configuration ou d'omissions.
  *   **Attaques de routage**: Des acteurs malveillants pourraient exploiter les différences ou les faiblesses de routage entre IPv4 et IPv6 pour intercepter ou rediriger le trafic réseau.
* **Mesures de protection et bonnes pratiques**:
  *   **Sécurité dès la conception**: Intégrer la sécurité pour les deux piles (IPv4 et IPv6) dès la planification et la configuration des systèmes et des réseaux.
  *   **Configuration des pare-feu Rigoureuse**: Appliquer des règles de pare-feu robustes et cohérentes pour le trafic IPv4 et IPv6, en s'assurant qu'aucune faille n'existe.
  *   **Audits de sécurité Réguliers**: Effectuer des tests d'intrusion et des audits de sécurité pour identifier et corriger les vulnérabilités spécifiques au Dual Stack, y compris les erreurs de configuration.
  *   **Sensibilisation et Formation**: S'assurer que les équipes cybersécurité et réseau sont formées aux spécificités de la sécurité IPv6 et aux défis posés par le Dual Stack.

## 🔗 Notes Connexes
*   Internet Protocol version 4
*   Internet Protocol version 6
*   Protocoles Réseau
*   Mécanismes de Transition IPv6
*   Couche Réseau
*   Surface d'attaque
*   Vulnérabilités de sécurité
*   Pare-feu
*   Contrôles d'accès
*   Attaques de routage