---
archetype: cour
module: "GEN (Culture Générale & Hors Cursus)"
aliases:
  - "Énumération Système et Services"
  - "System and Service Enumeration"
  - "Enumeration Systeme Services"
  - "01-11 | ÉNUMÉRATION SYSTÈME & SERVICES"
  - "ÉNUMÉRATION SYSTÈME & SERVICES"
cssclasses:
  - max
tags:
  - méthodologie
  - définition/enumeration
  - pentest/reconnaissance
  - reconnaissance
  - information/collecte
  - reseau
  - systeme-exploitation/windows
  - systeme-exploitation/linux
  - microsoft/active-directory
  - protocole/smb
  - protocole/netbios
  - protocole/snmp
  - protocole/ldap
  - protocole/dce-rpc
  - partage/fichiers
  - politique/securite
  - enumeration/groupes
  - enumeration/service
  - outil/enum4linux-ng
  - outil/smbclient
  - outil/rpcclient
  - outil/snmp-check
  - outil/ldapsearch
  - outil/whatweb
---

# 01-11 | ÉNUMÉRATION SYSTÈME & SERVICES

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Énumérer SMB/NetBIOS sur des systèmes Windows ou Linux.
> 2. Énumérer SNMP pour obtenir des informations système internes.
> 3. Interroger un serveur LDAP/Active Directory sans authentification ou avec des identifiants faibles.
> 4. Identifier les **partages**, **services**, **groupes** et **politiques** exposés par les machines cibles.
> 5. Compléter une *Fiche d'Exposition Système* pour documenter les vulnérabilités potentielles.

## 📝 Synthèse du Cours

L'**énumération système et services** est une phase cruciale dans l'évaluation de la sécurité d'un réseau. Elle consiste à collecter le maximum d'informations sur les cibles (comptes utilisateurs, partages de fichiers, versions de services, configurations d'Active Directory) sans procéder à des tentatives d'exploitation. L'objectif est d'identifier toutes les failles potentielles basées uniquement sur la collecte d'informations passives et actives mais non intrusives. Ce processus permet de comprendre précisément ce que chaque machine expose réellement, préparant ainsi les étapes d'exploitation ultérieures.

> [!note] Définition Clé
> **Énumération** : Processus de collecte d'informations détaillées sur un système ou un réseau, telles que les noms d'utilisateurs, les noms de machines, les partages réseau, les services en cours d'exécution et les configurations, sans exploitation directe.

### 1. Pré-requis et Outils Essentiels

Avant de débuter l'énumération, il est impératif d'avoir une cartographie préalable du réseau et la connaissance des adresses IP des cibles. Pour ce module, les pré-requis incluent la validation des modules 1 et 2 (exploration réseau). Les machines cibles devront avoir les services SMB, LDAP et SNMP actifs pour les exercices.

Les outils clés pour cette phase d'énumération sont :

| Outil           | Rôle                                                |
| :-------------- | :-------------------------------------------------- |
| `enum4linux-ng` | Énumération des informations SMB/NetBIOS sur Windows/Linux. |
| `smbclient`     | Accès et navigation dans les partages SMB.      |
| `rpcclient`     | Obtention d'informations Active Directory via RPC (y compris les sessions nulles). |
| `snmp-check`    | Énumération des informations système via SNMP.  |
| `ldapsearch`    | Interrogation des annuaires LDAP/Active Directory. |
| `WhatWeb`       | *Fingerprinting* avancé des services Web.           |

### 2. Énumération des Services SMB / NetBIOS

L'énumération SMB (Server Message Block) et NetBIOS vise à découvrir les comptes utilisateurs, les groupes et les partages réseau exposés par les systèmes Windows ou même certains serveurs Linux. Ces informations peuvent révéler des vulnérabilités de configuration.

#### Étape 1 — Identification des informations avec `enum4linux-ng`

`enum4linux-ng` est un script puissant pour automatiser la collecte d'informations SMB/NetBIOS.

*   **Commande Générale** : `enum4linux-ng -A 192.168.56.5`
*   **Options Utiles** :
    *   `-U` : Lister les utilisateurs.
    *   `-S` : Lister les partages réseau.
    *   `-G` : Lister les groupes.
    *   `-k` : Obtenir des informations Kerberos (spécifique à Active Directory).
*   **Sorties Attendues** : Une liste détaillée des utilisateurs locaux ou de domaine, des groupes de sécurité et des partages disponibles (ex: ADMIN$, C$, PUBLIC$).

#### Étape 2 — Accès direct aux partages avec `smbclient`

Une fois les partages identifiés, `smbclient` permet de vérifier leur accessibilité et leur contenu.

*   **Lister les Partages** : `smbclient -L //192.168.56.5/ -N` (l'option `-N` tente une connexion sans mot de passe).
*   **Se connecter à un Partage** : `smbclient //192.168.56.5/public -N`
*   **Actions dans `smbclient`** :
    *   `ls` : Lister les fichiers et répertoires.
    *   `get file.txt` : Récupérer un fichier.
    *   `recurse on` : Permet d'explorer l'arborescence des répertoires.
*   **Critère de Réussite** : Trouver un partage accessible sans nécessiter d'authentification.

### 3. Énumération RPC / Active Directory

RPC (Remote Procedure Call) et Active Directory sont des composants clés des environnements Windows. L'énumération de ces services peut révéler des informations précieuses sur la structure du domaine, les utilisateurs et les groupes, souvent même sans authentification grâce aux *sessions nulles*.

#### Étape 3 — Collecte d'informations AD avec `rpcclient`

`rpcclient` permet d'interroger les services RPC, souvent exploité pour les sessions nulles afin d'obtenir des détails sur le domaine.

*   **Connexion (session nulle)** : `rpcclient -U "" -N 192.168.56.5`
*   **Commandes utiles** dans `rpcclient` :
    *   `enumdomusers` : Énumérer les utilisateurs du domaine.
    *   `queryuser 0xRID` : Obtenir des informations spécifiques sur un utilisateur (remplacer 0xRID par l'identifiant).
    *   `enumdomgroups` : Énumérer les groupes du domaine.
    *   `lsaquery` : Afficher des informations sur la politique de sécurité locale.
    *   `lookupnames administrator` : Rechercher le SID (Security Identifier) d'un utilisateur ou d'un groupe.
*   **Critère de Réussite** : Identifier au moins deux utilisateurs du domaine Active Directory et un groupe sensible (par exemple, "Domain Admins").

### 4. Énumération SNMP

Le protocole SNMP (Simple Network Management Protocol) est utilisé pour la gestion des équipements réseau. Mal configuré, il peut exposer une multitude d'informations système sensibles, telles que la version de l'OS, les services en cours, l'uptime, les comptes utilisateurs et les interfaces réseau.

#### Étape 4 — Vérification SNMP avec `snmp-check`

`snmp-check` est l'outil standard pour interroger les agents SNMP.

*   **Commande** : `snmp-check -c public 192.168.56.10` (où `public` est la chaîne de communauté par défaut souvent utilisée et parfois non modifiée).
*   **Sorties Possibles** : Version du système d'exploitation, liste des services actifs, temps de fonctionnement de la machine (uptime), informations sur les comptes utilisateurs et détails sur les interfaces réseau.
*   **Critère de Réussite** : Découvrir au moins trois informations sensibles (par exemple, le nom de la machine, son uptime et la liste des processus).

### 5. Énumération LDAP / Active Directory Avancée

LDAP (Lightweight Directory Access Protocol) est le protocole standard pour interroger les services d'annuaire, notamment Active Directory. Une énumération LDAP permet de récupérer une richesse d'informations sur les utilisateurs, les ordinateurs, et la structure organisationnelle du domaine.

#### Étape 5 — Interrogation LDAP avec `ldapsearch`

`ldapsearch` est un outil en ligne de commande permettant d'effectuer des requêtes LDAP.

*   **Commande anonyme** : `ldapsearch -x -H ldap://192.168.56.5 -b "DC=lab,DC=local"` (l'option `-x` permet l'authentification simple, `-H` spécifie l'hôte LDAP, et `-b` définit le *base DN* de la recherche).
*   **Commandes Avancées** :
    *   Rechercher tous les utilisateurs : `ldapsearch -x -H ldap://192.168.56.5 -b "DC=lab,DC=local" "(objectClass=user)" cn`
    *   Rechercher tous les ordinateurs : `ldapsearch -x -H ldap://192.168.56.5 -b "DC=lab,DC=local" "(objectClass=computer)" cn`
*   **Sorties Attendues** : Listes d'utilisateurs et d'ordinateurs, détails sur les unités d'organisation (OU), et parfois des attributs sensibles (comme `pwdLastSet` ou `description`).
*   **Critère de Réussite** : Obtenir au moins dix comptes Active Directory (utilisateurs et ordinateurs).

### 6. Fingerprinting Web Avancé avec WhatWeb

Le *fingerprinting* Web avancé va au-delà de l'identification basique des ports ouverts pour extraire des informations détaillées sur les technologies Web utilisées (versions de CMS, de serveurs Web, de langages de script, plugins).

#### Étape 6 — Analyse approfondie avec `WhatWeb`

`WhatWeb` est un scanner de *fingerprinting* Web capable d'identifier une multitude de technologies.

*   **Commandes** :
    *   `whatweb -a 3 http://192.168.56.20` (l'option `-a` définit le niveau d'agressivité de la recherche, de 1 à 4).
    *   `whatweb --log-json=site.json http://192.168.56.20` (pour exporter les résultats au format JSON, utile pour les rapports).
*   **Options** :
    *   `-a 1/2/3/4` : Niveau d'agressivité de la détection (plus le chiffre est élevé, plus la détection est approfondie).
    *   `--log-json` : Permet d'enregistrer la sortie au format JSON.
*   **Sorties Intéressantes** : Versions de PHP, identification de CMS (WordPress, Joomla!), versions de serveurs Web (Apache, Nginx), et détection de plugins.
*   **Critère de Réussite** : Identifier au moins deux technologies Web spécifiques et une version potentiellement exploitable.

### 7. Fiche d'Exposition Système

La **Fiche d'Exposition Système** est un document récapitulatif essentiel pour consolider toutes les informations collectées. Elle servira de base pour les phases d'exploitation ultérieures.

| IP           | OS              | Comptes          | Groupes               | Partages                     | Services             | Vulnérabilités | Notes             |
| :----------- | :-------------- | :--------------- | :-------------------- | :--------------------------- | :------------------- | :------------- | :---------------- |
| 192.168.56.5 | Windows Server 2019 | admin, svc_print, test | Domain Admins, Users | SYSVOL, NETLOGON, ADMIN$, PUBLIC | SMB, LDAP, Kerberos  | Null session SMB ok | Cible AD, Dev       |
| 192.168.56.10 | Debian 11       | root, user_ftp   | ssh, ftp              | /var/www, /home/user_ftp     | Apache2, SSH, FTP, SNMP | SNMP public community | Serveur Web/FTP |

Cette fiche sera directement utilisée pour :
*   Le Module 8 (Exploitation Linux/Windows)
*   Le Module 9 (Attaques Active Directory)
*   Le Module 10 (Post-exploitation)

## 🧠 Carte Mentale / Schéma```mermaid
graph TD
    A["Énumération Système & Services"] --> B["Objectifs"]
    A --> C["Pré-requis & Outils"]
    A --> D["Procédures Détaillées"]
    D --> D1["Énumération SMB / NetBIOS"]
    D1 --> D1a[("enum4linux-ng")]
    D1 --> D1b[("smbclient")]
    D --> D2["Énumération RPC / AD"]
    D2 --> D2a[("rpcclient")]
    D --> D3["Énumération SNMP"]
    D3 --> D3a[("snmp-check")]
    D --> D4["Énumération LDAP / AD"]
    D4 --> D4a[("ldapsearch")]
    D --> D5["Fingerprinting Web"]
    D5 --> D5a[("WhatWeb")]
    D --> D6["Synthèse : Fiche d'Exposition"]
    D6 --> D6a[("Utilisée pour exploitation")]
```

## ❓ Quiz de Révision (Active Recall)
> [!question] Question 1
> Quel outil est spécifiquement utilisé pour énumérer les comptes, les groupes et les partages SMB/NetBIOS sur une cible, et quelles options permettent de cibler spécifiquement les utilisateurs ou les partages ?
> > [!success]- Réponse
> > L'outil est `enum4linux-ng`. Les options pour cibler sont `-U` pour les utilisateurs et `-S` pour les partages.

> [!question] Question 2
> Comment `rpcclient` peut-il être utilisé pour obtenir des informations d'Active Directory sans authentification préalable ? Nommez au moins deux commandes internes à `rpcclient` qui sont utiles dans ce scénario.
> > [!success]- Réponse
> > `rpcclient` peut être utilisé via une **session nulle** en se connectant avec un utilisateur vide : `rpcclient -U "" -N IP`. Deux commandes internes utiles sont `enumdomusers` (pour énumérer les utilisateurs du domaine) et `enumdomgroups` (pour énumérer les groupes du domaine).

> [!question] Question 3
> Le protocole SNMP, souvent mal configuré, peut révéler des informations sensibles. Quel outil est utilisé pour interroger un agent SNMP et quelles informations clés peut-on espérer obtenir ?
> > [!success]- Réponse
> > L'outil est `snmp-check`. On peut espérer obtenir la version de l'OS, les services en cours, l'uptime, les comptes utilisateurs et les interfaces réseau.

> [!question] Question 4
> Pour le *fingerprinting* Web avancé, quel outil permet d'identifier les technologies (CMS, serveurs Web, plugins) avec différents niveaux d'agressivité, et comment exporter les résultats pour un rapport ?
> > [!success]- Réponse
> > L'outil est `WhatWeb`. L'option `-a` permet de définir le niveau d'agressivité (ex: `-a 3`). Pour exporter les résultats au format JSON, on utilise `--log-json=nom_fichier.json`.

> [!question] Question 5
> Quel est l'objectif principal de la **Fiche d'Exposition Système** et à quoi servira-t-elle dans les modules suivants ?
> > [!success]- Réponse
> > L'objectif principal de la Fiche d'Exposition Système est de consolider toutes les informations collectées lors de l'énumération pour avoir une vue d'ensemble des vulnérabilités potentielles d'une machine. Elle servira de base pour les modules d'exploitation (Linux/Windows), d'attaques Active Directory et de post-exploitation.