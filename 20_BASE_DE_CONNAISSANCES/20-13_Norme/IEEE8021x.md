---
tags:
  - norme
  - norme/ieee8021x
  - authentification
  - controle/acces
  - securite/reseau
aliases:
  - IEEE 802.1X
  - 802.1X
  - Port-Based Network Access Control
archetype: norme
source:
  - 
cssclasses:
  - max
---

# IEEE 802.1X (Contrôle d'Accès Réseau Basé sur les Ports)

## 🎯 Objectif et Périmètre

La norme IEEE 802.1X est une norme du groupe de travail IEEE 802 qui définit un mécanisme d'authentification pour le contrôle d'accès réseau basé sur les ports. 
Son objectif principal est de fournir un cadre d'authentification pour les dispositifs souhaitant se connecter à un réseau, qu'il soit un LAN filaire ou un WLAN. 
Elle permet ainsi d'empêcher l'accès non autorisé aux ressources du réseau en exigeant que les utilisateurs et les dispositifs s'authentifient avant d'obtenir un accès complet.

## 🔑 Principales Exigences / Sections
*   **Composants Clés**: Le modèle 802.1X implique trois rôles principaux :
    *   Le **Supplicant**: Le client ou le dispositif (ex: ordinateur, téléphone intelligent, tablette) qui demande l'accès au réseau.
    *   L'**Authenticator**: Généralement un commutateur (pour les réseaux filaires) ou un point d'accès (pour les réseaux sans fil), qui agit comme un intermédiaire. Il transmet les messages d'authentification entre le supplicant et le serveur d'authentification et bloque ou autorise l'accès physique au réseau en fonction du résultat.
    *   Le **Serveur d'Authentification**: Un serveur centralisé, souvent un serveur RADIUS, qui contient la base de données des identifiants et effectue la vérification des identifiants du supplicant. Il envoie ensuite une décision d'autorisation ou de refus à l'authenticator.
*   **Protocole d'Authentification (EAP)**: L'Extensible Authentication Protocol (EAP) est le protocole utilisé pour encapsuler et échanger les messages d'authentification entre les trois parties. Il est extensible et prend en charge diverses méthodes d'authentification, telles que EAP-TLS, PEAP ou EAP-TTLS, offrant une flexibilité pour différents scénarios de sécurité.
*   **Contrôle des Ports**: L'Authenticator contrôle l'état des ports réseau (physiques ou virtuels). Avant une authentification réussie, le port est "non autorisé", ce qui signifie que seul le trafic EAP est permis. Une fois l'authentification réussie, le port passe à l'état "autorisé", donnant au supplicant un accès complet au réseau.

## 📈 Bénéfices de la Conformité
*   **Sécurité Renforcée**: En imposant l'authentification à la périphérie du réseau, 802.1X réduit considérablement le risque d'accès non autorisé, même pour des connexions physiques.
*   **Visibilité et Contrôle**: Il offre une visibilité granulaire sur qui et quoi se connecte au réseau, permettant une application plus stricte des politiques de sécurité.
*   **Conformité Règlementaire**: L'implémentation de 802.1X peut aider les organisations à satisfaire les exigences de diverses réglementations et normes de sécurité qui exigent un contrôle rigoureux de l'accès.
*   **Segmentation Dynamique**: En intégrant 802.1X avec des solutions de VLAN, il est possible d'attribuer dynamiquement les appareils et les utilisateurs à des segments réseau spécifiques après authentification, renforçant la segmentation réseau.

## 📜 Certifications Associées
La norme IEEE 802.1X elle-même n'est pas une certification. Cependant, elle est un élément clé des certifications de sécurité WPA2-Enterprise et WPA3-Enterprise pour les réseaux Wi-Fi, qui exigent son utilisation pour une authentification robuste.

## 🔗 Notes Connexes
*   **Principe de sécurité**: Principe du Moindre Privilège
*   **Modèle d'architecture**: Conception de Réseau Hiérarchique
*   **Contrôle d'accès avancé**: Contrôle d'accès basé sur les rôles (RBAC)
*   **Menace mitigée**: Usurpation d'adresse MAC
*   **Protocole complémentaire**: DHCP