---
tags:
  - attaque
aliases:
  - Escalade de Privilèges
  - Privilege Escalation
  - PE
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Escalade de Privilèges

## 📥 Définition
> Processus par lequel un [[ThreatActor|attaquant]] obtient un niveau d'[[AccessControl|accès]] ou de permissions plus élevé que ce qui lui était initialement autorisé sur un [[Computer|système informatique]]. Elle peut être verticale (passer d'un [[User|utilisateur]] standard à un [[AdministrativePrivileges|administrateur]] ou root) ou horizontale (accéder aux privilèges d'un autre utilisateur de même niveau).

## 🎯 Vecteurs d'Attaque
*   **[[SoftwareVulnerability|Vulnérabilités logicielles]]**: Exploitation de failles dans le [[OperatingSystem|noyau]], les services système ou les [[SoftwareApplication|applications]] (ex: [[BufferOverflow|dépassement de tampon]], [[MemoryCorruption|corruption de mémoire]], [[ZeroDay|zero-day]]).
*   **[[Misconfiguration|Mauvaises configurations système]]**: Permissions de fichiers ou de répertoires faibles, services s'exécutant avec des privilèges excessifs, utilisation de [[Password|mots de passe]] par défaut.
*   **[[CredentialTheft|Vol ou réutilisation d'identifiants]]**: Utilisation de [[Credential|informations d'identification]] obtenues via [[Phishing|hameçonnage]], [[Malware|logiciels malveillants]], ou [[PasswordReuse|réutilisation de mots de passe]].
*   **[[SocialEngineering|Ingénierie sociale]]**: Inciter un [[User|utilisateur]] à exécuter un [[Malware|logiciel malveillant]] ou un [[Script|script]] avec ses propres privilèges.

## 💥 Impacts Potentiels
*   `[[UnauthorizedAccess|Accès non autorisé]]` et contrôle total du [[System|système]] compromis.
*   `[[DataBreach|Fuite de données]]` sensibles ou critiques.
*   `[[SystemCompromise|Compromission système]]` étendue, affectant d'autres [[Resource|ressources]] réseau.
*   `[[Ransomware|Déploiement de rançongiciels]]` ou d'autres [[Malware|logiciels malveillants]].
*   `[[Persistence|Établissement de persistance]]` et `[[LateralMovement|mouvement latéral]]` dans le [[Network|réseau]].

##  concret
> Un [[ThreatActor|attaquant]] a obtenu un [[Login|accès]] initial à un [[Server|serveur]] via une [[SoftwareVulnerability|vulnérabilité logicielle]] dans une [[SoftwareApplication|application]] web. Il observe que le [[WebServer|serveur web]] s'exécute avec les [[AdministrativePrivileges|privilèges administratifs]]. L'attaquant identifie une [[SoftwareVulnerability|vulnérabilité logicielle]] locale dans une librairie utilisée par le [[WebServer|serveur web]]. En exploitant cette faille, il réussit à exécuter un [[Shellcode|code]] malveillant qui lui confère les mêmes privilèges que le [[WebServer|serveur web]], lui permettant d'obtenir un contrôle total sur le [[OperatingSystem|système]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Appliquer le `[[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]` pour tous les [[User|utilisateurs]] et [[Process|processus]].
    *   Mettre en œuvre une `[[PatchManagement|gestion des correctifs]]` rigoureuse pour les [[OperatingSystem|systèmes d'exploitation]] et les [[SoftwareApplication|applications]].
    *   Effectuer le `[[SecurityHardening|durcissement des systèmes]]` en configurant de manière sécurisée et en désactivant les services inutiles.
    *   Renforcer la `[[IdentityAndAccessManagement|gestion des identités et des accès (IAM)]]` avec `[[StrongPasswordPolicy|des politiques de mots de passe forts]]` et `[[MultiFactorAuthentication|l'authentification multi-facteurs (MFA)]]`.
    *   Réaliser des `[[CodeReview|revues de code]]` pour les [[SoftwareApplication|applications]] développées en interne.
*   **Détection** :
    *   Mettre en place une `[[SecurityMonitoring|surveillance de sécurité]]` continue des `[[Log|journaux d'événements]]` et des activités système suspectes.
    *   Utiliser des systèmes `[[IntrusionDetectionSystem|IDS/IPS]]` et `[[EndpointDetectionAndResponse|EDR]]` pour détecter les tentatives d'[[Exploitation|exploitation]] et les activités post-compromission.
    *   Employer la `[[AnomalyDetection|détection d'anomalies]]` pour repérer les comportements d'[[User|utilisateurs]] ou de [[Process|processus]] anormaux.
*   **Réponse** :
    *   Avoir un `[[IncidentResponse|plan de réponse à incident]]` bien défini et testé pour contenir et éradiquer rapidement l'attaque.
    *   Maintenir des `[[BackupAndRecovery|sauvegardes]]` régulières et les tester pour garantir la `[[Availability|disponibilité]]` des [[Data|données]] et des [[System|systèmes]].

## 🔗 Notes Connexes
*   `[[Vulnerability|Vulnérabilité]]`
*   `[[Exploitation|Exploitation]]`
*   `[[PostExploitation|Post-exploitation]]`
*   `[[LateralMovement|Mouvement latéral]]`
*   `[[Authorization|Autorisation]]`
*   `[[AccessControl|Contrôle d'accès]]`
*   `[[ZeroTrust|Zéro Confiance]]`