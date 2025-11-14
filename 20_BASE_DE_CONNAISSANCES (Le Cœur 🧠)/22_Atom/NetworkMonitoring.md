---
tags:
  - monitorage-reseau
  - analyse-trafic
  - detection-menaces
  - NetworkSegmentation
  - SecurityInformationAndEventManagement
  - IntrusionDetectionSystem
aliases:
  - Surveillance réseau
  - Supervision réseau
source:
  - null
cssclasses:
  - max
---

# Surveillance Réseau (Network Monitoring)

## 📥 Définition en une phrase
> Le [[NetworkMonitoring|monitorage réseau]] est le processus de collecte et d'analyse continue de [[Data|données]] sur l'état, les performances et le [[TrafficManagement|trafic]] d'un [[Network|réseau]] pour détecter les anomalies et les [[Threat|menaces]].

## 🧠 Concepts Clés / Fonctionnement
*   **Collecte de [[Data|Données]]**: Implique la capture de paquets, la collecte de [[Log|journaux]] d'[[NetworkDevice|équipements réseau]] et la surveillance des métriques de performance comme la [[Bandwidth|bande passante]], la [[Latency|latence]] et le [[Throughput|débit]].
*   **Analyse et Alerte**: Les [[Data|données]] collectées sont analysées en temps réel ou de manière historique pour identifier les schémas inhabituels, les goulots d'étranglement ou les signes d'[[Attack|attaques]]. Des alertes sont générées en cas de détection d'anomalies.
*   **Outils Spécialisés**: Utilise souvent des [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]], des [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]] et des [[SecurityInformationAndEventManagement|plateformes SIEM]] pour la corrélation des événements et la gestion centralisée.
*   **Visibilité et Optimisation**: Offre une visibilité complète sur le fonctionnement du [[Network|réseau]], permettant d'optimiser les performances, de planifier les capacités et de maintenir une [[HighAvailability|haute disponibilité]].

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaques par Déni de Service (DoS)]] ou [[DistributedDenialOfService|DDoS]] détectées par des pics de [[TrafficManagement|trafic]] anormaux.
*   [[DataExfiltration|Exfiltration de données]] via la détection de transferts de [[Data|données]] inhabituels vers l'extérieur.
*   [[UnauthorizedAccess|Accès non autorisé]] ou [[SystemCompromise|compromissions de système]] révélés par des activités de connexion ou des communications suspectes.
*   Propagation de [[Malware|logiciels malveillants]] ou de [[Worm|vers]] identifiée par des communications internes anormales ou des scans de ports.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre une [[SecurityMonitoring|surveillance de sécurité]] continue pour détecter et réagir rapidement aux [[Threat|menaces]].
*   Intégrer le [[NetworkMonitoring|monitorage réseau]] dans le processus de [[IncidentResponse|réponse aux incidents]] pour une résolution plus efficace.
*   Utiliser la [[NetworkSegmentation|segmentation réseau]] conjointement avec le [[NetworkMonitoring|monitorage]] pour isoler et contenir les problèmes.
*   Mettre en place des seuils d'alerte basés sur des bases de référence normales pour minimiser les faux positifs et prioriser les incidents.
*   Effectuer des [[SecurityAudit|audits de sécurité]] réguliers des configurations de [[NetworkMonitoring|monitorage]] et des [[Log|journaux]] collectés.

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[SecurityInformationAndEventManagement|Security Information and Event Management (SIEM)]]
*   [[IntrusionDetectionSystem|Intrusion Detection System (IDS)]]
*   [[IntrusionPreventionSystem|Intrusion Prevention System (IPS)]]
*   [[NetworkTrafficAnalysis|Analyse du Trafic Réseau]]
*   [[ThreatIntelligence|Renseignement sur les menaces]]
*   [[QualityOfService|Qualité de service (QoS)]]