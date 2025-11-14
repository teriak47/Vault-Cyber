---
tags:
  - suite-protocoles-internet
  - encapsulation-donnees
  - segmentation-reseau
  - reseau/protocoles
  - securite/attaque-mitm
  - securite/chiffrement
aliases:
  - Suite de Protocoles Internet
  - TCP/IP Stack
  - Protocoles TCP/IP
cssclasses:
  - max
---

# Suite de Protocoles Internet (TCP/IP)

## 📥 Définition en une phrase
> La Suite de [[InternetProtocol|Protocoles Internet]] (communément appelée TCP/IP) est un ensemble de [[NetworkProtocol|protocoles réseau]] qui constitue la base technique de l'[[Internet]] et des réseaux informatiques, permettant la [[NetworkCommunication|communication réseau]] entre des appareils diversifiés.

## 🧠 Concepts Clés / Fonctionnement
*   **Modèle en couches**: La suite [[InternetProtocolSuite|TCP/IP]] est organisée en un [[ProtocolStack|pile de protocoles]] à quatre couches (accès réseau, internet, transport et application), chacune responsable de fonctions spécifiques pour acheminer les données.
*   **[[TransmissionControlProtocol|TCP]]**: Le Protocole de Contrôle de Transmission gère la fiabilité et l'ordonnancement des données, assurant que les paquets arrivent sans erreur et dans le bon ordre à la destination.
*   **[[InternetProtocol|IP]]**: Le [[InternetProtocol|Protocole Internet]] est responsable de l'adressage et du routage des [[Packet|paquets]] de données à travers les différents réseaux, en utilisant des [[InternetProtocolAddress|adresses IP]].
*   **[[Interoperability|Interoperabilité]]**: Grâce à ces protocoles standards, des systèmes d'exploitation et matériels différents peuvent communiquer efficacement sur un même réseau ou via l'[[Internet]].
*   **Encapsulation**: Chaque couche ajoute ses propres informations d'[[Header|en-tête]] aux données lors de l'[[Encapsulation|encapsulation]], puis les supprime lors de la [[Decapsulation|décapsulation]] à la réception.

## 🛡️ Risques / Menaces Associés
*   **[[DenialOfService|Attaques par Déni de Service (DoS/DDoS)]]**: Ciblent la couche transport (TCP SYN Flood) ou la couche réseau (ICMP Flood) pour saturer les ressources et rendre les services inaccessibles.
*   **[[SpoofingAttack|Usurpation d'identité]]**: Les [[InternetProtocol|adresses IP]] ou les [[MediaAccessControlAddress|adresses MAC]] peuvent être falsifiées pour masquer l'identité d'un attaquant ou rediriger le trafic.
*   **[[ManInTheMiddle|Attaques de l'Homme du Milieu (MITM)]]**: Exploitation de faiblesses des protocoles (comme [[AddressResolutionProtocol|ARP]] ou [[DomainNameSystem|DNS]]) pour intercepter et potentiellement modifier les communications.
*   **[[Vulnerability|Vulnérabilités]] dans les implémentations**: Des défauts dans les logiciels implémentant les protocoles [[InternetProtocolSuite|TCP/IP]] peuvent être exploités pour diverses [[Attack|attaques]], y compris l'exécution de code à distance.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Firewall|Utilisation de Pare-feu]]**: Filtrent le trafic réseau en fonction des [[PortNumber|numéros de port]] et des [[InternetProtocolAddress|adresses IP]], bloquant les communications non autorisées.
*   **[[NetworkSegmentation|Segmentation Réseau]]**: Diviser un grand réseau en segments plus petits pour limiter la portée des [[Attack|attaques]] et contrôler le flux de trafic entre eux.
*   **[[DataEncryption|Chiffrement des Données]]**: Utiliser des protocoles sécurisés comme [[SecureSocketsLayer|SSL]]/[[TransportLayerSecurity|TLS]] pour chiffrer les données aux couches supérieures, protégeant ainsi la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des communications.
*   **[[PatchManagement|Gestion des Patchs]]**: Appliquer régulièrement les mises à jour de sécurité pour corriger les [[SoftwareVulnerability|vulnérabilités logicielles]] connues dans les implémentations des protocoles.
*   **[[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]]**: Surveillent le trafic pour détecter et/ou bloquer les activités malveillantes ou les tentatives d'[[Exploitation|exploitation]] de faiblesses protocolaires.

## 🔗 Notes Connexes
*   [[Internet]]
*   [[NetworkProtocol]]
*   [[TransmissionControlProtocol|TCP]]
*   [[InternetProtocol|IP]]
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[ProtocolStack|Pile de Protocoles]]
*   [[NetworkCommunication|Communication Réseau]]
*   [[NetworkSecurity|Sécurité Réseau]]