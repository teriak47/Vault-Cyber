---
tags:
  - analyse/comportementale
  - surveillance/continue
  - menaces/persistantes-avancees
  - detection-reponse
  - securite/point-terminaison
  - gestion/reponse-incident
aliases:
  - Détection et Réponse des Endpoints
  - EDR
  - Endpoint Detection and Response
source:
  - null
cssclasses:
  - max
---

# Détection et Réponse des Endpoints (EDR)

## 📥 Définition en une phrase
> L'Endpoint Detection and Response (EDR) est une solution de cybersécurité qui surveille en continu les activités des endpoints (ordinateurs, serveurs, appareils mobiles) afin de détecter et de répondre rapidement aux menaces de sécurité avancées.

## 🧠 Concepts Clés / Fonctionnement
*   **Surveillance Continue :** Collecte des données en temps réel sur l'activité des endpoints, incluant les processus, les connexions réseau, les accès aux fichiers et les modifications système.
*   **Analyse Comportementale :** Utilise des algorithmes et des règles pour analyser les données collectées, identifier les comportements anormaux ou malveillants, et détecter les attaques qui échappent aux protections traditionnelles.
*   **Détection des Menaces :** Permet d'identifier des menaces sophistiquées comme les [[FilelessMalware|logiciels malveillants sans fichier]], les [[AdvancedPersistentThreat|APT]] et les [[Ransomware|rançongiciels]].
*   **Capacités de Réponse :** Offre des outils pour contenir, isoler et éradiquer les menaces détectées, y compris la mise en quarantaine de fichiers, l'arrêt de processus et l'isolation des appareils compromis.
*   **Investigation et Forensic :** Fournit une visibilité approfondie sur la chronologie des événements d'une attaque, facilitant l'investigation et l'analyse post-incident.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Logiciels Malveillants]] (y compris zero-day)
*   [[AdvancedPersistentThreat|Menaces Persistantes Avancées (APT)]]
*   [[Ransomware|Rançongiciels]]
*   [[InsiderThreat|Menaces Internes]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   Intégrer l'EDR avec un [[SecurityInformationAndEventManagement|SIEM]] pour une vue d'ensemble de la sécurité.
*   Mettre en place une [[ThreatHunting|chasse aux menaces]] proactive en utilisant les données EDR.
*   Développer des plans de [[IncidentResponse|réponse aux incidents]] clairs basés sur les capacités de l'EDR.
*   Assurer une mise à jour régulière des agents EDR et des bases de signatures ou modèles comportementaux.

## 🔗 Notes Connexes
*   [[ExtendedDetectionAndResponse|XDR]]
*   [[ManagedDetectionAndResponse|MDR]]
*   [[Antivirus|Antivirus]]
*   [[SecurityOperationsCenter|SOC]]