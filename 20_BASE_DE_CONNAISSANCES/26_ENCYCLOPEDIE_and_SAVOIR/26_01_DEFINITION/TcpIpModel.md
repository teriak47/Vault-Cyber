---
aliases:
  - Modèle TCP/IP
  - TCP/IP Model
  - TCP IP
archetype: definition
cssclasses:
  - max
tags:
  - modele/tcp-ip
  - architecture/reseau
  - reseau
  - internet
  - communication/reseau
  - protocole
  - routage-reseau
  - modele/tcp-ip/couche-application
  - modele/tcp-ip/couche-transport
  - modele/tcp-ip/couche-internet
  - modele/tcp-ip/couche-acces-reseau
  - protocole/http
  - protocole/https
  - protocole/ftp
  - protocole/smtp
  - protocole/pop3
  - protocole/imap
  - protocole/dns
  - protocole/tcp
  - protocole/udp
  - protocole/ip
  - protocole/icmp
  - protocole/arp
  - protocole/ethernet
  - protocole/ppp
  - reseau/adressage
  - reseau/adressage/ip
  - reseau/adressage/mac
---

# TCP/IP Model

> [!question] C'est quoi ?
> Le *Modèle TCP/IP* est un ensemble de protocoles de communication qui définit la manière dont les ordinateurs se connectent à Internet et échangent des données.

## 📜 Origine / Contexte
> [!info] Le saviez-vous ?
> Le modèle TCP/IP a été développé par le Département de la Défense des États-Unis (DoD) dans les années 1970 pour assurer la résilience et la robustesse des communications en réseau, même en cas de panne de certains composants. Il est devenu le fondement technique d'Internet.

## 💡 Exemples Concrets
*   **Navigation Web** : Lorsque vous accédez à un site web, les données de la page sont encapsulées par les protocoles TCP et IP pour être acheminées de manière fiable jusqu'à votre navigateur.
*   **Envoi d'email** : L'envoi d'un courrier électronique utilise des protocoles comme SMTP (Couche Application), qui s'appuient sur TCP (Couche Transport) et IP (Couche Internet) pour garantir la livraison.

## 🧱 Architecture du Modèle TCP/IP

Le modèle TCP/IP est généralement décrit avec quatre couches, chacune ayant des responsabilités spécifiques pour assurer la communication de bout en bout.

### 1. Couche Application (Application Layer)
*   **Fonction principale** : Cette couche est la plus proche de l'utilisateur final et interagit directement avec les applications logicielles. Elle fournit des services de réseau aux applications et gère la présentation, l'encodage et le contrôle du dialogue.
*   **Exemples de protocoles** :
    *   **HTTP/HTTPS** : Pour la navigation web.
    *   **FTP** : Pour le transfert de fichiers.
    *   **SMTP/POP3/IMAP** : Pour l'envoi et la réception d'e-mails.
    *   **DNS** : Pour la résolution de noms de domaine en adresses IP.

### 2. Couche Transport (Transport Layer)
*   **Fonction principale** : Elle est responsable de la communication de bout en bout entre les applications, en assurant un [[ReliableDataTransfer|transfert de données fiable]] et ordonné, ou un transfert plus rapide mais sans garantie de livraison.
*   **Exemples de protocoles** :
    *   **TCP (Transmission Control Protocol)** : Fournit une connexion fiable, orientée connexion, avec contrôle de flux et de congestion. Il garantit que les paquets arrivent dans l'ordre et sans perte.
    *   **UDP (User Datagram Protocol)** : Fournit un service sans connexion, plus rapide mais sans garantie de livraison, d'ordre ou de contrôle de flux. Souvent utilisé pour le streaming vidéo ou les jeux en ligne où la rapidité prime sur la fiabilité absolue.

### 3. Couche Internet (Internet Layer ou Network Layer)
*   **Fonction principale** : Cette couche est responsable de l'adressage logique et du routage des paquets de données à travers différents réseaux interconnectés (internetwork). Elle détermine le meilleur chemin pour les paquets.
*   **Exemples de protocoles** :
    *   **IP (Internet Protocol)** : Gère l'adressage (adresses IP) et le routage des paquets. C'est le protocole central pour l'interconnexion des réseaux.
    *   **ICMP ([[ICMPProtocol|Internet Control Message Protocol]])** : Utilisé pour envoyer des messages d'erreur et des informations opérationnelles (ex: commandes *ping* et *traceroute*).
    *   **ARP (Address Resolution Protocol)** : Permet de mapper une adresse IP à une adresse MAC (physique) sur un réseau local.

### 4. Couche Accès Réseau (Network Access Layer ou Link Layer)
*   **Fonction principale** : Cette couche combine les fonctionnalités des couches Liaison de Données et Physique du modèle OSI. Elle est responsable de la transmission physique des données sur le média réseau (câble, Wi-Fi) et gère l'adressage physique (adresses MAC) ainsi que la détection et correction d'erreurs au niveau de la liaison.
*   **Exemples de protocoles** :
    *   **Ethernet** : Protocole le plus courant pour les réseaux locaux filaires.
    *   **Wi-Fi (IEEE 802.11)** : Pour les réseaux locaux sans fil.
    *   **PPP (Point-to-Point Protocol)** : Pour les liaisons série point à point.
    *   **Frame Relay / ATM** : Pour les réseaux étendus (WAN) plus anciens.