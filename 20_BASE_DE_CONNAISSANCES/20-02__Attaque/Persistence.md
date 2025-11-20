---
tags:
  - attaque
  - post-exploitation
aliases:
  - Persistence
  - Persistance
  - Maintain Access
archetype: attaque
source:
  -
cssclasses:
  - max
---

# Persistance

## 📥 Définition
> La persistance est une technique employée par un acteur de menace pour conserver un accès non autorisé à un système ou réseau compromis, même après un redémarrage, une déconnexion de l'utilisateur ou la correction de la vulnérabilité initiale. L'objectif est de maintenir le contrôle à long terme sur la cible.

## 🎯 Vecteurs d'Attaque
*   **Modification du Registre (Windows)** : Altération des clés de registre (ex: `Run`, `RunOnce`) pour exécuter un charge utile au démarrage du système.
*   **Tâches Planifiées** : Création ou modification de tâches planifiées pour exécuter des scripts ou applications malveillantes à des intervalles définis ou lors d'événements spécifiques.
*   **Manipulation des Services Système** : Installation de nouveaux services système ou modification d'existants pour lancer des logiciels malveillants avec des privilèges élevés.
*   **Web Shells** : Déploiement de scripts malveillants sur des serveurs web compromis, permettant un accès distant via un navigateur web.
*   **Création de Comptes Utilisateurs et Backdoors** : Création de nouveaux comptes utilisateurs avec des privilèges élevés ou installation de portes dérobées dédiées pour un accès furtif.
*   **Injection de Code / Hooks** : Injection de code malveillant dans des processus légitimes ou modification de bibliothèques dynamiques pour intercepter des appels et exécuter du code.
*   **Fichiers de Démarrage et Scripts de Connexion** : Modification des fichiers de configuration ou des scripts exécutés au démarrage du système ou à la connexion d'un utilisateur.
*   **Rootkits** : Logiciels conçus pour masquer la présence de l'attaquant et d'autres logiciels malveillants sur le système.

## 💥 Impacts Potentiels
*   Exfiltration de Données
*   Élévation de privilèges continue
*   Mouvement Latéral à travers le réseau
*   Déploiement ultérieur de ransomware ou spyware
*   Maintien d'une APT (Menace Persistante Avancée)

##  concret
> Après avoir réussi une attaque par phishing et obtenu un accès initial à un ordinateur d'entreprise, un attaquant déploie un RAT et configure une tâche planifiée pour que le RemoteAccessTrojan se lance à chaque démarrage du système. Même si l'utilisateur déconnecte sa session ou si la vulnérabilité initiale est patchée, l'attaquant conserve son accès via la tâche planifiée, lui permettant de continuer à surveiller le système ou à effectuer des mouvements latéraux.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   Application du Principe du Moindre Privilège.
    *   Gestion rigoureuse des correctifs et gestion des vulnérabilités.
    *   Sensibilisation des utilisateurs aux techniques d'ingénierie sociale.
*   **Détection** :
    *   Déploiement de solutions EDR pour détecter les activités suspectes (modifications du registre, création de services, exécutions de tâches planifiées inhabituelles).
    *   Utilisation de SIEM pour la corrélation des logs et la détection d'anomalies.
    *   Threat Hunting proactif pour rechercher des signes de compromission et de persistance.
*   **Réponse** :
    *   Mise en place d'un plan de réponse à incident incluant des procédures d'éradication des mécanismes de persistance.
    *   Réalisation de audits de sécurité réguliers pour identifier les modifications non autorisées.

## 🔗 Notes Connexes
*   Accès Initial
*   Post-Exploitation
*   Commande et Contrôle (C2)
*   MITRE ATT&CK
*   Forensique Numérique et Réponse aux Incidents (DFIR)
*   Acteur de menace