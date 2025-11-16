---
aliases:
  - Protocole de Transfert de Fichiers
  - FTP
  - File Transfer Protocol
archetype: protocole
rfc: RFC 959
cssclasses:
  - max
---

# Protocole de Transfert de Fichiers (FTP)

## 🎯 Rôle et Couche OSI
> Le [[FileTransferProtocol|Protocole de Transfert de Fichiers (FTP)]] est un [[NetworkProtocol|protocole réseau]] client-serveur utilisé pour le transfert de [[Data|fichiers]] entre un [[Client|client]] et un [[Server|serveur]] sur un [[Network|réseau]] [[TransmissionControlProtocol|TCP/IP]]. Il opère à la [[ApplicationLayer|couche Application]] du [[OpenSystemsInterconnectionModel|modèle OSI]] et du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
1.  **Établissement des Connexions**: FTP établit deux connexions distinctes entre le client et le serveur :
    *   **Canal de contrôle**: Sur le [[PortNumber|port]] [[TransmissionControlProtocol|TCP]]/21, utilisé pour l'échange de commandes (authentification, commandes de gestion de fichiers) et de réponses.
    *   **Canal de données**: Généralement sur le port TCP/20 (mode actif) ou un port éphémère négocié (mode passif), utilisé pour le transfert effectif des données de fichiers.
2.  **Authentification**: Le client se connecte au serveur FTP et fournit des [[Credential|informations d'identification]] ([[Username|nom d'utilisateur]] et [[Password|mot de passe]]) pour l'[[Authentication|authentification]]. Certains serveurs peuvent autoriser des connexions anonymes.
3.  **Transfert de Données**: Une fois authentifié, le client peut utiliser des commandes pour naviguer dans le système de fichiers du serveur, télécharger ([[FileTransfer|GET]]) des fichiers depuis le serveur, ou téléverser ([[FileTransfer|PUT]]) des fichiers vers le serveur. Le transfert de données s'effectue via le canal de données.
*   **Ports par défaut**: [[TransmissionControlProtocol|TCP]]/21 (contrôle), [[TransmissionControlProtocol|TCP]]/20 (données en mode actif).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   **Absence de chiffrement**: FTP transmet les [[Credential|identifiants]] et les données en [[Cleartext|texte clair]], ce qui les rend vulnérables à l'[[Eavesdropping|écoute clandestine]] et aux [[ManInTheMiddle|attaques de l'homme du milieu]].
    *   **[[BruteForceAttack|Attaques par force brute]]**: Les [[Password|mots de passe]] faibles peuvent être la cible d'[[PasswordAttacks|attaques de mots de passe]].
    *   **Problèmes de [[PortSecurity|sécurité des ports]]**: Une mauvaise configuration des [[Firewall|pare-feu]] peut exposer inutilement les ports FTP.
*   **Versions sécurisées**:
    *   [[FileTransferProtocolSecure|FTPS]] (FTP Secure): Utilise [[SecureSocketLayer|SSL]]/[[TransportLayerSecurity|TLS]] pour chiffrer les canaux de contrôle et de données, offrant ainsi une [[Encryption|confidentialité]] et une [[Integrity|intégrité]] des données.
    *   [[SSHFileTransferProtocol|SFTP]] (SSH File Transfer Protocol): Bien que le nom soit similaire, SFTP est un protocole entièrement différent qui s'exécute sur le protocole [[SecureShell|SSH]], offrant un chiffrement fort et une [[Authentication|authentification]] robuste.

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|TCP]]
*   [[InternetProtocol|IP]]
*   [[FileTransfer|Transfert de Fichiers]]
*   [[ClientServerArchitecture|Architecture Client-Serveur]]
*   [[Authentication|Authentification]]
*   [[Wireshark|Wireshark]]