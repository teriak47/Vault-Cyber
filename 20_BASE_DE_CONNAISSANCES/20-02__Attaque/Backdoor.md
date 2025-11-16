---
tags:
  - attaque
aliases:
  - Porte Dérobée
  - Backdoor
  - porte dérobée
archetype: attaque
source:
cssclasses:
  - max
---

# Porte Dérobée (Backdoor)

## 📥 Définition
> Une méthode secrète pour contourner les contrôles d'[[Authentication|authentification]] ou d'[[AccessControl|accès]] normaux dans un [[System|système informatique]], un [[Software|logiciel]] ou un [[Network|réseau]], permettant un [[UnauthorizedAccess|accès non autorisé]] et [[Persistence|persistant]]. Les [[Backdoor|portes dérobées]] peuvent être intentionnellement créées ou insérées par des [[ThreatActor|acteurs de menace]] après une [[SystemCompromise|compromission système]].

## 🎯 Vecteurs d'Attaque
*   **[[SupplyChainAttack|Attaques sur la chaîne d'approvisionnement]]**: Insertion intentionnelle par des développeurs malveillants lors de la conception du [[Software|logiciel]] ou via des composants tiers compromis.
*   **[[Exploitation|Exploitation de vulnérabilités]]**: Utilisation de [[SoftwareVulnerability|failles logicielles]] connues ou de [[ZeroDay|zero-days]] pour installer la [[Backdoor|porte dérobée]] et obtenir un [[Persistence|accès persistant]].
*   **[[MalwareDistribution|Distribution de logiciels malveillants]]**: Intégration dans des [[Trojan|chevaux de Troie]], des [[Virus|virus]] ou des [[Worm|vers]] pour une installation discrète sur les [[EndDevices|systèmes cibles]].

## 💥 Impacts Potentiels
*   [[UnauthorizedAccess|Accès Non Autorisé]] aux [[Resource|ressources]] et aux [[SensitiveData|données sensibles]].
*   [[DataExfiltration|Exfiltration de Données]] et [[DataTheft|vol de données]].
*   [[SystemCompromise|Compromission complète du système]] ou du [[Network|réseau]].
*   [[PrivilegeEscalation|Élévation de Privilèges]] pour l'[[ThreatActor|attaquant]].
*   [[ServiceDisruption|Interruption de service]] ou altération de l'[[Integrity|intégrité]] du [[System|système]].

## concret
> Un [[ThreatActor|attaquant]] réussit à exploiter une [[SoftwareVulnerability|vulnérabilité logicielle]] sur un [[WebServer|serveur web]]. Après avoir obtenu un accès initial, il installe une [[Backdoor|porte dérobée]] sous la forme d'un script ou d'un [[RemoteAccessTrojan|RAT]]. Cette [[Backdoor|porte dérobée]] lui permet de contourner les futures [[Authentication|authentifications]] et de maintenir un [[Persistence|accès persistant]] au [[System|système]], même si la [[Vulnerability|vulnérabilité initiale]] est corrigée ou si les [[Credential|identifiants]] sont modifiés. L'[[ThreatActor|attaquant]] peut ensuite utiliser cet accès pour réaliser de l'[[DataExfiltration|exfiltration de données]], héberger d'autres [[Malware|logiciels malveillants]] ou lancer des [[Attack|attaques]] vers d'autres [[System|systèmes]].

## 🛡️ Mesures de Mitigation
*   **Prévention** : [[CodeReview|Révisions de code]] et [[SecurityAudit|audits de sécurité]] réguliers pour détecter des fonctionnalités non documentées ; [[SoftwareSupplyChainSecurity|Sécurité de la chaîne d'approvisionnement logicielle]] ; [[SecurityByDesign|Sécurité dès la conception]] ; [[PatchManagement|Gestion des correctifs]] et [[VulnerabilityManagement|gestion des vulnérabilités]].
*   **Détection** : Utilisation de [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour surveiller les comportements réseau et système anormaux ; [[EndpointDetectionAndResponse|Solutions EDR]] pour détecter les activités malveillantes au niveau des [[EndDevices|points de terminaison]] ; [[SecurityInformationAndEventManagement|SIEM]] pour l'[[SecurityMonitoring|analyse des logs]] et la détection d'[[AnomalyDetection|anomalies]].
*   **Réponse** : Mise en place et test régulier d'un [[IncidentResponse|plan de réponse à incident]] pour éradiquer la [[Backdoor|porte dérobée]] et restaurer le [[System|système]] compromis.

## 🔗 Notes Connexes
*   [[Malware|Logiciel Malveillant]]
*   [[Trojan|Cheval de Troie]]
*   [[RemoteAccessTrojan|RAT]]
*   [[Persistence|Persistance]]
*   [[ZeroDay|Vulnérabilité Zero-Day]]
*   [[SystemCompromise|Compromission de Système]]
*   [[Vulnerability|Vulnérabilité]]
*   [[AttackVector|Vecteur d'attaque]]
*   [[SupplyChainAttack|Attaque sur la chaîne d'approvisionnement]]
---