---
tags:
  - protocole
  - protocole/routage
aliases:
  - Protocoles de Routage Sécurisés
  - Secure Routing Protocols
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocoles de Routage Sécurisés

## 🎯 Rôle et Couche OSI
> Les protocoles de routage sécurisés sont des extensions ou des implémentations renforcées des protocoles réseau standards. Leur rôle principal est de protéger les informations de routage contre les attaques, en garantissant l'intégrité et l'authentification des mises à jour de routage. Ils opèrent principalement au niveau de la couche réseau du modèle OSI et du modèle TCP/IP.

## ⚙️ Fonctionnement
1.  **Authentification des Mises à Jour**: Ces protocoles intègrent des mécanismes cryptographiques pour vérifier l'origine et l'authenticité des messages de routage. Cela empêche les entités non autorisées (acteurs de menace) d'injecter ou de modifier des informations de routage, évitant ainsi les usurpations et les fausses annonces.
2.  **Intégrité des Données**: Ils utilisent des fonctions de hachage et des signatures numériques pour s'assurer que les informations de routage n'ont pas été altérées (altérées) pendant la transmission. Tout changement non autorisé rendrait l'information invalide et serait rejeté.
3.  **Prévention des Anomalies de Routage**: L'objectif est de contrer des problèmes graves qui peuvent perturber la connectivité réseau, tels que les boucles de routage persistantes, les trous noirs de routage (où le trafic est dirigé vers une destination inexistante) et les annonces de routes non valides.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités atténuées**:
    *   Attaques de routage (y compris attaques de l'homme du milieu sur les informations de routage)
    *   Détournement de routes (où un attaquant annonce des routes qu'il ne possède pas)
    *   Injection de routes malveillantes
    *   Altération des messages de routage
*   **Implémentations et versions sécurisées**:
    *   **BGPsec**: Une extension du Border Gateway Protocol qui utilise la cryptographie pour authentifier l'ensemble du chemin d'une route, renforçant la confiance dans les annonces de routes entre systèmes autonomes.
    *   **OSPFv3 avec IPsec**: Le protocole Open Shortest Path First pour IPv6 peut être sécurisé en utilisant IPsec pour chiffrer et authentifier l'échange de ses messages, garantissant la confidentialité et l'intégrité.
    *   **RPKI (Resource Public Key Infrastructure)**: Un système de PKI qui authentifie la propriété des blocs d'adresses IP et des numéros de système autonome (ASN). Il permet aux opérateurs de réseau de vérifier que les annonces de routes sont légitimes, prévenant ainsi les détournements de routes.

## 🔗 Notes Connexes
*   Routage
*   Couche Réseau
*   Internet Protocol
*   Protocole Réseau
*   IPsec
*   Signature Numérique
*   Acteur de Menace