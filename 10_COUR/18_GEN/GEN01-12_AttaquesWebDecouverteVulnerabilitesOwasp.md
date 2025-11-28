---
cssclasses:
  - max
aliases:
  - "ATTAQUES WEB (Découverte + Vulnérabilités OWASP)"
  - "01-12 | ATTAQUES WEB (Découverte + Vulnérabilités OWASP)"
  - "Web Attacks (Discovery + OWASP Vulnerabilities)"
archetype: cour
module: "GEN (Culture Générale & Hors Cursus)"
tags:
  - attaque/web
  - reconnaissance
  - exploitation
  - fuzzing
  - attaque/force-brute
  - owasp-top-10
  - vulnerabilite/injection
  - vulnerabilite/authentification
  - vulnerabilite/directory-listing
  - vulnerabilite/inclusion-fichiers
  - vulnerabilite/xss
  - vulnerabilite/csrf
  - vulnerabilite/idor
  - vulnerabilite/divulgation
  - outil/gobuster
  - outil/ffuf
  - outil/nikto
  - outil/burp-suite
  - outil/owasp-zap
  - outil/scanner-web
  - labo/environnement-vulnerable
  - logiciel/wordpress
  - protocole/http
  - protocole/https
---

# 01-12 | ATTAQUES WEB (Découverte + Vulnérabilités OWASP)

> [!goal] Objectifs Pédagogiques
> À la fin de cette fiche, je dois être capable de :
> 1. Découvrir les répertoires et *endpoints* cachés à l'aide d'outils comme **Gobuster** et **ffuf**.
> 2. Identifier des vulnérabilités Web de surface avec des scanners comme **Nikto**.
> 3. Intercepter, modifier et rejouer des requêtes HTTP/HTTPS en utilisant **Burp Suite**.
> 4. Lancer un scan actif et passif automatisé d'applications Web avec **OWASP ZAP**.
> 5. Comprendre les principales vulnérabilités de l'OWASP, incluant l'**Injection**, l'**Authentification Brisée**, le *Directory Listing*, l'*Inclusion de Fichiers*, le **XSS**, le **CSRF**, l'**IDOR** et l'**Exposition de Données Sensibles**.

## 📝 Synthèse du Cours

Ce module s'adresse aux niveaux *Débutant* à *Intermédiaire* et a pour but de fournir une introduction pratique aux techniques de découverte de vulnérabilités Web et à la compréhension des failles de sécurité les plus courantes selon l'OWASP. Les cibles typiques pour la pratique incluent des environnements volontairement vulnérables tels que **DVWA**, **Mutillidae**, **WebGoat**, des installations **WordPress** vulnérables, et **Metasploitable2**.

Les **pré-requis** essentiels pour aborder ce module sont la validation des modules 1 à 3, la disponibilité d'au moins un serveur Web vulnérable actif, l'installation des *seclists* (listes de mots utilisées pour le *brute force* et le *fuzzing*), et un environnement **Burp Suite** fonctionnel avec le certificat installé pour l'interception HTTPS.

### 1. Outils Essentiels pour la Découverte et l'Analyse

Pour explorer et identifier les failles de sécurité dans les applications Web, plusieurs outils sont indispensables. Ils permettent d'automatiser des tâches répétitives et de révéler des comportements anormaux ou des configurations dangereuses.

| Outil      | Rôle                                        |
| :--------- | :------------------------------------------ |
| **Gobuster**   | Outil de *brute force* rapide pour découvrir des dossiers, fichiers, sous-domaines DNS, et *buckets* Amazon S3/Google Cloud.        |
| **ffuf**       | Outil de *fuzzing* polyvalent et avancé. Il permet de découvrir du contenu Web caché, des paramètres, des *vhosts* (hôtes virtuels), des *headers* HTTP, et d'autres points d'entrée en utilisant des listes de mots. |
| **Nikto**      | Un scanner de vulnérabilités Web "legacy" mais toujours utile, conçu pour effectuer des tests complets sur les serveurs Web, incluant la détection de plus de 6700 fichiers et programmes CGI/Web potentiellement dangereux, la vérification de versions de serveur obsolètes et de problèmes de configuration spécifiques.     |
| **Burp Suite** | Une suite d'outils intégrés pour effectuer des tests de sécurité sur les applications Web. Il inclut un proxy d'interception, un *repeater* pour rejouer les requêtes, et un *intruder* pour le *brute force* ou le *fuzzing* ciblé. |
| **OWASP ZAP**  | (Zed Attack Proxy) Un scanner de sécurité d'application Web gratuit et open source, maintenu par l'OWASP. Il est conçu pour être utilisé par des experts en sécurité ainsi que par des débutants, offrant des fonctionnalités de scan actif et passif pour trouver automatiquement diverses vulnérabilités. |

### 2. Procédures Détaillées : De la Découverte au Scan Automatisé

L'approche de test de sécurité Web suit une méthodologie structurée, progressant de la reconnaissance initiale à l'analyse approfondie des vulnérabilités.

#### Étape 1 — Découverte des répertoires (*Gobuster*)
L'objectif est de trouver les ressources cachées sur un serveur Web. Cela inclut les pages d'administration, les fichiers de sauvegarde, les répertoires d'upload, ou les scripts de test laissés en production.

```bash
gobuster dir -u http://192.168.56.20 -w /usr/share/seclists/Discovery/Web-Content/common.txt -x php,html,txt -t 20 -k
```
Cette commande utilise `gobuster` pour *brute forcer* les répertoires d'une URL cible, en utilisant une liste de mots commune, en cherchant des extensions `.php`, `.html`, `.txt`, avec 20 *threads* et en ignorant les erreurs TLS. Les résultats attendus sont des *endpoints* tels que `/admin`, `/uploads`, `/backup`, `/test`, `/phpinfo.php`. Le critère de validation est de trouver au moins 5 *endpoints*.

#### Étape 2 — *Fuzzing* avancé (*ffuf*)
Le *fuzzing* avec `ffuf` permet de tester des paramètres, des fichiers, des *vhosts* ou des *headers* HTTP pour découvrir des points faibles ou des comportements inattendus.

1.  **Découverte de répertoires :**
    `ffuf -u http://192.168.56.20/FUZZ -w /usr/share/seclists/Discovery/Web-Content/common.txt`
2.  **Fuzzing de paramètres GET :**
    `ffuf -u "http://192.168.56.20/index.php?FUZZ=test" -w /usr/share/seclists/Fuzzing/parameters.txt`
3.  **Fuzzing VHOSTs :**
    `ffuf -u http://192.168.56.20/ -H "Host: FUZZ.lab.local" -w wordlist.txt`

Le critère est d'identifier au moins 3 comportements anormaux, indiquant des réactions spécifiques du serveur à des entrées malveillantes ou inattendues.

#### Étape 3 — Scan de vulnérabilités Web (*Nikto*)
Nikto est utilisé pour détecter des configurations dangereuses ou des versions logicielles obsolètes sur le serveur Web, qui peuvent être exploitées.

```bash
nikto -h http://192.168.56.20
```
Les résultats peuvent inclure des fichiers sensibles exposés, des versions de logiciels vulnérables, des *headers* HTTP non sécurisés ou des *CGI* obsolètes. Il faut identifier au moins 2 vulnérabilités avec cet outil.

#### Étape 4 — **Burp Suite** (Proxy, Repeater, Intruder)
**Burp Suite** permet la manipulation manuelle et détaillée des requêtes HTTP/HTTPS, ce qui est crucial pour comprendre et tester les interactions client-serveur.

1.  **Configuration du proxy :** Le navigateur est configuré pour passer par le proxy de Burp (généralement 127.0.0.1:8080). L'interception doit être activée dans Burp.
2.  **Interception d'une requête HTTP :** En naviguant vers une page et en interagissant (ex: envoi d'un formulaire de connexion), la requête est capturée dans Burp pour analyse (méthode, *headers*, *cookies*, corps).
3.  **Repeater (tests manuels) :** Les requêtes capturées peuvent être envoyées au *Repeater* pour être modifiées et rejouées manuellement. C'est utile pour tester des changements de paramètres, la suppression de *cookies* ou des injections simples comme `' OR '1'='1`.
4.  **Intruder (*bruteforce* HTTP) :** Le module *Intruder* permet de réaliser des attaques automatisées, telles que le *bruteforce* de formulaires de connexion en insérant des *payloads* dans des positions spécifiques de la requête.

Le critère est de trouver un comportement vulnérable (ex: *login bypass*, *XSS*, *IDOR*) grâce à ces manipulations.

#### Étape 5 — **OWASP ZAP** (scan actif/passif)
**OWASP ZAP** automatise le processus de scan de sécurité en explorant l'application (*spidering*) et en lançant des attaques actives et passives.

1.  **Démarrer ZAP :** `zaproxy &`
2.  **Mode "Automated Scan" :** Après avoir entré l'URL cible, ZAP procède à un *spider* pour découvrir l'application, puis un *Active Scan* pour identifier les vulnérabilités.

ZAP peut révéler des vulnérabilités telles que le *XSS*, le *CSRF*, l'**Injection**, des configurations dangereuses, des *cookies* non sécurisés ou des *headers* manquants. Le critère est d'identifier au moins 3 failles OWASP.

### 3. Vulnérabilités Web OWASP : Comprendre les Risques

L'**OWASP (Open Web Application Security Project)** est une communauté en ligne qui produit des articles, des méthodologies, de la documentation, des outils et des technologies librement disponibles dans le domaine de la sécurité des applications Web. Le "OWASP Top 10" est un document de sensibilisation standard pour les développeurs et les professionnels de la sécurité Web, listant les 10 risques de sécurité les plus critiques pour les applications Web.

#### Injection
> [!note] Définition Clé
> L'**Injection** est une vulnérabilité où des données non fiables sont envoyées à un interpréteur dans le cadre d'une commande ou d'une requête. Les données hostiles de l'attaquant peuvent amener l'interpréteur à exécuter des commandes involontaires ou à accéder à des données sans autorisation.
>
> **Exemples courants** : *SQL Injection* (SQLi), *NoSQL Injection*, *OS Command Injection*, *LDAP Injection*.

#### Authentification Brisée (Broken Authentication)
> [!note] Définition Clé
> L'**Authentification Brisée** fait référence à des implémentations incorrectes des fonctions liées à l'authentification et à la gestion des sessions, permettant aux attaquants de compromettre les identifiants, de voler des sessions ou d'usurper l'identité d'autres utilisateurs.
>
> **Exemples courants** : Attaques par *brute force*, utilisation de faibles identifiants, sessions non sécurisées (non expiration, ID prévisibles), contournement de la logique d'authentification.

#### Directory Listing (Listage de Répertoire)
> [!note] Définition Clé
> Le **Directory Listing** est une vulnérabilité qui se produit lorsque le serveur Web est configuré pour afficher le contenu d'un répertoire s'il ne trouve pas de page d'index (par exemple, `index.html` ou `index.php`). Cela peut exposer des fichiers sensibles ou la structure interne du serveur à un attaquant.
>
> **Exemples courants** : Accès à des fichiers de configuration, fichiers de sauvegarde, codes sources non compilés, fichiers temporaires.

#### Inclusion de Fichiers (File Inclusion)
> [!note] Définition Clé
> L'**Inclusion de Fichiers** permet à un attaquant d'inclure un fichier, généralement en exploitant une fonction de script sur le serveur Web. Il existe deux types principaux :
> *   **Local File Inclusion (LFI)** : L'attaquant peut inclure des fichiers situés sur le serveur local.
> *   **Remote File Inclusion (RFI)** : L'attaquant peut inclure des fichiers provenant d'une source externe, souvent sous son contrôle.
>
> **Exemples courants** : Injection de *shell* Web, lecture de fichiers système sensibles, exécution de code arbitraire.

#### XSS (Cross-Site Scripting)
> [!note] Définition Clé
> Le **Cross-Site Scripting (XSS)** est une vulnérabilité Web qui permet aux attaquants d'injecter des scripts côté client (généralement JavaScript) dans les pages Web consultées par d'autres utilisateurs. Cela peut voler des informations de session, défigurer des sites Web ou rediriger des utilisateurs malveillamment.
>
> **Types principaux** : *Reflected XSS* (non persistant), *Stored XSS* (persistant), *DOM-based XSS*.

#### CSRF (Cross-Site Request Forgery)
> [!note] Définition Clé
> Le **Cross-Site Request Forgery (CSRF)** est une attaque qui force l'utilisateur final à exécuter des actions indésirables sur une application Web à laquelle il est déjà authentifié. Si la victime est connectée au site, son navigateur peut envoyer une requête forgée, qui est traitée comme une requête légitime.
>
> **Exemples courants** : Changement de mot de passe, transfert d'argent, modification d'adresse e-mail sans consentement de l'utilisateur.

#### IDOR (Insecure Direct Object Reference)
> [!note] Définition Clé
> L'**Insecure Direct Object Reference (IDOR)** se produit lorsqu'une application expose une référence directe à un objet d'implémentation interne (comme un fichier, une base de données ou une clé d'URL) sans vérifier les autorisations suffisantes de l'utilisateur. Un attaquant peut manipuler ces références pour accéder à des ressources non autorisées.
>
> **Exemples courants** : Accès aux comptes d'autres utilisateurs en modifiant un ID dans l'URL, accès à des documents ou fichiers privés en modifiant un chemin de fichier.

#### Exposition de Données Sensibles (Sensitive Data Exposure)
> [!note] Définition Clé
> L'**Exposition de Données Sensibles** survient lorsque les applications Web ne protègent pas adéquatement les données sensibles, telles que les informations financières, les informations de santé, ou les identifiants personnels. Les attaquants peuvent voler ou modifier ces données mal protégées pour réaliser des fraudes par carte de crédit, le vol d'identité, ou d'autres crimes.
>
> **Exemples courants** : Données en transit non chiffrées, mots de passe stockés en clair, données non supprimées après utilisation, manque de contrôles d'accès aux données.

### 4. Fiche d'exposition Web
Une fiche d'exposition Web est un document synthétique qui récapitule les vulnérabilités découvertes lors d'un audit de sécurité. Elle inclut des détails cruciaux pour comprendre et corriger les failles, tels que l'URL concernée, les chemins identifiés, les services actifs, les vulnérabilités spécifiques, les technologies utilisées et des notes additionnelles.

| URL                        | Paths trouvés    | Services | Vulnérabilités                         | Techno     | Notes      |
| :------------------------- | :--------------- | :------- | :------------------------------------- | :--------- | :--------- |
| http://192.168.56.20/admin | /admin/backup/uploads | PHP Apache | XSS, SQLi pot., CSRF                  | PHP 7.2 | Cible Web 1 |

## 🧠 Carte Mentale / Schéma
```mermaid
graph TD
    Start["Découverte & Analyse des Vulnérabilités Web"] --> A[Réconnaissance Initiale];

    A --> B[Découverte de Contenu (Gobuster)];
    A --> C[Fuzzing Avancé (ffuf)];
    A --> D[Scan de Vulnérabilités (Nikto)];

    B --> E[Collecte d'Endpoints Cachés];
    C --> F[Identification de Comportements Anormaux];
    D --> G[Détection de Configs Dangereuses];

    E & F & G --> H[Analyse Manuelle (Burp Suite)];
    H --> I[Interception & Modification Requêtes];
    H --> J[Repeater: Tests d'Injections];
    H --> K[Intruder: Brute Force HTTP];

    I & J & K --> L[Scan Automatisé (OWASP ZAP)];
    L --> M[Spidering & Active Scan];
    M --> N[Identification Failles OWASP];

    N --> O[Rédaction Fiche d'Exposition];
    O --> End[Validation du Module];

    subgraph Outils
        B --> GobusterTool["Gobuster"];
        C --> FfufTool["ffuf"];
        D --> NiktoTool["Nikto"];
        H --> BurpSuiteTool["Burp Suite"];
        L --> ZapTool["OWASP ZAP"];
    end

    subgraph Vulnérabilités OWASP
        N --> OWASP["Compréhension Vulnérabilités OWASP"];
        OWASP --> Inject["Injection"];
        OWASP --> AuthBroken["Authentification Brisée"];
        OWASP --> DirListing["Directory Listing"];
        OWASP --> FileIncl["File Inclusion"];
        OWASP --> XSSVuln["XSS"];
        OWASP --> CSRFVuln["CSRF"];
        OWASP --> IDORVuln["IDOR"];
        OWASP --> DataExp["Exposition Données Sensibles"];
    end

```

## ❓ Quiz de Révision (Active Recall)

> [!question] Question 1
> Quel outil est principalement utilisé pour le *brute force* de répertoires et de fichiers sur un serveur Web, et quelle option permet de spécifier des extensions de fichiers à rechercher ?
> > [!success]- Réponse
> > L'outil est **Gobuster**. L'option pour spécifier les extensions de fichiers est `-x` (ex: `gobuster dir -u http://IP -w wordlist.txt -x php,html`).

> [!question] Question 2
> Expliquez la différence entre une vulnérabilité *Local File Inclusion (LFI)* et *Remote File Inclusion (RFI)*.
> > [!success]- Réponse
> > Une vulnérabilité **LFI** permet à un attaquant d'inclure et d'exécuter des fichiers situés sur le serveur local, tandis qu'une vulnérabilité **RFI** permet à un attaquant d'inclure et d'exécuter des fichiers provenant d'une source externe, souvent sous son contrôle.

> [!question] Question 3
> Quel module de **Burp Suite** permet de modifier manuellement une requête HTTP interceptée et de la rejouer plusieurs fois pour tester des injections simples ?
> > [!success]- Réponse
> > Le module est le **Repeater**.

> [!question] Question 4
> Citez au moins trois types de vulnérabilités que **OWASP ZAP** est capable d'identifier automatiquement lors d'un *Active Scan*.
> > [!success]- Réponse
> > OWASP ZAP peut identifier automatiquement des vulnérabilités telles que le **XSS**, le **CSRF**, l'**Injection**, des configurations dangereuses, des *cookies* non sécurisés et des *headers* manquants.

> [!question] Question 5
> Qu'est-ce que l'**IDOR** et comment un attaquant pourrait-il l'exploiter concrètement ?
> > [!success]- Réponse
> > L'**IDOR** (Insecure Direct Object Reference) est une vulnérabilité où une application expose une référence directe à un objet interne sans vérifier les autorisations. Un attaquant pourrait l'exploiter en modifiant une valeur numérique ou textuelle dans l'URL (ex: `?id=123` en `?id=124`) pour accéder à des données ou des fonctions d'un autre utilisateur ou à des ressources non autorisées.