---
tags:
  - attaque
  - attaque/intrusion
  - sécurité/compromission
aliases:
  - Intrusion
  - Cyber intrusion
  - Compromission (sécurité)
archetype: attaque
mitre_id: 
source:
  - MITRE ATT&CK
cssclasses:
  - max
---

# Intrusion

> [!summary] En Bref
> Une intrusion est l'accès non autorisé à un [[Network|réseau]], un système informatique ou une ressource numérique, souvent dans le but de voler des [[Data|données]], de perturber les opérations ou d'établir une [[Persistence|persistance]] malveillante.

## 🔬 Analyse Technique

### Fonctionnement
Une [[Intrusion|intrusion]] cybernétique se déroule généralement en plusieurs étapes. Elle commence souvent par une phase d'[[InitialAccess|accès initial]] où un attaquant exploite une [[SecurityVulnerabilities|vulnérabilité de sécurité]] pour obtenir un point d'entrée. Cela peut impliquer l'utilisation d'un [[Exploit|exploit]] contre des applications ou des services exposés, ou l'ingénierie sociale pour compromettre les [[Credential|identifiants]] d'un [[UserIdentity|utilisateur]]. Une fois l'accès obtenu, l'attaquant cherche à exécuter du [[Malware|logiciel malveillant]], à élever ses [[PrivilegeEscalation|privilèges]] et à établir une [[Persistence|persistance]] au sein du système ou du [[EnterpriseNetwork|réseau d'entreprise]] afin de maintenir l'accès même après un redémarrage ou une correction de la vulnérabilité initiale. Les objectifs peuvent varier, allant du [[DataTheft|vol de données]] et de l'[[DataExfiltration|exfiltration de données]] à la modification ou la destruction de [[Data|données]].

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant effectue un [[PortScanning|balayage de ports]] pour identifier les services ouverts et les [[SecurityVulnerabilities|vulnérabilités]] potentielles sur les systèmes cibles.
> 2.  **Accès Initial** : Une faille de sécurité connue est exploitée dans un serveur web, permettant à l'attaquant d'exécuter du [[RemoteCodeExecution|code à distance]] et d'accéder au système.
> 3.  **Exécution & Persistance** : Un [[RemoteAccessTrojan|cheval de Troie d'accès à distance (RAT)]] est installé, assurant la [[Persistence|persistance]] et un contrôle discret sur la machine compromise.
> 4.  **Élévation de Privilèges** : L'attaquant utilise une [[Exploitation|exploitation]] locale pour passer d'un compte utilisateur standard à un compte avec des droits d'administrateur.
> 5.  **Exfiltration** : Les [[SensitiveData|données sensibles]] sont identifiées et transférées vers un serveur contrôlé par l'attaquant.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : Initial Access / Execution / Persistence / Privilege Escalation
*   **Technique** : `T1190` - Exploit Public-Facing Application
*   **Technique** : `T1078` - Valid Accounts
*   **Technique** : `T1566` - Phishing

## 🎯 Vecteurs d'Attaque
*   **[[SecurityVulnerabilities|Vulnérabilités logicielles]]** : Exploitation de failles dans les systèmes d'exploitation, applications web ou services réseau.
*   **[[CredentialStuffing|Bourrage d'identifiants]]** : Utilisation de [[Password|mots de passe]] volés ou faibles pour accéder à des comptes.
*   **[[Phishing|Hameçonnage]]** : Incitation des [[User|utilisateurs]] à révéler des informations sensibles ou à exécuter des [[Malware|logiciels malveillants]].
*   **[[MalwareDistribution|Distribution de logiciels malveillants]]** : Infection via [[Email|courriels]], sites web compromis, ou [[USB|clés USB]].

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   Mettre en œuvre une [[PatchManagement|gestion des correctifs]] rigoureuse pour éliminer les [[SecurityVulnerabilities|vulnérabilités]] connues.
> *   Appliquer le [[LeastPrivilege|principe du moindre privilège]] pour tous les [[Account|comptes utilisateurs]] et de service.
> *   Utiliser une [[MultiFactorAuthentication|authentification multi-facteurs (MFA)]] pour protéger les [[Login|connexions]].
> *   Déployer une [[EndpointProtectionPlatform|plateforme de protection des endpoints (EPP)]] et une [[EndpointDetectionAndResponse|détection et réponse des endpoints (EDR)]].
*   Éduquer les [[User|utilisateurs]] sur la [[SecurityAwareness|sensibilisation à la sécurité]] afin de reconnaître les tentatives de [[Phishing|hameçonnage]] et autres attaques d'ingénierie sociale.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **Logs Système** : Surveillance des [[Log|journaux]] d'événements pour les activités suspectes (tentatives de [[Login|connexion]] échouées, exécutions de [[Process|processus]] anormaux).
> *   **[[NetworkTrafficAnalysis|Analyse du trafic réseau]]** : Détection de [[MessagePattern|modèles de messages]] ou de [[DataExfiltration|flux de données anormaux]] vers des destinations externes inattendues.
> *   **[[SecurityInformationAndEventManagement|SIEM]]** : Corrélation des événements de sécurité provenant de diverses sources pour identifier les [[AnomalyDetection|anomalies]] et les indicateurs de compromission.
> *   **[[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]]** : Utilisation de signatures pour identifier les attaques connues.

### 🚒 Réponse à Incident
1.  **Identification** : Confirmer la nature et l'étendue de l'[[Intrusion|intrusion]] en analysant les [[Log|journaux]] et les alertes des [[SecurityMonitoring|systèmes de surveillance]].
2.  **Isolation** : [[Isolation|Isoler]] les systèmes et [[NetworkSegment|segments de réseau]] affectés pour contenir la menace et prévenir sa propagation.
3.  **Éradication** : Supprimer la source de l'[[Intrusion|intrusion]] (par exemple, supprimer le [[Malware|logiciel malveillant]], corriger les [[SecurityVulnerabilities|vulnérabilités]], révoquer les [[Credential|identifiants]] compromis).
4.  **Récupération** : Restaurer les systèmes et les [[Data|données]] à un état sain et sécurisé, souvent à partir de [[Backup|sauvegardes]] validées.

## 🔗 Connexions
*   **[[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]**
*   **[[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]**
*   **[[PenetrationTesting|Test d'Intrusion]]**
*   **[[ZeroTrust|Architecture Zero Trust]]**