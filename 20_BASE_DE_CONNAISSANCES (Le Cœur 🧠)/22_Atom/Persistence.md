---
tags:
  - accès/web-shell
  - méthode-persistance/tâches-planifiées
  - gestion-d-incidents/eradication
  - logiciel-malveillant/persistance
  - cybersécurité/post-exploitation
  - menaces/persistantes-avancees
aliases:
  - Persistence
  - Persistance
  - Maintain Access
source:
  - null
cssclasses:
  - max
---

# Persistence (Persistance)

## 📥 Définition en une phrase
> La persistance est une technique utilisée par les acteurs de la menace pour maintenir leur accès à un système ou un réseau compromis, même après un redémarrage, une déconnexion ou la correction d'une vulnérabilité initiale.

## 🧠 Concepts Clés / Fonctionnement
*   **Objectif Principal**: Assurer un accès continu, durable et souvent furtif au système cible, permettant à l'attaquant de conserver le contrôle pour de futures opérations.
*   **Méthodes Courantes**:
    *   **Modifications du Registre (Windows)**: Altération des clés `Run`, `RunOnce`, ou création/modification de services système pour exécuter des payloads au démarrage.
    *   **Tâches Planifiées (Scheduled Tasks)**: Création de nouvelles tâches ou modification de celles existantes pour exécuter des scripts ou des exécutables à intervalles réguliers ou lors d'événements spécifiques.
    *   **Services Système**: Installation de nouveaux services système ou modification de services existants pour lancer des programmes malveillants avec des privilèges élevés.
    *   **Web Shells**: Déploiement de scripts malveillants sur des serveurs web compromis pour permettre un accès distant via un navigateur.
    *   **Comptes Utilisateurs et Backdoors**: Création de nouveaux comptes utilisateurs avec des privilèges élevés ou installation de [[Backdoor|portes dérobées]] dédiées.
    *   **Hooks et Injections**: Injection de code malveillant dans des processus légitimes ou modification de bibliothèques système pour intercepter des appels ou exécuter du code.
    *   **Fichiers de Démarrage et Scripts de Connexion**: Modification des fichiers de configuration ou des scripts exécutés au démarrage du système ou lors de la connexion d'un utilisateur.
    *   [[Rootkit|Rootkits]]: Logiciels conçus pour masquer la présence de l'attaquant et d'autres logiciels malveillants sur le système.

## 🛡️ Risques / Menaces Associés
*   [[AdvancedPersistentThreat|APT]] (Menaces Persistantes Avancées)
*   [[LateralMovement|Mouvement Latéral]]
*   [[DataExfiltration|Exfiltration de Données]]
*   [[PrivilegeEscalation|Élévation de Privilèges]]
*   [[Ransomware|Ransomware]] (déploiement post-compromission)
*   [[Spyware|Logiciel Espion]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Surveillance et Détection**: Utilisation de solutions [[EndpointDetectionAndResponse|EDR]] et [[SecurityInformationAndEventManagement|SIEM]] pour détecter les activités suspectes (modifications du registre, création de services, exécutions de tâches planifiées inhabituelles).
*   **Gestion des Accès**: Application du [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]] pour limiter les capacités des comptes compromis.
*   **Audits et Contrôles**: Réalisation d'audits réguliers des systèmes pour identifier les modifications non autorisées (fichiers, registre, services, tâches).
*   **Authentification Robuste**: Implémentation de l'[[MultiFactorAuthentication|MFA]] et de politiques de mots de passe complexes.
*   **Hygiène Cybernétique**: Maintien à jour des systèmes et applications ([[PatchManagement|gestion des correctifs]]) et [[VulnerabilityManagement|gestion des vulnérabilités]] pour réduire les vecteurs d'accès initiaux.
*   **Réponse aux Incidents**: Établir des procédures claires de [[IncidentResponse|réponse aux incidents]] incluant l'éradication des mécanismes de persistance.
*   [[ThreatHunting|Threat Hunting]]: Recherche proactive de signes de compromission et de persistance sur le réseau.

## 🔗 Notes Connexes
*   [[InitialAccess|Accès Initial]]
*   [[PostExploitation|Post-Exploitation]]
*   [[CommandAndControl|C2 (Command and Control)]]
*   [[MitreAttck|MITRE ATT&CK]]
*   [[DigitalForensicsAndIncidentResponse|DFIR (Forensique Numérique et Réponse aux Incidents)]]