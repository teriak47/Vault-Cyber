---
tags:
  - protocole
aliases:
  - SSH
  - Secure Shell Protocol
  - Shell Sécurisé
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Secure Shell (SSH)

## 🎯 Rôle et Couche OSI
> SSH (Secure Shell) est un [[NetworkProtocol|protocole réseau]] cryptographique qui fournit un accès sécurisé aux [[Computer|ordinateurs]] sur un [[InsecureNetwork|réseau non sécurisé]], tel qu'Internet. Il permet l'[[RemoteCodeExecution|exécution de commandes à distance]], le [[FileTransfer|transfert de fichiers]] sécurisé (via [[SecureCopyProtocol|SCP]] et [[SFTP|SFTP]]) et la [[PortForwarding|redirection de port]]. Il opère principalement à la [[ApplicationLayer|couche Application]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
1.  **Établissement de la session**: Le [[Client|client SSH]] initie une connexion avec le [[Server|serveur SSH]] (généralement sur le [[PortNumber|port TCP/22]]). Un échange de clés cryptographiques a lieu pour établir un canal sécurisé.
2.  **[[Authentication|Authentification]]**: Le client s'authentifie auprès du serveur. Cela peut se faire via un [[Password|mot de passe]], des [[DigitalCertificate|clés publiques/privées]] (méthode la plus courante et sécurisée), ou d'autres mécanismes d'[[Authentication|authentification]].
3.  **[[Encryption|Chiffrement]] et Intégrité**: Une fois authentifié, toutes les communications entre le client et le serveur sont [[Encryption|chiffrées]] pour garantir la [[Confidentiality|confidentialité]] et l'[[Integrity|intégrité]] des [[Data|données]] échangées.
*   **Ports par défaut**: TCP/22

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   Faiblesses dans les [[Software|implémentations logicielles]] de SSH ou dans la [[KeyManagement|gestion des clés]] (clés faibles, réutilisation, non-rotation).
    *   Attaques par [[BruteForceAttack|force brute]] ou [[DictionaryAttack|dictionnaire]] sur les [[Password|mots de passe]] si l'authentification par mot de passe est utilisée et mal configurée (par exemple, sans [[RateLimiting|limitation de débit]] ou [[MultiFactorAuthentication|MFA]]).
    *   [[ManInTheMiddle|Attaques de l'homme du milieu]] si les clés hôtes du serveur ne sont pas correctement vérifiées lors de la première connexion.
    *   Exploitation de [[SoftwareVulnerability|vulnérabilités logicielles]] dans les clients ou serveurs SSH (ex: [[BufferOverflow|dépassement de tampon]]).
*   **Mesures de sécurité**:
    *   Utiliser des versions récentes et à jour du protocole et des implémentations.
    *   Préférer l'[[Authentication|authentification]] par [[DigitalCertificate|clé publique/privée]] plutôt que par mot de passe.
    *   Mettre en œuvre une [[StrongPasswordPolicy|politique de mots de passe forts]] et l'[[MultiFactorAuthentication|authentification multi-facteurs]] pour les accès par mot de passe.
    *   Effectuer une [[KeyManagement|gestion rigoureuse des clés]] SSH (génération sécurisée, stockage, rotation, révocation).
    *   Restreindre l'accès au [[PortNumber|port SSH]] (22) via un [[Firewall|pare-feu]].
    *   Implémenter un [[IntrusionDetectionSystem|système de détection d'intrusion]] ou [[IntrusionPreventionSystem|de prévention d'intrusion]] pour surveiller les tentatives d'accès.

## 🔗 Notes Connexes
*   [[ApplicationLayer|Couche Application]]
*   [[InternetProtocolSuite|Modèle TCP/IP]]
*   [[Authentication|Authentification]]
*   [[Encryption|Chiffrement]]
*   [[FileTransferProtocol|FTP]] (alternative non sécurisée pour le transfert de fichiers)
*   [[Wireshark|Outil pour l'analyse de protocole (Wireshark)]]
*   [[RemoteCodeExecution|Exécution de Code à Distance]]
*   [[KeyManagement|Gestion des Clés]]
*   [[PortForwarding|Redirection de Port]]
*   [[SecureCopyProtocol|SCP]]
*   [[SFTP|SFTP]]