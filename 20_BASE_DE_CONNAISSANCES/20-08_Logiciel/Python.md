---
tags:
  - logiciel
  - langage-de-programmation
  - scripting
aliases:
  - Python
  - Langage Python
archetype: logiciel
version:
cssclasses:
  - max
---

# Logiciel : Python

## 🎯 Rôle et Fonction
> [[Python|Python]] est un langage de [[Programming|programmation]] de haut niveau, interprété et polyvalent, connu pour sa syntaxe claire et lisible. Il est largement utilisé dans le développement web, l'[[Automation|automatisation]] de tâches, l'analyse de [[Data|données]], l'[[MachineLearning|apprentissage automatique]], l'[[Cybersecurity|cybersécurité]] (pour le développement d'[[Tool|outils]] et l'[[Exploitation|exploitation]] de [[Vulnerability|vulnérabilités]]), et bien plus encore.

## ⚙️ Configuration
* **Fichiers de configuration clés**:
  * `pip.ini` (Windows) ou `pip.conf` (Linux/macOS) : pour configurer le gestionnaire de paquets [[Pip|pip]].
  * `.venv/` ou `env/` : répertoire typique pour les [[VirtualEnvironment|environnements virtuels]] isolant les dépendances de projet.
* **Modules importants**:
  * **Standard Library**: `os`, `sys`, `subprocess`, `json`, `re`.
  * **Librairies tierces courantes**: `requests` (HTTP), `Django` (web), `Flask` (web), `pandas` (données), `numpy` (calcul numérique), `scikit-learn` (ML).
* **Dépendances**: Nécessite un [[OperatingSystem|système d'exploitation]] (par exemple, [[Linux]], [[Windows]], [[MacOS]]).

## 🔒 Sécurisation (Durcissement / Hardening)
* **[[SecureCodingPractices|Pratiques de codage sécurisé]]**:
  * Valider et désinfecter toutes les [[UnvalidatedInput|entrées non validées]] pour prévenir les [[SqlInjection|injections SQL]], les [[CrossSiteScripting|XSS]] et autres [[AttackVector|vecteurs d'attaque]].
  * Éviter l'utilisation de `eval()` avec des entrées utilisateur, qui peut mener à l'[[RemoteCodeExecution|exécution de code à distance]].
  * Gérer les erreurs de manière sécurisée pour éviter de divulguer des [[SensitiveData|informations sensibles]].
* **[[VulnerabilityManagement|Gestion des dépendances]]**:
  * Maintenir les librairies et paquets [[Python|Python]] à jour pour corriger les [[SoftwareVulnerability|vulnérabilités logicielles]] connues.
  * Utiliser des outils comme `pip-audit` pour vérifier les dépendances par rapport aux bases de données de [[CommonVulnerabilitiesAndExposures|CVE]].
  * Mettre en œuvre la [[SoftwareSupplyChainSecurity|sécurité de la chaîne d'approvisionnement logicielle]] pour les composants [[OpenSource|open source]].
* **[[PrincipleOfLeastPrivilege|Principe du moindre privilège]]**: Exécuter les [[Process|processus]] [[Python|Python]] avec les permissions minimales nécessaires sur le [[System|système]].
* **[[VirtualEnvironment|Environnements virtuels]]**: Isoler les dépendances de chaque projet pour éviter les conflits et limiter la surface d'[[AttackSurface|attaque]].
* **[[CodeReview|Revue de code]]**: Effectuer des revues de code régulières pour identifier les failles de [[Security|sécurité]] et les [[SoftwareBugs|bugs logiciels]].

## 🔍 Audit et Surveillance
* **Logs importants**:
  * Les logs d'applications [[Python|Python]] configurés (souvent dans `/var/log/` sur [[Linux]] ou des emplacements spécifiques pour les applications web).
  * Les journaux d'erreurs et de sortie standard (`stderr`, `stdout`) de l'application.
* **Commandes d'audit**:
```bash
# Vérifier la version de Python
python --version

# Lister les paquets Python installés
pip list

# Vérifier les dépendances pour les problèmes
pip check

# Auditer les dépendances pour les vulnérabilités connues (nécessite l'installation de pip-audit)
pip install pip-audit
pip-audit
```

## 🔗 Notes Connexes
* [[Programming|Programmation]]
* [[Script|Script informatique]]
* [[OperatingSystem|Système d'exploitation]]
* [[SoftwareVulnerability|Vulnérabilité Logicielle]]
* [[SoftwareBugs|Bugs Logiciels]]
* [[SoftwareSupplyChainSecurity|Sécurité de la chaîne d'approvisionnement logicielle]]
* [[Exploit|Exploit]]
* [[Malware|Logiciel malveillant]]
* [[Automation|Automatisation]]
* [[ThreatActor|Acteur de menace]] (souvent utilise [[Python|Python]] pour ses [[Attack|attaques]])
* [[SecureCodingPractices|Pratiques de codage sécurisé]] (concept à créer si non existant)
* [[VirtualEnvironment|Environnement Virtuel]] (concept à créer si non existant)
* [[Pip|Pip]] (gestionnaire de paquets, concept à créer si non existant)
* [[OpenSource|Open Source]]
* [[WebDevelopment|Développement Web]] (concept à créer si non existant)
* [[DataScience|Science des Données]] (concept à créer si non existant)
* [[MachineLearning|Apprentissage Automatique]]
* [[CommonVulnerabilitiesAndExposures|Vulnérabilités connues (CVEs)]]
* [[PrincipleOfLeastPrivilege|Principe du moindre privilège]]
* [[CodeReview|Revue de Code]]
* [[RemoteCodeExecution|Exécution de Code à Distance]]
* [[SqlInjection|Injection SQL]]
* [[CrossSiteScripting|Scripting Inter-sites (XSS)]]
* [[UnvalidatedInput|Entrée Non Validée]]
* [[VulnerabilityManagement|Gestion des Vulnérabilités]]
* [[SensitiveData|Données Sensibles]]
* [[AttackVector|Vecteur d'attaque]]
* [[AttackSurface|Surface d'attaque]]
* [[Linux|Linux]]
* [[Windows|Windows]]
* [[MacOS|macOS]]