---
tags:
  - attaque
  - reconnaissance
aliases:
  - Balayage de ports
  - Port Scan
  - PortScanning
archetype: attaque
source:
  -
cssclasses:
  - max
---

# Balayage de Ports (Port Scanning)

## 📥 Définition
> Le [[PortScanning|balayage de ports]] est une technique de [[Reconnaissance|reconnaissance réseau]] qui consiste à sonder un [[Host|hôte]] cible pour identifier les [[PortNumber|ports]] ouverts, les [[Service|services]] associés et potentiellement le [[OperatingSystem|système d'exploitation]]. C'est une étape préliminaire cruciale pour cartographier la [[AttackSurface|surface d'attaque]] d'un [[System|système]].

## 🎯 Méthodes et Fonctionnement
*   **Objectif principal** : Découvrir quels [[Service|services]] sont actifs et écoutent sur un [[Network|réseau]] ou une [[Computer|machine]] spécifique.
*   **Méthode** : Envoi de [[Packet|paquets réseau]] à une plage de [[PortNumber|ports]] sur une [[InternetProtocolVersion4|adresse IP]] cible et analyse des réponses pour déterminer l'état de chaque [[PortNumber|port]] (ouvert, fermé, filtré).
*   **Types de Scan Courants** :
    *   **[[TransmissionControlProtocol|Scan SYN (Half-Open)]]** : Envoie uniquement le [[TransmissionControlProtocol#SYN_Flag|drapeau SYN]], puis un [[TransmissionControlProtocol#RST_Flag|RST]] si le [[PortNumber|port]] est fermé, ou un [[TransmissionControlProtocol#RST_Flag|RST]] après le [[TransmissionControlProtocol#SYN_ACK_Flag|SYN/ACK]] si le [[PortNumber|port]] est ouvert, sans établir de [[TransmissionControlProtocol|connexion TCP]] complète. Moins intrusif et plus furtif.
    *   **[[TransmissionControlProtocol|Scan Connect]]** : Tente d'établir une [[TransmissionControlProtocol|connexion TCP]] complète (poignée de main [[TransmissionControlProtocol#Three_Way_Handshake|SYN]], [[TransmissionControlProtocol#SYN_ACK_Flag|SYN/ACK]], [[TransmissionControlProtocol#ACK_Flag|ACK]]). Plus "bruyant", mais ne nécessite pas de [[Privilege|privilèges spéciaux]].
    *   **[[UserDatagramProtocol|Scan UDP]]** : Envoie des [[UserDatagramProtocol|paquets UDP]] aux [[PortNumber|ports]] cibles. L'absence de réponse ou un [[InternetControlMessageProtocol|message ICMP]] "Port Unreachable" indique généralement un [[PortNumber|port]] fermé ; l'absence de message indique un [[PortNumber|port]] potentiellement ouvert.
*   **Informations Recueillies** : [[PortNumber|Ports]] ouverts, [[Service|services]] fonctionnant sur ces [[PortNumber|ports]] (ex: [[HypertextTransferProtocol|HTTP]] sur le [[PortNumber|port]] 80, [[SecureShell|SSH]] sur le [[PortNumber|port]] 22), versions des [[Service|services]], et parfois le [[OperatingSystem|système d'exploitation]] de la cible.

## 💥 Impacts Potentiels
*   [[Reconnaissance|Amélioration de la reconnaissance]] par l'[[ThreatActor|acteur de menace]]
*   Découverte de [[SoftwareVulnerability|vulnérabilités logicielles]] ou de [[Misconfiguration|mauvaises configurations]]
*   Identification de [[Service|services]] obsolètes ou non patchés, propices à l'[[Exploitation|exploitation]]
*   Cartographie de la [[AttackSurface|surface d'attaque]] pour des [[DigitalAttack|attaques]] ciblées

## concret
> Un [[ThreatActor|attaquant]] utilise un [[Tool|outil]] comme [[Nmap|Nmap]] pour sonder une [[InternetProtocolVersion4|plage d'adresses IP]] sur un [[CorporateNetwork|réseau d'entreprise]]. Le [[PortScanning|balayage de ports]] révèle que le [[PortNumber|port]] 22 (pour [[SecureShell|SSH]]) est ouvert sur plusieurs [[Server|serveurs]], le [[PortNumber|port]] 80 (pour [[HypertextTransferProtocol|HTTP]]) sur un [[WebServer|serveur web]], et le [[PortNumber|port]] 3389 (pour [[RemoteDesktopProtocol|RDP]]) sur une station de travail [[Windows|Windows]]. Ces informations permettent à l'[[ThreatActor|attaquant]] de cibler spécifiquement ces [[Service|services]] avec des [[Vulnerability|vulnérabilités]] connues ou de tenter des [[BruteForceAttack|attaques par force brute]] sur [[SecureShell|SSH]] ou [[RemoteDesktopProtocol|RDP]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[Firewall|Pare-feu]] : Configuration de [[FirewallRule|règles de pare-feu]] strictes pour bloquer les tentatives de [[NetworkCommunication|connexion]] non autorisées aux [[PortNumber|ports]] et filtrer le [[NetworkTraffic|trafic entrant]] et sortant.
    *   [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]] : Fermer les [[PortNumber|ports]] inutilisés et désactiver les [[Service|services]] non essentiels pour réduire la [[AttackSurface|surface d'attaque]].
    *   [[NetworkSegmentation|Segmentation réseau]] : Isoler les [[NetworkSegment|segments de réseau]] pour limiter la portée d'un [[PortScanning|balayage]] réussi.
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] : Détecter et alerter ou bloquer les activités de [[PortScanning|balayage de ports]] suspectes.
    *   [[NetworkMonitoring|Surveillance réseau]] : Utiliser des [[Tool|outils]] de [[NetworkMonitoring|supervision réseau]] comme [[NetFlow|NetFlow]] pour analyser les [[NetworkTraffic|flux de trafic]] anormaux qui pourraient indiquer un [[PortScanning|balayage]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] : Définir des procédures pour réagir rapidement en cas de détection d'activités de [[PortScanning|balayage]] ou d'[[Exploitation|exploitation]] subséquente.
    *   [[VulnerabilityManagement|Gestion des Vulnérabilités]] : Auditer régulièrement les [[System|systèmes]] pour identifier les [[PortNumber|ports]] ouverts et les [[Service|services]] exposés, puis corriger les [[SoftwareVulnerability|vulnérabilités]].

## 🔗 Notes Connexes
*   [[Reconnaissance|Reconnaissance réseau]]
*   [[Nmap|Nmap]]
*   [[ServiceEnumeration|Énumération de services]]
*   [[TransmissionControlProtocol|Protocole de Contrôle de Transmission (TCP)]]
*   [[UserDatagramProtocol|Protocole de Datagrammes Utilisateur (UDP)]]
*   [[AttackSurface|Surface d'attaque]]
*   [[Vulnerability|Vulnérabilité]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[PortNumber|Numéro de Port]]
---