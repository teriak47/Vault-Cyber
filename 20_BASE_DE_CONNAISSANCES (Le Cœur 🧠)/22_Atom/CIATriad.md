---
tags:
  - securite/objectifs-fondamentaux
  - protection/mesures-securite
  - donnees/exactitude-fiabilite
  - securite/triade-cia
  - securite-information
  - confidentialité
aliases:
  - Triade CIA
  - Confidentiality, Integrity, Availability
  - Triade C-I-A
source:
  - 
cssclasses:
  - max
---

# Triade CIA

## 📥 Définition en une phrase
> La Triade CIA est un modèle fondamental de la cybersécurité qui définit les trois piliers essentiels à la protection des informations et des systèmes : la [[Confidentiality|Confidentialité]], l'[[Integrity|Intégrité]] et la [[Availability|Disponibilité]].

## 🧠 Concepts Clés / Fonctionnement
*   **[[Confidentiality|Confidentialité]]** : Assurer que les informations ne sont accessibles qu'aux entités (personnes, processus, systèmes) autorisées. Elle vise à empêcher la divulgation non autorisée de données.
    *   Exemples de menaces: [[Eavesdropping|Écoute clandestine]], [[DataBreach|Fuite de données]].
    *   Mesures: [[Encryption|Chiffrement]], [[AccessControl|Contrôle d'accès]], authentification forte.
*   **[[Integrity|Intégrité]]** : Garantir l'exactitude, la complétude et la fiabilité des informations tout au long de leur cycle de vie. Elle vise à empêcher la modification, la suppression ou l'altération non autorisée ou accidentelle des données.
    *   Exemples de menaces: [[Tampering|Altération de données]], injection de code malveillant.
    *   Mesures: [[Hashing|Fonctions de hachage]], [[DigitalSignature|Signatures numériques]], [[Checksum|Sommes de contrôle]], [[VersionControl|Contrôle de version]].
*   **[[Availability|Disponibilité]]** : Assurer que les utilisateurs autorisés ont un accès fiable et en temps opportun aux informations et aux ressources du système lorsqu'ils en ont besoin.
    *   Exemples de menaces: [[DenialOfService|Attaque par déni de service (DoS)]], [[Ransomware|Rançongiciel]], pannes matérielles.
    *   Mesures: [[Redundancy|Redondance]], [[Backup|Sauvegardes et restauration]], [[DisasterRecovery|Plans de reprise après sinistre (DRP)]], [[BusinessContinuity|Continuité des activités]].

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] (affecte la Confidentialité)
*   [[Malware|Logiciel malveillant]] (peut affecter la Confidentialité, l'Intégrité, la Disponibilité)
*   [[DenialOfService|Attaque par déni de service]] (affecte la Disponibilité)
*   [[InsiderThreat|Menace interne]] (peut affecter les trois piliers)
*   [[Ransomware|Rançongiciel]] (affecte principalement la Disponibilité et parfois la Confidentialité)

## 💎 Mesures de Protection / Bonnes Pratiques
*   [[RiskAssessment|Évaluation des risques]] pour identifier les vulnérabilités par rapport à la CIA.
*   Implémentation de [[SecurityControl|Contrôles de sécurité]] techniques et organisationnels.
*   [[SecurityPolicy|Définition et application de politiques de sécurité]] robustes.
*   [[IncidentResponse|Plans de réponse aux incidents]] pour minimiser l'impact en cas de compromission d'un des piliers.
*   [[SecurityAwarenessTraining|Sensibilisation à la sécurité]] du personnel.

## 🔗 Notes Connexes
*   [[SecurityGoals|Objectifs de sécurité]]
*   [[RiskManagement|Gestion des risques]]
*   [[InformationSecurity|Sécurité de l'information]]
*   [[DefenseInDepth|Défense en profondeur]]