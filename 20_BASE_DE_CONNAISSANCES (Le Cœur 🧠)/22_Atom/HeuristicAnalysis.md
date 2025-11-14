---
tags:
  - bac-a-sable
  - malware/polymorphe
  - faux-positifs
  - cybersécurité/analyse-heuristique
  - analyse/comportementale
  - vulnerabilite/zero-day
aliases:
  - Analyse Heuristique
  - Heuristic Analysis
source:
  - null
cssclasses:
  - max
---

# Analyse Heuristique

## 📥 Définition en une phrase
> L'analyse heuristique est une méthode de détection des menaces informatiques qui identifie les comportements suspects ou les schémas d'activité anormaux, plutôt que de se fier uniquement à des signatures connues de menaces.

## 🧠 Concepts Clés / Fonctionnement
*   **Détection Comportementale** : Au lieu de chercher une correspondance exacte avec une [[MalwareSignature|signature]] de malware connue, l'heuristique analyse le comportement d'un programme, d'un fichier ou d'un flux réseau pour identifier des actions potentiellement malveillantes.
*   **Règles et Algorithmes** : Utilise un ensemble de règles prédéfinies, d'algorithmes et parfois d'[[MachineLearning|apprentissage automatique]] pour évaluer les actions et déterminer si elles correspondent à des activités connues pour être dangereuses.
*   **Capacité de Détection de Menaces Inconnues** : Permet de détecter de nouvelles variantes de logiciels malveillants ou des attaques de type [[ZeroDay|zero-day]] pour lesquelles aucune signature n'existe encore.
*   **Analyse Statique et Dynamique** : Peut analyser le code d'un programme sans l'exécuter (statique) ou observer son comportement pendant son exécution dans un environnement contrôlé comme un [[Sandbox|bac à sable]] (dynamique).
*   **Potentiel de Faux Positifs** : En raison de sa nature basée sur l'inférence, l'analyse heuristique peut générer plus de [[FalsePositive|faux positifs]] que la détection basée sur les signatures, signalant des comportements légitimes comme suspects.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Logiciels Malveillants]] (y compris polymorphes et métamorphes)
*   [[Ransomware|Ransomwares]]
*   [[AdvancedPersistentThreat|Menaces Persistantes Avancées (APT)]]
*   [[ZeroDay|Attaques Zero-Day]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[AntivirusSoftware|Logiciels Antivirus]] (incorporant des moteurs heuristiques)
*   [[EndpointDetectionAndResponse|EDR]] (solutions de détection et réponse aux points de terminaison)
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] / [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]]
*   [[SecurityInformationAndEventManagement|SIEM]] (pour la corrélation des événements et la détection d'anomalies)

## 🔗 Notes Connexes
*   [[SignatureBasedDetection|Détection Basée sur les Signatures]]
*   [[BehavioralAnalysis|Analyse Comportementale]]
*   [[ThreatIntelligence|Renseignement sur les Menaces]]