---
tags:
  - reseau
  - ip/addressing
aliases:
  - Adresse IP Privée
  - Private IP Address
  - Adresse IP Interne
  - Internal IP Address
archetype: concept-general
rfc:
  - RFC 1918
  - RFC 4193
cssclasses:
  - max
---

# Adresse IP Privée

## 🎯 Rôle et Place dans l'Architecture Réseau
> Une adresse IP privée est un type d'adressage IP conçu pour être utilisé exclusivement au sein d'un réseau local (LAN) ou d'un réseau interne. Ces adresses ne sont pas routables sur l'Internet public, offrant une isolation native et opérant principalement au niveau de la couche réseau du modèle TCP/IP.

## ⚙️ Fonctionnement et Caractéristiques Clés
1.  **Non-Routabilité Publique**: Les paquets de données dont l'adresse IP de destination est une adresse privée sont bloqués et ne sont pas acheminés par les routeurs de l'Internet public. Cette caractéristique fondamentale assure une première couche de sécurité et d'isolation pour les réseaux internes.
2.  **Réutilisation Globale**: Les mêmes plages d'adresses IP privées peuvent être utilisées de manière indépendante et simultanée dans un nombre illimité de réseaux locaux différents sans causer de conflits d'adressage IP globaux.
3.  **Plages Réservées pour IPv4 (RFC 1918)**:
    *   Classe A: `10.0.0.0` à `10.255.255.255` (bloc `/8`) - Masque de sous-réseau par défaut: `255.0.0.0`
    *   Classe B: `172.16.0.0` à `172.31.255.255` (bloc `/12`) - Masque de sous-réseau par défaut: `255.255.0.0`
    *   Classe C: `192.168.0.0` à `192.168.255.255` (bloc `/16`) - Masque de sous-réseau par défaut: `255.255.255.0`
4.  **Plages Réservées pour IPv6**:
    *   Adresses Uniques Locales (ULA): `fc00::/7` (RFC 4193). Similaires aux adresses IP privées IPv4, elles sont utilisées pour la communication locale et ne sont pas routées sur l'Internet global.
    *   Adresses Link-Local: `fe80::/10`. Utilisées pour la communication au sein d'un même segment de réseau, elles sont automatiquement configurées et ne sont pas routables au-delà du lien local.
5.  **Communication Externe**: Pour qu'un appareil configuré avec une adresse IP privée puisse accéder aux services en ligne sur l'Internet, son trafic doit passer par un processus de Traduction d'Adresses Réseau (NAT). Ce processus est généralement effectué par un routeur ou un pare-feu situé à la passerelle du réseau interne, traduisant l'adresse IP privée en une adresse IP publique routable.

## 🛡️ Sécurité et Bonnes Pratiques
*   **Vulnérabilités associées**:
    *   **Menaces internes**: Bien que les adresses IP privées ne soient pas directement accessibles depuis l'extérieur, elles sont la cible principale des menaces provenant de l'intérieur du réseau ou d'attaques ayant déjà compromis le périmètre.
    *   **Dérive de configuration et exposition involontaire**: Une mauvaise configuration du NAT ou des règles de pare-feu peut entraîner l'exposition accidentelle de serveurs ou ressources internes à l'Internet public, créant ainsi des vulnérabilités de sécurité.
*   **Mesures de Protection / Bonnes Pratiques**:
    *   **Segmentation Réseau**: L'utilisation de VLANs et le sous-réseautage permettent d'isoler différents groupes d'appareils et de utilisateurs au sein du réseau privé, limitant ainsi la propagation d'logiciels malveillants ou d'attaques.
    *   **Règles de Pare-feu**: Implémenter des contrôles de sécurité stricts via des pare-feu pour réguler et filtrer le trafic réseau entre les différents segments privés et entre le réseau interne et l'Internet externe.
    *   **Audit de Configuration Réseau**: Des audits réguliers de la configuration réseau sont essentiels pour identifier et corriger toute vulnérabilité ou exposition involontaire due à une configuration erronée ou obsolète.

## 🔗 Notes Connexes
*   Adresse IP Publique
*   Traduction d'Adresses Réseau (NAT)
*   Réseau Local (LAN)
*   Protocole Internet (IP)
*   Protocole Internet version 4 (IPv4)
*   Protocole Internet version 6 (IPv6)
*   Subdivision de réseau
*   Adressage IP
*   Couche Réseau
*   Adressage Hiérarchique
*   DHCP
*   Adresse Internet Routable
---