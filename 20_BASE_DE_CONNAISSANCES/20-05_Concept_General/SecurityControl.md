---
tags:
  - securite/prevention
  - securite/detection
  - gestion/risques
  - securite/mesure
  - cia
aliases:
  - Contrôle de Sécurité
  - Mesure de Sécurité
  - Security Control
archetype: concept-general
source:
cssclasses:
  - max
---

# Contrôle de Sécurité

## 📥 Définition en une phrase
> Un [[SecurityControl|contrôle de sécurité]] est une mesure technique, physique ou administrative mise en œuvre pour prévenir, détecter ou corriger les failles de [[Security|sécurité]] et ainsi réduire les [[RiskManagement|risques]] pour les [[Resource|actifs informationnels]].

## 🧠 Concepts Clés / Piliers
*   **Objectifs de Sécurité**: Les [[SecurityControl|contrôles de sécurité]] visent principalement à préserver la [[Confidentiality|Confidentialité]], l'[[Integrity|Intégrité]] et la [[Availability|Disponibilité]] (les piliers de la [[CIATriad|Triade CIA]]) des [[System|systèmes]] et des [[Data|données]].
*   **Typologie Fonctionnelle**:
    *   [[PreventiveControl|Contrôles Préventifs]]: Conçus pour empêcher les [[Attack|attaques]] ou les [[Vulnerability|vulnérabilités]] d'être exploitées (ex: [[Firewall|pare-feu]], [[Encryption|chiffrement]], [[AccessControl|politiques d'accès]]).
    *   [[DetectiveControl|Contrôles Détectifs]]: Mis en place pour identifier les [[IncidentResponse|incidents de sécurité]] lorsqu'ils se produisent (ex: [[IntrusionDetectionSystem|systèmes de détection d'intrusion]] (IDS), [[Log|logs]] d'[[SecurityAudit|audit]], [[SecurityMonitoring|surveillance]]).
    *   [[CorrectiveControl|Contrôles Correctifs]]: Permettent de restaurer les [[System|systèmes]] à un état normal après un [[IncidentResponse|incident]] et de minimiser les [[FinancialLoss|dommages]] (ex: [[Backup|sauvegardes]], [[DisasterRecoveryPlanning|plans de reprise après sinistre]], [[PatchManagement|mises à jour]]).
*   **Catégories d'Implémentation**:
    *   **Techniques**: Intégrés dans le [[Hardware|matériel]] ou le [[Software|logiciel]] (ex: [[Antivirus|logiciels antivirus]], [[Firewall|pare-feu]], [[MultiFactorAuthentication|MFA]]).
    *   **Administratives**: Basées sur des [[SecurityPolicy|politiques]], des [[Process|procédures]] et la [[20_BASE_DE_CONNAISSANCES/20-05_Concept_General/UserAwarenessTraining|formation]] du [[User|personnel]] (ex: [[StrongPasswordPolicy|politique de mots de passe forts]], [[SecurityAwareness|sensibilisation à la sécurité]]).
    *   **Physiques**: Mesures de [[PhysicalSecurity|sécurité physique]] pour protéger les [[Resource|actifs]] et les [[Computer|équipements]] (ex: serrures, [[Biometric|biométrie]], caméras de surveillance).

## 💡 Importance en Cybersécurité
> Les [[SecurityControl|contrôles de sécurité]] sont la pierre angulaire de toute stratégie de [[Cybersecurity|cybersécurité]] efficace. Ils fournissent les mécanismes nécessaires pour gérer les [[RiskManagement|risques]], protéger les [[Data|données]] et les [[System|systèmes]] contre les [[Threat|menaces]], et garantir la [[BusinessContinuity|continuité des activités]]. Sans des contrôles appropriés, les [[Enterprise|organisations]] seraient constamment vulnérables aux [[DigitalAttack|attaques numériques]], aux [[DataBreach|fuites de données]] et aux [[ServiceDisruption|interruptions de service]].

## 🔗 Notes Connexes
* [[RiskManagement|Gestion des Risques]]
* [[SecurityPolicy|Politique de sécurité]]
* [[Vulnerability|Vulnérabilité]]
* [[Threat|Menace]]
* [[CIATriad|Triade CIA]]
* [[DefenseInDepth|Défense en Profondeur]]
* [[IncidentResponse|Réponse aux incidents]]
* [[SecurityGoals|Objectifs de Sécurité]]
* [[AccessControl|Contrôle d'Accès]]
* [[PreventiveControl|Contrôle Préventif]]
* [[DetectiveControl|Contrôle Détectif]]
* [[CorrectiveControl|Contrôle Correctif]]