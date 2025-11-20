---
tags:
  - attaque
  - attaque/persistance
  - attaque/porte-derobee
aliases:
  - Porte Dérobée
  - Backdoor
  - porte dérobée
archetype: attaque
mitre_id: T1505
source:
cssclasses:
  - max
---

# Porte Dérobée (Backdoor)

> [!summary] En Bref
> Une porte dérobée est une méthode secrète qui permet de contourner les contrôles d'[[Authentication|authentification]] ou d'[[AccessControl|accès]] normaux dans un système, un logiciel ou un [[Network|réseau]], offrant un [[UnauthorizedAccess|accès non autorisé]] et [[Persistence|persistant]]. Ces portes dérobées peuvent être délibérément intégrées par les développeurs pour la maintenance ou installées par des [[ThreatActor|acteurs de menace]] après une [[SystemCompromise|compromission du système]].

## 🔬 Analyse Technique

### Fonctionnement
Une porte dérobée fonctionne en établissant un point d'entrée caché qui permet à un attaquant d'éviter les mécanismes de [[Authentication|sécurité]] standards pour obtenir un accès de haut niveau, tel que l'accès root ou administratif. Une fois installée, elle assure une [[Persistence|persistance]] au sein du système, même après des redémarrages ou des modifications des [[Credential|identifiants]]. Ce mécanisme peut se présenter sous diverses formes, comme des scripts malveillants, des modules logiciels, ou des [[RemoteAccessTrojan|chevaux de Troie d'accès à distance (RAT)]]. Les attaquants peuvent alors utiliser cet accès pour exécuter des commandes, [[DataExfiltration|exfiltrer des données sensibles]], déployer d'autres [[Malware|logiciels malveillants]], ou servir de passerelle pour des [[Attack|attaques]] ultérieures. La difficulté de détection des portes dérobées réside souvent dans leur capacité à se faire passer pour des processus légitimes.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : Un [[ThreatActor|attaquant]] identifie un [[WebServer|serveur web]] comme cible potentielle, souvent par l'[[PortScanning|analyse de ports]] ou la recherche de [[SecurityVulnerabilities|vulnérabilités]].
> 2.  **Exploitation** : Il réussit à exploiter une [[SoftwareVulnerability|vulnérabilité logicielle]] (par exemple, une injection de fichier à distance pour installer une [[WebShell|coque web]]) sur le [[WebServer|serveur web]].
> 3.  **Installation de la Backdoor** : Après avoir obtenu un [[Access|accès]] initial, l'attaquant installe une [[Backdoor|porte dérobée]], souvent sous la forme d'un script ou d'un [[RemoteAccessTrojan|RAT]]. Cette porte dérobée lui permet de contourner les futures [[Authentication|authentifications]] et de maintenir un [[Persistence|accès persistant]] au système, même si la [[Vulnerability|vulnérabilité initiale]] est corrigée ou si les identifiants sont modifiés.
> 4.  **Accès et Contrôle** : L'attaquant utilise cet [[Access|accès]] persistant pour réaliser de l'[[DataExfiltration|exfiltration de données]], héberger d'autres [[Malware|logiciels malveillants]] ou lancer des [[Attack|attaques]] vers d'autres systèmes au sein du [[Network|réseau]].

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : [[Persistence]], [[DefenseEvasion]], [[PrivilegeEscalation]]
*   **Technique** : `T1505` - [[ServerSoftwareComponent|Server Software Component]]
    *   `T1505.003` - [[WebShell|Web Shell]] (une forme courante de porte dérobée)

## 🎯 Vecteurs d'Attaque
*   **[[SupplyChainAttack|Attaques sur la chaîne d'approvisionnement]]**: Insertion intentionnelle par des développeurs malveillants lors de la conception du logiciel ou via des composants tiers compromis.
*   **[[Exploitation|Exploitation de vulnérabilités]]**: Utilisation de [[SoftwareVulnerability|failles logicielles]] connues ou de [[ZeroDay|zero-days]] pour installer la porte dérobée et obtenir un [[Persistence|accès persistant]].
*   **[[MalwareDistribution|Distribution de logiciels malveillants]]**: Intégration dans des [[Trojan|chevaux de Troie]], des [[Virus|virus]] ou des [[Worm|vers]] pour une installation discrète sur les [[EndDevices|systèmes cibles]].

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   [[CodeReview|Révisions de code]] et [[SecurityAudit|audits de sécurité]] réguliers pour détecter des fonctionnalités non documentées.
> *   [[SoftwareSupplyChainSecurity|Sécurité de la chaîne d'approvisionnement logicielle]] pour prévenir l'insertion de portes dérobées.
> *   [[SecurityByDesign|Sécurité dès la conception]] des applications et des systèmes.
> *   [[PatchManagement|Gestion des correctifs]] et [[VulnerabilityManagement|gestion des vulnérabilités]] pour minimiser les surfaces d'attaque.
> *   Appliquer le [[LeastPrivilege|principe de moindre privilège]] pour les comptes utilisateurs et de service.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   Utilisation de [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour surveiller les comportements réseau et système anormaux.
> *   [[EndpointDetectionAndResponse|Solutions EDR]] pour détecter les activités malveillantes au niveau des [[EndDevices|points de terminaison]].
> *   [[SecurityInformationAndEventManagement|SIEM]] pour l'[[SecurityMonitoring|analyse des logs]] et la détection d'[[AnomalyDetection|anomalies]].
> *   Surveillance des logs d'application pour tout comportement inhabituel lié à l'installation de composants logiciels.
> *   Vérification régulière de l'[[Integrity|intégrité]] des composants logiciels sur les services critiques.
> *   Surveillance du [[NetworkTraffic|trafic réseau]] pour des communications inhabituelles ou des canaux de commande et contrôle cachés.
> *   Analyse des modifications de fichiers dans les répertoires web des serveurs pour identifier l'implantation de scripts de [[WebShell|coque web]].

### 🚒 Réponse à Incident
1.  **Isolation** : Isoler immédiatement le système compromis du [[Network|réseau]] pour empêcher la [[Propagation|propagation]] de l'attaque et la [[DataExfiltration|fuite de données]].
2.  **Eradication** : Supprimer la porte dérobée et tout [[Malware|logiciel malveillant]] associé. Cela peut nécessiter une reconstruction complète du système dans les cas graves.
3.  **Récupération** : Restaurer les systèmes à partir de [[Backup|sauvegardes]] saines et durcir la [[Security|sécurité]] pour prévenir de futures intrusions.

## 🔗 Connexions
*   **Variante** : [[Rootkit]]
*   **Outil lié** : [[WebShell]], [[ReverseShell]]