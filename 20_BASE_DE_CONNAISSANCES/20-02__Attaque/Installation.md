---
tags:
  - attaque
  - cyberkillchain
aliases:
  - Phase d'Installation
  - Installation Phase
  - Installation (Cyberattaque)
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Phase d'Installation (Cyberattaque)

## 📥 Définition
> La phase d'[[Installation]] est une étape cruciale d'une [[CyberKillChain|cyberattaque]] où l'[[ThreatActor|attaquant]] établit une présence durable ou déploie des composants malveillants sur le [[System|système]] cible après un [[InitialAccess|accès initial]] réussi. Son objectif principal est d'assurer la [[Persistence|persistance]] et de préparer les actions ultérieures.

## 🚀 Techniques d'Installation
*   **Déploiement de [[Malware|Logiciels Malveillants]]**: L'[[ThreatActor|attaquant]] installe divers types de logiciels nuisibles, tels que des [[Ransomware|rançongiciels]], des [[Virus|virus]], des [[Worm|vers]], des [[Trojan|chevaux de Troie]] (y compris des [[RemoteAccessTrojan|RAT]]), ou d'autres programmes pour atteindre ses objectifs.
*   **Mise en place de [[Backdoor|Portes Dérobées]] et [[Rootkit|Rootkits]]**: Création de points d'[[UnauthorizedAccess|accès non autorisé]] cachés ou d'outils pour masquer la présence de l'[[ThreatActor|attaquant]] et maintenir l'accès futur, souvent avec des [[PrivilegeEscalation|privilèges élevés]].
*   **Modification du [[System|système]]**: Altération de la [[NetworkConfiguration|configuration du système]], des registres, des services ou des fichiers de démarrage pour assurer la [[Persistence|persistance]] des artefacts malveillants même après un redémarrage.
*   **Staging d'[[Tool|Outils]]**: Téléchargement et préparation d'[[Tool|outils]] supplémentaires nécessaires pour les phases ultérieures de l'[[Attack|attaque]], comme le [[LateralMovement|mouvement latéral]] ou l'[[DataExfiltration|exfiltration de données]].

## 💥 Impacts Potentiels
*   [[SystemCompromise|Compromission complète du système]]
*   [[DataBreach|Vol de données]] ou [[DataCorruption|corruption de données]]
*   [[ServiceDisruption|Interruption de service]] (via [[Ransomware|rançongiciel]] ou destruction)
*   [[PrivilegeEscalation|Élévation de privilèges]] durable
*   [[FinancialLoss|Pertes financières]] et [[ReputationalDamage|dommages à la réputation]]

## 📝 Exemple d'Actions d'Installation
> Après avoir exploité une [[SoftwareVulnerability|vulnérabilité logicielle]] pour obtenir un [[InitialAccess|accès initial]], l'[[ThreatActor|attaquant]] télécharge et exécute un [[Trojan|cheval de Troie]] sur le [[Server|serveur]] compromis. Ce [[Malware|logiciel malveillant]] modifie alors les entrées du registre pour se lancer automatiquement au démarrage du [[System|système]] et ouvre une [[Backdoor|porte dérobée]] pour permettre un [[RemoteAccess|accès à distance]] permanent. Il peut également installer des [[Tool|outils]] de [[PacketSniffing|capture de paquets]] pour préparer l'étape de [[LateralMovement|mouvement latéral]].

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   [[PatchManagement|Gestion des patchs]] rigoureuse pour éliminer les [[SoftwareVulnerability|vulnérabilités logicielles]].
    *   [[PrincipleOfLeastPrivilege|Principe du moindre privilège]] appliqué aux [[User|utilisateurs]] et [[Process|processus]].
    *   [[ApplicationWhitelisting|Liste blanche d'applications]] pour restreindre l'exécution de programmes non autorisés.
    *   [[EndpointProtectionPlatform|Plateformes de protection des endpoints (EPP)]] et [[Antivirus|logiciels antivirus]] mis à jour.
*   **Détection** :
    *   [[EndpointDetectionAndResponse|Solutions EDR]] pour détecter les activités suspectes post-compromission.
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|IPS]] pour surveiller le [[Network|réseau]] et bloquer les téléchargements de [[Payload|charges utiles]] malveillantes.
    *   [[SecurityInformationAndEventManagement|SIEM]] pour l'agrégation et l'analyse des [[Log|logs]] et [[Event|événements]].
*   **Réponse** :
    *   [[IncidentResponse|Plans de réponse à incident]] clairs pour contenir et éradiquer rapidement les [[Threat|menaces]].
    *   [[BackupAndRecovery|Sauvegardes et récupération]] des [[Data|données]] pour restaurer les [[System|systèmes]] affectés.

## 🔗 Notes Connexes
*   [[CyberKillChain|Cyber Kill Chain]]
*   [[InitialAccess|Accès Initial]]
*   [[Persistence|Persistance]]
*   [[Execution|Exécution]]
*   [[LateralMovement|Mouvement Latéral]]
*   [[TacticsTechniquesAndProcedures|Tactiques, Techniques et Procédures (TTPs)]]
*   [[Malware|Logiciel Malveillant]]
*   [[Backdoor|Porte Dérobée]]
*   [[Rootkit|Rootkit]]
*   [[SupplyChainAttack|Attaque sur la chaîne d'approvisionnement]]
---