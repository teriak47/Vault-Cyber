---
tags:
  - attaque
  - attaque/web/xss
  - injection/script
  - securite/web
aliases:
  - XSS
  - Cross-Site Scripting
  - Faille XSS
  - Attaque XSS
archetype: attaque
mitre_id: T1190
source:
  - OWASP
  - MITRE ATT&CK
cssclasses:
  - max
---

# Cross-Site Scripting (XSS)

> [!summary] En Bref
> Une attaque [[CrossSiteScripting|Cross-Site Scripting (XSS)]] est un type d'[[DigitalAttack|attaque numérique]] où des scripts malveillants sont injectés dans des [[WebApplication|applications web]] légitimes via des [[Vulnerability|vulnérabilités]], puis exécutés dans le [[WebBrowser|navigateur]] de la victime.

## 🔬 Analyse Technique

### Fonctionnement
L'[[CrossSiteScripting|XSS]] exploite des [[WebApplication|applications web]] qui ne valident pas ou n'encodent pas correctement les [[UserInput|données utilisateur]] avant de les afficher. Un attaquant injecte un [[MaliciousScript|script malveillant]] (souvent en JavaScript) dans le flux d'une page web. Lorsque la page est chargée par le [[WebBrowser|navigateur]] d'une victime, ce script est exécuté côté [[Client|client]], ce qui permet à l'attaquant de voler des [[HttpCookies|cookies]] de session, de dégrader le site, de rediriger l'utilisateur, ou d'effectuer d'autres actions au nom de la victime.

> [!example] Scénario Concret (XSS Refléchi)
> 1.  **Reconnaissance** : L'attaquant identifie une application web acceptant des entrées utilisateur non validées (ex: un champ de recherche).
> 2.  **Armement** : L'attaquant insère un script malveillant (ex: `<script>alert(document.cookie)</script>`) dans une URL malveillante : `https://exemple.com/recherche?q=<script>alert(document.cookie)</script>`.
> 3.  **Exploitation** : L'utilisateur clique sur un [[MaliciousLink|lien malveillant]] contenant le [[Payload|payload]] XSS. Le serveur reflète le script dans la réponse HTML. Le navigateur de la victime exécute le script, compromettant potentiellement sa session en affichant ses cookies.

### 🗺️ Mapping MITRE ATT&CK
*   **Tactique** : [[InitialAccess]], [[Execution]]
*   **Technique** : `T1190` - Exploit Public-Facing Application

## 🎯 Vecteurs d'Attaque
*   **XSS Refléchi (Non-persistent)** : Le script est "reflété" par le serveur suite à une requête utilisateur et exécuté instantanément par le navigateur sans être [[DataStorage|stocké]]. L'attaque nécessite une interaction de la victime (ex: cliquer sur un lien).
*   **XSS Stocké (Persistent)** : Le script est stocké de manière persistante sur le serveur (ex: dans une [[Database|base de données]]) et délivré à chaque fois que la page affectée est consultée. Ce type est plus dangereux car il ne nécessite pas d'interaction directe pour chaque victime.
*   **XSS Basé sur le DOM (DOM-based)** : L'attaque se déroule entièrement côté client. Le script est exécuté en manipulant le Document Object Model (DOM) de la page web, sans interaction directe avec le serveur pour l'injection initiale.

## 🛡️ Stratégies de Défense

### 🧱 Prévention (Hardening)
> [!tip] Bonnes Pratiques
> *   [[InputValidation|Validation stricte des entrées]] : Toutes les données utilisateur doivent être validées, nettoyées et encodées avant d'être affichées ou traitées. Utiliser des listes blanches plutôt que des listes noires.
> *   [[OutputEncoding|Encodage des sorties]] : Appliquer l'encodage HTML approprié à toutes les données avant de les insérer dans le document HTML pour éviter l'interprétation de caractères spéciaux comme du code.
> *   [[ContentSecurityPolicy|Content Security Policy (CSP)]] : Utiliser un [[ContentSecurityPolicy|CSP]] pour restreindre les sources de contenu que le navigateur est autorisé à charger et à exécuter, réduisant ainsi l'impact d'une injection de script.
> *   Utiliser des [[WebApplicationFirewall|WAF]] : Un [[WebApplicationFirewall|WAF]] peut filtrer et bloquer les requêtes malveillantes avant qu'elles n'atteignent l'application.

### 🚨 Détection (Hunting)
> [!info] Signatures & Logs
> *   **[[SecurityMonitoring|Surveillance des logs]]** du WAF pour des [[AttackPattern|attaques XSS]].
> *   **[[SecurityMonitoring|Surveillance]] des [[WebLogs|journaux d'accès]]** du serveur web pour des [[AttackPattern|séquences suspectes]] ou des payloads XSS (ex: `<script>`, `onerror`, `javascript:`).
> *   Utilisation de [[IntrusionDetectionSystem|IDS]] / [[IntrusionPreventionSystem|IPS]] pour détecter et alerter sur les tentatives d'injection de scripts.

### 🚒 Réponse à Incident
1.  **Isolation** : Identifier et bloquer immédiatement la [[NetworkSource|source de l'attaque]] (adresse IP de l'attaquant) si possible. Désactiver temporairement la fonctionnalité ou la page web vulnérable.
2.  **Eradication** : Supprimer le script injecté de la base de données ou de tout autre système de stockage. Appliquer les correctifs (patches) nécessaires à l'application web pour corriger la [[Vulnerability|vulnérabilité]].
3.  **Récupération** : Rétablir le service après avoir vérifié que toutes les vulnérabilités sont corrigées et que les scripts malveillants ont été complètement supprimés.

## 🔗 Connexions
*   **Variante** : [[SQLInjection]], [[CSRF]]
*   **Outil lié** : [[BurpSuite]], [[OWASPZAP]]