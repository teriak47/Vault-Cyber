---
aliases:
  - Vulnérabilité de Sécurité
  - Security Vulnerability
  - Vulnerabilities
  - Failles de sécurité
  - Weaknesses
archetype: concept-general
cssclasses:
  - max
tags:
  - vulnerabilite
  - definition
  - menace
  - modele/cia-triade
  - confidentialite
  - integrite
  - disponibilite
  - cvss
  - vulnerabilite/owasp-top-10
  - vulnerabilite/erreur/code
  - vulnerabilite/mauvaise-configuration
  - vulnerabilite/erreur/conception
  - ingenierie-sociale
  - vulnerabilite/injection-sql
  - vulnerabilite/xss
  - vulnerabilite/authentification
  - vulnerabilite/gestion-session
  - vulnerabilite/deserialisation
  - vulnerabilite/buffer-overflow
  - vulnerabilite/acces/controle
  - vulnerabilite/xxe
---

# Security Vulnerabilities

## 📥 Description Technique
Une **vulnérabilité de sécurité** est une faiblesse ou un défaut dans la conception, la mise en œuvre, le fonctionnement ou la configuration d'un système informatique, d'une application ou d'un réseau, qui peut être exploité par un acteur malveillant (attaquant) pour compromettre la confidentialité, l'intégrité ou la disponibilité des données ou des ressources. Ces failles peuvent résider dans le code, la configuration, l'architecture du système, ou même dans les processus opérationnels. Elles représentent un maillon faible qu'une menace peut utiliser pour causer des dommages. La présence d'une vulnérabilité ne signifie pas qu'une attaque a eu lieu ou est imminente, mais elle indique un risque potentiel si une menace l'exploite. Une vulnérabilité est souvent distinguée d'une **exploit**, qui est le code ou la technique utilisée pour tirer parti de la vulnérabilité, et d'une **menace**, qui est la capacité ou l'intention d'un acteur de causer des dommages.

## 📊 Classification des Vulnérabilités

Les vulnérabilités peuvent être classifiées de plusieurs manières, notamment par leur origine, leur type technique, leur impact, ou leur exploitabilité.

### Par Type Technique (Exemples de CWE - Common Weakness Enumeration)
*   **Erreurs de code/logiciel** : Failles dues à des erreurs de programmation (ex: dépassements de tampon, injections SQL, XSS).
*   **Mauvaise configuration** : Paramètres par défaut non sécurisés, services inutiles activés, permissions incorrectes.
*   **Erreurs de conception** : Faiblesses inhérentes à l'architecture du système ou de l'application.
*   **Défaillances humaines** : Ingénierie sociale, erreurs d'utilisateurs.

### Par Impact sur la Triade CIA (Confidentialité, Intégrité, Disponibilité)
*   **Confidentialité** : L'accès non autorisé à des informations sensibles (ex: divulgation de données).
*   **Intégrité** : La modification ou la destruction non autorisée de données (ex: corruption de base de données).
*   **Disponibilité** : L'interruption de l'accès à un système ou à des données (ex: attaque par déni de service - DDoS).

### Par Score CVSS (Common Vulnerability Scoring System)
Le CVSS est un cadre standard ouvert permettant de communiquer les caractéristiques et la gravité des vulnérabilités logicielles. Il attribue un score numérique (de 0 à 10) qui peut être utilisé pour évaluer la criticité d'une vulnérabilité. Il se compose de trois groupes métriques :
*   **Base** : Représente les caractéristiques intrinsèques de la vulnérabilité (ex: vecteur d'attaque, complexité de l'attaque, impact sur la CIA).
*   **Temporel** : Reflète les caractéristiques qui évoluent au fil du temps (ex: existence de preuves de concept, disponibilité de patchs).
*   **Environnemental** : Tient compte des caractéristiques spécifiques à l'environnement de l'utilisateur.

## 💥 Exemples Courants de Vulnérabilités

De nombreuses vulnérabilités sont régulièrement découvertes et documentées. Les exemples suivants sont parmi les plus répandus et souvent exploités :

*   **Injection SQL (SQLi)** : Permet à un attaquant d'insérer des requêtes SQL malveillantes dans un champ de saisie d'une application web, menant à la lecture, la modification ou la suppression de données de la base de données, voire à l'exécution de commandes sur le serveur.
*   **Cross-Site Scripting (XSS)** : Consiste à injecter des scripts côté client (généralement JavaScript) dans des pages web visualisées par d'autres utilisateurs. Cela peut permettre le vol de cookies de session, la redirection vers des sites malveillants ou la dégradation de l'expérience utilisateur.
*   **Broken Authentication and Session Management (Authentification et gestion de session défaillantes)** : Faiblesses dans les fonctions d'authentification ou de gestion des sessions, permettant aux attaquants d'usurper l'identité d'autres utilisateurs (ex: par force brute, vol de session, contournement de l'authentification).
*   **Insecure Deserialization (Désérialisation non sécurisée)** : Permet à un attaquant d'exécuter du code arbitraire sur le serveur en manipulant des objets sérialisés. C'est une vulnérabilité particulièrement dangereuse pouvant mener à une exécution de code à distance (RCE).
*   **Buffer Overflow (Dépassement de tampon)** : Se produit lorsqu'un programme tente d'écrire plus de données dans un bloc de mémoire tampon qu'il ne peut en contenir. Cela peut écraser les données adjacentes, causer des plantages ou permettre l'exécution de code arbitraire.
*   **Missing Function Level Access Control (Contrôle d'accès au niveau des fonctions manquant)** : Une application ne vérifie pas correctement les droits d'un utilisateur avant d'accorder l'accès à certaines fonctionnalités. Un attaquant peut ainsi accéder à des fonctions d'administration ou à des données sensibles auxquelles il ne devrait pas avoir droit.
*   **XML External Entities (XXE)** : Failles liées au traitement des entités externes dans les analyseurs XML. Un attaquant peut exploiter ces entités pour divulguer des fichiers locaux, exécuter des attaques SSRF, scanner des ports internes ou exécuter des commandes à distance.

## 🛡️ Patch & Mitigation (Principes Généraux)

La gestion des vulnérabilités est un processus continu visant à identifier, évaluer, traiter et rendre compte des failles de sécurité.

### Correctif Officiel
*   **Application de patchs et mises à jour** : Le moyen le plus efficace de corriger une vulnérabilité est d'appliquer les correctifs et mises à jour de sécurité fournis par les éditeurs de logiciels ou les développeurs.
*   **Mise à jour des configurations** : Appliquer les bonnes pratiques de sécurité pour la configuration des systèmes, des applications et des réseaux.

### Contournement (Workaround)
Si un correctif n'est pas immédiatement disponible, des mesures d'atténuation (workarounds) peuvent être mises en place :
*   **Désactivation de fonctionnalités** : Désactiver temporairement des services ou des fonctions vulnérables.
*   **Filtrage réseau** : Utiliser des pare-feu ou des WAF (Web Application Firewalls) pour bloquer les requêtes malveillantes.
*   **Segmentation réseau** : Isoler les systèmes vulnérables pour limiter l'étendue d'une potentielle exploitation.
*   **Renforcement des politiques de sécurité** : Appliquer le principe du moindre privilège, renforcer les politiques de mot de passe.

## 🔍 Détection
Pour savoir si un système est vulnérable, diverses méthodes et outils sont utilisés :
*   **Scanners de vulnérabilités** : Outils automatisés qui analysent les systèmes et applications à la recherche de failles connues (ex: Nessus, OpenVAS).
*   **Tests d'intrusion (Pentesting)** : Des experts simulent des attaques pour identifier les vulnérabilités exploitables et évaluer la robustesse des défenses.
*   **Audits de code** : Examen manuel ou automatisé du code source pour y détecter des faiblesses.
*   **Bug Bounty Programs** : Inciter les chercheurs en sécurité à découvrir et signaler des vulnérabilités de manière responsable.

## 🔗 Références
*   OWASP Top 10 : [https://owasp.org/www-project-top-ten/](https://owasp.org/www-project-top-ten/)
*   NIST National Vulnerability Database (NVD) : [https://nvd.nist.gov/](https://nvd.nist.gov/)
*   Common Weakness Enumeration (CWE) : [https://cwe.mitre.org/](https://cwe.mitre.org/)
*   MITRE ATT&CK Framework : [https://attack.mitre.org/](https://attack.mitre.org/)