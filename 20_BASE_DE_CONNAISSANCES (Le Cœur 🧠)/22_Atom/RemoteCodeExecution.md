---
tags:
  - vulnerabilite/deserialisation
  - vulnerabilite/rce
  - securite/sandboxing
  - impact/execution-code-distance
  - cybersécurité/exploitation-vulnerabilite
  - vulnerabilite/logicielle
aliases:
  - Exécution de Code à Distance
  - RCE
  - Remote Code Execution
source: null
cssclasses:
  - max
---
# Exécution de Code à Distance (RCE)  
  
## 📥 Définition en une phrase  
  
> L’**Exécution de Code à Distance (Remote Code Execution, RCE)** est une vulnérabilité qui permet à un attaquant d’exécuter arbitrairement du code malveillant sur une machine distante, souvent à travers un réseau, compromettant ainsi le système visé.  
  
## 🧠 Concepts Clés / Fonctionnement  
  
* **Par injection de commandes ou de code** : L’attaquant exploite une faille dans une application (ex : faille de désérialisation, injection SQL, vulnérabilité dans un parser, etc.) qui lui permet de fournir du code ou des commandes malveillantes.  
* **Prise de contrôle du serveur ou de l’hôte** : Une fois le code exécuté, l’attaquant peut obtenir un shell, installer des backdoors, voler des données, ou étendre son accès.  
* **Exposition réseau** : RCE est généralement exploitée via un service exposé (web, API, serveur applicatif) accessible à distance.  
* **Différents vecteurs d’attaque** : Incluent les attaques via des injections, traitements de fichiers malicieux, vulnérabilités dans les frameworks ou composants tiers.  
* **Impact souvent critique** : RCE est considérée comme une vulnérabilité d’une criticité très élevée dans les évaluations de sécurité (ex : CVSS proche de 10).  
  
## 🛡️ Risques / Menaces Associés  
  
* [[PrivilegeEscalation|Escalade de privilèges]] suite à l’exécution de code initiale  
* [[InitialAccess|Accès initial]] d’une chaîne d’attaque (exploitation RCE pour installer un [[Backdoor|backdoor]])  
* Déploiement de [[Malware]] (ex: [[Ransomware]])  
* [[DataBreach|Fuite de données]] sensibles  
* Possibilité de déni de service par exploitation inappropriée ou crash lié au code exécuté  
  
## 💎 Mesures de Protection / Bonnes Pratiques  
  
* [[SecurityControl|Contrôles rigoureux de validation et nettoyage des entrées utilisateur]] (input validation/sanitization)  
* Application de [[PatchManagement|correctifs de sécurité]] et mise à jour régulière des composants logiciels  
* Réduction au strict minimum des privilèges des services exposés (principe de moindre privilège)  
* Utilisation de sandboxing et d’environnements d’exécution sécurisés pour isoler les processus exposés  
* Surveillance des logs, détection d’anomalies et mise en place d’IDS/IPS  
* Utilisation de solutions de [[ApplicationSecurity|sécurité applicative]], comme le WAF (Web Application Firewall)  
* Tests de sécurité réguliers : audits, pentests et analyses de vulnérabilités  
  
## 🔗 Notes Connexes  
  
* [[CodeInjection|Injection de Code]]  
* [[DeserializationAttack|Attaque par Désérialisation]]  
* [[VulnerabilityManagement|Gestion des Vulnérabilités]]  
* [[ExploitDevelopment|Développement d’Exploits]]  
* [[SecurityPatch|Correctif de Sécurité]]