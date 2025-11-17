---
tags:
  - norme
  - mitre-attack
  - cadre-de-reference
  - renseignement/menaces
  - analyse/menaces
  - securite/offensive
  - securite/defensive
  - methodologie/securite
  - modele
aliases:
  - MITRE ATT&CK
  - MITRE ATT&CK Framework
  - Cadre ATT&CK de MITRE
archetype: modele
source:
  - https://attack.mitre.org/
cssclasses:
  - max
---

# Cadre MITRE ATT&CK

## 🎯 Objectif et Périmètre

Le cadre [[MITREATTACKFramework|MITRE ATT&CK]] (Adversarial Tactics, Techniques, and Common Knowledge) est une base de connaissances accessible au public qui recense les tactiques et les techniques des cyberattaquants. Son objectif principal est de documenter les [[Attack|attaques]] du monde réel et les comportements des [[ThreatActor|acteurs de menaces]] sur différentes plateformes (entreprise, mobile, et ICS - systèmes de contrôle industriels). Il s'applique aux équipes de [[RedTeam|Red Team]] pour simuler des [[DigitalAttack|attaques]], aux équipes de [[BlueTeam|Blue Team]] pour améliorer la [[SecurityMonitoring|surveillance de sécurité]] et la [[IncidentResponse|réponse aux incidents]], et aux analystes pour le [[ThreatIntelligence|renseignement sur les menaces]].

## 🧩 Composants Clés et Structure

Le cadre `MITRE ATT&CK` est structuré autour de plusieurs concepts fondamentaux :

- **Tactiques (Tactics)**: Elles représentent les objectifs techniques de haut niveau d'un acteur de menace. Ce sont les "pourquoi" derrière une [[Attack|attaque]] (ex: [[Reconnaissance|Reconnaissance]], [[Persistence|Persistance]], [[PrivilegeEscalation|Escalade de Privilèges]], [[DataExfiltration|Exfiltration de données]]).
- **Techniques (Techniques)**: Elles décrivent les moyens par lesquels les acteurs de menaces atteignent leurs objectifs tactiques. Ce sont les "comment" (ex: [[CredentialStuffing|Bourrage d'identifiants]] pour l'accès initial, [[RemoteCodeExecution|Exécution de Code à Distance]] pour l'exécution).
- **Procédures (Procedures)**: Elles détaillent les implémentations spécifiques des techniques utilisées par les acteurs de menaces, souvent dans le contexte d'une [[ThreatActor|campagne d'attaque]] ou d'un groupe spécifique. Ce sont les "ce que" spécifiques (ex: l'utilisation d'un [[Tool|outil]] précis ou d'une [[Command|commande]] particulière).
- **Sous-techniques (Sub-Techniques)**: Des raffinements des techniques pour une granularité accrue, décrivant des méthodes plus spécifiques.

## 📈 Bénéfices de l'Utilisation

L'adoption du cadre `MITRE ATT&CK` offre plusieurs avantages significatifs :

- **Amélioration de la Posture de [[NetworkSecurity|Sécurité Réseau]]**: Permet d'identifier les lacunes dans la [[SecurityMonitoring|surveillance]] et les [[SecurityControl|contrôles de sécurité]].
- **Partage de [[ThreatIntelligence|Renseignement sur les menaces]]**: Facilite une compréhension et une communication communes des comportements des [[ThreatActor|attaquants]] entre les équipes de [[Cybersecurity|cybersécurité]].
- **Priorisation des Défenses**: Aide à concentrer les efforts de [[Security|sécurité]] sur les techniques les plus pertinentes pour une [[Enterprise|organisation]] donnée.
- **Simulation d'[[Attack|Attaques]] (Red Teaming)**: Fournit une base pour créer des scénarios d'attaque réalistes, permettant aux équipes de [[RedTeam|Red Team]] de tester la résilience des défenses.
- **Maturité des Opérations de [[Security|Sécurité]]**: Soutient le développement de playbooks de [[IncidentResponse|réponse aux incidents]] basés sur des comportements réels d'attaquants.

## 🛠️ Utilisation Pratique

Le cadre `MITRE ATT&CK` est utilisé de diverses manières dans la [[Cybersecurity|cybersécurité]] :

- **Analyse de [[Threat|Menaces]]**: Les analystes de [[ThreatIntelligence|renseignement sur les menaces]]mappent les comportements observés aux tactiques et techniques`ATT&CK` pour mieux comprendre les intentions des [[ThreatActor|adversaires]].
- **Évaluation des Capacités de Défense**: Les équipes [[BlueTeam|Blue Team]] utilisent le cadre pour évaluer leur capacité à détecter et à répondre à des techniques spécifiques.
- **Développement de Détections**: Le cadre guide la création de règles de détection et de signatures pour les [[SecurityInformationAndEventManagement|SIEM]] et les [[EndpointDetectionAndResponse|EDR]].
- **Formation et Sensibilisation**: Sert de référence pour éduquer le personnel sur les comportements des [[ThreatActor|attaquants]] et sur les [[AttackVector|vecteurs d'attaque]] courants.

## 🔗 Notes Connexes

- **Concept parent**: [[ThreatIntelligence|Renseignement sur les menaces]]
- **Acteur impliqué**: [[ThreatActor|Acteur de menace]]
- **Équipe offensive**: [[RedTeam|Red Team]]
- **Équipe défensive**: [[BlueTeam|Blue Team]]
- **Domaine d'application**: [[SecurityMonitoring|Surveillance de sécurité]]
