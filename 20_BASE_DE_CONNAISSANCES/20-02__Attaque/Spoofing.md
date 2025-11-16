---
tags:
  - attaque
  - attaque/usurpation
  - attaque/homme-du-milieu
  - attaque/usurpation-mac
  - attaque/usurpation-dns
  - attaque/usurpation-email
  - attaque/usurpation-ip
  - securite/communication
aliases:
  - Usurpation
  - Usurpation d'identité
  - Spoofing Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Spoofing (Usurpation)

## 📥 Définition
> Le Spoofing est une technique d'[[Attack|attaque]] où un [[ThreatActor|acteur malveillant]] se déguise en entité légitime (utilisateur, appareil, programme) pour obtenir un [[UnauthorizedAccess|accès non autorisé]], dissimuler son [[UserIdentity|identité]] ou tromper des [[System|systèmes]] et des [[User|utilisateurs]]. Cette falsification exploite souvent des faiblesses dans les [[NetworkProtocol|protocoles réseau]] qui ne valident pas rigoureusement l'identité de l'émetteur.

## 🎯 Vecteurs d'Attaque
*   **[[IPSpoofing|Usurpation d'IP]]** : Falsification de l'[[InternetProtocolAddressBlocks|adresse IP]] source dans les [[Packet|paquets]] [[Network|réseau]] pour masquer l'origine réelle de l'[[Attack|attaquant]].
*   **[[MACSpoofing|Usurpation d'adresse MAC]]** : Modification de l'[[MediaAccessControlAddress|adresse MAC]] d'une [[NetworkInterface|interface réseau]] pour contourner les [[MacAddressFiltering|filtres d'adresses MAC]] ou se faire passer pour un [[WirelessDevices|appareil]] autorisé sur un [[LocalAreaNetwork|réseau local]].
*   **[[EmailSpoofing|Usurpation d'e-mail]]** : Falsification de l'adresse de l'expéditeur dans un [[Email|e-mail]] pour le faire apparaître comme provenant d'une [[TrustedSource|source de confiance]], souvent utilisée dans le cadre du [[Phishing|hameçonnage]] ou du [[Spam|pourriel]].
*   **[[DnsSpoofing|Usurpation DNS]]** : Redirection du [[NetworkTrafficAnalysis|trafic réseau]] vers des [[WebServer|serveurs malveillants]] ou non autorisés en falsifiant les enregistrements [[DomainNameSystem|DNS]] ou en exploitant les [[SoftwareVulnerability|vulnérabilités]] des [[Server|serveurs DNS]].
*   **[[AddressResolutionProtocolPoisoning|ARP Spoofing]]** : Association de l'[[MediaAccessControlAddress|adresse MAC]] de l'[[Attack|attaquant]] à l'[[InternetProtocolAddressBlocks|adresse IP]] d'une [[Gateway|passerelle]] par défaut ou d'un autre [[Host|hôte]] sur un [[LocalAreaNetwork|réseau local]], permettant l'interception du [[NetworkCommunication|trafic]].

## 💥 Impacts Potentiels
*   [[DataBreach|Vol de données]] (par exemple, [[Credential|identifiants]] de connexion ou [[PersonalData|données personnelles]])
*   [[DenialOfService|Indisponibilité de service]] via des [[Attack|attaques]] redirigées ou la perturbation du [[NetworkCommunication|trafic]]
*   [[PrivilegeEscalation|Élévation de privilèges]] suite à un [[UnauthorizedAccess|accès non autorisé]]
*   [[FinancialLoss|Perte financière]] due à la fraude ou à la [[SystemCompromise|compromission de système]]
*   [[ReputationalDamage|Dommage à la réputation]] pour l'organisation ou les individus ciblés

##  concret
> Un [[ThreatActor|attaquant]] configure son [[Computer|ordinateur]] pour utiliser une [[MediaAccessControlAddress|adresse MAC]] falsifiée identique à celle d'une imprimante réseau légitime (`[[NetworkPrinter|Network Printer]]`) déjà connectée au [[CorporateNetwork|réseau d'entreprise]]. Si le [[NetworkSwitch|commutateur réseau]] n'implémente pas de [[PortSecurity|sécurité des ports]] ou de [[MacAddressFiltering|filtrage d'adresses MAC]], l'attaquant pourrait réussir à se faire passer pour l'imprimante, potentiellement en interceptant le [[NetworkCommunication|trafic]] destiné à cette dernière, ou en accédant à des ressources du [[NetworkSegment|segment réseau]] auquel l'imprimante était autorisée.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] aux risques d'[[EmailSpoofing|usurpation d'e-mail]] et de [[Phishing|hameçonnage]].
    *   Configuration rigoureuse des [[Firewall|pare-feu]] et [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]].
    *   Mise en œuvre de mécanismes d'[[Authentication|authentification]] robustes comme la [[MultiFactorAuthentication|MFA]].
    *   Utilisation de [[SecureRoutingProtocols|protocoles de routage sécurisés]] et de [[NetworkSegmentation|segmentation réseau]] (par exemple, [[VirtualLocalAreaNetwork|VLAN]]).
    *   Pour l'[[DnsSpoofing|usurpation DNS]], déploiement de [[DomainNameSystemSecurityExtensions|DNSSEC]] (DNS Security Extensions) pour valider l'origine des réponses DNS.
    *   Pour l'[[MACSpoofing|usurpation d'adresse MAC]], activer le [[PortSecurity|filtrage d'adresses MAC]] sur les [[NetworkSwitch|commutateurs réseau]] et les points d'accès sans fil ([[AccessPoint|Access Point]]).
    *   Pour l'[[EmailSpoofing|usurpation d'e-mail]], implémentation de protocoles comme SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail) et DMARC (Domain-based Message Authentication, Reporting, and Conformance).
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[SecurityInformationAndEventManagement|SIEM]] pour l'[[SecurityMonitoring|analyse des logs]] et la détection d'[[AnomalyDetection|activités anormales]].
    *   [[NetworkMonitoring|Surveillance réseau]] et [[NetworkTrafficAnalysis|analyse du trafic]] pour identifier les [[MessagePattern|modèles de messages]] suspects.
    *   Utilisation d'outils comme [[Wireshark|Wireshark]] pour l'[[PacketSniffing|interception de paquets]] et l'analyse forensique.
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] bien défini pour isoler, contenir et éradiquer l'[[Attack|attaque]].
    *   Mise à jour et [[PatchManagement|patch management]] réguliers des [[System|systèmes]] et [[Software|logiciels]] pour corriger les [[SoftwareVulnerability|vulnérabilités]].

## 🔗 Notes Connexes
*   [[AttackVector|Vecteur d'attaque]]
*   [[Vulnerability|Vulnérabilité exploitée]]
*   [[ThreatActor|Acteur de menace associé]]
*   [[ManInTheMiddle|Attaque de l'Homme du Milieu]]
*   [[Phishing|Hameçonnage]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[Authentication|Authentification]]
*   [[Encryption|Chiffrement]]
*   [[DigitalSignature|Signature numérique]]
*   [[NetworkProtocol|Protocole Réseau]]