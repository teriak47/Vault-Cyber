---
tags:
  - attaque
aliases:
  - Attaque Numérique
  - Digital Attack
  - Cyber Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Attaque Numérique (Digital Attack)

## 📥 Définition
> Une [[DigitalAttack|attaque numérique]] est toute tentative malveillante visant à compromettre, endommager, voler ou détruire les [[Data|données]], les [[Computer|systèmes informatiques]] ou les [[Network|réseaux]] d'une [[Enterprise|organisation]] ou d'un individu. Elle exploite les [[Vulnerability|vulnérabilités]] des systèmes d'[[InformationSecurity|information]] pour atteindre les objectifs du [[ThreatActor|cyberacteur]].

## 🎯 Vecteurs d'Attaque
*   **[[Email|Courriel]]** : [[Phishing|Hameçonnage]], [[MalwareDistribution|distribution de logiciels malveillants]].
*   **[[WebBrowsers|Navigateurs Web]] et [[OnlineServices|Services en ligne]]** : [[CrossSiteScripting|XSS]], [[SqlInjection|injections SQL]], [[CredentialStuffing|bourrage d'identifiants]].
*   **[[Network|Réseaux]]** : [[DistributedDenialOfService|attaques DDoS]], [[ManInTheMiddle|attaques de l'Homme du Milieu]], [[PortScanning|balayage de ports]].
*   **[[Software|Logiciels]] et [[OperatingSystem|Systèmes d'exploitation]]** : Exploitation de [[SoftwareVulnerability|vulnérabilités logicielles]], déploiement de [[Malware|malware]].
*   **[[InternetofThings|IoT]]** : Dispositifs connectés peu sécurisés, servant de porte d'entrée ou de point de relais pour des [[Attack|attaques]].

## 💥 Impacts Potentiels
*   [[DataBreach|Fuite de données]] et [[DataTheft|vol de données]] sensibles.
*   [[ServiceDisruption|Interruption de service]] et [[DenialOfService|déni de service]].
*   [[SystemCompromise|Compromission de systèmes]] et [[PrivilegeEscalation|élévation de privilèges]].
*   [[FinancialLoss|Perte financière]] directe (rançons, fraudes) ou indirecte (coûts de récupération, amendes).
*   [[ReputationalDamage|Atteinte à la réputation]] et perte de confiance.

##  Exemple concret
> Un [[ThreatActor|cyberacteur]] identifie une [[SoftwareVulnerability|vulnérabilité logicielle]] sur un [[WebServer|serveur web]] public. Il utilise un [[Exploit|exploit]] pour exécuter du [[RemoteCodeExecution|code à distance]] et prendre le contrôle du serveur. Après avoir obtenu l'[[UnauthorizedAccess|accès non autorisé]], il tente de se déplacer latéralement dans le [[CorporateNetwork|réseau d'entreprise]] pour [[DataExfiltration|exfiltrer des données]] sensibles.

## 🛡️ Mesures de Mitigation
*   **Prévention** : [[SecurityPolicy|Politiques de sécurité]] robustes, [[PatchManagement|gestion des patchs]] régulière, [[Firewall|pare-feu]], [[Antivirus|logiciels antivirus]], [[EmailFiltering|filtrage d'emails]], [[SecurityAwareness|sensibilisation des utilisateurs]].
*   **Détection** : [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]], [[SecurityInformationAndEventManagement|SIEM]] pour la [[SecurityMonitoring|surveillance de sécurité]].
*   **Réponse** : [[IncidentResponse|Plan de réponse à incident]] bien défini, [[BackupAndRecovery|stratégies de sauvegarde et de récupération]], [[BusinessContinuityPlanning|planification de la continuité des activités]].
*   **Contrôle d'accès** : [[Authentication|Authentification]] forte, y compris [[MultiFactorAuthentication|MFA]], et [[AccessControl|contrôles d'accès]] basés sur le [[PrincipleOfLeastPrivilege|principe du moindre privilège]].

## 🔗 Notes Connexes
*   [[Cybersecurity|Cybersécurité]]
*   [[Threat|Menace]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Exploit|Exploit]]
*   [[AttackVector|Vecteur d'attaque]]
*   [[AttackSurface|Surface d'attaque]]
*   [[DefenseInDepth|Défense en Profondeur]]