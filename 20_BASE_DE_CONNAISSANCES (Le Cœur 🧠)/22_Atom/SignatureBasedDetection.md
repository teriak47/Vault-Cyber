---
tags:
  - base-donnees/signatures
  - techniques-evasion
  - mise-a-jour-signatures
  - cybersécurité
  - detection/par-signature
  - systeme/detection-intrusion
aliases:
  - Détection par signature
  - Signature-Based Detection
source:
  - null
cssclasses:
  - max
---

# Détection Basée sur les Signatures

## 📥 Définition en une phrase
> Une méthode de détection des menaces qui identifie les logiciels malveillants ou les activités suspectes en recherchant des motifs (signatures) spécifiques, pré-enregistrés, dans le code ou le comportement.

## 🧠 Concepts Clés / Fonctionnement
*   **[[Signature|Signatures]] :** Des motifs uniques, des hachages de fichiers, des séquences d'octets ou des règles de comportement connus associés à des menaces spécifiques (malware, intrusions).
*   **Base de données de signatures :** Une collection constamment mise à jour de signatures de logiciels malveillants et d'intrusions connus.
*   **Correspondance :** Le système de détection compare le trafic réseau, les fichiers ou les processus système aux signatures stockées dans sa base de données.
*   Offre un faible taux de faux positifs pour les menaces déjà identifiées et est très efficace contre les attaques connues.
*   Repose sur la connaissance préalable de la menace pour pouvoir la détecter.

## 🛡️ Risques / Menaces Associés
*   [[ZeroDayExploit|Attaques Zero-Day]] : Incapacité à détecter les menaces totalement nouvelles ou non encore répertoriées dans la base de signatures.
*   [[EvasionTechnique|Techniques d'évasion]] : Les attaquants peuvent modifier légèrement le code ou le comportement de leurs malwares pour altérer leur signature et échapper à la détection.
*   [[OutdatedDatabase|Bases de données obsolètes]] : Une efficacité réduite si la base de signatures n'est pas régulièrement mise à jour avec les dernières menaces.

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[AntivirusSoftware|logiciels antivirus]] avec des mises à jour automatiques et fréquentes de leurs bases de signatures.
*   Complémentarité avec des méthodes de détection avancées comme l'[[HeuristicAnalysis|analyse heuristique]] ou l'[[BehavioralAnalysis|analyse comportementale]] pour détecter l'inconnu.
*   [[ThreatIntelligence|Veille sur les menaces]] continue pour alimenter et enrichir les bases de signatures.

## 🔗 Notes Connexes
*   [[IntrusionDetectionSystem|Système de Détection d'Intrusion (IDS)]]
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[HeuristicAnalysis|Analyse Heuristique]]
*   [[BehavioralAnalysis|Analyse Comportementale]]
*   [[AnomalyDetection|Détection d'Anomalies]]