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

Le cadre MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) est une base de connaissances accessible au public qui recense les tactiques et les techniques des cyberattaquants. Son objectif principal est de documenter les attaques du monde réel et les comportements des acteurs de menaces sur différentes plateformes (entreprise, mobile, et ICS - systèmes de contrôle industriels). Il s'applique aux équipes de Red Team pour simuler des attaques, aux équipes de Blue Team pour améliorer la surveillance de sécurité et la réponse aux incidents, et aux analystes pour le renseignement sur les menaces.

## 🧩 Composants Clés et Structure

Le cadre `MITRE ATT&CK` est structuré autour de plusieurs concepts fondamentaux :

- **Tactiques (Tactics)**: Elles représentent les objectifs techniques de haut niveau d'un acteur de menace. Ce sont les "pourquoi" derrière une attaque (ex: Reconnaissance, Persistance, Escalade de Privilèges, Exfiltration de données).
- **Techniques (Techniques)**: Elles décrivent les moyens par lesquels les acteurs de menaces atteignent leurs objectifs tactiques. Ce sont les "comment" (ex: Bourrage d'identifiants pour l'accès initial, Exécution de Code à Distance pour l'exécution).
- **Procédures (Procedures)**: Elles détaillent les implémentations spécifiques des techniques utilisées par les acteurs de menaces, souvent dans le contexte d'une campagne d'attaque ou d'un groupe spécifique. Ce sont les "ce que" spécifiques (ex: l'utilisation d'un outil précis ou d'une commande particulière).
- **Sous-techniques (Sub-Techniques)**: Des raffinements des techniques pour une granularité accrue, décrivant des méthodes plus spécifiques.

## 📈 Bénéfices de l'Utilisation

L'adoption du cadre `MITRE ATT&CK` offre plusieurs avantages significatifs :

- **Amélioration de la Posture de Sécurité Réseau**: Permet d'identifier les lacunes dans la surveillance et les contrôles de sécurité.
- **Partage de Renseignement sur les menaces**: Facilite une compréhension et une communication communes des comportements des attaquants entre les équipes de cybersécurité.
- **Priorisation des Défenses**: Aide à concentrer les efforts de sécurité sur les techniques les plus pertinentes pour une organisation donnée.
- **Simulation d'Attaques (Red Teaming)**: Fournit une base pour créer des scénarios d'attaque réalistes, permettant aux équipes de Red Team de tester la résilience des défenses.
- **Maturité des Opérations de Sécurité**: Soutient le développement de playbooks de réponse aux incidents basés sur des comportements réels d'attaquants.

## 🛠️ Utilisation Pratique

Le cadre `MITRE ATT&CK` est utilisé de diverses manières dans la cybersécurité :

- **Analyse de Menaces**: Les analystes de renseignement sur les menacesmappent les comportements observés aux tactiques et techniques`ATT&CK` pour mieux comprendre les intentions des adversaires.
- **Évaluation des Capacités de Défense**: Les équipes Blue Team utilisent le cadre pour évaluer leur capacité à détecter et à répondre à des techniques spécifiques.
- **Développement de Détections**: Le cadre guide la création de règles de détection et de signatures pour les SIEM et les EDR.
- **Formation et Sensibilisation**: Sert de référence pour éduquer le personnel sur les comportements des attaquants et sur les vecteurs d'attaque courants.

## 🔗 Notes Connexes

- **Concept parent**: Renseignement sur les menaces
- **Acteur impliqué**: Acteur de menace
- **Équipe offensive**: Red Team
- **Équipe défensive**: Blue Team
- **Domaine d'application**: Surveillance de sécurité
