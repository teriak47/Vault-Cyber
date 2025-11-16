---
tags:
  - attaque
  - attaque/reverse-shell
aliases:
  - Reverse Shell
  - Shell inversé
  - Coque inversée
  - Reverse Shell Attack
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Reverse Shell (Coque Inversée)

## 📥 Définition
> Une [[ReverseShell|Reverse Shell]] est une technique d'[[Exploitation|exploitation]] où un [[Computer|ordinateur]] cible est contraint d'établir une connexion [[Network|réseau]] *sortante* vers un [[ThreatActor|acteur de menace]] qui est en écoute. L'objectif principal est de contourner les [[Firewall|pare-feu]] qui bloquent les connexions entrantes mais autorisent les connexions sortantes, permettant ainsi à l'attaquant d'obtenir un [[Shell|shell]] interactif sur le [[System|système]] cible et d'en prendre le [[CommandAndControl|contrôle]].

## 🎯 Vecteurs d'Attaque
*   **[[RemoteCodeExecution|Exécution de Code à Distance (RCE)]]**: L'attaquant exploite une [[SoftwareVulnerability|vulnérabilité logicielle]] pour exécuter un [[Script|script]] ou une [[Command|commande]] sur le [[System|système]] cible qui initie la connexion inverse.
*   **[[Phishing|Phishing]] / [[SocialEngineering|Ingénierie Sociale]]**: Un [[User|utilisateur]] est trompé pour télécharger et exécuter un [[Malware|logiciel malveillant]] (souvent un [[Trojan|Cheval de Troie]]) qui contient le code du reverse shell.
*   **[[MalwareDistribution|Distribution de Malware]]**: Un [[Worm|ver]] ou autre [[Malware|logiciel malveillant]] déjà présent sur le [[Network|réseau]] peut installer une [[Backdoor|porte dérobée]] avec une fonctionnalité de reverse shell.

## 💥 Impacts Potentiels
*   [[UnauthorizedAccess|Accès non autorisé]] complet au [[System|système]] compromis.
*   [[DataTheft|Vol de données]] et [[DataExfiltration|exfiltration de données]] sensibles.
*   [[PrivilegeEscalation|Élévation de privilèges]] sur le [[System|système]] compromis.
*   [[Persistence|Persistance]] sur le [[System|système]] pour maintenir l'[[UnauthorizedAccess|accès non autorisé]].
*   Utilisation du [[System|système]] compromis comme point de pivot pour attaquer d'autres [[Resource|ressources]] internes.

## 💡 Exemple concret
> Un [[ThreatActor|acteur de menace]] identifie une [[SoftwareVulnerability|vulnérabilité logicielle]] sur un [[WebServer|serveur web]] qui permet l'[[RemoteCodeExecution|exécution de code à distance]]. Il envoie une [[Attack|attaque]] via une requête [[HypertextTransferProtocol|HTTP]] malveillante, forçant le [[WebServer|serveur]] à exécuter une [[Command|commande]] qui lance un [[Script|script]] [[Python|Python]]. Ce [[Script|script]] établit ensuite une connexion [[TransmissionControlProtocol|TCP]] sortante vers l'[[InternetProtocolAddress|adresse IP]] de l'attaquant sur un [[PortNumber|port]] spécifique où l'attaquant écoute avec un [[Tool|outil]] comme [[Netcat|Netcat]]. Une fois la connexion établie, l'attaquant obtient un [[Shell|shell]] interactif sur le [[WebServer|serveur]], lui permettant d'exécuter des [[Command|commandes]] comme s'il était directement connecté.

## 🛡️ Mesures de Mitigation
*   **Prévention** : 
    *   Application rigoureuse du [[PatchManagement|patch management]] pour corriger les [[SoftwareVulnerability|vulnérabilités logicielles]].
    *   Configuration stricte des [[Firewall|pare-feu]] pour limiter les connexions sortantes aux seuls [[OnlineServices|services]] autorisés.
    *   [[CodeReview|Revue de code]] régulière pour identifier et corriger les failles menant à des [[RemoteCodeExecution|RCE]].
    *   Mise en œuvre du [[PrincipleOfLeastPrivilege|principe du moindre privilège]] pour les [[Process|processus]] et [[User|utilisateurs]].
    *   [[SecurityByDesign|Sécurité dès la conception]] dans le développement [[Software|logiciel]].
*   **Détection** :
    *   Utilisation de [[IntrusionDetectionSystem|systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour surveiller le [[NetworkTrafficAnalysis|trafic réseau]] et les activités [[System|système]] inhabituelles (connexions sortantes inattendues, [[Shell|shells]] interactifs).
    *   [[SecurityInformationAndEventManagement|SIEM]] pour l'analyse des [[Log|logs]] à la recherche de schémas d'[[Attack|attaque]] ou de comportements anormaux.
    *   [[NetworkMonitoring|Surveillance réseau]] active pour identifier les connexions [[TransmissionControlProtocol|TCP]] suspectes.
    *   [[EndpointDetectionAndResponse|EDR]] et [[EndpointProtectionPlatform|EPP]] pour la surveillance des [[EndDevices|endpoints]].
*   **Réponse** :
    *   Mise en place d'un [[IncidentResponse|plan de réponse à incident]] pour réagir rapidement aux compromissions.
    *   [[ForensicAnalysis|Analyse forensique]] des [[System|systèmes]] compromis pour comprendre le mode opératoire et les impacts.

## 🔗 Notes Connexes
*   [[Shellcode|Shellcode]]
*   [[Exploitation|Exploitation]]
*   [[CommandAndControl|Commande et Contrôle (C2)]]
*   [[Persistence|Persistance]]
*   [[Firewall|Pare-feu]]
*   [[Shell|Shell]]
*   [[RemoteCodeExecution|Exécution de Code à Distance]]
*   [[Vulnerability|Vulnérabilité]]
*   [[ThreatActor|Acteur de menace]]