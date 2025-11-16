---
tags:
  - protocole
aliases:
  - Protocole de Transfert de Fichiers Sécurisé
  - FTPS
  - File Transfer Protocol Secure
archetype: protocole
rfc: 
cssclasses:
  - max
---

# Protocole de Transfert de Fichiers Sécurisé (FTPS)

## 🎯 Rôle et Couche OSI
Le [[FileTransferProtocolSecure|FTPS]] est une extension du [[FileTransferProtocol|Protocole de Transfert de Fichiers]] (FTP) qui ajoute des fonctionnalités de sécurité par l'utilisation de [[TransportLayerSecurity|TLS]] (ou historiquement [[SecureSocketLayer|SSL]]). Il est conçu pour sécuriser les [[FileTransfer|transferts de fichiers]] sur un [[Network|réseau]] en fournissant l'[[Confidentiality|intégrité]] et la [[Confidentiality|confidentialité]] des [[Data|données]]. Il opère à la [[ApplicationLayer|couche Application]] du [[InternetProtocolSuite|modèle TCP/IP]].

## ⚙️ Fonctionnement
Le [[FileTransferProtocolSecure|FTPS]] fonctionne en encapsulant les commandes et les [[Data|données]] du [[FileTransferProtocol|FTP]] dans une connexion [[TransportLayerSecurity|TLS]] chiffrée. Il existe deux modes principaux :

1.  **FTPS Explicite (AUTH TLS)**:
    *   Le [[Client|client]] se connecte d'abord sur un [[FileTransferProtocol|port FTP]] standard (généralement [[PortNumber|TCP]]/21).
    *   Le [[Client|client]] initie explicitement une négociation [[TransportLayerSecurity|TLS]] en envoyant la commande `AUTH TLS`.
    *   Si la négociation réussit, le [[CommunicationChannel|canal de communication]] de contrôle et/ou de données est chiffré.
2.  **FTPS Implicite**:
    *   Le [[Client|client]] se connecte directement à un [[PortNumber|port]] désigné pour le [[FileTransferProtocolSecure|FTPS]] implicite (généralement [[PortNumber|TCP]]/990 pour le contrôle et [[PortNumber|TCP]]/989 pour les [[Data|données]]).
    *   La connexion [[TransportLayerSecurity|TLS]] est établie immédiatement au début de la session, sans commande de négociation.

*   **Ports par défaut**:
    *   **Contrôle**: [[PortNumber|TCP]]/21 (FTPS Explicite), [[PortNumber|TCP]]/990 (FTPS Implicite)
    *   **Données**: [[PortNumber|TCP]]/20 (mode actif, avec TLS négocié via le canal de contrôle), ou des [[PortNumber|ports]] dynamiques (mode passif), [[PortNumber|TCP]]/989 (FTPS Implicite)

## 🛡️ Sécurité du Protocole
*   **Vulnérabilités connues**:
    *   **Configuration incorrecte de [[DigitalCertificate|certificats]]**: Si les [[DigitalCertificate|certificats numériques]] du [[Server|serveur]] ne sont pas correctement validés par le [[Client|client]], une [[ManInTheMiddle|attaque de l'homme du milieu]] reste possible.
    *   **Vulnérabilités du [[FileTransferProtocol|FTP]] sous-jacent**: Bien que le [[FileTransferProtocolSecure|FTPS]] chiffre le trafic, il peut hériter de certaines [[SoftwareVulnerability|vulnérabilités logicielles]] ou [[ConfigurationDrift|dérives de configuration]] de l'[[FileTransferProtocol|implémentation FTP]] sous-jacente.
    *   **Problèmes de [[Firewall|pare-feu]]**: Le mode passif du [[FileTransferProtocol|FTP]] (et donc du [[FileTransferProtocolSecure|FTPS]]) peut être difficile à gérer avec les [[Firewall|pare-feux]] en raison de l'utilisation de [[PortNumber|ports]] de données dynamiques, potentiellement conduisant à des [[SecurityVulnerabilities|vulnérabilités de sécurité]] si les règles de [[Firewall|pare-feu]] ne sont pas strictes.
    *   **Exposition de la liste de répertoires**: Si les informations de liste de répertoires sont chiffrées mais que des métadonnées (comme les noms de fichiers) sont divulguées avant la négociation [[TransportLayerSecurity|TLS]] dans le mode explicite, une certaine [[InadvertentExposure|exposition involontaire]] d'information est possible.
*   **Versions sécurisées**:
    *   Le [[FileTransferProtocolSecure|FTPS]] est la version sécurisée du [[FileTransferProtocol|FTP]] grâce à l'intégration de [[TransportLayerSecurity|TLS]].
    *   Alternativement, le [[SSHFileTransferProtocol|SFTP]] (SSH File Transfer Protocol) offre une méthode de [[FileTransfer|transfert de fichiers]] sécurisée basée sur [[SecureShell|SSH]], qui est une approche de sécurité fondamentalement différente et souvent préférée pour sa simplicité de gestion des [[Firewall|pare-feux]].

## 🔗 Notes Connexes
*   [[FileTransferProtocol|Protocole de Transfert de Fichiers (FTP)]]
*   [[TransportLayerSecurity|Transport Layer Security (TLS)]]
*   [[SecureSocketLayer|Secure Sockets Layer (SSL)]]
*   [[DigitalCertificate|Certificat Numérique]]
*   [[SSHFileTransferProtocol|SSH File Transfer Protocol (SFTP)]]
*   [[Authentication|Authentification]]
*   [[Confidentiality|Confidentialité]]
*   [[Integrity|Intégrité]]
*   [[Wireshark|Wireshark]]