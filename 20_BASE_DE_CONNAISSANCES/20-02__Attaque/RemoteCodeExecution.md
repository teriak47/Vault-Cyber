---
tags:
  - attaque
aliases:
  - Exécution de Code à Distance
  - RCE
  - Remote Code Execution
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Exécution de Code à Distance (RCE)

## 📥 Définition
> L'[[RemoteCodeExecution|Exécution de Code à Distance]] (RCE) est une [[Attack|attaque]] où un [[ThreatActor|attaquant]] peut exécuter du [[CodeDevelopment|code]] arbitraire sur une [[Computer|machine]] ou un [[Server|serveur]] cible. L'objectif est généralement d'obtenir un [[SystemCompromise|contrôle total]] sur le [[System|système]] compromis, de voler des [[Data|données]] ou d'établir une [[Persistence|persistance]].

## 🎯 Vecteurs d'Attaque
*   **[[SoftwareVulnerability|Vulnérabilités logicielles]]** : Exploitation de failles dans les [[Software|logiciels]] (ex: [[BufferOverflow|dépassements de tampon]], [[SqlInjection|injections SQL]], [[DeserializationVulnerability|vulnérabilités de désérialisation]] [[UnvalidatedInput|ou entrées non validées]]).
*   **[[WebApplications|Applications web]] vulnérables** : Failles dans les [[WebServer|serveurs web]] ou les applications qui permettent l'injection de commandes via des formulaires, des API ou des URL.
*   **[[FileTransfer|Téléchargements de fichiers]] malveillants** : Incitation des [[User|utilisateurs]] à exécuter des fichiers contenant du [[Malware|code malveillant]].
*   **[[RemoteAccessTrojan|Chevaux de Troie d'accès à distance (RAT)]]** : Utilisation de [[Trojan|Trojans]] pour établir un [[CommandAndControl|canal de commande et contrôle]] et exécuter du code à distance.

## 💥 Impacts Potentiels
*   [[SystemCompromise|Compromission complète du système]]
*   [[DataTheft|Vol de données]] ou [[DataExfiltration|exfiltration]]
*   [[MalwareDistribution|Déploiement de logiciels malveillants]] supplémentaires (ex: [[Ransomware|ransomware]], [[Worm|vers]])
*   [[DenialOfService|Déni de service]]
*   [[PrivilegeEscalation|Élévation de privilèges]]
*   Intégration dans un [[Botnet|botnet]]

## 💡 Exemple concret
> Un [[ThreatActor|attaquant]] découvre une [[SoftwareVulnerability|vulnérabilité]] dans une [[WebApplications|application web]] permettant à un [[User|utilisateur]] de télécharger une image. En manipulant le processus de téléchargement, l'attaquant remplace l'image par un fichier de script malveillant (par exemple, un [[Shellcode|script PHP]]) qui est ensuite exécuté par le [[WebServer|serveur web]]. Ce script lui donne accès à un [[Shell|shell]] sur le [[Server|serveur]], lui permettant d'exécuter des [[Command|commandes]] à distance.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[PatchManagement|Gestion rigoureuse des patchs]] et des mises à jour logicielles.
    *   [[CodeReview|Revue de code]] et [[SecureDevelopmentLifeCycle|cycle de développement sécurisé]] [[SecureDevelopmentLifeCycle|pour identifier et corriger les vulnérabilités]].
    *   [[InputValidation|Validation des entrées]] stricte pour toutes les données fournies par l'[[User|utilisateur]].
    *   [[WebApplicationFirewall|Pare-feu applicatifs web (WAF)]] pour filtrer le trafic malveillant.
    *   Application du [[PrincipleOfLeastPrivilege|principe du moindre privilège]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|de prévention d'intrusion (IPS)]].
    *   [[EndpointDetectionAndResponse|Solutions EDR]] et [[EndpointProtectionPlatform|EPP]].
    *   [[SecurityInformationAndEventManagement|SIEM]] pour la [[SecurityMonitoring|surveillance de sécurité]] et l'[[AnomalyDetection|analyse des anomalies]].
*   **Réponse** :
    *   Mise en place et test d'un [[IncidentResponse|plan de réponse aux incidents]] robuste.
    *   Isolation rapide des systèmes compromis.

## 🔗 Notes Connexes
*   [[Exploit|Exploit]]
*   [[Vulnerability|Vulnérabilité]]
*   [[Shellcode|Shellcode]]
*   [[ZeroDay|Vulnérabilité Zero-Day]]
*   [[BufferOverflow|Buffer Overflow]]
*   [[SqlInjection|Injection SQL]]