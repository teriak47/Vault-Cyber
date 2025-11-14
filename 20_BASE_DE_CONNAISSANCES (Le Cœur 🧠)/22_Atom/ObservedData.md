---
tags:
  - donnees-observées
  - analyse-securite/evenements
  - gestion-donnees/retention-archivage
  - surveillance/siem
  - cybersécurité/indicateurs-compromission
  - collecte/donnees
aliases:
  - Données Observées
  - Observed Data
source:
  - null
cssclasses:
  - max
---

# Données Observées

## 📥 Définition en une phrase
> Les données observées en cybersécurité désignent toute information collectée sur l'activité, les états et les événements au sein d'un système d'information, d'un réseau ou d'un utilisateur, essentielle pour la détection, l'analyse et la réponse aux incidents.

## 🧠 Concepts Clés / Fonctionnement
*   **Collecte Passive**: Ces données sont généralement collectées de manière non-intrusive à partir de diverses sources sans modifier l'opération normale des systèmes.
*   **Diversité des Sources**: Elles peuvent inclure des [[LogFile|fichiers de logs]] (système, application, sécurité), des flux réseau ([[NetFlow|NetFlow]], [[IPFIX|IPFIX]]), des événements de sécurité, des alertes générées par des [[SecurityTool|outils de sécurité]], et des télémétries d'endpoints.
*   **Indicateurs de Compromission (IoC)**: Les données observées sont analysées pour identifier des [[IndicatorOfCompromise|IoC]] qui signalent une activité malveillante ou une compromission.
*   **Contexte et Analyse**: Leur valeur réside dans la capacité à les corréler et les analyser pour former une vue holistique des événements, permettant de distinguer les activités normales des comportements anormaux ou malveillants.

## 🛡️ Risques / Menaces Associés
*   [[DataExfiltration|Exfiltration de Données]]: Si les systèmes de collecte sont compromis, les données observées (qui peuvent contenir des [[SensitiveData|informations sensibles]]) pourraient être exfiltrées.
*   [[DataTampering|Altération des Données]]: Un attaquant pourrait tenter de modifier ou de supprimer les données observées pour masquer ses traces.
*   [[PrivacyViolation|Violation de la Vie Privée]]: Si les données observées contiennent des [[PersonallyIdentifiableInformation|informations personnellement identifiables]] (PII) et ne sont pas correctement protégées.

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Collecte et Stockage Sécurisés**: Utiliser des systèmes comme les [[SecurityInformationAndEventManagement|SIEM]] pour collecter, agréger et stocker les données de manière sécurisée et immuable.
*   **Surveillance Continue**: Mettre en place une [[SecurityMonitoring|surveillance]] en temps réel et des alertes basées sur des règles ou des modèles comportementaux pour détecter rapidement les anomalies.
*   **Gestion des Accès**: Appliquer le principe du moindre privilège pour l'accès aux systèmes de collecte et aux données observées.
*   **Rétention et Archivage**: Définir une politique de rétention des données conforme aux exigences légales et réglementaires.

## 🔗 Notes Connexes
*   [[LogManagement|Gestion des Logs]]
*   [[ThreatIntelligence|Renseignement sur les Menaces]]
*   [[IncidentResponse|Réponse aux Incidents]]
*   [[SecurityInformationAndEventManagement|SIEM]]