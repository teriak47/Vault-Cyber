---
tags:
  - tunnelisation-reseau
  - détection-tunnelisation
  - Encapsulation
  - VirtualPrivateNetwork
  - Firewall
aliases:
  - Tunnelisation
  - Network Tunneling
  - Encapsulation de protocole
source:
  - null
cssclasses:
  - max
---

# Tunneling

## 📥 Définition en une phrase
> Le tunneling est une technique de [[NetworkCommunication|communication réseau]] qui consiste à encapsuler des paquets d'un [[NetworkProtocol|protocole réseau]] au sein d'un autre protocole, créant ainsi un [[CommunicationChannel|canal de communication]] virtuel et sécurisé au-dessus d'un [[Network|réseau]] existant.

## 🧠 Concepts Clés / Fonctionnement
*   **[[Encapsulation|Encapsulation]] de [[Data|Données]]**: Un paquet entier d'un protocole est "emballé" dans la charge utile d'un autre protocole.
*   **[[Protocol|Protocoles]] de Transport**: Le protocole externe (de transport) peut être le [[InternetProtocol|IP]], le [[TransmissionControlProtocol|TCP]], ou l'[[UserDatagramProtocol|UDP]].
*   **Point à Point**: Crée souvent une [[OneToOneCommunications|communication un à un]] logique entre deux points, même si le chemin physique passe par de nombreux [[IntermediateDevices|dispositifs intermédiaires]].
*   **Applications Courantes**: Utilisé pour créer des [[VirtualPrivateNetwork|réseaux privés virtuels (VPN)]], pour contourner les [[Firewall|pare-feux]], ou pour fournir des [[SecureStorage|communications sécurisées]] sur un [[PublicNetwork|réseau public]].
*   **Fonctionnalités**: Permet la [[Confidentiality|confidentialité]] (via le [[Encryption|chiffrement]] du tunnel), l'[[Integrity|intégrité]] et l'[[Authentication|authentification]] des [[DataTransmission|données transmises]].

## 🛡️ Risques / Menaces Associés
*   **[[DataExfiltration|Exfiltration de données]]**: Les [[ThreatActor|acteurs de menaces]] peuvent utiliser le tunneling pour dissimuler l'[[DataExfiltration|exfiltration de données sensibles]] à travers des [[CommunicationChannel|canaux]] qui seraient normalement surveillés.
*   **Contournement des [[SecurityControl|contrôles de sécurité]]**: Un tunnel peut contourner les [[Firewall|pare-feux]] et les [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]] en encapsulant le trafic malveillant dans un protocole autorisé.
*   **[[Backdoor|Portes dérobées]]**: Le tunneling peut être utilisé pour établir des [[Backdoor|portes dérobées]] persistantes dans un [[System|système]] compromis, permettant un [[RemoteAccessTrojan|accès à distance]] furtif.
*   **[[MalwareDistribution|Distribution de logiciels malveillants]]**: Le trafic encapsulé peut masquer la livraison de [[Malware|logiciels malveillants]] ou d'[[Exploit|exploits]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[NetworkMonitoring|Surveillance réseau]] Avancée**: Utiliser des solutions de [[NetworkTrafficAnalysis|surveillance du trafic réseau]] incluant la [[DeepPacketInspection|Deep Packet Inspection (DPI)]] pour analyser le contenu des paquets tunnelisés.
*   **Règles de [[Firewall|Pare-feu]] Strictes**: Configurer les [[Firewall|pare-feux]] pour bloquer les protocoles ou les ports non autorisés qui pourraient être utilisés pour le tunneling.
*   **[[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]]**: Déployer des [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] et des [[IntrusionPreventionSystem|systèmes de prévention d'intrusion]] capables d'identifier les motifs de trafic de tunneling suspects.
*   **[[SecurityPolicy|Politiques de sécurité]]**: Établir des [[SecurityPolicy|politiques claires]] concernant l'utilisation du tunneling et l'accès [[RemoteNetwork|aux réseaux distants]].
*   **Segmentation Réseau**: Utiliser la [[NetworkSegmentation|segmentation réseau]] pour limiter la portée des tunnels malveillants s'ils devaient être établis.

## 🔗 Notes Connexes
*   [[VirtualPrivateNetwork|Réseau Privé Virtuel]]
*   [[Encapsulation|Encapsulation]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[Protocol|Protocole]]
*   [[Firewall|Pare-feu]]
*   [[DataExfiltration|Exfiltration de données]]