---
tags:
  - logiciel
  - oracle
  - base-de-donnees
  - serveur
  - gestion/donnees
  - securite/base-de-donnees
aliases:
  - Oracle Database
  - Oracle DB
  - Oracle Corporation
archetype: logiciel
version:
cssclasses:
  - max
---

# Oracle (Base de Données)

## 🎯 Rôle et Fonction
Oracle est principalement connu pour son système de gestion de base de données relationnelle (RDBMS), Oracle Database. Il est conçu pour stocker, organiser et récupérer de grandes quantités de données de manière efficace et sécurisée, étant un pilier pour les applications d'entreprise critiques, la gestion des transactions, et l'analyse de la continuité des activités. C'est une solution robuste utilisée dans des environnements exigeants nécessitant une haute disponibilité, une évolutivité et une sécurité avancée.

## ⚙️ Configuration
L'architecture d'Oracle Database est complexe et inclut plusieurs composants clés :
*   **Instance Oracle**: Composée du System Global Area (SGA) et des processus d'arrière-plan.
*   **Fichiers de base de données**: Incluent les fichiers de données, les fichiers de contrôle et les journaux de réexécution (redo logs).
*   **Listener**: Un processus réseau qui gère les demandes de connexion entrantes des clients à l'instance Oracle.
*   **Tablespaces**: Unités logiques de stockage dans la base de données qui regroupent les segments.

## 🔒 Sécurisation (Durcissement / Hardening)
La sécurisation d'Oracle Database est cruciale et implique diverses mesures :
*   **Authentification et Autorisation robustes**: Mise en œuvre de politiques de mots de passe forts, MFA, et utilisation du principe du moindre privilège pour l'accès aux ressources.
*   **Chiffrement des données**: Utilisation de TDE (Transparent Data Encryption) pour chiffrer les données au repos et de TLS pour chiffrer les données en transit entre la base de données et les applications.
*   **Contrôle d'accès basé sur les rôles (RBAC)**: Restriction des privilèges aux utilisateurs et aux applications à un strict minimum nécessaire pour leurs fonctions.
*   **Gestion des correctifs**: Application régulière des mises à jour de sécurité et des correctifs d'Oracle pour corriger les vulnérabilités connues.
*   **Auditing**: Configuration d'une journalisation détaillée des activités des utilisateurs et des administrateurs pour la détection des menaces et la redevabilité.

## 🔍 Audit et Surveillance
La surveillance continue est essentielle pour maintenir la sécurité d'Oracle Database :
*   **Journaux d'audit (Audit Trails)**: Enregistrent les actions des utilisateurs, les connexions, et les modifications apportées à la base de données. Ils sont critiques pour la surveillance de sécurité et la réponse aux incidents.
    *   `AUDIT_TRAIL`: Paramètre de base de données configurant l'audit.
    *   `DBA_AUDIT_TRAIL` / `V$XML_AUDIT_TRAIL`: Vues pour consulter les journaux d'audit.
*   **Surveillance des performances**: Outils comme Oracle Enterprise Manager (OEM) permettent de surveiller les performances et de détecter des anomalies qui pourraient indiquer une attaque ou un compromission.
*   **Commandes SQL d'audit et de configuration**:
```sql
-- Vérifier la configuration d'audit actuelle
SHOW PARAMETER audit_trail;

-- Afficher les utilisateurs et leurs rôles
SELECT USERNAME, ACCOUNT_STATUS FROM DBA_USERS;
SELECT GRANTEE, GRANTED_ROLE FROM DBA_ROLE_PRIVS WHERE GRANTED_ROLE LIKE '%DBA%';

-- Vérifier les privilèges système accordés
SELECT GRANTEE, PRIVILEGE FROM DBA_SYS_PRIVS WHERE GRANTEE IN ('PUBLIC', 'SYS', 'SYSTEM');
```
> Ces commandes permettent de vérifier les configurations de sécurité clés, les statuts des comptes et les privilèges accordés.

## 🔗 Notes Connexes
*   **Concept de base**: Base de données
*   **Vulnérabilité typique**: Injection SQL
*   **Mesure de sécurité fondamentale**: Contrôle d'accès
*   **Pratique de durcissement**: Gestion des correctifs
*   **Gestion des risques**: Gestion des vulnérabilités