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
> Le Protocole de Transfert de Fichiers (FTP) est un protocole réseau client-serveur utilisé pour le transfert de fichiers entre un client et un serveur sur un réseau TCP/IP. Il opère à la couche Application du modèle OSI et du modèle TCP/IP.

## ⚙️ Fonctionnement
1.  **Établissement des Connexions**: FTP établit deux connexions distinctes entre le client et le serveur :
    *   **Canal de contrôle**: Sur le port TCP/21, utilisé pour l'échange de commandes (authentification, commandes de gestion de fichiers) et de réponses.
    *   **Canal de données**: Généralement sur le port TCP/20 (mode actif) ou un port éphémère négocié (mode passif), utilisé pour le transfert effectif des données de fichiers.
2.  **Authentification**: Le client se connecte au serveur FTP et fournit des informations d'identification (nom d'utilisateur et mot de passe) pour l'authentification. Certains serveurs peuvent autoriser des connexions anonymes.
3.  **Transfert de Données**: Une fois authentifié, le client peut utiliser des commandes pour naviguer dans le système de fichiers du serveur, télécharger (GET) des fichiers depuis le serveur, ou téléverser (PUT) des fichiers vers le serveur. Le transfert de données s'effectue via le canal de données.
*   **Ports par défaut**: TCP/21 (contrôle), TCP/20 (données en mode actif).

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   **Absence de chiffrement**: FTP transmet les identifiants et les données en texte clair, ce qui les rend vulnérables à l'écoute clandestine et aux attaques de l'homme du milieu.
    *   **Attaques par force brute**: Les mots de passe faibles peuvent être la cible d'attaques de mots de passe.
    *   **Problèmes de sécurité des ports**: Une mauvaise configuration des pare-feu peut exposer inutilement les ports FTP.
*   **Versions sécurisées**:
    *   FTPS (FTP Secure): Utilise SSL/TLS pour chiffrer les canaux de contrôle et de données, offrant ainsi une confidentialité et une intégrité des données.
    *   SFTP (SSH File Transfer Protocol): Bien que le nom soit similaire, SFTP est un protocole entièrement différent qui s'exécute sur le protocole SSH, offrant un chiffrement fort et une authentification robuste.

## 🔗 Notes Connexes
*   TCP
*   IP
*   Transfert de Fichiers
*   Architecture Client-Serveur
*   Authentification
*   Wireshark