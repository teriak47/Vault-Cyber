---
aliases:
  - Ports et protocoles courants
  - Common Ports and Protocols
  - Network Ports
  - Network Protocols
  - TCP UDP Ports
  - protocole réseau
  - port réseau
archetype: concept-general
cssclasses:
  - max
tags:
  - protocole
  - port
  - protocole/reseau
  - communication/reseau
  - modele-osi
  - modele/tcp-ip
  - protocole/ip
  - protocole/tcp
  - protocole/udp
  - protocole/http
  - protocole/https
  - protocole/ftp
  - protocole/ssh
  - protocole/telnet
---

# Ports et Protocoles Courants

Les **ports** et les **protocoles** sont des concepts fondamentaux dans la communication réseau, permettant aux appareils de communiquer efficacement et de manière organisée sur un réseau, y compris Internet. 
Les protocoles définissent les règles et les formats pour l'échange de données, tandis que les ports sont des points d'accès virtuels qui dirigent ce trafic vers des applications ou services spécifiques sur un appareil.

## ⚙️ Fonctionnement des Ports et Protocoles

### Les Protocoles : Le Langage Commun
Un **protocole réseau** est un ensemble de règles standardisées qui régissent le formatage et le traitement des données pour la communication entre appareils. Ils constituent un langage commun, permettant aux ordinateurs de communiquer quels que soient leurs différences matérielles ou logicielles.

Les protocoles sont souvent classés selon le modèle OSI (Open Systems Interconnection) ou le modèle TCP/IP, qui divisent le processus de communication en différentes couches, chacune gérant des fonctions spécifiques. Par exemple, le protocole IP (Internet Protocol) est responsable du routage des données en indiquant l'origine et la destination des paquets.

### Les Ports : Les Points d'Accès Virtuels
Un **port** est un point de départ et d'arrêt virtuel, basé sur un logiciel, pour les connexions réseau au sein d'un système d'exploitation. Les ports sont gérés par le système d'exploitation d'un ordinateur et identifiés par des numéros. Chaque port est associé à un processus ou un service spécifique, ce qui permet aux ordinateurs de trier le trafic réseau qu'ils reçoivent et de diriger les données vers l'application appropriée.

Les numéros de port sont codés sur 16 bits, ce qui signifie qu'il existe 65 536 ports possibles, numérotés de 0 à 65 535. L'IANA ([[InternetAssignedNumbersAuthority|Internet Assigned Numbers Authority]]) est l'organisme responsable de l'attribution officielle des numéros de port pour des usages spécifiques.

Les ports sont divisés en trois catégories principales:
*   **Ports connus (Well-Known Ports)**: De 0 à 1023. Ils sont réservés aux services système privilégiés et aux applications courantes (ex: HTTP, FTP, SSH).
*   **Ports enregistrés (Registered Ports)**: De 1024 à 49151. Ils sont attribués à des applications spécifiques par des organisations ou des développeurs.
*   **Ports dynamiques ou privés (Dynamic/Private Ports)**: De 49152 à 65535. Utilisés pour les connexions temporaires établies par les applications clientes.

### Interaction entre Ports et Protocoles
Les ports et les protocoles travaillent ensemble pour assurer la communication. Une adresse IP identifie un appareil unique sur le réseau, tandis que le numéro de port identifie l'application ou le service spécifique sur cet appareil auquel les données sont destinées.

Par exemple, lorsque vous accédez à une page web, votre navigateur (une application client) envoie une requête via le protocole HTTP ou HTTPS, généralement sur les ports 80 ou 443 respectivement. Le serveur web qui héberge la page écoute sur ce port, reçoit la requête, et renvoie la page demandée.

Les principaux protocoles de transport qui utilisent les ports sont TCP (Transmission Control Protocol) et UDP (User Datagram Protocol).

#### **TCP** ([[TransmissionControlProtocol|Transmission Control Protocol]])
*   **Fiable et orienté connexion** : TCP établit une connexion fiable entre deux appareils avant de transmettre les données (via un "handshake" en trois étapes).
*   **Garantit la livraison** : Il assure que les paquets de données arrivent dans le bon ordre, sans erreur et sans perte, en utilisant des accusés de réception et des mécanismes de retransmission.
*   **Contrôle de flux et de congestion** : Gère la quantité de données envoyées pour éviter de submerger le récepteur ou le réseau.
*   **Utilisation** : Idéal pour les applications où l'intégrité des données est cruciale, comme la navigation web (HTTP/HTTPS), le transfert de fichiers (FTP) et l'email (SMTP, IMAP, POP3).

#### **UDP** ([[UserDatagramProtocol|User Datagram Protocol]])
*   **Non fiable et sans connexion** : UDP envoie des paquets de données (datagrammes) sans établir de connexion préalable et sans garantir leur livraison, leur ordre ou l'absence d'erreurs.
*   **Rapide et léger** : Moins de surcharge que TCP, ce qui le rend plus rapide.
*   **Utilisation** : Préférable pour les applications en temps réel où la vitesse est plus importante que la fiabilité absolue, comme le streaming vidéo/audio, les jeux en ligne et le DNS.

## 📦 Protocoles et Ports Courants

Voici une liste des protocoles couramment utilisés et de leurs ports par défaut associés :

| Protocole                                     | Description                                                                                 | Port(s) par défaut                 | Transport                   | Couche OSI (Application) |
| --------------------------------------------- | ------------------------------------------------------------------------------------------- | ---------------------------------- | --------------------------- | ------------------------ |
| **FTP** (File Transfer Protocol)              | Transfert de fichiers entre un client et un serveur.                                        | 20 (données), 21 (contrôle)        | TCP                         | Application (7)          |
| **SSH** (Secure Shell)                        | Connexion sécurisée à distance, exécution de commandes et transfert de fichiers.            | 22                                 | TCP                         | Application (7)          |
| **Telnet**                                    | Connexion à distance non sécurisée à un serveur.                                            | 23                                 | TCP                         | Application (7)          |
| **SMTP** (Simple Mail Transfer Protocol)      | Envoi d'e-mails entre serveurs ou d'un client vers un serveur.                              | 25, 587 (SMTP sécurisé/submission) | TCP                         | Application (7)          |
| **DNS** (Domain Name System)                  | Traduction des noms de domaine en adresses IP.                                              | 53                                 | UDP (requêtes), TCP (zones) | Application (7)          |
| **HTTP** (Hypertext Transfer Protocol)        | Transfert de données pour le World Wide Web.                                                | 80                                 | TCP                         | Application (7)          |
| **POP3** (Post Office Protocol 3)             | Réception d'e-mails depuis un serveur.                                                      | 110, 995 (POP3S sécurisé)          | TCP                         | Application (7)          |
| **NTP** (Network Time Protocol)               | Synchronisation des horloges entre systèmes informatiques.                                  | 123                                | UDP                         | Application (7)          |
| **IMAP** (Internet Message Access Protocol)   | Réception et gestion d'e-mails sur un serveur.                                              | 143, 993 (IMAPS sécurisé)          | TCP                         | Application (7)          |
| **SNMP** (Simple Network Management Protocol) | Gestion et supervision des équipements réseau.                                              | 161 (agents), 162 (managers)       | UDP                         | Application (7)          |
| **HTTPS** (HTTP Secure)                       | Version sécurisée de HTTP, utilisant SSL/TLS pour le chiffrement.                           | 443                                | TCP                         | Application (7)          |
| **SMB** (Server Message Block)                | Partage de fichiers, d'imprimantes et de communications interprocessus sur un réseau local. | 445                                | TCP                         | Application (7)          |
| **RDP** (Remote Desktop Protocol)             | Permet la connexion à distance à un ordinateur de bureau.                                   | 3389                               | TCP                         | Application (7)          |

## 🛡️ Sécurité des Ports et Protocoles

La gestion des ports et des protocoles est cruciale pour la sécurité des réseaux.
*   **[[Firewall|Pare-feu]]** : Les pare-feu sont configurés pour bloquer ou autoriser le trafic vers des ports spécifiques, permettant ainsi de contrôler l'accès aux services. Une bonne configuration implique de n'ouvrir que les ports absolument nécessaires.
*   **[[Vulnerabilities|Vulnérabilités]]** : Les protocoles peuvent présenter des vulnérabilités (ex: le *sniffing* si le trafic n'est pas chiffré, le *spoofing* si l'authentification est faible). L'utilisation de versions sécurisées des protocoles (ex: HTTPS au lieu de HTTP, SSH au lieu de Telnet) est essentielle pour protéger les données.
*   **[[Surveillance]]** : La surveillance des ports actifs et du trafic réseau aide à détecter les activités suspectes ou les tentatives d'intrusion.

## 🔗 Notes Connexes
*   [[FileTransferProtocol|File Transfer Protocol]]
*  [[SecureShell|Secure Shell]]
*  [[TelnetProtocol|Telnet Protocol]]
*  [[SmtpProtocol|SMTP]]
*  [[DomainNameSystem|DNS]]
*  [[HttpProtocol|HTTP]]
*  [[POP3]]
*  [[NtpProtocol|NTP]]
*  [[ImapProtocol|IMAP]]
*  [[SimpleNetworkManagementProtocol|SNMP]]
*  [[HTTPS]]
*  [[ServerMessageBlock|SMB]]
*  [[RdpProtocol|RDP]]
