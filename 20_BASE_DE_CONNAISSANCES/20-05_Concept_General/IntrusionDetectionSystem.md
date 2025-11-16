---
tags:
aliases:
  - Système de détection d'intrusion
  - IDS
  - Intrusion Detection System
  - Intrusion Detection Systems
  - Systèmes de Détection d'Intrusion
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Système de Détection d'Intrusion (IDS)

## 📥 Définition en une phrase
> Un [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]] est un dispositif ou une [[SoftwareApplication|application logicielle]] qui [[SecurityMonitoring|surveille]] un [[Network|réseau]] ou des [[System|systèmes]] à la recherche d'activités [[Malware|malveillantes]], de violations de [[SecurityPolicy|politiques]] ou de signes d'[[UnauthorizedAccess|accès non autorisé]], et alerte les [[SecurityAdministrator|administrateurs de sécurité]] en cas de [[ThreatDetection|détection]].

## 🧠 Concepts Clés / Piliers
*   **Types d'IDS**: Distinction basée sur l'emplacement de la [[SecurityMonitoring|surveillance]].
    *   [[NetworkIntrusionDetectionSystem|NIDS]] (Network-based IDS): Surveille le [[NetworkTraffic|trafic réseau]] sur un segment spécifique, analysant les [[Packet|paquets]] pour identifier les [[Attack|attaques]] par [[SignatureBasedDetection|signature]] ou [[AnomalyDetection|anomalie]].
    *   [[HostIntrusionDetectionSystem|HIDS]] (Host-based IDS): Surveille les [[Log|journaux]], les [[Process|processus du système]], les [[SystemCall|appels système]] et l'[[Integrity|intégrité des fichiers]] sur un [[Host|hôte]] individuel (serveur, poste de travail) pour détecter des activités suspectes.
*   **Méthodes de Détection**: Les approches utilisées pour identifier les menaces.
    *   [[SignatureBasedDetection|Détection par Signature]]: Compare les [[NetworkTraffic|données]] ou les [[Log|événements]] à une base de données de [[Signature|signatures]] d'[[Attack|attaques connues]] (motifs spécifiques). Efficace contre les [[Threat|menaces]] identifiées, mais inefficace contre les [[ZeroDay|nouvelles menaces]].
    *   [[AnomalyDetection|Détection par Anomalie]]: Établit une ligne de base du [[NormalBehavior|comportement normal]] et signale toute déviation significative. Permet la détection de [[ZeroDay|menaces inconnues]] mais peut générer des [[FalsePositive|faux positifs]].
*   **Mode de Fonctionnement**: La nature des actions entreprises par l'IDS.
    *   **Passif**: Un [[IntrusionDetectionSystem|IDS]] se contente d'alerter les [[SecurityAnalyst|analystes de sécurité]] et les [[SecurityTeam|équipes de sécurité]] sans bloquer activement le [[NetworkTraffic|trafic]] ou les activités suspectes.
    *   **Complémentarité**: Souvent déployé en tandem avec un [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]] qui, lui, peut bloquer ou mitiger activement les [[Attack|attaques]].

## 💡 Importance en Cybersécurité
> L'[[IntrusionDetectionSystem|IDS]] est un composant fondamental de la [[Cybersecurity|cybersécurité]] moderne, offrant une [[SecurityMonitoring|surveillance]] continue et une [[ThreatDetection|détection précoce]] des [[Threat|menaces]] sur les [[Network|réseaux]] et les [[System|systèmes]]. En alertant rapidement les [[SecurityAdministrator|administrateurs]] face à des activités suspectes, des [[UnauthorizedAccess|tentatives d'accès non autorisé]], des [[Malware|infections]] ou des [[DenialOfService|attaques par déni de service]], il joue un rôle pivot dans la [[IncidentResponse|réponse aux incidents]]. Bien que passif par nature, il est une couche essentielle de la [[DefenseInDepth|défense en profondeur]], fournissant des informations cruciales qui complètent d'autres [[SecurityControl|contrôles de sécurité]] comme les [[Firewall|pare-feu]] et les [[IntrusionPreventionSystem|IPS]]. Il aide également à identifier les [[EvasionTechniques|techniques d'évasion d'IDS]] utilisées par les [[ThreatActor|attaquants]].

## 🔗 Notes Connexes
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[Firewall|Pare-feu]]
*   [[SecurityInformationAndEventManagement|Security Information and Event Management (SIEM)]]
*   [[ThreatDetection|Détection des Menaces]]
*   [[NetworkMonitoring|Surveillance Réseau]]
*   [[SignatureBasedDetection|Détection par Signature]]
*   [[AnomalyDetection|Détection par Anomalie]]
*   [[EndpointDetectionAndResponse|Endpoint Detection and Response (EDR)]]
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]
*   [[AttackSurface|Surface d'attaque]]
*   [[NetworkIntrusionDetectionSystem|Network-based IDS (NIDS)]]
*   [[HostIntrusionDetectionSystem|Host-based IDS (HIDS)]]
*   [[EvasionTechniques|Techniques d'évasion]]