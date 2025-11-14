---
tags:
  - correlation-evenements
  - agregation-donnees
  - centre-operations-securite
  - surveillance/siem
  - detection-reponse
  - journalisation/audit
aliases:
  - Gestion des informations et des événements de sécurité
  - SIEM
  - Security Information and Event Management
source:
  - null
cssclasses:
  - max
---

# Gestion des Informations et des Événements de Sécurité (SIEM)

## 📥 Définition en une phrase
> Un système SIEM est une solution de sécurité qui collecte, normalise, analyse et corrèle les données d'événements de sécurité provenant de diverses sources afin de fournir une surveillance en temps réel, une détection des incidents et des rapports de conformité.

## 🧠 Concepts Clés / Fonctionnement
*   **Collection et Agrégation de Logs :** Les systèmes SIEM centralisent les journaux d'événements et les données de sécurité de nombreux systèmes hétérogènes (serveurs, pare-feu, routeurs, IDS/IPS, applications, bases de données).
*   **Normalisation et Corrélation :** Les données brutes sont transformées en un format standardisé, puis analysées pour identifier les relations entre les événements et détecter des schémas d'activité malveillante ou suspecte.
*   **Analyse et Alertes :** Grâce à des règles prédéfinies, l'analyse comportementale (UEBA) et parfois l'intelligence artificielle, le SIEM identifie les menaces potentielles et génère des alertes pour les équipes de sécurité.
*   **Tableaux de Bord et Rapports :** Il offre une visibilité globale sur la posture de sécurité et génère des rapports pour la conformité réglementaire et les audits.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] (aide à la détection précoce)
*   [[Malware|Logiciels malveillants]] (détecte leur activité et propagation)
*   [[InsiderThreat|Menaces internes]] (identifie les comportements utilisateurs anormaux)
*   [[AdvancedPersistentThreat|APT]] (permet de corréler des activités discrètes sur de longues périodes)
*   [[ComplianceViolation|Non-conformité réglementaire]] (facilite la preuve de conformité)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[ContinuousMonitoring|Surveillance continue]] des infrastructures et des applications.
*   [[ThreatDetection|Détection des menaces]] avancées et des anomalies comportementales.
*   [[IncidentResponse|Amélioration de la réponse aux incidents]] en fournissant des informations contextuelles rapides.
*   [[LogManagement|Gestion centralisée et sécurisée des journaux]] pour l'audit et la forensique.
*   Définition et ajustement régulier des règles de corrélation et des seuils d'alerte.

## 🔗 Notes Connexes
*   [[LogManagement|Gestion des journaux]]
*   [[SecurityOperationsCenter|Centre d'Opérations de Sécurité (SOC)]]
*   [[ThreatIntelligence|Renseignement sur les menaces]]
*   [[ExtendedDetectionAndResponse|XDR]]
*   [[UnifiedEndpointManagement|UEM]]