---
tags:
  - detection-reponse/etendue
  - gestion/terminaux-mobiles
  - architecture/securite-distribuee
  - securite/point-terminaison
  - securite/point-terminaison/detection-reponse
  - securite/gestion-correctifs
aliases:
  - Sécurité des points d'accès
  - Sécurité des terminaux
  - Endpoint Security
source:
  - null
cssclasses:
  - max
---

# Sécurité des Points d'Accès

## 📥 Définition en une phrase
> La sécurité des points d'accès est une approche de cybersécurité visant à protéger les appareils terminaux (ordinateurs portables, postes de travail, serveurs, smartphones, tablettes) contre les menaces sophistiquées.

## 🧠 Concepts Clés / Fonctionnement
*   **Protection Distribuée** : Se concentre sur la sécurisation des appareils individuels (les "endpoints") qui sont connectés à un réseau, plutôt qu'uniquement la périphérie du réseau.
*   **Installation Locale** : Implique l'installation de logiciels de sécurité directement sur chaque terminal pour surveiller, détecter et bloquer les activités malveillantes.
*   **Fonctionnalités Intégrées** : Les solutions modernes combinent souvent des capacités antivirus et anti-malware, un pare-feu personnel, la détection et réponse des points d'accès ([[EndpointDetectionAndResponse|EDR]]), la prévention des pertes de données ([[DataLossPrevention|DLP]]), et la gestion des vulnérabilités.
*   **Point d'Interaction** : Protège les points où les utilisateurs interagissent avec les données et le réseau, qui sont des vecteurs d'attaque courants.

## 🛡️ Risques / Menaces Associés
*   [[Malware|Malwares]] (Virus, Chevaux de Troie, Spyware)
*   [[Ransomware|Ransomwares]]
*   [[Phishing|Hameçonnage]] et attaques de spear-phishing
*   [[AdvancedPersistentThreat|Menaces Persistantes Avancées (APT)]]
*   [[ZeroDayVulnerability|Vulnérabilités Zero-Day]]
*   [[InsiderThreat|Menaces internes]] (négligence ou malveillance)

## 💎 Mesures de Protection / Bonnes Pratiques
*   **Solutions EDR/XDR** : Déployer des systèmes de [[EndpointDetectionAndResponse|Détection et Réponse des Points d'Accès (EDR)]] ou de [[ExtendedDetectionAndResponse|Détection et Réponse Étendues (XDR)]] pour une visibilité et une réponse proactives.
*   **Antivirus/Anti-malware à jour** : Maintenir des [[AntivirusSoftware|logiciels antivirus]] et anti-malware avec les dernières définitions.
*   **Gestion des Correctifs** : Appliquer régulièrement les [[PatchManagement|correctifs de sécurité]] pour toutes les applications et systèmes d'exploitation.
*   **Pare-feu Personnel** : Configurer et activer les [[Firewall|pare-feu personnels]] sur chaque terminal.
*   **Contrôle d'Accès** : Implémenter le [[LeastPrivilegePrinciple|principe du moindre privilège]] et le [[MultiFactorAuthentication|MFA]].
*   **Sensibilisation des Utilisateurs** : Former les utilisateurs aux risques de cybersécurité, notamment le phishing.

## 🔗 Notes Connexes
*   [[NetworkSecurity|Sécurité Réseau]]
*   [[ZeroTrust|Zero Trust]]
*   [[VulnerabilityManagement|Gestion des Vulnérabilités]]
*   [[SecurityOperationsCenter|Centre d'Opérations de Sécurité (SOC)]]