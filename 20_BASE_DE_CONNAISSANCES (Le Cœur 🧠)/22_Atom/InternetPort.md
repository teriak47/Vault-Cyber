---
tags:
  - port-internet
  - analyse-port
  - pare-feu
aliases:
  - Port Internet
  - Internet Port
source:
  - 
cssclasses:
  - max
---

# Port Internet

## 📥 Définition en une phrase
> Un port Internet est un point de communication logiciel, identifié par un numéro, qui permet à des applications ou services spécifiques sur un système informatique d'envoyer et de recevoir des données via un réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Numérotation :** Les ports sont numérotés de 0 à 65535.
    *   **Ports Bien Connus (0-1023) :** Réservés aux services système courants (ex: [[HypertextTransferProtocol|HTTP]] sur 80, [[SecureShell|SSH]] sur 22, [[FileTransferProtocol|FTP]] sur 21).
    *   **Ports Enregistrés (1024-49151) :** Utilisés par des applications ou services enregistrés auprès de l'IANA (Internet Assigned Numbers Authority).
    *   **Ports Dynamiques/Privés (49152-65535) :** Utilisés par les clients pour initier des connexions vers des serveurs, attribués dynamiquement.
*   **Combinaison IP et Port :** Un port est toujours associé à une [[InternetProtocol|adresse IP]] pour former une "socket", identifiant de manière unique une application spécifique sur un hôte dans un réseau.
*   **Protocoles de Transport :** Les ports sont principalement utilisés par les protocoles de couche transport, tels que le [[TransmissionControlProtocol|TCP]] (Transmission Control Protocol) et l'[[UserDatagramProtocol|UDP]] (User Datagram Protocol), pour multiplexer et démultiplexer les flux de données entre différentes applications.
*   **Ouverture et Fermeture :** Les ports peuvent être "ouverts" (acceptant les connexions entrantes), "fermés" (refusant les connexions), ou "filtrés" (ne répondant pas aux requêtes).

## 🛡️ Risques / Menaces Associés
*   [[PortScanning|Analyse de ports]] (Port Scanning) : Permet aux attaquants de découvrir quels services sont exposés et potentiellement vulnérables sur un hôte.
*   [[UnsecuredService|Services non sécurisés]] : L'exposition de services non patchés ou mal configurés sur des ports ouverts crée des vecteurs d'attaque.
*   [[DenialOfService|Attaques par déni de service]] (DoS) : Cibler des ports spécifiques pour submerger un service et le rendre indisponible.
*   [[UnauthorizedAccess|Accès non autorisé]] : Utilisation abusive de services exposés pour obtenir un accès au système.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Configuration de pare-feu]] : Bloquer l'accès aux ports inutiles et autoriser uniquement le trafic légitime vers les services exposés.
*   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] : N'ouvrir que les ports absolument nécessaires pour le fonctionnement des applications.
*   [[VulnerabilityManagement|Gestion des vulnérabilités]] : Maintenir les services et applications à jour pour corriger les failles de sécurité exploitables via les ports exposés.
*   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion]] (IDS) : Surveiller le trafic réseau pour détecter les tentatives d'analyse de ports ou d'exploitation de services.
*   [[NetworkSegmentation|Segmentation réseau]] : Isoler les serveurs et services critiques dans des zones réseau (ex: [[DemilitarizedZone|DMZ]]) avec des règles de pare-feu strictes.

## 🔗 Notes Connexes
*   [[InternetProtocol|Adresse IP]]
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[NetworkService|Service Réseau]]
*   [[Firewall|Pare-feu]]