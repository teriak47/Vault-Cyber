---
tags:
aliases:
  - Base de données
  - Data Base
  - Database
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Base de Données

## 📥 Définition en une phrase
> Une [[Database|base de données]] est une collection organisée de [[Data|données]] structurées, généralement stockées et accessibles électroniquement à partir d'un [[Computer|ordinateur]].

## 🧠 Concepts Clés / Piliers
*   **Organisation des [[Data|Données]]**: Les informations sont structurées en tables, lignes et colonnes, ou selon des modèles plus flexibles comme relationnel ou [[NoSQLDatabase|NoSQL]].
*   **[[DatabaseManagementSystem|Système de Gestion de Base de Données (SGBD)]]**: Logiciel clé qui gère le stockage, la récupération, la modification et la suppression des [[Data|données]]. Il agit comme une interface entre la [[Database|base de données]] et ses utilisateurs ou [[SoftwareApplication|applications]].
*   **[[Server|Serveur]] de Base de Données**: Un [[Server|serveur]] hôte exécutant le [[DatabaseManagementSystem|SGBD]], rendant les [[Data|données]] accessibles et gérant les requêtes des [[Client|clients]].
*   **[[Integrity|Intégrité]] et [[DataConsistency|Cohérence]]**: Mécanismes et règles garantissant la validité, la fiabilité et la cohérence des [[Data|données]] stockées, souvent via des contraintes et des transactions.

## 💡 Importance en Cybersécurité
> Les [[Database|bases de données]] sont des référentiels centraux pour les [[SensitiveData|données sensibles]] (par exemple, [[PersonalData|personnelles]], financières, opérationnelles) d'une [[Enterprise|entreprise]], ce qui en fait des cibles privilégiées pour les [[ThreatActor|acteurs de menace]]. Leur [[Security|sécurité]] est donc vitale pour maintenir la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] de ces informations critiques, conformes aux exigences réglementaires telles que le [[GeneralDataProtectionRegulation|RGPD]]. Des [[Attack|attaques]] réussies comme l'[[SqlInjection|injection SQL]], le [[DataTheft|vol de données]] ou la [[DataCorruption|corruption de données]] peuvent entraîner des [[FinancialLoss|pertes financières]] considérables, des [[ReputationalDamage|dommages à la réputation]] et une [[ServiceDisruption|interruption de service]]. Des mesures robustes telles que le [[DataEncryption|chiffrement]], le [[AccessControl|contrôle d'accès]] strict, la [[VulnerabilityManagement|gestion des vulnérabilités]] et la [[BackupAndRecovery|sauvegarde]] sont indispensables pour protéger ces actifs fondamentaux.

## 🔗 Notes Connexes
*   [[Server|Serveur]]
*   [[DataEncryption|Chiffrement des Données]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[Integrity|Intégrité]]
*   [[BackupAndRecovery|Sauvegarde et Récupération]]
*   [[SqlInjection|Injection SQL]]
*   [[DataBreach|Fuite de données]]
*   [[Confidentiality|Confidentialité]]
*   [[Availability|Disponibilité]]
*   [[GeneralDataProtectionRegulation|Règlement Général sur la Protection des Données (RGPD)]]
*   [[DatabaseManagementSystem|Système de Gestion de Base de Données]]