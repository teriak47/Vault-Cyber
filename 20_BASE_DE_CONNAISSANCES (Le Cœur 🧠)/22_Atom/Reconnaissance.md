---
tags:
  - cybersécurité/reconnaissance
  - reconnaissance/passive
  - reconnaissance/active
  - cybersécurité
  - ingenierie-sociale
  - audit/tests-intrusion
aliases:
  - Reconnaissance
  - Reconnaissance (Pentest)
  - Information Gathering
  - Footprinting
source:
  - null
cssclasses:
  - max
---

# Reconnaissance (Renseignement)

## 📥 Définition en une phrase
> La reconnaissance est la phase initiale d'une [[CyberAttack|cyber-attaque]] ou d'un [[Pentest|test d'intrusion]], consistant à collecter un maximum d'informations sur une cible avant de tenter toute interaction directe ou exploit.

## 🧠 Concepts Clés / Fonctionnement
*   **Collecte d'informations** : Il s'agit de recueillir des données sur le réseau, les systèmes, les applications et le personnel de la cible.
*   **Types de reconnaissance** :
    *   **Passive** : Collecte d'informations sans interaction directe avec la cible (ex: [[OpenSourceIntelligence|OSINT]], recherche WHOIS, consultation de réseaux sociaux publics).
    *   **Active** : Interaction directe avec la cible pour obtenir des informations (ex: [[PortScanning|balayage de ports]], [[VulnerabilityScanning|analyse de vulnérabilités]], ping sweeps).
*   **Informations ciblées** : Adresses IP, noms de domaine, technologies utilisées, adresses e-mail d'employés, structure organisationnelle, points d'entrée potentiels (portes, fenêtres, serveurs exposés).
*   **Objectif** : Construire une "carte" détaillée de la surface d'attaque de la cible pour identifier les vecteurs d'attaque et les [[Vulnerability|vulnérabilités]] potentiels.

## 🛡️ Risques / Menaces Associés
*   **Précurseur d'attaques** : La reconnaissance est la première étape de la plupart des [[CyberAttack|cyber-attaques]], y compris les intrusions, le [[SocialEngineering|hameçonnage]] et les attaques par déni de service.
*   **Exposition de vulnérabilités** : Les informations collectées peuvent révéler des faiblesses dans l'infrastructure ou les processus de l'organisation.
*   **Ingénierie Sociale Facilitée** : Les données sur les employés et la structure organisationnelle peuvent être utilisées pour des attaques d'[[SocialEngineering|ingénierie sociale]].

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Minimisation de l'exposition publique** : Limiter les [[SensitiveData|informations sensibles]] disponibles via [[OpenSourceIntelligence|OSINT]].
*   **Surveillance et journalisation** : Mettre en place des systèmes de [[SecurityMonitoring|surveillance de sécurité]] pour détecter les tentatives de reconnaissance active (ex: [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]]).
*   **Gestion des vulnérabilités** : Identifier et corriger proactivement les [[Vulnerability|vulnérabilités]] via des [[VulnerabilityScanning|scans réguliers]] et des [[Pentest|tests d'intrusion]].
*   **Sensibilisation du personnel** : Former les employés aux risques de l'[[SocialEngineering|ingénierie sociale]] et à la protection des informations.
*   **Politique de gestion des informations** : Contrôler les informations partagées sur les sites web, les réseaux sociaux et dans les bases de données publiques.

## 🔗 Notes Connexes
*   [[OpenSourceIntelligence|OSINT]]
*   [[Pentest|Pentesting]]
*   [[VulnerabilityScanning|Analyse de Vulnérabilités]]
*   [[SocialEngineering|Ingénierie Sociale]]
*   [[ThreatIntelligence|Renseignement sur les Menaces]]