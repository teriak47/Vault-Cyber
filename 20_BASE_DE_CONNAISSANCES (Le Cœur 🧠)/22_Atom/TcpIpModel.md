---
tags:
  - reseau/couche-transport
  - sécurité/par-couche
  - modele/tcp-ip
  - architecture/couches
aliases:
  - Modèle TCP/IP
  - TCP/IP Model
  - TCP/IP
source:
  - 
cssclasses:
  - max
---

# Modèle TCP/IP

## 📥 Définition en une phrase
> Le modèle TCP/IP est un cadre conceptuel et un ensemble de protocoles de communication qui sous-tendent l'Internet et la plupart des réseaux modernes, décrivant comment les données sont formatées, adressées, transmises, routées et reçues.

## 🧠 Concepts Clés / Fonctionnement
Le modèle TCP/IP est divisé en quatre couches abstraites, chacune ayant un rôle spécifique dans le processus de communication :

*   **1. Couche d'Accès Réseau (Network Access Layer)** :
    *   Gère les détails physiques de la transmission des données, y compris les technologies de réseau telles que l'[[Ethernet|Ethernet]], le [[WirelessFidelity|Wi-Fi]], et la gestion des adresses physiques ([[MediaAccessControlAddress|adresses MAC]]).
    *   Elle est responsable de la transformation des paquets IP en trames adaptées au médium physique et vice versa.
    *   Protocoles clés : [[AddressResolutionProtocol|ARP]], Ethernet.

*   **2. Couche Internet (Internet Layer)** :
    *   Principalement responsable de l'adressage logique (avec les [[InternetProtocolAddress|adresses IP]]), du routage des paquets à travers différentes interconnexions de réseaux, et de la fragmentation/réassemblage des paquets.
    *   Son rôle est de s'assurer que les données arrivent à la bonne destination.
    *   Protocole clé : [[InternetProtocol|IP]] (IPv4 et IPv6), [[InternetControlMessageProtocol|ICMP]].

*   **3. Couche Transport (Transport Layer)** :
    *   Assure la communication de bout en bout entre les applications sur les hôtes. Elle gère la fiabilité, le contrôle de flux et la segmentation des données.
    *   [[TransmissionControlProtocol|TCP]] offre une connexion fiable, orientée connexion, avec retransmission des paquets perdus et contrôle de flux.
    *   [[UserDatagramProtocol|UDP]] offre une communication sans connexion, non fiable, avec une faible latence, adaptée au streaming ou aux requêtes DNS.
    *   Protocoles clés : [[TransmissionControlProtocol|TCP]], [[UserDatagramProtocol|UDP]].

*   **4. Couche Application (Application Layer)** :
    *   Contient les protocoles de plus haut niveau utilisés par les applications pour interagir avec le réseau.
    *   Ces protocoles définissent comment les applications échangent des données et fournissent des services aux utilisateurs.
    *   Exemples : [[HyperTextTransferProtocol|HTTP]]/HTTPS (web), [[FileTransferProtocol|FTP]] (transfert de fichiers), [[SimpleMailTransferProtocol|SMTP]] (email), [[DomainNameSystem|DNS]] (résolution de noms).

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS)]] ciblant la disponibilité des couches Transport et Application.
*   [[PacketSniffing|Reniflage de paquets]] sur la couche d'Accès Réseau pour intercepter des données non chiffrées.
*   [[IpSpoofing|Usurpation d'adresse IP]] (IP Spoofing) et [[ArpSpoofing|Usurpation d'ARP]] (ARP Spoofing) sur les couches Internet et Accès Réseau.
*   [[Vulnerability|Vulnérabilités]] dans les implémentations de protocoles spécifiques (ex: bugs dans les piles TCP/IP).

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mise en place de [[Firewall|pare-feu]] pour contrôler le trafic entre les couches.
*   Utilisation de [[VirtualPrivateNetwork|VPN]] et de protocoles de chiffrement comme [[TransportLayerSecurity|TLS]]/[[SecureSocketLayer|SSL]] pour protéger les données sur les couches Transport et Application.
*   Implémentation de [[IntrusionDetectionSystem|systèmes de détection d'intrusion (IDS)]] et de [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]] pour surveiller et bloquer les activités suspectes.
*   Configuration sécurisée des périphériques réseau et application de [[PatchManagement|gestion des correctifs]] régulière.
*   Utilisation de protocoles sécurisés au niveau de l'application (ex: HTTPS au lieu de HTTP, SFTP au lieu de FTP).

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[NetworkProtocol|Protocole Réseau]]
*   [[TransmissionControlProtocol|TCP]]
*   [[InternetProtocol|IP]]
*   [[ApplicationLayer|Couche Application]]
*   [[TransportLayer|Couche Transport]]
*   [[InternetLayer|Couche Internet]]
*   [[NetworkAccessLayer|Couche Accès Réseau]]
* [[ComparaisonModeleOsiEtModeleTcpip_Cour|Comparaison modele osi et modele TCP/ip]]