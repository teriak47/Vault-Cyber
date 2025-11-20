---
tags:
  - adressage
  - reseau
  - ipv4
aliases:
  - Adresse IP de Destination IPv4
  - Destination IPv4 Address
  - Destination IP Address
  - Destination Internet Protocol Version 4 Address
archetype: concept-general
rfc:
cssclasses:
  - max
---

# Adresse IP de Destination IPv4

## 🎯 Rôle et Couche OSI
> L'adresse IP de destination IPv4 est l'identifiant numérique unique du système final destiné à recevoir un paquet de données au sein d'un réseau IPv4. Elle opère principalement à la couche Réseau du modèle TCP/IP, responsable de l'adressage logique et du routage inter-réseaux.

## ⚙️ Fonctionnement
1.  **Identification du destinataire**: Chaque paquet IPv4 contient une adresse IP source et une adresse IP de destination. Cela permet aux périphériques réseau et aux routeurs d'acheminer le paquet vers son récepteur final.
2.  **Rôle des routeurs**: Les routeurs examinent l'adresse IP de destination dans l'en-tête du paquet pour déterminer le chemin optimal à travers l'Internet ou un réseau d'entreprise, en utilisant leur table de routage.
3.  **Types d'adressage**: L'adresse de destination peut prendre différentes formes pour cibler :
    *   **Unidiffusion**: Un seul destinataire spécifique.
    *   **Multidiffusion**: Un groupe de destinataires spécifiques.
    *   **Diffusion**: Tous les destinataires sur un segment de réseau donné.
4.  **Encapsulation et décapsulation**: Lors de la transmission des données, le paquet IPv4 avec son adresse de destination est encapsulé dans une trame Ethernet (ou équivalent) à la couche Liaison de Données. L'adresse de destination est lue et traitée lors de la décapsulation à chaque saut de routeur pour un routage correct.

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Usurpation d'adresse IP (IP Spoofing) : Un attaquant peut falsifier l'adresse IP source pour masquer son identité ou diriger des réponses vers une autre cible.
    *   Attaques par déni de service (DoS) et attaques par déni de service distribué (DDoS) : L'envoi de vastes volumes de paquets avec des adresses de destination légitimes peut submerger un serveur ou un réseau, provoquant une interruption de service.
    *   Écoute clandestine : Si le routage est compromis, des paquets destinés à une cible légitime peuvent être redirigés ou interceptés par un attaquant.
*   **Mesures de protection**:
    *   **Pare-feux**: Configurer des pare-feux pour filtrer le trafic entrant et sortant en fonction des adresses IP de destination autorisées.
    *   **Segmentation réseau**: Utiliser des VLAN et d'autres méthodes de segmentation réseau pour isoler les services et réduire la surface d'attaque.
    *   **Systèmes de prévention d'intrusion (IPS)**: Déployer des IPS pour détecter et bloquer le trafic malveillant basé sur l'analyse des adresses de destination et du comportement.
    *   **Protocoles de routage sécurisés**: Implémenter des protocoles de routage sécurisés pour prévenir les modifications non autorisées des tables de routage et les redirections de trafic malveillantes.
    *   **Contrôles au niveau de la couche d'accès réseau**: Mettre en œuvre le filtrage de ports et d'autres contrôles sur les commutateurs réseau pour empêcher les usurpations d'adresses MAC et IP.

## 🔗 Notes Connexes
*   Adresse IP Source IPv4
*   Adresse IP
*   Internet Protocol version 4
*   Couche Réseau
*   Routeur
*   Paquet
*   Modèle TCP/IP
*   Wireshark