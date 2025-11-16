---
tags:
  - protocole
aliases:
  - SFTP
  - SSH File Transfer Protocol
  - Secure File Transfer Protocol
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocole de Transfert de Fichiers SSH (SFTP)

## 🎯 Rôle et Couche OSI
Le Protocole de Transfert de Fichiers [[SecureShell|SSH]] (SFTP) est un [[NetworkProtocol|protocole réseau]] qui fournit des capacités de transfert, d'accès et de gestion de fichiers fiables et sécurisées. Il est conçu pour fonctionner sur une connexion de données [[SecureShell|SSH]] établie, offrant ainsi une couche de [[Cryptography|cryptographie]] et d'[[Authentication|authentification]] robuste.

SFTP opère principalement à la [[ApplicationLayer|couche application]] du [[InternetProtocolSuite|modèle TCP/IP]], en s'appuyant sur les services sécurisés de [[SecureShell|SSH]] qui, lui-même, utilise le [[TransmissionControlProtocol|TCP]] à la [[TransportLayer|couche transport]].

## ⚙️ Fonctionnement
1.  **Établissement de la connexion SSH**: Un client SFTP initie une connexion à un [[Server|serveur]] SFTP. Cette connexion est d'abord une session [[SecureShell|SSH]], où le client et le serveur effectuent l'[[Authentication|authentification]] et établissent un canal de communication sécurisé et chiffré.
2.  **Initialisation du sous-système SFTP**: Une fois la session [[SecureShell|SSH]] établie, le client demande au serveur de démarrer le sous-système SFTP. Le serveur répond en envoyant une confirmation et en indiquant la version du protocole SFTP à utiliser.
3.  **Opérations de fichiers**: Le client SFTP envoie ensuite des requêtes au serveur via le canal [[SecureShell|SSH]] chiffré pour effectuer diverses opérations de fichiers. Celles-ci incluent:
    *   Lister le contenu des répertoires.
    *   Télécharger des [[FileTransfer|fichiers]] du serveur vers le client.
    *   Uploader des [[FileTransfer|fichiers]] du client vers le serveur.
    *   Créer, supprimer et renommer des [[FileTransfer|fichiers]] et des répertoires.
    *   Modifier les permissions des [[FileTransfer|fichiers]].
4.  **Transfert de données**: Toutes les données et commandes sont encapsulées et chiffrées par [[SecureShell|SSH]], garantissant la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] pendant le [[DataTransmission|transfert]].
* **Ports par défaut**: SFTP utilise le même [[PortNumber|port]] par défaut que [[SecureShell|SSH]], soit [[PortNumber|TCP/22]].

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  * Étant donné que SFTP s'exécute sur [[SecureShell|SSH]], sa sécurité dépend fortement de la robustesse de l'implémentation et de la configuration de [[SecureShell|SSH]]. Les vulnérabilités seraient plutôt liées à [[SecureShell|SSH]] lui-même (par exemple, des failles dans les algorithmes de [[Cryptography|cryptographie]], des clés [[PrivateKey|privées]] compromises, des [[StrongPasswordPolicy|politiques de mot de passe]] faibles permettant des [[BruteForceAttack|attaques par force brute]] ou du [[CredentialStuffing|bourrage d'identifiants]]).
  * Une mauvaise gestion des [[AccessControl|contrôles d'accès]] sur le [[FileServer|serveur de fichiers]] peut permettre un [[UnauthorizedAccess|accès non autorisé]] même si la connexion est sécurisée.
* **Versions sécurisées**:
  * SFTP est lui-même une méthode de transfert de [[FileTransfer|fichiers]] sécurisée. Il est la version sécurisée du protocole [[FileTransferProtocol|FTP]] non chiffré. Il n'y a pas de "version sécurisée" de SFTP en tant que telle, mais plutôt des configurations [[SecureShell|SSH]] plus robustes et des pratiques de [[SecurityPolicy|politiques de sécurité]] strictes pour son utilisation.

## 🔗 Notes Connexes
* [[SecureShell|SSH]]
* [[FileTransferProtocol|FTP]]
* [[TransmissionControlProtocol|TCP]]
* [[Cryptography|Cryptographie]]
* [[Wireshark|Outil pour l'analyser (ex: Wireshark)]]