---
tags:
  - planification/reprise-sinistre
  - infrastructure/redondance
  - systeme/resilience
  - securite/disponibilite
  - cyberattaque/deni-service
  - planification/continuite-activite
aliases:
  - Interruption de Service
  - Disruption de Service
source:
  - null
cssclasses:
  - max
---

# ServiceDisruption (Interruption de Service)

## 📥 Définition en une phrase
> Un événement qui empêche un système, un réseau ou une application de fonctionner normalement ou d'être accessible aux utilisateurs, entraînant une perte de disponibilité.

## 🧠 Concepts Clés / Fonctionnement
*   **Causes Variées** : Peut être le résultat d'attaques malveillantes (ex: [[DenialOfService|Déni de Service]]), de pannes matérielles ou logicielles, d'erreurs humaines, de catastrophes naturelles ou de problèmes d'infrastructure.
*   **Impact Principal** : La perte de [[Availability|disponibilité]] des services essentiels, ce qui peut entraîner des pertes financières, une atteinte à la réputation et des problèmes opérationnels.
*   **Objectif Attaquant** : Dans le contexte de la cybersécurité, l'interruption de service est souvent l'objectif direct ou indirect d'une attaque, visant à rendre un système inutilisable ou inopérant.
*   **Durée et Étendue** : Peut varier d'une brève interruption affectant un seul service à une panne prolongée impactant l'ensemble de l'infrastructure d'une organisation.

## 🛡️ Risques / Menaces Associés
*   [[DenialOfService|Attaque par Déni de Service (DoS/DDoS)]]
*   [[Ransomware|Rançongiciel]] (qui peut chiffrer les données et rendre les systèmes inaccessibles)
*   [[Malware|Logiciels Malveillants]]
*   [[HumanError|Erreurs Humaines]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[BusinessContinuityPlanning|Planification de la Continuité des Activités]]
*   [[DisasterRecovery|Reprise après Sinistre]]
*   [[Redundancy|Redondance]] (systèmes, serveurs, connexions réseau)
*   [[SecurityControl|Contrôles d'accès]] robustes et gestion des privilèges
*   [[IntrusionDetectionSystem|Systèmes de Détection d'Intrusion (IDS)]] et [[IntrusionPreventionSystem|Systèmes de Prévention d'Intrusion (IPS)]]
*   [[PatchManagement|Gestion des Correctifs]] régulière
*   [[BackupAndRecovery|Sauvegardes]] fréquentes et vérifiées

## 🔗 Notes Connexes
*   [[Availability|Disponibilité]]
*   [[Resilience|Résilience]]
*   [[IncidentResponse|Réponse aux Incidents]]
*   [[CyberAttack|Attaque Cybernétique]]