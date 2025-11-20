---
tags:
  - attaque
  - menace/intention-nuisible
  - cyberattaque/destruction
  - cyberattaque/sabotage
  - impact/disponibilite-systeme
  - impact/integrite-donnees
aliases:
  - Vandalisme
archetype: attaque
mitre_id: T1499
source:
  - ENISA
  - MITRE ATT&CK
cssclasses:
  - max
---

# Vandalisme Numérique

> [!summary] En Bref
> Le vandalisme numérique est une [[Attack|attaque]] visant à altérer, endommager ou perturber des [[Data|données]], des [[OnlineServices|services en ligne]] ou des [[System|systèmes informatiques]], souvent dans un but malveillant ou idéologique, entraînant une [[ReputationalDamage|atteinte à la réputation]] ou une [[FinancialLoss|perte financière]].

## 🔬 Analyse Technique

### Fonctionnement
Le vandalisme numérique, ou cyber-vandalisme, consiste à modifier ou détruire intentionnellement des données ou l'apparence de [[OnlineServices|services en ligne]] sans autorisation. Cela peut inclure le défacement de sites web, la [[DataCorruption|corruption de bases de données]], ou le déploiement d'[[DistributedDenialOfService|attaques par déni de service distribué (DDoS)]] pour rendre des ressources indisponibles. Les attaquants exploitent souvent des [[SecurityVulnerabilities|vulnérabilités]] dans les applications web, les [[OperatingSystem|systèmes d'exploitation]], ou via des [[Credential|informations d'identification]] compromises pour obtenir un accès non autorisé et exécuter leurs actions destructrices.

> [!example] Scénario Concret
> 1.  **Reconnaissance** : L'attaquant identifie des [[SecurityVulnerabilities|vulnérabilités de sécurité]] sur un [[Server|serveur web]].
> 2.  **Exploitation** : Utilise une [[Exploit|faille]] (ex: [[CrossSiteScripting|XSS]]) pour obtenir un accès non autorisé.
> 3.  **Action sur Cible** : Modifie le contenu d'un site web, supprime des données de la [[Database|base de données]], ou lance une [[DenialOfService|attaque DoS]] pour rendre le service indisponible.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : [[Impact]] / [[InitialAccess]]
*   **Technique** : `T1499` - Defacement, `T1485` - [[DataCorruption|Destruction de Données]], `T1498` - [[DenialOfService|Déni de Service Réseau]]

## 🎯 Vecteurs d'Attaque
*   **[[SecurityVulnerabilities|Vulnérabilités de sécurité]] logicielles** : Exploitation de failles dans les [[OperatingSystem|systèmes d'exploitation]] ou applications web.
*   **[[Credential|Identifiants]] compromis** : Accès via des informations d'identification volées ou devinées (ex: [[BruteForceAttack|force brute]], [[PasswordSpraying|password spraying]]).
*   **[[NetworkConfiguration|Mauvaises configurations]]** : [[Server|Serveurs]] ou [[Database|bases de données]] mal configurés, laissant des portes ouvertes.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   Mises à jour régulières des [[OperatingSystem|systèmes d'exploitation]] et [[Firmware|micrologiciels]].
> *   [[InputValidation|Validation stricte des entrées]] pour prévenir les [[CrossSiteScripting|attaques XSS]] ou autres.
> *   [[RoleBasedAccessControl|Contrôles d'accès basés sur les rôles (RBAC)]] et [[LeastPrivilege|principe de moindre privilège]].
> *   [[SecurityMonitoring|Surveillance de sécurité]] continue avec [[IntrusionDetectionSystem|IDS]] / [[IntrusionPreventionSystem|IPS]].
> *   [[BackupAndRecovery|Sauvegardes]] régulières et testées pour restaurer les données.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   Surveillance des [[Log|journaux]] d'accès aux [[Server|serveurs web]], aux [[OperatingSystem|OS]] et aux [[Firewall|pare-feu]].
> *   [[AnomalyDetection|Détection d'anomalies]] dans le trafic [[Network|réseau]] ou les modifications de fichiers.
> *   Utilisation de [[SecurityInformationAndEventManagement|SIEM]] pour l'analyse et l'alerte sur les événements suspects.

### 🚒 Réponse à Incident
1.  **Isolation** : Déconnecter les systèmes affectés du [[Network|réseau]] pour empêcher la propagation.
2.  **Eradication** : Supprimer le contenu illicite, restaurer les systèmes à partir des [[Backup|sauvegardes]] saines, et corriger les [[SecurityVulnerabilities|vulnérabilités]].
3.  **Récupération** : Remettre les [[OnlineServices|services]] en ligne après vérification complète.

## 🔗 Connexions
*   **Variante** : [[DataCorruption|Corruption de données]], [[DenialOfService|Déni de Service]], [[DistributedDenialOfService|DDoS]]