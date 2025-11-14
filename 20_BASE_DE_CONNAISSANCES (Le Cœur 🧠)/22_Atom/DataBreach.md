---
tags:
  - cybersécurité/escalade-privileges
  - securite/prevention-perte-donnees
  - impact/atteinte-reputation
  - vol-donnees/exfiltration
  - protection-des-données
  - rgpd
aliases:
  - Fuite de données
  - Violation de données
  - Data Breach
source:
  - null
cssclasses:
  - max
---

# Fuite de Données (Data Breach)

## 📥 Définition en une phrase
> Une fuite de données est un incident de sécurité où des [[SensitiveData|informations sensibles]], protégées ou confidentielles sont accédées, divulguées, copiées, volées ou utilisées par des personnes non autorisées, ce qui entraîne souvent des conséquences graves pour les individus et les organisations.

## 🧠 Concepts Clés / Fonctionnement
*   **Origines Variées** : Peut être le résultat d'attaques externes (piratage, logiciels malveillants), d'erreurs internes (mauvaise configuration, perte de matériel), de menaces internes malveillantes ou de vulnérabilités exploitées.
*   **Type de Données Affectées** : Les données compromises peuvent inclure des informations personnelles identifiables ([[PersonallyIdentifiableInformation|PII]]), des secrets commerciaux, des données financières, des informations médicales protégées ([[ProtectedHealthInformation|PHI]]) ou des données de propriété intellectuelle.
*   **Phases de l'Attaque** : Souvent, une fuite de données est l'aboutissement de plusieurs étapes, telles que la reconnaissance, l'accès initial, l'escalade de privilèges, le mouvement latéral et l'exfiltration de données.
*   **Impacts Multiples** : Entraîne une perte de confiance des clients, des amendes réglementaires (ex: [[GeneralDataProtectionRegulation|RGPD]]), des coûts de remédiation élevés, des litiges juridiques et une atteinte à la réputation de l'organisation.

## 🛡️ Risques / Menaces Associés
*   [[SocialEngineering|Ingénierie Sociale]] (Phishing, Vishing)
*   [[Malware|Logiciels Malveillants]] (Rançongiciels, Chevaux de Troie)
*   [[VulnerabilityExploitation|Exploitation de Vulnérabilités]] (Zero-Day, configurations par défaut)
*   [[InsiderThreat|Menaces Internes]] (employés malveillants ou négligents)
*   [[WeakAuthentication|Authentification Faible]]

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[Encryption|Chiffrement]] des données au repos et en transit.
*   [[AccessControl|Contrôles d'Accès]] stricts et basés sur le moindre privilège.
*   [[MultiFactorAuthentication|Authentification Multi-Facteurs (MFA)]] pour tous les accès.
*   [[DataLossPrevention|Prévention de la Perte de Données (DLP)]] pour surveiller et bloquer les exfiltrations.
*   [[IncidentResponse|Plan de Réponse aux Incidents]] bien défini et testé régulièrement.
*   [[SecurityAwarenessTraining|Formation de Sensibilisation à la Sécurité]] pour les employés.
*   Audits de sécurité réguliers et gestion des correctifs.

## 🔗 Notes Connexes
*   [[CybersecurityIncident|Incident de Cybersécurité]]
*   [[InformationSecurity|Sécurité de l'Information]]
*   [[Privacy|Confidentialité]]
*   [[Compliance|Conformité]]
*   [[DataProtection|Protection des Données]]