---
tags:
  - gestion-donnees/sauvegarde
  - exfiltration-donnees
  - securite/controle-acces
  - securite/chiffrement
  - vulnerabilite/injection-web
aliases:
  - Base de données
  - Data Base
source:
  - null
cssclasses:
  - max
---

# Base de Données

## 📥 Définition en une phrase
> Une base de données est une collection organisée de données structurées, généralement stockées et accessibles électroniquement à partir d'un [[Computer|ordinateur]].

## 🧠 Concepts Clés / Fonctionnement
*   **Organisation**: Les [[DataFrames|données]] sont structurées en tables, lignes et colonnes, ou selon d'autres modèles (relationnel, NoSQL).
*   **[[Server|Serveur]] de Base de Données**: Logiciel qui gère le stockage, la récupération, la modification et la suppression des [[DataFrames|données]].
*   **Système de Gestion de Base de Données (SGBD)**: Interface logicielle permettant aux utilisateurs et aux applications d'interagir avec la base de données.
*   **[[Integrity|Intégrité]] et Cohérence**: Les bases de données sont conçues pour maintenir l'[[Integrity|intégrité]] et la cohérence des [[DataFrames|données]] grâce à des contraintes et des transactions.

## 🛡️ Risques / Menaces Associés
*   [[DataBreach|Fuite de données]] et [[DataTheft|vol de données]] par accès non autorisé.
*   [[DataCorruption|Corruption de données]] due à des erreurs logicielles, matérielles ou des attaques malveillantes.
*   [[DenialOfService|Déni de service]] (DoS) ou [[DistributedDenialOfService|DDoS]] affectant la [[Availability|disponibilité]].
*   [[SqlInjection|Injection SQL]] et autres [[Exploitation|exploits]] permettant l'exécution de commandes non autorisées.
*   Vulnérabilités dans le SGBD ou les applications qui y accèdent.

## 💎 Mesures de Protection / Bonnes Pratiques
*   Mettre en œuvre un [[AccessControl|contrôle d'accès]] strict basé sur les rôles (par exemple, [[RoleBasedAccessControl|RBAC]]).
*   Effectuer des [[BackupAndRecovery|sauvegardes et récupérations]] régulières des [[DataFrames|données]].
*   Utiliser le [[DataEncryption|chiffrement des données]] au repos et en transit.
*   Appliquer des correctifs de [[Security|sécurité]] (patch management) pour les SGBD et les systèmes d'exploitation.
*   Protéger contre les [[SqlInjection|injections SQL]] par la validation des entrées et les requêtes préparées.
*   Surveiller les activités des bases de données avec des outils [[SecurityInformationAndEventManagement|SIEM]].

## 🔗 Notes Connexes
*   [[Server|Serveur]]
*   [[DataEncryption|Chiffrement des Données]]
*   [[AccessControl|Contrôle d'Accès]]
*   [[Integrity|Intégrité]]
*   [[BackupAndRecovery|Sauvegarde et Récupération]]
*   [[SqlInjection|Injection SQL]]