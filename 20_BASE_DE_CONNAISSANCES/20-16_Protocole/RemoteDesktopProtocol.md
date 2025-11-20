---
tags:
  - protocole
  - protocole/rdp
  - acces/distance
  - communication/reseau
  - connexion
aliases:
  - Protocole de Bureau à Distance
  - RDP
  - Remote Desktop Protocol
archetype: protocole
rfc:
cssclasses:
  - max
---

# Remote Desktop Protocol (RDP)

## 🎯 Rôle et Couche OSI
> Le Remote Desktop Protocol (RDP) est un protocole propriétaire développé par Microsoft, qui permet à un utilisateur de se connecter à distance à un ordinateur exécutant des services Windows Terminal Services ou Remote Desktop Services. Il fournit une interface graphique à l'utilisateur depuis le client RDP. Il opère principalement à la couche application (couche 7) du modèle OSI, en s'appuyant sur les services de la couche transport (TCP).

## ⚙️ Fonctionnement
1.  **Initiation de la Connexion**: Le client RDP initie une connexion TCP sur le port 3389 (par défaut) vers le serveur RDP. Une fois la connexion TCP établie, une séquence de négociation RDP est lancée, y compris l'échange de capacités et l'authentification de l'utilisateur.
2.  **Transfert de Données**: Après une authentification réussie, le serveur envoie les mises à jour de l'écran graphique au client RDP, tandis que le client transmet les entrées (clavier, souris) au serveur. Le RDP optimise la transmission des données en envoyant uniquement les modifications de l'écran.
3.  **Gestion de Session**: Le protocole gère la session à distance, permettant à l'utilisateur d'interagir avec le système distant comme s'il était directement assis devant. La session peut être déconnectée et reconnectée sans perdre le travail en cours.
* **Ports par défaut**: TCP/3389

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  *   Attaques par force brute et bourrage d'identifiants contre les informations d'identification RDP.
  *   Vulnérabilités logicielles dans les implémentations RDP du serveur ou du client, pouvant mener à des exécutions de code à distance (ex: BlueKeep).
  *   Attaques de l'homme du milieu si la connexion n'est pas correctement chiffrée.
  *   Exposition des services RDP directement sur l'Internet sans protections adéquates, augmentant la surface d'attaque.
* **Mesures de mitigation et versions sécurisées**:
  *   Utilisation de l'authentification multi-facteurs (MFA).
  *   Mise en œuvre de politiques de mots de passe forts et de mécanismes de verrouillage de compte.
  *   Chiffrement de la connexion via TLS/SSL pour protéger les informations d'identification et les données en transit.
  *   Restriction de l'accès RDP via des pare-feu ou des listes de contrôle d'accès (ACL).
  *   Utilisation de VPN pour isoler le trafic RDP sur un tunnel sécurisé.
  *   Gestion des patchs et mises à jour régulières des systèmes RDP pour corriger les vulnérabilités connues.
  *   Segmentation réseau pour isoler les serveurs RDP sensibles.

## 🔗 Notes Connexes
* **Couche OSI**: ApplicationLayer
* **Sécurité associée**: NetworkSecurity
* **Contrôle d'accès**: Authentication
* **Accès sécurisé**: VirtualPrivateNetwork
* **Type d'attaque**: BruteForceAttack