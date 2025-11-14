---
tags:
  - siem
  - détection-anomalies
  - réponse-incident
  - IntrusionDetectionSystem
  - IntrusionPreventionSystem
  - gestion-d-incidents
aliases:
  - Surveillance de sécurité
  - Monitorage de sécurité
  - Security Monitoring
source:
  - null
cssclasses:
  - max
---

# Surveillance de Sécurité

## 📥 Définition en une phrase
> La surveillance de sécurité est le processus continu de collecte, d'analyse et d'évaluation des informations de sécurité provenant de diverses sources afin de détecter les [[Threat|menaces]], les [[SoftwareVulnerability|vulnérabilités]] et les incidents de [[Security|sécurité]] potentiels.

## 🧠 Concepts Clés / Fonctionnement
*   **Collecte de données**: Implique la collecte de [[Log|journaux]], d'événements système, de données de trafic [[Network|réseau]] et d'autres informations pertinentes provenant des [[EndDevices|terminaux]], des [[Server|serveurs]], des [[NetworkSwitch|commutateurs]], des [[Router|routeurs]] et des [[Firewall|pare-feu]].
*   **Analyse en temps réel**: Utilise des outils comme les [[SecurityInformationAndEventManagement|SIEM]] (Security Information and Event Management) pour corréler les événements, identifier les schémas anormaux et générer des alertes.
*   **Détection d'anomalies**: Recherche les activités suspectes qui pourraient indiquer une [[Attack|attaque]] en cours, une [[Exploitation|exploitation]] de [[SoftwareVulnerability|vulnérabilités]] ou une [[DataBreach|violation de données]].
*   **Réactivité**: Permet une [[IncidentResponse|réponse aux incidents]] rapide en cas de détection d'une [[Threat|menace]] confirmée, minimisant ainsi les dommages potentiels.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuites de données]] et [[DataTheft|vol de données]] non détectés.
*   [[ServiceDisruption|Interruptions de service]] prolongées dues à des [[Attack|attaques]] non identifiées.
*   [[PrivilegeEscalation|Escalade de privilèges]] par des acteurs malveillants internes ou externes.
*   [[Exploitation|Exploitation]] de [[SoftwareVulnerability|vulnérabilités]] avant leur correction.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Implémenter un système [[SecurityInformationAndEventManagement|SIEM]] pour la centralisation et l'analyse des [[Log|journaux]].
*   Déployer des [[IntrusionDetectionSystem|IDS]] (Intrusion Detection Systems) et des [[IntrusionPreventionSystem|IPS]] (Intrusion Prevention Systems) pour détecter et bloquer les activités malveillantes.
*   Mettre en place des [[SecurityAudit|audits de sécurité]] réguliers et des tests d'intrusion.
*   Développer et maintenir un [[IncidentResponse|plan de réponse aux incidents]] robuste et testé.
*   Assurer une [[SecurityAwareness|sensibilisation à la sécurité]] continue du personnel.

## 🔗 Notes Connexes
*   [[SecurityInformationAndEventManagement|Gestion des informations et des événements de sécurité (SIEM)]]
*   [[IntrusionDetectionSystem|Système de détection d'intrusion (IDS)]]
*   [[IntrusionPreventionSystem|Système de prévention d'intrusion (IPS)]]
*   [[IncidentResponse|Réponse aux incidents]]
*   [[NetworkSecurity|Sécurité Réseau]]