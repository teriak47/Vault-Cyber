---
tags:
aliases:
  - Numéro de Port
  - Port Number
  - Port
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Numéro de Port

## 📥 Définition en une phrase
> Un [[PortNumber|numéro de port]] est une adresse logique de 16 bits, utilisée par les [[Protocol|protocoles]] de la [[TransportLayer|couche Transport]] (tels que [[TransmissionControlProtocol|TCP]] et [[UserDatagramProtocol|UDP]]), pour identifier un [[SoftwareApplication|service]] ou une [[SoftwareApplication|application]] spécifique sur un [[Host|hôte]] [[Network|réseau]].

## 🧠 Concepts Clés / Piliers
*   **Identification des Services**: Un [[PortNumber|numéro de port]] permet à plusieurs [[SoftwareApplication|applications]] d'utiliser la même [[InternetProtocol|adresse IP]] sur un [[Host|hôte]], en dirigeant spécifiquement le trafic [[NetworkCommunication|réseau]] vers le [[SoftwareApplication|service]] approprié via les [[Protocol|protocoles]] de la [[TransportLayer|couche Transport]]. Cette capacité à distinguer les [[Process|processus]] individuels est fondamentale pour l'[[NetworkCommunication|interopérabilité réseau]].
*   **Organisation et Standardisation**: Les ports sont divisés en plages numérotées de 0 à 65535, définies par l'[[InternetAssignedNumbersAuthority|IANA]]. On distingue les **Ports Bien Connus** (0-1023) réservés aux services standards (ex: [[HypertextTransferProtocol|HTTP]] 80, [[FileTransferProtocol|FTP]] 21, [[SecureShell|SSH]] 22, [[DomainNameSystem|DNS]] 53), les **Ports Enregistrés** (1024-49151) attribués par l'[[InternetAssignedNumbersAuthority|IANA]] à des applications spécifiques, et les **Ports Éphémères/Dynamiques** (49152-65535) utilisés temporairement par les [[Client|clients]] pour initier des connexions.
*   **Communication de Processus à Processus**: Au sein du [[InternetProtocolSuite|modèle TCP/IP]], les ports sont cruciaux pour le multiplexage et le démultiplexage des [[Message|messages]] au niveau de la [[TransportLayer|couche Transport]]. Ils garantissent que les [[Data|données]] entrantes atteignent le [[Process|processus]] [[SoftwareApplication|applicatif]] correct sur le [[System|système de destination]], et que les [[Data|données]] sortantes sont correctement identifiées par leur [[SoftwareApplication|service]] source.

## 💡 Importance en Cybersécurité
> Les [[PortNumber|numéros de port]] sont des points d'accès critiques et une composante fondamentale de la [[NetworkSecurity|sécurité réseau]]. Leur mauvaise gestion peut mener à des [[Vulnerability|vulnérabilités]] majeures. Ils sont fréquemment la cible de [[Reconnaissance|reconnaissance]] via le [[PortScanning|scan de ports]] pour identifier les [[SoftwareApplication|services]] exposés, et peuvent servir de vecteurs pour des [[DigitalAttack|attaques]] telles que le [[DenialOfService|déni de service]] ou l'[[Exploitation|exploitation]] de [[SoftwareVulnerability|vulnérabilités logicielles]]. La [[SecurityPolicy|gestion rigoureuse]] des ports par des [[Firewall|pare-feu]], le [[ServiceHardening|durcissement des services]] et la [[NetworkSegmentation|segmentation réseau]] est indispensable pour minimiser la [[AttackSurface|surface d'attaque]] et protéger les [[Resource|ressources]] [[System|système]] contre l'[[UnauthorizedAccess|accès non autorisé]].

## 🔗 Notes Connexes
*   [[TransmissionControlProtocol|TCP]]
*   [[UserDatagramProtocol|UDP]]
*   [[InternetProtocol|Adresse IP]]
*   [[Firewall|Pare-feu]]
*   [[PortScanning|Scan de ports]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[TransportLayer|Couche Transport]]