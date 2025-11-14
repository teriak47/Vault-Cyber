---
tags:
  - reseau/port/bien-connu
  - reseau/port/ephemere
  - securite/durcissement-services
  - securite/port-reseau
  - couche/transport
  - balayage-ports
aliases:
  - Numéro de Port
  - Port Number
source:
  - null
cssclasses:
  - max
---

# Numéro de Port

## 📥 Définition en une phrase
> Un numéro de port est une adresse logique de 16 bits, utilisée par les protocoles de la [[TransportLayer|couche transport]] (comme [[TransmissionControlProtocol|TCP]] et [[UserDatagramProtocol|UDP]]), pour identifier un service ou une application spécifique sur un hôte réseau.

## 🧠 Concepts Clés / Fonctionnement
*   **Identification des Services** : Permet à plusieurs applications d'utiliser la même adresse [[InternetProtocolAddress|IP]] tout en étant accessibles individuellement, en dirigeant le trafic vers le service approprié.
*   **Plage de Valeurs** : Les numéros de port vont de 0 à 65535.
*   **Catégories de Ports** :
    *   **Ports Bien Connus (Well-Known Ports)** : 0-1023, réservés aux services système ou aux applications courantes (ex: [[HypertextTransferProtocol|HTTP]] 80, [[FileTransferProtocol|FTP]] 21, [[SecureShell|SSH]] 22, [[DomainNameSystem|DNS]] 53).
    *   **Ports Enregistrés (Registered Ports)** : 1024-49151, enregistrés par l'IANA pour des applications ou services spécifiques.
    *   **Ports Éphémères / Dynamiques (Dynamic/Private Ports)** : 49152-65535, utilisés par les clients pour initier des connexions et sont attribués temporairement par le système d'exploitation.
*   **Protocoles** : Principalement utilisés par [[TransmissionControlProtocol|TCP]] pour les communications fiables et orientées connexion, et [[UserDatagramProtocol|UDP]] pour les communications sans connexion et non fiables.

## 🛡️ Risques / Menaces Associés
*   [[PortScanning|Scan de ports]] : Les attaquants utilisent cette technique de [[Reconnaissance|reconnaissance]] pour identifier les services exposés et les versions des logiciels.
*   [[Exploitation|Exploitation]] de Vulnérabilités : Des services vulnérables écoutant sur des ports ouverts peuvent être la cible d'attaques.
*   [[DenialOfService|Attaques par déni de service]] (DoS/DDoS) : Cibler des services spécifiques écoutant sur des ports particuliers pour les saturer et les rendre indisponibles.
*   [[UnauthorizedAccess|Accès non autorisé]] : Ports mal configurés ou laissés ouverts peuvent servir de portes d'entrée.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Firewall|Pare-feu]] : Configurer les pare-feu pour autoriser uniquement le trafic nécessaire sur les ports essentiels, et bloquer le reste (principe du [[LeastPrivilege|moindre privilège]]).
*   [[ServiceHardening|Durcissement des Services]] : Désactiver les services non utilisés et fermer leurs ports associés.
*   [[IntrusionDetectionSystem|IDS]] / [[IntrusionPreventionSystem|IPS]] : Surveiller le trafic sur les ports pour détecter des activités suspectes ou des tentatives de scan.
*   [[VulnerabilityManagement|Gestion des vulnérabilités]] : Maintenir les services et applications à jour pour patcher les vulnérabilités connues associées aux ports ouverts.
*   [[NetworkSegmentation|Segmentation réseau]] : Isoler les services sensibles sur des segments réseau dédiés, limitant ainsi l'exposition de leurs ports.

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetProtocolAddress|Adresse IP]]
*   [[NetworkService|Service réseau]]
*   [[Firewall|Pare-feu]]
*   [[PortScanning|Scan de ports]]