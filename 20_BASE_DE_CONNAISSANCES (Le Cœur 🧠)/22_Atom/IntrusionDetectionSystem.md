---
tags:
  - detection/anomalie
  - detection-intrusion/base-hote
  - prevention/intrusion
  - systeme/detection-intrusion
  - detection/par-signature
  - gestion-d-incidents
aliases:
  - Système de détection d'intrusion
  - IDS
  - Intrusion Detection System
source:
  - null
cssclasses:
  - max
---

# Système de Détection d'Intrusion (IDS)

## 📥 Définition en une phrase
> Un Système de Détection d'Intrusion (IDS) est un dispositif ou une application logicielle qui surveille un réseau ou des systèmes à la recherche d'activités malveillantes, de violations de politiques ou de signes d'accès non autorisé, et alerte les administrateurs en cas de détection.

## 🧠 Concepts Clés / Fonctionnement
*   **Types d'IDS**:
    *   **[[NetworkIntrusionDetectionSystem|NIDS (Network-based IDS)]]**: Surveille le trafic réseau sur un segment spécifique en comparant les paquets à des signatures d'attaques connues ou à des profils de comportement normaux.
    *   **[[HostIntrusionDetectionSystem|HIDS (Host-based IDS)]]**: Surveille les fichiers journaux, les processus du système, les appels système et l'intégrité des fichiers sur un hôte individuel (serveur, poste de travail) pour détecter des activités suspectes.
*   **Méthodes de Détection**:
    *   **Détection par Signature**: Compare le trafic ou les événements à une base de données de signatures d'attaques connues (patterns spécifiques). Efficace contre les menaces connues mais inefficace contre les nouvelles menaces (zero-day).
    *   **Détection par Anomalie**: Établit une ligne de base du comportement normal et signale toute déviation significative. Permet de détecter des menaces inconnues mais peut générer plus de faux positifs.
*   **Mode de Fonctionnement**: Les IDS sont généralement passifs, se contentant d'alerter sans bloquer activement le trafic. Pour la prévention, un [[IntrusionPreventionSystem|IPS]] est utilisé.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par déni de service (DoS/DDoS)]]
*   [[Malware|Infections par logiciels malveillants]]
*   [[UnauthorizedAccess|Tentatives d'accès non autorisé]]
*   [[Exploit|Exploitation de vulnérabilités]]
*   [[EvasionTechniques|Techniques d'évasion d'IDS]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Positionnement Stratégique**: Placer les capteurs NIDS aux points critiques du réseau (périmètre, segments sensibles).
*   **Mises à Jour Régulières**: Maintenir les bases de signatures à jour pour la détection des dernières menaces.
*   **Tuning et Optimisation**: Ajuster les règles et les seuils pour réduire les faux positifs et les faux négatifs.
*   **Intégration SIEM**: Envoyer les alertes IDS à un [[SecurityInformationAndEventManagement|SIEM]] pour une corrélation et une analyse centralisées.
*   **Procédures de Réponse**: Définir des procédures claires pour la [[IncidentResponse|réponse aux incidents]] déclenchés par les alertes IDS.

## 🔗 Notes Connexes
*   [[IntrusionPreventionSystem|Système de Prévention d'Intrusion (IPS)]]
*   [[Firewall|Pare-feu]]
*   [[SecurityInformationAndEventManagement|Security Information and Event Management (SIEM)]]
*   [[ThreatDetection|Détection des Menaces]]
*   [[NetworkMonitoring|Surveillance Réseau]]