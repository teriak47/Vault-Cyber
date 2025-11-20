---
tags:
  - reseau
  - ip/addressing
aliases:
  - Adresse IP Publique
  - Public IP Address
  - Adresse Internet Routable
  - Routable IP Address
archetype: concept-general
rfc:
source:
cssclasses:
  - max
---

# Adresse IP Publique

## 🎯 Définition et Caractéristiques
> Une adresse IP publique est une adresse IP globalement unique et routable sur l'Internet. Elle est utilisée pour identifier un appareil ou un réseau sur le réseau mondial, permettant ainsi la communication directe avec des services en ligne externes.

## ⚙️ Fonctionnement et Attributions
Les adresses IP publiques sont essentielles pour la connectivité Internet et le routage des paquets de données.

1.  **Globalement Unique**: Chaque adresse IP publique est unique à l'échelle de l'Internet à un moment donné, évitant les conflits d'adressage.
2.  **Attribution**: Elles sont généralement attribuées par les Fournisseurs d'Accès Internet (FAI) à un routeur ou un serveur en amont du réseau domestique ou du réseau d'entreprise.
3.  **Accessibilité**: Elles permettent à un hôte ou à un réseau d'être directement accessible depuis n'importe quel point de l'Internet, ce qui est crucial pour héberger des serveurs web, des serveurs de fichiers ou d'autres services en ligne.
4.  **Types**: Une adresse IP publique peut être:
    *   **Statique**: Une adresse fixe qui ne change pas, souvent utilisée pour les serveurs ou les périphériques réseau nécessitant une identification constante.
    *   **Dynamique**: Une adresse allouée temporairement par un serveur DHCP et qui peut changer périodiquement.
5.  **Distinction avec les adresses privées**: Contrairement aux adresses IP privées, qui sont utilisées au sein d'un LAN et ne sont pas routables sur l'Internet, les adresses IP publiques sont directement exposées au réseau mondial.

## 🛡️ Implications de Sécurité
L'exposition d'une adresse IP publique rend les systèmes et réseaux potentiellement visibles et accessibles à tous les acteurs de menace sur l'Internet.

*   **Risques et Menaces Associés**:
    *   Attaques par déni de service distribué (DDoS) visant à saturer la bande passante ou les ressources du serveur ou du réseau ciblé.
    *   Scans de ports et tentatives de reconnaissance pour découvrir les services actifs et les vulnérabilités logicielles potentielles.
    *   Fuite d'informations via des services mal configurés ou des bugs logiciels sur les serveurs exposés.
    *   Exploitation de vulnérabilités logicielles sur les serveurs ou périphériques réseau accessibles publiquement.
    *   Attaques par force brute sur les mécanismes d'authentification des services exposés.

*   **Mesures de Protection et Bonnes Pratiques**:
    *   Implémenter un pare-feu robuste pour contrôler et filtrer le trafic réseau entrant et sortant, en n'autorisant que les connexions légitimes et nécessaires.
    *   Utiliser la Traduction d'Adresses Réseau (NAT) pour masquer les adresses IP privées du réseau interne et n'exposer que les serveurs ou applications spécifiques via le pare-feu.
    *   Déployer un VPN pour chiffrer le transfert de données et sécuriser l'accès distant aux ressources internes.
    *   Assurer la gestion des patchs et les mises à jour régulières de tous les systèmes d'exploitation, logiciels et micrologiciels des périphériques réseau exposés publiquement.
    *   Désactiver les protocoles et services en ligne inutiles ou non essentiels sur les hôtes avec des adresses IP publiques afin de réduire la surface d'attaque.
    *   Appliquer le principe du moindre privilège pour tous les utilisateurs et processus accédant ou étant exposés publiquement.

## 🔗 Notes Connexes
*   Adresse IP Privée
*   NAT
*   Protocole Internet
*   IPv4
*   IPv6
*   Adressage IP
*   Adresse Internet Routable