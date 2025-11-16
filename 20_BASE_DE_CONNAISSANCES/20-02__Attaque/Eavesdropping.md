---
tags:
  - attaque
aliases:
  - Écoute Clandestine
  - Interception
  - Eavesdropping
  - Surveillance non autorisée
  - Wiretapping
archetype: attaque
source:
cssclasses:
  - max
---

# Écoute Clandestine (Eavesdropping)

## 📥 Définition
> L'écoute clandestine est l'acte d'intercepter secrètement et sans [[Authorization|autorisation]] des [[CommunicationChannel|communications privées]] entre deux ou plusieurs parties. Cette [[Attack|attaque]] de [[Confidentiality|confidentialité]] vise à obtenir des [[SensitiveData|informations sensibles]] ou confidentielles en surveillant le [[NetworkTraffic|trafic réseau]].

## 🎯 Vecteurs d'Attaque
*   **Interception Passive** : L'[[ThreatActor|attaquant]] se contente d'observer et de [[PacketSniffing|collecter des informations]] sans interagir ou modifier le [[NetworkTraffic|trafic]]. Cela inclut l'[[PacketSniffing|écoute de paquets]] sur des [[WirelessNetwork|réseaux sans fil]] non chiffrés (ex: Wi-Fi ouvert) ou des [[Ethernet|réseaux Ethernet]] où le trafic est en [[Broadcast|diffusion]]. Ce type d'[[Eavesdropping|écoute clandestine]] est difficile à détecter.
*   **Interception Active** : L'[[ThreatActor|attaquant]] intercepte, et potentiellement modifie, le [[NetworkTraffic|trafic]] en se positionnant entre les parties communicantes. Les techniques incluent l'[[ManInTheMiddle|Attaque de l'Homme du Milieu]] et l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]].
*   **Exploitation de Vulnérabilités** : L'exploitation de [[SoftwareVulnerability|vulnérabilités logicielles]] ou [[Hardware|matérielles]] sur des [[NetworkDevice|périphériques réseau]] ou des [[System|systèmes]] permet à l'[[ThreatActor|attaquant]] d'accéder au [[CommunicationChannel|canal de communication]] et d'intercepter les [[DataTransmission|transmissions de données]].

## 💥 Impacts Potentiels
*   [[DataBreach|Vol de données]] ou [[DataExfiltration|exfiltration de données]]
*   [[InformationDisclosure|Divulgation d'informations sensibles]] (ex: [[Credential|identifiants]], [[PersonalData|données personnelles]], secrets commerciaux)
*   [[PrivacyInvasion|Violation de la vie privée]]
*   [[UnauthorizedAccess|Accès non autorisé]] à des [[System|systèmes]] ou [[Account|comptes]]
*   [[ReputationalDamage|Dommage à la réputation]] pour les organisations concernées

##  concret
> Un [[ThreatActor|attaquant]] installe un [[PacketSniffing|logiciel de capture de paquets]] sur un [[AccessPoint|point d'accès Wi-Fi]] non sécurisé dans un café public. Lorsque des utilisateurs se connectent à ce [[WirelessNetwork|réseau]] et accèdent à des [[OnlineServices|services en ligne]] ou à des sites web via des [[UnencryptedTraffic|connexions non chiffrées]] (HTTP au lieu de [[HypertextTransferProtocolSecure|HTTPS]]), leurs [[Credential|identifiants]], leurs [[Message|messages]] et autres [[SensitiveData|informations sensibles]] sont interceptés en [[Cleartext|texte clair]] par l'[[ThreatActor|attaquant]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Utilisation systématique du [[Encryption|chiffrement]] de bout en bout pour toutes les [[NetworkCommunication|communications réseau]] (ex: [[HypertextTransferProtocolSecure|HTTPS]] pour le web, [[VirtualPrivateNetwork|VPN]] pour le trafic général, [[SecureShell|SSH]] pour l'accès distant, [[SSHFileTransferProtocol|SFTP]] ou [[FileTransferProtocolSecure|FTPS]] pour le [[FileTransfer|transfert de fichiers]]).
    *   Mise en œuvre de [[WirelessSecurity|protocoles de sécurité robustes]] pour les [[WirelessNetwork|réseaux sans fil]] (ex: [[WirelessProtectedAccessThree|WPA3]], [[WirelessProtectedAccessTwo|WPA2]] avec un [[StrongPassword|mot de passe fort]]).
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] aux risques des [[PublicNetwork|réseaux publics]] et à l'importance de vérifier la sécurité des [[WebBrowsers|navigateurs]] (cadenas [[HypertextTransferProtocolSecure|HTTPS]]).
    *   [[NetworkSegmentation|Segmentation réseau]] et [[Isolation|isolation]] des [[NetworkSegment|segments de réseau]] critiques pour limiter la portée d'une éventuelle interception.
*   **Détection** :
    *   Déploiement de [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et de [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]] pour surveiller le [[NetworkTraffic|trafic réseau]] et alerter sur les activités suspectes.
    *   [[NetworkMonitoring|Surveillance réseau]] continue et [[NetworkTrafficAnalysis|analyse du trafic réseau]] pour identifier les [[AnomalyDetection|anomalies]].
*   **Réponse** :
    *   Établissement et pratique de [[IncidentResponse|plans de réponse à incident]] pour réagir efficacement en cas de détection d'[[Eavesdropping|écoute clandestine]] et de [[SecurityIncident|violation de sécurité]].

## 🔗 Notes Connexes
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[PacketSniffing|Capture de Paquets]]
*   [[Confidentiality|Confidentialité]]
*   [[Privacy|Vie Privée]]
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[DataProtection|Protection des Données]]
*   [[UnencryptedTraffic|Trafic non chiffré]]
*   [[NetworkTraffic|Trafic Réseau]]
*   [[SecurityIncident|Incident de Sécurité]]
*   [[InformationDisclosure|Divulgation d'Informations]]
---