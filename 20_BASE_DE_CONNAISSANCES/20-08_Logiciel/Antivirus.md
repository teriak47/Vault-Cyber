---
aliases:
  - Logiciel Antivirus
  - Anti-malware
  - Anti-virus
  - Antivirus
archetype: logiciel
version:
cssclasses:
  - max
---

# Logiciel : Antivirus

## 🎯 Rôle et Fonction
> Logiciel conçu pour détecter, prévenir et supprimer les [[Malware|logiciels malveillants]] (tels que les [[Virus]], [[Worm|vers]], et [[Trojan|chevaux de Troie]]) d'un [[System|système informatique]]. Il protège contre l'infection, la [[DataLoss|perte de données]], la [[DataCorruption|corruption de fichiers]] et la [[SystemCompromise|compromission du système]].

## ⚙️ Caractéristiques / Mécanismes
*   **[[SignatureBasedDetection|Détection basée sur les signatures]]**: Compare les fichiers et le code exécutable à une base de données de [[Signature|signatures]] connues de [[Malware|logiciels malveillants]] déjà identifiés.
*   **[[HeuristicAnalysis|Analyse heuristique]]**: Examine le comportement et la structure des programmes pour identifier des schémas suspects, permettant de détecter de nouvelles [[Threat|menaces]] ou des variantes inconnues de [[Malware|malware]].
*   **Surveillance comportementale**: Observe les activités des programmes en [[RealTimeProtection|temps réel]] pour détecter des actions typiquement malveillantes (ex: modifications non autorisées de [[SystemFile|fichiers système]], tentatives de [[PrivilegeEscalation|privilèges]]).
*   **[[RealTimeProtection|Protection en temps réel]]**: Scanne automatiquement les fichiers au fur et à mesure qu'ils sont accédés, téléchargés ou exécutés, bloquant les [[Threat|menaces]] avant qu'elles ne causent des dommages.
*   **[[Quarantine|Quarantaine]] et suppression**: Isole les fichiers malveillants détectés dans un espace sécurisé pour empêcher leur exécution, ou les supprime définitivement du [[System|système]].
*   **Mises à jour des définitions**: Télécharge régulièrement les nouvelles [[Signature|signatures]] de [[Malware|malware]] et les mises à jour du moteur d'analyse depuis les serveurs du fournisseur.

## 🔒 Mesures de Sécurité (Bonnes Pratiques)
*   **Mises à jour régulières**: Maintenir le [[Antivirus|logiciel antivirus]] et sa base de données de [[Signature|signatures]] constamment à jour pour une protection optimale contre les dernières [[Threat|menaces]].
*   **Analyses complètes et planifiées**: Configurer des analyses régulières du [[System|système]] pour détecter les [[Malware|menaces]] potentiellement passées inaperçues ou les infections latentes.
*   **Combiner avec d'autres [[SecurityControl|contrôles de sécurité]]**: Utiliser l'[[Antivirus|antivirus]] en conjonction avec un [[Firewall|pare-feu]], un [[IntrusionDetectionSystem|système de détection d'intrusion (IDS)]] et des solutions de [[EndpointProtectionPlatform|protection des endpoints (EPP)]] ou [[EndpointDetectionAndResponse|EDR]].
*   **[[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|Sensibilisation des utilisateurs]]**: Former les utilisateurs aux bonnes pratiques de [[Security|sécurité]] et à la reconnaissance des tentatives de [[Phishing|hameçonnage]] ou de téléchargements malveillants.

## 🔍 Audit et Surveillance
*   **Journaux d'événements de l'antivirus**:
    *   Les [[Log|journaux]] de l'antivirus enregistrent les détections de [[Malware|malware]], les actions effectuées (quarantaine, suppression), et les mises à jour. Ces [[Log|journaux]] sont cruciaux pour la [[SecurityMonitoring|surveillance de sécurité]] et la [[IncidentResponse|réponse aux incidents]].
*   **Commandes d'audit courantes**: (dépendent du fournisseur)
```bash
# Exemple générique pour vérifier le statut d'un service antivirus (Linux)
systemctl status <nom_service_antivirus>

# Exemple générique pour lancer une analyse (Windows - PowerShell)
# Get-MpThreat | Remove-MpThreat -Force (pour Windows Defender)
```

## 🔗 Notes Connexes
*   [[Malware|Logiciel malveillant]]
*   [[EndpointProtectionPlatform|Plateforme de Protection des Endpoints (EPP)]]
*   [[EndpointDetectionAndResponse|Endpoint Detection and Response (EDR)]]
*   [[SignatureBasedDetection|Détection Basée sur les Signatures]]
*   [[HeuristicAnalysis|Analyse Heuristique]]
*   [[CommonVulnerabilitiesAndExposures|Vulnérabilités connues (CVEs)]]