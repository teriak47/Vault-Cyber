---
tags:
  - attaque
  - attaque/mouvement-lateral
  - cyber-kill-chain
  - mitre-attack
  - compromission
  - reseau
  - securite/reseau
  - technique/post-exploitation
aliases:
  - Mouvement latéral
  - Lateral Movement
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Mouvement Latéral (Lateral Movement)

## 📥 Définition
> Le [[LateralMovement|mouvement latéral]] est une technique utilisée par les [[ThreatActor|attaquants]] pour naviguer et étendre leur accès au sein d'un [[InternalNetwork|réseau interne]] après avoir obtenu un point d'entrée initial. L'objectif est de trouver et d'accéder à des [[Resource|ressources]] de plus grande valeur, telles que des [[Server|serveurs]] critiques, des [[Database|bases de données]] sensibles ou des [[Account|comptes]] à [[PrivilegeEscalation|privilèges]] élevés, afin de faciliter l'[[DataExfiltration|exfiltration de données]], la [[Persistence|persistance]] ou d'autres objectifs malveillants. Cette phase est cruciale dans la [[CyberKillChain|chaîne d'attaque cyber]].

## 🎯 Vecteurs d'Attaque
*   **Vol d'[[Credential|identifiants]]** : Utilisation de techniques comme le [[CredentialStuffing|bourrage d'identifiants]], le [[PasswordSpraying|password spraying]] ou le [[PasswordCracking|cassage de mot de passe]] pour obtenir des identifiants valides.
*   **[[RemoteCodeExecution|Exécution de code à distance (RCE)]]** : Exploitation de [[SoftwareVulnerability|vulnérabilités logicielles]] sur les [[OperatingSystem|systèmes d'exploitation]] ou les [[SoftwareApplication|applications]] pour exécuter du [[Payload|code]] sur d'autres [[Host|hôtes]] du réseau.
*   **[[Exploitation|Exploitation]] de [[SoftwareVulnerability|vulnérabilités]]** : Cible des faiblesses dans les [[System|systèmes]] ou les configurations, y compris des [[ZeroDay|vulnérabilités Zero-Day]].
*   **[[Spoofing|Usurpation]] d'identité** : Techniques telles que le [[MACSpoofing|MAC spoofing]] ou l'[[AddressResolutionProtocolPoisoning|empoisonnement ARP]] pour se faire passer pour un dispositif légitime.
*   **[[Malware|Malwares]]** : Utilisation de logiciels malveillants comme les [[Trojan|chevaux de Troie]] (y compris les [[RemoteAccessTrojan|RAT]]), les [[Virus|virus]] ou les [[Worm|vers]] qui se propagent automatiquement.
*   **Services et protocoles légitimes** : Abus de services comme [[SecureShell|SSH]], [[PowerShell]], ou [[RemoteDesktopProtocol]] (non listé, donc pas de lien mais pertinent conceptuellement) pour accéder à d'autres [[Computer|ordinateurs]].
*   **[[Tunneling|Tunnelisation]]** : Création de tunnels pour masquer le [[NetworkTraffic|trafic réseau]] et contourner les [[Firewall|pare-feu]].

## 💥 Impacts Potentiels
*   [[SystemCompromise|Compromission]] étendue des systèmes
*   [[DataExfiltration|Exfiltration de données]] sensibles
*   [[PrivilegeEscalation|Élévation de privilèges]] vers des comptes d'administration
*   [[DataTheft|Vol d'informations]] d'identification et d'[[UserIdentity|identités d'utilisateur]]
*   [[Ransomware|Déploiement de rançongiciels]] sur l'ensemble du réseau
*   [[ServiceDisruption|Interruption de services]] critiques
*   [[ReputationalDamage|Dommage à la réputation]] de l'[[Enterprise|entreprise]]
*   [[FinancialLoss|Pertes financières]]

##  concret
> Un [[ThreatActor|attaquant]] parvient à compromettre un [[Client|client]] via une attaque de [[Phishing|hameçonnage]] ou l'exploitation d'une [[SoftwareVulnerability|vulnérabilité]]. Sur ce premier [[Computer|ordinateur]], il exécute un [[Script|script]] qui collecte les [[Credential|identifiants]] mis en cache de l'[[User|utilisateur]] local. Grâce à ces identifiants, il utilise ensuite [[PowerShell]] pour se connecter à un autre [[Server|serveur]] de fichiers ou une [[VirtualMachine|machine virtuelle]] dans le même [[NetworkSegment|segment réseau]]. À partir de ce nouveau point, l'attaquant répète le processus, recherchant des informations d'identification supplémentaires ou des [[SecurityVulnerabilities|vulnérabilités]] qui lui permettront d'atteindre le [[CoreLayer|cœur]] du réseau, comme un [[DomainController|contrôleur de domaine]] (non listé, donc pas de lien).

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[NetworkSegmentation|Segmentation réseau]] et [[VirtualLocalAreaNetwork|VLAN]] pour isoler les systèmes critiques.
    *   Implémentation du [[PrincipleOfLeastPrivilege|principe du moindre privilège]] et de [[RoleBasedAccessControl|contrôles d'accès basés sur les rôles]].
    *   [[MultiFactorAuthentication|Authentification multi-facteurs (MFA)]] pour tous les comptes, en particulier ceux avec des privilèges élevés.
    *   [[PatchManagement|Gestion rigoureuse des correctifs]] pour réduire les [[SoftwareVulnerability|vulnérabilités]].
    *   Politiques de mots de passe forts et [[PasswordReuse|interdiction de la réutilisation de mots de passe]].
    *   [[ZeroTrust|Architecture Zero Trust]] pour ne faire confiance à aucune entité par défaut, même à l'intérieur du réseau.
*   **Détection** :
    *   [[EndpointDetectionAndResponse|Solutions EDR]] et [[EndpointProtectionPlatform|EPP]] pour surveiller l'activité sur les [[EndDevices|terminaux]].
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour identifier les activités suspectes sur le réseau.
    *   [[SecurityInformationAndEventManagement|SIEM]] et [[NetworkMonitoring|surveillance réseau]] pour analyser les [[Log|journaux]] et les [[NetworkTrafficAnalysis|flux de trafic]].
    *   [[AnomalyDetection|Détection d'anomalies]] comportementales pour identifier les activités inhabituelles des [[User|utilisateurs]] ou des [[System|systèmes]].
*   **Réponse** :
    *   [[IncidentResponse|Plans de réponse à incident]] bien définis pour contenir, éradiquer et récupérer rapidement.
    *   Capacité de déconnexion et d'[[Isolation|isolation]] rapide des [[NetworkSegment|segments réseau]] ou [[Host|hôtes]] compromis.

## 🔗 Notes Connexes
*   **Cadre d'attaque**: [[CyberKillChain]]
*   **Référentiel de techniques**: [[MITREATTACKFramework]]
*   **Objectif fréquent**: [[PrivilegeEscalation]]
*   **Mesure de sécurité**: [[NetworkSegmentation]]
*   **Outil de défense**: [[EndpointDetectionAndResponse]]
---
