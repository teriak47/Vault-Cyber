---
tags:
  - protocole
  - protocole/rdp
  - acces/distance
  - communication/reseau
  - connexion
aliases:
  - Protocole de Bureau à Distance
  - RDP
  - Remote Desktop Protocol
archetype: protocole
rfc:
cssclasses:
  - max
---

# Remote Desktop Protocol (RDP)

## 🎯 Rôle et Couche OSI
> Le [[RemoteDesktopProtocol|Remote Desktop Protocol (RDP)]] est un protocole propriétaire développé par Microsoft, qui permet à un [[User|utilisateur]] de se connecter à distance à un [[Computer|ordinateur]] exécutant des services [[Windows|Windows Terminal Services]] ou Remote Desktop Services. Il fournit une interface graphique à l'[[User|utilisateur]] depuis le [[Client|client]] RDP. Il opère principalement à la [[ApplicationLayer|couche application]] (couche 7) du [[OpenSystemsInterconnectionModel|modèle OSI]], en s'appuyant sur les services de la [[TransportLayer|couche transport]] ([[TransmissionControlProtocol|TCP]]).

## ⚙️ Fonctionnement
1.  **Initiation de la Connexion**: Le [[Client|client]] RDP initie une connexion [[TransmissionControlProtocol|TCP]] sur le [[PortNumber|port]] 3389 (par défaut) vers le [[Server|serveur]] RDP. Une fois la connexion [[TransmissionControlProtocol|TCP]] établie, une séquence de négociation RDP est lancée, y compris l'échange de capacités et l'[[Authentication|authentification]] de l'[[User|utilisateur]].
2.  **Transfert de Données**: Après une [[Authentication|authentification]] réussie, le [[Server|serveur]] envoie les mises à jour de l'écran graphique au [[Client|client]] RDP, tandis que le [[Client|client]] transmet les entrées (clavier, souris) au [[Server|serveur]]. Le [[RemoteDesktopProtocol|RDP]] optimise la [[DataTransmission|transmission des données]] en envoyant uniquement les modifications de l'écran.
3.  **Gestion de Session**: Le protocole gère la [[SessionLayer|session]] à distance, permettant à l'[[User|utilisateur]] d'interagir avec le [[Computer|système]] distant comme s'il était directement assis devant. La [[SessionLayer|session]] peut être déconnectée et reconnectée sans perdre le travail en cours.
* **Ports par défaut**: [[TransmissionControlProtocol|TCP]]/3389

## 🛡️ Sécurité du Protocole
* **Vulnérabilités connues**:
  *   [[BruteForceAttack|Attaques par force brute]] et [[CredentialStuffing|bourrage d'identifiants]] contre les informations d'identification RDP.
  *   [[SoftwareVulnerability|Vulnérabilités logicielles]] dans les implémentations [[RemoteDesktopProtocol|RDP]] du [[Server|serveur]] ou du [[Client|client]], pouvant mener à des [[RemoteCodeExecution|exécutions de code à distance]] (ex: BlueKeep).
  *   [[ManInTheMiddle|Attaques de l'homme du milieu]] si la connexion n'est pas correctement chiffrée.
  *   Exposition des services RDP directement sur l'[[Internet|Internet]] sans protections adéquates, augmentant la [[AttackSurface|surface d'attaque]].
* **Mesures de mitigation et versions sécurisées**:
  *   Utilisation de [[MultiFactorAuthentication|l'authentification multi-facteurs (MFA)]].
  *   Mise en œuvre de [[StrongPasswordPolicy|politiques de mots de passe forts]] et de mécanismes de [[AccountLockout|verrouillage de compte]].
  *   Chiffrement de la connexion via [[TransportLayerSecurity|TLS]]/[[SecureSocketLayer|SSL]] pour protéger les [[Credential|informations d'identification]] et les données en transit.
  *   Restriction de l'accès RDP via des [[Firewall|pare-feu]] ou des listes de contrôle d'accès (ACL).
  *   Utilisation de [[VirtualPrivateNetwork|VPN]] pour isoler le trafic RDP sur un [[Tunneling|tunnel]] sécurisé.
  *   [[PatchManagement|Gestion des patchs]] et mises à jour régulières des systèmes RDP pour corriger les [[SoftwareVulnerability|vulnérabilités connues]].
  *   [[NetworkSegmentation|Segmentation réseau]] pour isoler les [[Server|serveurs]] RDP sensibles.

## 🔗 Notes Connexes
* **Couche OSI**: [[ApplicationLayer]]
* **Sécurité associée**: [[NetworkSecurity]]
* **Contrôle d'accès**: [[Authentication]]
* **Accès sécurisé**: [[VirtualPrivateNetwork]]
* **Type d'attaque**: [[BruteForceAttack]]