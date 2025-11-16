---
tags:
  - attaque
  - post-exploitation
aliases:
  - Persistence
  - Persistance
  - Maintain Access
archetype: attaque
source:
  -
cssclasses:
  - max
---

# Persistance

## 📥 Définition
> La persistance est une technique employée par un [[ThreatActor|acteur de menace]] pour conserver un [[UnauthorizedAccess|accès non autorisé]] à un [[System|système]] ou [[Network|réseau]] compromis, même après un redémarrage, une déconnexion de l'utilisateur ou la correction de la [[Vulnerability|vulnérabilité]] initiale. L'objectif est de maintenir le [[CommandAndControl|contrôle]] à long terme sur la cible.

## 🎯 Vecteurs d'Attaque
*   **[[RegistryModification|Modification du Registre]] (Windows)** : Altération des clés de registre (ex: `Run`, `RunOnce`) pour exécuter un [[Payload|charge utile]] au démarrage du [[OperatingSystem|système]].
*   **[[ScheduledTask|Tâches Planifiées]]** : Création ou modification de [[Task|tâches]] planifiées pour exécuter des [[Script|scripts]] ou [[SoftwareApplication|applications]] malveillantes à des intervalles définis ou lors d'événements spécifiques.
*   **[[SystemServiceManipulation|Manipulation des Services Système]]** : Installation de nouveaux [[Process|services système]] ou modification d'existants pour lancer des [[Malware|logiciels malveillants]] avec des [[PrivilegeEscalation|privilèges élevés]].
*   **[[WebShell|Web Shells]]** : Déploiement de [[Scripting|scripts]] malveillants sur des [[WebServer|serveurs web]] compromis, permettant un [[RemoteAccess|accès distant]] via un [[WebBrowsers|navigateur web]].
*   **[[UserAccountCreation|Création de Comptes Utilisateurs]] et [[Backdoor|Backdoors]]** : Création de nouveaux [[Account|comptes utilisateurs]] avec des [[PrivilegeEscalation|privilèges élevés]] ou installation de [[Backdoor|portes dérobées]] dédiées pour un accès furtif.
*   **[[CodeInjection|Injection de Code]] / [[Hooking|Hooks]]** : Injection de [[Shellcode|code malveillant]] dans des [[Process|processus]] légitimes ou modification de [[DynamicLinkLibraries|bibliothèques dynamiques]] pour intercepter des appels et exécuter du code.
*   **[[StartupItems|Fichiers de Démarrage]] et [[Login|Scripts de Connexion]]** : Modification des fichiers de configuration ou des [[Script|scripts]] exécutés au démarrage du [[System|système]] ou à la [[Authentication|connexion]] d'un [[User|utilisateur]].
*   **[[Rootkit|Rootkits]]** : Logiciels conçus pour masquer la présence de l'[[ThreatActor|attaquant]] et d'autres [[Malware|logiciels malveillants]] sur le [[System|système]].

## 💥 Impacts Potentiels
*   [[DataExfiltration|Exfiltration de Données]]
*   [[PrivilegeEscalation|Élévation de privilèges]] continue
*   [[LateralMovement|Mouvement Latéral]] à travers le [[Network|réseau]]
*   Déploiement ultérieur de [[Ransomware|ransomware]] ou [[Spyware|spyware]]
*   Maintien d'une [[AdvancedPersistentThreat|APT]] (Menace Persistante Avancée)

##  concret
> Après avoir réussi une [[InitialAccess|attaque par phishing]] et obtenu un accès initial à un [[Computer|ordinateur]] d'entreprise, un attaquant déploie un [[RemoteAccessTrojan|RAT]] et configure une [[ScheduledTask|tâche planifiée]] pour que le [[RAT]] se lance à chaque démarrage du [[System|système]]. Même si l'utilisateur déconnecte sa session ou si la [[Vulnerability|vulnérabilité]] initiale est patchée, l'attaquant conserve son accès via la [[tâche planifiée]], lui permettant de continuer à surveiller le [[System|système]] ou à effectuer des [[LateralMovement|mouvements latéraux]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Application du [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]].
    *   [[PatchManagement|Gestion rigoureuse des correctifs]] et [[VulnerabilityManagement|gestion des vulnérabilités]].
    *   [[SecurityAwareness|Sensibilisation des utilisateurs]] aux [[SocialEngineering|techniques d'ingénierie sociale]].
*   **Détection** :
    *   Déploiement de [[EndpointDetectionAndResponse|solutions EDR]] pour détecter les activités suspectes (modifications du registre, création de services, exécutions de tâches planifiées inhabituelles).
    *   Utilisation de [[SecurityInformationAndEventManagement|SIEM]] pour la corrélation des [[Log|logs]] et la détection d'[[AnomalyDetection|anomalies]].
    *   [[ThreatHunting|Threat Hunting]] proactif pour rechercher des signes de compromission et de persistance.
*   **Réponse** :
    *   Mise en place d'un [[IncidentResponse|plan de réponse à incident]] incluant des procédures d'éradication des mécanismes de persistance.
    *   Réalisation de [[SecurityAudit|audits de sécurité]] réguliers pour identifier les modifications non autorisées.

## 🔗 Notes Connexes
*   [[InitialAccess|Accès Initial]]
*   [[PostExploitation|Post-Exploitation]]
*   [[CommandAndControl|Commande et Contrôle (C2)]]
*   [[MITREATTACKFramework|MITRE ATT&CK]]
*   [[DigitalForensicsAndIncidentResponse|Forensique Numérique et Réponse aux Incidents (DFIR)]]
*   [[ThreatActor|Acteur de menace]]