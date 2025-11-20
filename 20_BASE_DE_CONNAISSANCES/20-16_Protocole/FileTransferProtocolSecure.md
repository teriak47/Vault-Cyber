---
tags:
  - protocole
aliases:
  - Protocole de Transfert de Fichiers Sécurisé
  - FTPS
  - File Transfer Protocol Secure
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocole de Transfert de Fichiers Sécurisé (FTPS)

## 🎯 Rôle et Couche OSI
Le FTPS est une extension du Protocole de Transfert de Fichiers (FTP) qui ajoute des fonctionnalités de sécurité par l'utilisation de TLS (ou historiquement SSL). Il est conçu pour sécuriser les transferts de fichiers sur un réseau en fournissant l'intégrité et la confidentialité des données. Il opère à la couche Application du modèle TCP/IP.

## ⚙️ Fonctionnement
Le FTPS fonctionne en encapsulant les commandes et les données du FTP dans une connexion TLS chiffrée. Il existe deux modes principaux :

1.  **FTPS Explicite (AUTH TLS)**:
    *   Le client se connecte d'abord sur un port FTP standard (généralement TCP/21).
    *   Le client initie explicitement une négociation TLS en envoyant la commande `AUTH TLS`.
    *   Si la négociation réussit, le canal de communication de contrôle et/ou de données est chiffré.
2.  **FTPS Implicite**:
    *   Le client se connecte directement à un port désigné pour le FTPS implicite (généralement TCP/990 pour le contrôle et TCP/989 pour les données).
    *   La connexion TLS est établie immédiatement au début de la session, sans commande de négociation.

*   **Ports par défaut**:
    *   **Contrôle**: TCP/21 (FTPS Explicite), TCP/990 (FTPS Implicite)
    *   **Données**: TCP/20 (mode actif, avec TLS négocié via le canal de contrôle), ou des ports dynamiques (mode passif), TCP/989 (FTPS Implicite)

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   **Configuration incorrecte de certificats**: Si les certificats numériques du serveur ne sont pas correctement validés par le client, une attaque de l'homme du milieu reste possible.
    *   **Vulnérabilités du FTP sous-jacent**: Bien que le FTPS chiffre le trafic, il peut hériter de certaines vulnérabilités logicielles ou dérives de configuration de l'implémentation FTP sous-jacente.
    *   **Problèmes de pare-feu**: Le mode passif du FTP (et donc du FTPS) peut être difficile à gérer avec les pare-feux en raison de l'utilisation de ports de données dynamiques, potentiellement conduisant à des vulnérabilités de sécurité si les règles de pare-feu ne sont pas strictes.
    *   **Exposition de la liste de répertoires**: Si les informations de liste de répertoires sont chiffrées mais que des métadonnées (comme les noms de fichiers) sont divulguées avant la négociation TLS dans le mode explicite, une certaine exposition involontaire d'information est possible.
*   **Versions sécurisées**:
    *   Le FTPS est la version sécurisée du FTP grâce à l'intégration de TLS.
    *   Alternativement, le SFTP (SSH File Transfer Protocol) offre une méthode de transfert de fichiers sécurisée basée sur SSH, qui est une approche de sécurité fondamentalement différente et souvent préférée pour sa simplicité de gestion des pare-feux.

## 🔗 Notes Connexes
*   Protocole de Transfert de Fichiers (FTP)
*   Transport Layer Security (TLS)
*   Secure Sockets Layer (SSL)
*   Certificat Numérique
*   SSH File Transfer Protocol (SFTP)
*   Authentification
*   Confidentialité
*   Intégrité
*   Wireshark