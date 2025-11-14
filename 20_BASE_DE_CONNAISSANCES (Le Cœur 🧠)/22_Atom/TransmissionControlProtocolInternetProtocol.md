---
tags:
  - protocole/transport
  - securite/pare-feu
  - modele/tcp-ip
  - architecture/couches
aliases:
  - TCP/IP
  - Transmission Control Protocol/Internet Protocol
  - Pile de protocoles TCP/IP
  - Suite de protocoles TCP/IP
source:
  - 
cssclasses:
  - max
---

# Pile de Protocoles TCP/IP (TCP/IP)

## 📥 Définition en une phrase
> La suite de protocoles TCP/IP est l'ensemble fondamental de protocoles de communication qui sous-tend Internet et permet l'échange de données entre les ordinateurs et les réseaux à l'échelle mondiale.

## 🧠 Concepts Clés / Fonctionnement
*   **Architecture en couches:** TCP/IP est structuré en quatre couches principales, distinctes mais interdépendantes, chacune gérant des aspects spécifiques de la communication réseau :
    *   **Couche d'Accès Réseau (ou Liaison de Données) :** Gère les détails physiques de la transmission de données (Ethernet, Wi-Fi, etc.).
    *   **Couche Internet (ou Réseau) :** Responsable de l'adressage (via l'[[InternetProtocol|IP]]) et du routage des paquets sur les réseaux interconnectés.
    *   **Couche Transport :** Fournit des services de communication de bout en bout. Le [[TransmissionControlProtocol|TCP]] assure une livraison fiable et ordonnée, tandis que l'[[UserDatagramProtocol|UDP]] offre une transmission plus rapide mais sans garantie de fiabilité.
    *   **Couche Application :** Contient les protocoles de haut niveau pour des services spécifiques comme le web (HTTP/S), le courrier électronique (SMTP, POP3, IMAP), le transfert de fichiers (FTP), etc.
*   **[[InternetProtocol|IP]] (Internet Protocol):** Protocole principal de la couche Internet, responsable de l'adressage logique et du routage des paquets de données d'une source à une destination à travers différents réseaux.
*   **[[TransmissionControlProtocol|TCP]] (Transmission Control Protocol):** Protocole principal de la couche Transport, il fournit une connexion fiable, orientée connexion, assurant que les données sont livrées sans erreur, dans le bon ordre, et sans perte.
*   **Encapsulation:** Les données sont encapsulées à chaque couche, avec l'ajout d'en-têtes spécifiques au protocole de la couche, puis désencapsulées à la réception.

## 🛡️ Risques / Menaces Associés
*   **[[DenialOfServiceAttack|Attaques par Déni de Service (DoS)]]:** Des vulnérabilités ou des conceptions spécifiques à certains protocoles TCP/IP (comme le [[SynFloodAttack|SYN Flood]] ciblant TCP) peuvent être exploitées pour saturer les ressources et rendre les services indisponibles.
*   **[[ManInTheMiddle|Attaques de l'Homme du Milieu (MitM)]]:** Des protocoles non sécurisés dans la suite TCP/IP peuvent permettre à un attaquant d'intercepter et potentiellement modifier le trafic entre deux parties.
*   **[[IPSpoofing|Usurpation d'IP]]:** Un attaquant peut falsifier son adresse IP source pour masquer son identité ou contourner des contrôles d'accès basés sur l'IP.
*   **Vulnérabilités des implémentations:** Des failles dans les logiciels implémentant les protocoles TCP/IP peuvent être exploitées (ex: buffer overflows).

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[Firewall|Pare-feu]]:** Utiliser des pare-feu pour filtrer le trafic réseau et bloquer les communications non autorisées basées sur les adresses IP et les ports.
*   **[[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]]:** Surveiller le trafic réseau pour détecter et bloquer les activités malveillantes ou les schémas d'attaque connus.
*   **Mises à jour régulières:** Appliquer régulièrement les patchs et mises à jour aux systèmes d'exploitation et équipements réseau pour corriger les vulnérabilités connues dans les implémentations de protocoles.
*   **Utilisation de protocoles sécurisés:** Privilégier des protocoles de couche application sécurisés comme [[HypertextTransferProtocolSecure|HTTPS]] (via [[TransportLayerSecurity|TLS]]), [[SecureShell|SSH]], ou [[SecureFileTransferProtocol|SFTP]] pour la transmission de [[SensitiveData|données sensibles]].
*   **Segmenter le réseau:** Utiliser des [[VirtualLocalAreaNetwork|VLAN]] et des [[NetworkSegmentation|segmentations réseau]] pour isoler les systèmes critiques et limiter la propagation des attaques.

## 🔗 Notes Connexes
*   [[OpenSystemsInterconnectionModel|Modèle OSI]]
*   [[InternetProtocolVersion4|IPv4]]
*   [[InternetProtocolVersion6|IPv6]]
*   [[DomainNameSystem|DNS]]
*   [[DynamicHostConfigurationProtocol|DHCP]]
*   [[Ethernet|Ethernet]]
*   [[NetworkLayer|Couche Réseau]]
*   [[TransportLayer|Couche Transport]]
*   [[ApplicationLayer|Couche Application]]