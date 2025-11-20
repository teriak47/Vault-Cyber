---
tags:
  - protocole
aliases:
  - SSH
  - Secure Shell Protocol
  - Shell Sécurisé
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Secure Shell (SSH)

## 🎯 Rôle et Couche OSI
> SSH (Secure Shell) est un protocole réseau cryptographique qui fournit un accès sécurisé aux ordinateurs sur un réseau non sécurisé, tel qu'Internet. Il permet l'exécution de commandes à distance, le transfert de fichiers sécurisé (via SCP et SSHFileTransferProtocol) et la redirection de port. Il opère principalement à la couche Application du modèle TCP/IP.

## ⚙️ Fonctionnement
1.  **Établissement de la session**: Le client SSH initie une connexion avec le serveur SSH (généralement sur le port TCP/22). Un échange de clés cryptographiques a lieu pour établir un canal sécurisé.
2.  **Authentification**: Le client s'authentifie auprès du serveur. Cela peut se faire via un mot de passe, des clés publiques/privées (méthode la plus courante et sécurisée), ou d'autres mécanismes d'authentification.
3.  **Chiffrement et Intégrité**: Une fois authentifié, toutes les communications entre le client et le serveur sont chiffrées pour garantir la confidentialité et l'intégrité des données échangées.
*   **Ports par défaut**: TCP/22

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Faiblesses dans les implémentations logicielles de SSH ou dans la gestion des clés (clés faibles, réutilisation, non-rotation).
    *   Attaques par force brute ou dictionnaire sur les mots de passe si l'authentification par mot de passe est utilisée et mal configurée (par exemple, sans limitation de débit ou MFA).
    *   Attaques de l'homme du milieu si les clés hôtes du serveur ne sont pas correctement vérifiées lors de la première connexion.
    *   Exploitation de vulnérabilités logicielles dans les clients ou serveurs SSH (ex: dépassement de tampon).
*   **Mesures de sécurité**:
    *   Utiliser des versions récentes et à jour du protocole et des implémentations.
    *   Préférer l'authentification par clé publique/privée plutôt que par mot de passe.
    *   Mettre en œuvre une politique de mots de passe forts et l'authentification multi-facteurs pour les accès par mot de passe.
    *   Effectuer une gestion rigoureuse des clés SSH (génération sécurisée, stockage, rotation, révocation).
    *   Restreindre l'accès au port SSH (22) via un pare-feu.
    *   Implémenter un système de détection d'intrusion ou de prévention d'intrusion pour surveiller les tentatives d'accès.

## 🔗 Notes Connexes
*   Couche Application
*   Modèle TCP/IP
*   Authentification
*   Chiffrement
*   FTP (alternative non sécurisée pour le transfert de fichiers)
*   Outil pour l'analyse de protocole (Wireshark)
*   Exécution de Code à Distance
*   Gestion des Clés
*   Redirection de Port
*   SCP
*   SSHFileTransferProtocol