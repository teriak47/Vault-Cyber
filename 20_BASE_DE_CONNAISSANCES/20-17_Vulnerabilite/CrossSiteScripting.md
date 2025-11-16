---
tags:
  - vulnerabilite
aliases:
  - Scripting Inter-sites
  - XSS
  - Cross-Site Scripting
archetype: vulnerabilite
cve: 
cvss_score: 0.0
cssclasses:
  - max
source: 
---

# Vulnérabilité : Cross-Site Scripting (XSS)

## 📥 Définition et Impact
> Le [[CrossSiteScripting|Cross-Site Scripting (XSS)]] est une [[Vulnerability|vulnérabilité]] de [[Security|sécurité]] des [[SoftwareApplication|applications web]] qui permet à un [[ThreatActor|attaquant]] d'injecter du [[Malware|code malveillant]] (généralement JavaScript) côté [[Client|client]] dans les pages web vues par d'autres [[User|utilisateurs]]. L'impact peut inclure le [[SessionHijacking|détournement de session]] via le vol de [[HttpCookies|cookies]], le [[DataTheft|vol de données sensibles]], la [[Defacement|défiguration]] de site web, et la [[MalwareDistribution|distribution de logiciels malveillants]].

## 📝 Détails Techniques
*   **Vecteur d'attaque**: L'[[AttackVector|attaque]] exploite une [[Vulnerability|faille]] dans la [[InputValidation|validation]] ou l'[[OutputEncoding|encodage]] des entrées utilisateur. Le [[Malware|code malveillant]] est injecté via des champs de saisie, des paramètres d'[[InternetAddress|URL]], ou stocké dans la [[Database|base de données]] du serveur.
*   **Composant affecté**: Principalement les [[SoftwareApplication|applications web]] et les [[WebBrowsers|navigateurs web]] qui ne traitent pas correctement les [[UnvalidatedInput|entrées non validées]] ou non échappées.
*   **Type de faille (CWE)**: [[CommonWeaknessEnumeration|CWE-79]] - Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')
*   **Types de XSS**:
    *   **Persistant (Stored XSS)**: Le [[Malware|code malveillant]] est stocké sur le [[Server|serveur]] et servi aux [[User|utilisateurs]].
    *   **Reflété (Reflected XSS)**: Le [[Malware|code malveillant]] est réfléchi immédiatement par le [[Server|serveur]] suite à une requête [[Client|client]] spécifique.
    *   **Basé sur le [[DocumentObjectModel|DOM]] (DOM-based XSS)**: La [[Vulnerability|vulnérabilité]] réside côté [[Client|client]], où le [[Script|script]] malveillant modifie le [[DocumentObjectModel|DOM]] de la page directement dans le [[WebBrowsers|navigateur]] de l'[[User|utilisateur]].

## 🛡️ Correctifs et Contournements
*   **Versions patchées**: La [[Vulnerability|vulnérabilité]] est de nature logique, donc des versions spécifiques de [[Software|logiciels]] sont moins pertinentes que des pratiques de [[Programming|programmation]] sécurisées.
*   **Mesures de contournement (Workarounds)**:
    *   Appliquer une [[InputValidation|validation rigoureuse]] de toutes les entrées côté [[Server|serveur]] et, si possible, côté [[Client|client]].
    *   Utiliser l'[[OutputEncoding|encodage contextuel]] approprié pour toutes les sorties affichées sur une page web.
    *   Implémenter des [[ContentSecurityPolicy|Politiques de Sécurité du Contenu (CSP)]] strictes.
    *   Marquer les [[HttpCookies|cookies de session]] avec le [[HttpOnlyFlag|drapeau HttpOnly]] pour empêcher leur accès via JavaScript.
    *   Déployer un [[WebApplicationFirewall|Pare-feu d'Application Web (WAF)]] pour filtrer les [[Attack|attaques]] XSS.
    *   Effectuer des [[CodeReview|revues de code]] et des [[PenetrationTesting|tests d'intrusion]] réguliers.

## 🔍 Comment la détecter ?
*   **Signatures réseau/IDS**: Les [[IntrusionDetectionSystem|IDS]]/[[IntrusionPreventionSystem|IPS]] peuvent être configurés avec des [[SignatureBasedDetection|signatures]] pour détecter des motifs d'injection de scripts courants dans le [[NetworkTrafficAnalysis|trafic réseau]].
*   **Commandes de détection locale**:
    *   Des [[Tool|outils]] de [[PenetrationTesting|test d'intrusion]] comme [[BurpSuite|Burp Suite]] ou [[OWASPZAP|OWASP ZAP]] sont utilisés pour le [[Fuzzing|fuzzing]] et la détection automatisée de [[Vulnerability|vulnérabilités]] XSS.
    *   La [[CodeReview|revue de code]] manuelle est essentielle pour identifier les failles de [[InputValidation|validation]] et d'[[OutputEncoding|encodage]].

## 🔗 Notes Connexes
*   [[WebApplicationSecurity|Sécurité des applications web]]
*   [[SqlInjection|Injection SQL]]
*   [[CrossSiteRequestForgery|Cross-Site Request Forgery (CSRF)]]
*   [[InputValidation|Validation des entrées]]
*   [[OutputEncoding|Encodage de Sortie]]
*   [[ContentSecurityPolicy|Politique de Sécurité du Contenu]]
*   [[HttpOnlyFlag|Drapeau HttpOnly]]
*   [[WebApplicationFirewall|Pare-feu d'Application Web]]
*   [[DocumentObjectModel|Document Object Model (DOM)]]