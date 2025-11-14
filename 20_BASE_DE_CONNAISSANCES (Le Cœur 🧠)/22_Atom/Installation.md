---
tags:
  - cybersécurité/chaine-attaque/phase-installation
  - liste-blanche-applications
  - securite/point-terminaison/detection-reponse
  - cybersécurité/chaine-attaque
  - logiciel-malveillant
  - logiciel-malveillant/persistance
aliases:
  - Phase d'Installation
  - Installation Phase
source:
  - null
cssclasses:
  - max
---

# Phase d'Installation (Cyberattaque)

## 📥 Définition en une phrase
> La phase d'installation est l'étape d'une [[CyberKillChain|cyberattaque]] où l'attaquant établit une présence durable ou déploie des composants malveillants sur le système cible après un [[InitialAccess|accès initial]] réussi.

## 🧠 Concepts Clés / Fonctionnement
*   **Déploiement de [[Malware|Logiciels Malveillants]]**: L'attaquant installe des logiciels nuisibles tels que des [[Ransomware|rançongiciels]], des [[Virus|virus]], des [[Worm|vers]] ou des [[Trojan|chevaux de Troie]] sur le système compromis.
*   **Mise en place de [[Backdoor|Portes Dérobées]] et [[Rootkit|Rootkits]]**: Création de points d'accès cachés ou d'outils pour masquer la présence de l'attaquant et maintenir l'accès futur, souvent avec des [[PrivilegeEscalation|privilèges élevés]].
*   **Modification du système**: Altération de la configuration du système, des registres, des services ou des fichiers de démarrage pour assurer la [[Persistence|persistance]] des artefacts malveillants même après un redémarrage.
*   **Staging de Outils**: Téléchargement et préparation d'outils supplémentaires nécessaires pour les phases ultérieures de l'attaque, comme l'[[LateralMovement|Mouvement Latéral]] ou l'[[DataExfiltration|Exfiltration de Données]].

## 🛡️ Risques / Menaces Associés
*   [[Malware|Logiciels Malveillants]]
*   [[AdvancedPersistentThreat|Menaces Persistantes Avancées (APT)]]
*   [[ZeroDay|Vulnérabilités Zero-Day]] exploitées pour l'installation
*   [[SupplyChainAttack|Attaques sur la Chaîne d'Approvisionnement]] introduisant des malwares lors de l'installation légitime

## 💎 Mesures de Protection / Bonnes Pratiques
*   **[[EndpointDetectionAndResponse|EDR]] et [[Antivirus|Antivirus]]**: Détection et prévention des malwares sur les points de terminaison.
*   **[[PatchManagement|Gestion des Patchs]]**: Application régulière des mises à jour de sécurité pour corriger les [[SoftwareVulnerability|vulnérabilités logicielles]].
*   **[[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]**: Limiter les droits d'installation et d'exécution aux seuls utilisateurs et processus nécessaires.
*   **[[ApplicationWhitelisting|Liste Blanche d'Applications]]**: Autoriser uniquement l'exécution de programmes approuvés.
*   **[[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|IPS]]**: Surveillance du trafic réseau pour détecter les tentatives d'installation ou de déploiement de charges utiles malveillantes.

## 🔗 Notes Connexes
*   [[CyberKillChain|Cyber Kill Chain]]
*   [[TacticsTechniquesAndProcedures|Tactiques, Techniques et Procédures (TTPs)]]
*   [[InitialAccess|Accès Initial]]
*   [[Persistence|Persistance]]
*   [[Execution|Exécution]]