---
tags:
  - attaque
  - attaque/injection-sql
  - manipulation/donnees
  - base-de-donnees
  - securite/donnees
aliases:
  - Injection SQL
  - SQL Injection
  - SQLi
  - Structured Query Language Injection
archetype: attaque
source:
  - 
cssclasses:
  - max
---

# Injection SQL

## 📥 Définition
> L'[[SqlInjection|Injection SQL]] est une [[Attack|attaque]] qui exploite des [[SoftwareVulnerability|vulnérabilités logicielles]] dans le code d'une [[SoftwareApplication|application]] pour injecter des requêtes [[StructuredQueryLanguage|SQL]] (new link) malveillantes dans une [[Database|base de données]], permettant un [[UnauthorizedAccess|accès non autorisé]] ou une [[Tampering|manipulation de données]].

## 🎯 Vecteurs d'Attaque
*   **Champs de saisie web**: Formulaires (connexion, recherche), paramètres d'URL où les entrées [[UnvalidatedInput|non validées]] sont utilisées pour construire des requêtes [[StructuredQueryLanguage|SQL]].
*   **Cookies HTTP**: Les données stockées dans les [[HttpCookies|cookies HTTP]] si elles sont intégrées directement dans les requêtes [[StructuredQueryLanguage|SQL]] sans vérification.
*   **En-têtes HTTP**: Certains en-têtes (ex: User-Agent, Referer) peuvent être vulnérables si l'[[SoftwareApplication|application]] les utilise dans des requêtes [[StructuredQueryLanguage|SQL]].

## 💥 Impacts Potentiels
*   [[UnauthorizedAccess|Accès non autorisé]] à la [[Database|base de données]] et aux [[System|systèmes]] sous-jacents.
*   [[DataExfiltration|Exfiltration de données]] sensibles (informations d'[[UserIdentity|identité]] des [[User|utilisateurs]], [[Password|mots de passe]], informations financières, etc.).
*   [[DataCorruption|Altération de données]] (modification, suppression de [[Data|registres]] importants).
*   [[Authentication|Contournement de l'authentification]], permettant à un [[ThreatActor|attaquant]] de se connecter sans [[Credential|identifiants]] valides.
*   [[PrivilegeEscalation|Élévation de privilèges]] au sein de la [[Database|base de données]] ou du [[OperatingSystem|système d'exploitation]].
*   [[RemoteCodeExecution|Exécution de code à distance]] sur le [[Server|serveur]] de la [[Database|base de données]] (selon la configuration et les privilèges).

##  concret
> Un [[ThreatActor|attaquant]] trouve un formulaire de recherche sur un [[WebServer|site web]] qui ne valide pas correctement les entrées. Au lieu de taper un terme de recherche normal, il entre `' OR '1'='1' --`. Si l'[[SoftwareApplication|application]] construit la requête [[StructuredQueryLanguage|SQL]] comme `SELECT * FROM produits WHERE nom LIKE '%` + `entrée_utilisateur` + `%'`, l'injection transformerait la requête en `SELECT * FROM produits WHERE nom LIKE '%' OR '1'='1' --%'`. Le `' OR '1'='1'` est toujours vrai, et `--` commente la fin de la requête originale, permettant à l'attaquant de récupérer toutes les informations de la table sans avoir à se connecter ou à connaître des critères spécifiques.

## 🛡️ Mesures de Mitigation
*   **Prévention** :
    *   **[[PreparedStatements|Requêtes préparées]] et paramétrées**: Utiliser des requêtes préparées avec des paramètres pour toutes les interactions avec la [[Database|base de données]], empêchant l'interprétation des entrées utilisateur comme du code [[StructuredQueryLanguage|SQL]].
    *   **[[InputValidation|Validation des entrées]]**: Valider et nettoyer rigoureusement toutes les entrées utilisateur côté [[Client|client]] et [[Server|serveur]] (filtrage, échappement des caractères spéciaux).
    *   **[[PrincipleOfLeastPrivilege|Principe du moindre privilège]]**: Configurer les comptes d'[[Database|accès à la base de données]] avec les privilèges minimaux nécessaires.
    *   **[[CodeReview|Revue de code]]**: Effectuer des revues de code régulières et des [[PenetrationTesting|tests d'intrusion]] pour identifier les [[SoftwareVulnerability|vulnérabilités]].
    *   **[[WebApplicationFirewall|Pare-feu applicatif web (WAF)]]** (new link): Déployer un WAF pour filtrer le trafic malveillant avant qu'il n'atteigne l'[[SoftwareApplication|application]].
*   **Détection** :
    *   [[IntrusionDetectionSystem|Systèmes de détection d'intrusion (IDS)]] et [[IntrusionPreventionSystem|systèmes de prévention d'intrusion (IPS)]] pour surveiller les motifs d'[[Attack|attaque]].
    *   [[SecurityMonitoring|Surveillance de sécurité]] et analyse des [[Log|journaux]] de la [[Database|base de données]] et de l'[[WebServer|application web]].
*   **Réponse** :
    *   [[IncidentResponse|Plan de réponse à incident]] pour réagir rapidement aux [[DigitalAttack|attaques]].
    *   Correction immédiate des [[SoftwareVulnerability|vulnérabilités]] découvertes.

## 🔗 Notes Connexes
*   [[Vulnerability|Vulnérabilité]]
*   [[Database|Base de données]]
*   [[WebApplicationSecurity|Sécurité des applications web]] (new link)
*   [[CrossSiteScripting|Cross-Site Scripting (XSS)]]
*   [[RemoteCodeExecution|Exécution de Code à Distance (RCE)]]
*   [[DataExfiltration|Exfiltration de données]]
*   [[UnvalidatedInput|Entrée Non Validée]]