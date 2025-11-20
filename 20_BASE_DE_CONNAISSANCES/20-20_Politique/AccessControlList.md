---
tags:
  - politique
  - sécurité/contrôle-accès
  - système/droits-accès
  - politique/règles-accès
aliases:
  - Liste de Contrôle d'Accès
  - ACL
archetype: politique
cssclasses:
  - max
---

# Politique : Gestion des Listes de Contrôle d'Accès (ACL)

> [!summary] Objet
> Cette politique définit les règles concernant la gestion et l'application des [[AccessControlList|Listes de Contrôle d'Accès (ACL)]] afin de limiter les accès non autorisés aux [[Resource|ressources]] et de renforcer la [[Confidentiality|confidentialité]], l'[[Integrity|intégrité]] et la [[Availability|disponibilité]] des systèmes d'information.

## 👥 Périmètre d'Application

* **Qui ?** : Tous les [[Account|comptes]] d'utilisateurs et de services, [[Administrateurs système]], [[Équipes réseau]], et personnel opérationnel.
* **Quoi ?** : Applicable à tous les [[Server|serveurs]], [[NetworkDevice|équipements réseau]] (routeurs, [[Firewall|pare-feu]]), [[FileServer|serveurs de fichiers]], et [[OperatingSystem|systèmes d'exploitation]] gérant des permissions d'accès.

## 📜 Règles & Directives

### 1. Principe du Moindre Privilège
> [!important] Règle d'Or
> L'accès aux [[Resource|ressources]] doit être limité au strict minimum nécessaire pour accomplir une [[Task|tâche]] spécifique.

* **Doit** :
    *   Accorder uniquement les permissions minimales requises pour chaque [[UserIdentity|identité utilisateur]] ou [[Process|processus]].
    *   Révoquer immédiatement les accès devenus obsolètes ou non utilisés.
    *   Réviser périodiquement les droits d'accès pour s'assurer de leur pertinence.
* **Ne doit pas** :
    *   Accorder des accès larges, génériques (ex: "tout le monde") ou permanents sans justification et revue.
    *   Laisser des droits d'accès non documentés ou non vérifiés.

### 2. Gestion et Documentation des ACL
Une gestion rigoureuse des ACL est essentielle pour maintenir la [[Security|sécurité]] du système.

* **Doit** :
    *   Documenter chaque [[AccessControlList|ACL]] avec sa finalité, ses règles, les [[UserIdentity|identités]] concernées et la date de dernière revue.
    *   Utiliser des groupes plutôt que des utilisateurs individuels pour simplifier la gestion des permissions.
    *   Revoir et valider les [[AccessControlList|ACL]] au moins annuellement, ou après tout changement majeur d'organisation ou de système.
    *   Prioriser les [[AccessControlModel|modèles de contrôle d'accès]] basés sur les rôles (par exemple, [[RoleBasedAccessControl|RBAC]]) lorsque cela est possible.
    *   Implémenter des politiques de [[ZeroTrust|Zero Trust]] où les accès sont vérifiés en continu.
* **Ne doit pas** :
    *   Modifier des [[AccessControlList|ACL]] sans une procédure de demande, d'approbation et de documentation formelle.
    *   Créer des [[AccessControlList|ACL]] complexes, redondantes ou difficiles à auditer.

## 🚨 Gestion des Exceptions
Toute dérogation à cette politique doit être :
1. Documentée avec une justification de sécurité et métier.
2. Validée par le CISO (Chief Information Security Officer) ou un responsable désigné.
3. Limitée dans le temps avec une date de réévaluation obligatoire.

## 👮 Contrôle & Sanctions
Le non-respect de cette politique peut entraîner :
* Des [[SecurityVulnerabilities|vulnérabilités de sécurité]] augmentant le risque de [[DataBreach|violation de données]] ou de [[DenialOfService|déni de service]].
* Des actions disciplinaires pouvant aller jusqu'au licenciement pour les [[HumanError|erreurs humaines]] intentionnelles ou la négligence grave.

## 🔗 Références
* **Modèles d'Accès** : [[AccessControlModel|Modèle de Contrôle d'Accès]]
* **Gestion des Identités** : [[IdentityAndAccessManagement|Gestion des Identités et des Accès (IAM)]]
* **Contrôles de Sécurité** : [[SecurityControl|Contrôle de Sécurité]]
* **Méthodes de Contrôle d'Accès** : [[RoleBasedAccessControl|Contrôle d'accès basé sur les rôles (RBAC)]]
* **Principes de Sécurité** : [[ZeroTrust|Zéro Confiance]]