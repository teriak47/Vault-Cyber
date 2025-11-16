---
tags:
aliases:
  - Architecture Client-Serveur
  - Client-Server Architecture
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Architecture Client-Serveur

## 📥 Définition en une phrase
> Modèle d'[[Network|architecture réseau]] fondamental où les [[Client|clients]] initient des requêtes de services ou de ressources à des [[Server|serveurs]], qui les fournissent en réponse.

## 🧠 Concepts Clés / Piliers
*   **Clients**: Des applications, [[Computer|postes de travail]] ou [[EndDevices|appareils terminaux]] qui demandent des services ou des ressources. Ils sont généralement moins puissants et interagissent directement avec l'[[User|utilisateur]].
*   **Serveurs**: Des [[Computer|ordinateurs]] ou des [[SoftwareApplication|programmes]] dédiés qui fournissent des services, stockent des [[Data|données]] ou hébergent des [[SoftwareApplication|applications]] en réponse aux requêtes des [[Client|clients]]. Ils sont conçus pour être robustes et [[HighAvailability|disponibles]].
*   **Communication**: La [[NetworkCommunication|communication]] entre [[Client|clients]] et [[Server|serveurs]] s'effectue généralement via des [[NetworkProtocol|protocoles réseau]] standardisés (ex: [[HypertextTransferProtocol|HTTP]] pour le web, [[FileTransferProtocol|FTP]] pour le [[FileTransfer|transfert de fichiers]], [[SimpleMailTransferProtocol|SMTP]] pour l'email).
*   **Requête/Réponse**: Le [[Client|client]] envoie une [[Message|requête]] au [[Server|serveur]], qui la traite et renvoie une [[Message|réponse]] au [[Client|client]].
*   **Séparation des rôles**: Les rôles et les responsabilités sont clairement distincts, ce qui facilite la gestion, la maintenance et l'évolution des [[System|systèmes]].

## 💡 Importance en Cybersécurité
> L'[[ClientServerArchitecture|architecture client-serveur]] est au cœur de la plupart des [[OnlineServices|services en ligne]] et [[EnterpriseNetwork|réseaux d'entreprise]]. Sa robustesse est essentielle pour la [[CIATriad|triade C-I-A]] de la [[InformationSecurity|sécurité de l'information]]. Une [[Security|sécurité]] mal implémentée ou des [[Vulnerability|vulnérabilités]] peuvent entraîner des [[DenialOfService|dénis de service]], des [[DataBreach|fuites de données]] ou des [[UnauthorizedAccess|accès non autorisés]], rendant la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et l'[[Availability|disponibilité]] des [[Resource|ressources]] critiques. La centralisation des [[Server|serveurs]] rend leur [[Security|protection]] primordiale, mais crée également des [[SinglePointOfFailure|points de défaillance uniques]] qui doivent être défendus avec des [[DefenseInDepth|défenses en profondeur]].

## 🔗 Notes Connexes
*   [[NetworkProtocol|Protocole Réseau]]
*   [[DistributedSystem|Système Distribué]]
*   [[PeerToPeer|Peer-to-Peer]]
*   [[WebApplication|Application Web]]
*   [[Server|Serveur]]
*   [[Client|Client]]
*   [[AccessControl|Contrôle d'accès]]
*   [[Firewall|Pare-feu]]
*   [[DataEncryption|Chiffrement des Données]]
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion]]
*   [[SoftwareVulnerability|Vulnérabilité Logicielle]]