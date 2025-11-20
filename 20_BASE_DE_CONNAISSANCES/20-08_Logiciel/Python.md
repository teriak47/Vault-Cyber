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
> Python est un langage de programmation de haut niveau, interprété et polyvalent, connu pour sa syntaxe claire et lisible. Il est largement utilisé dans le développement web, l'automatisation de tâches, l'analyse de données, l'apprentissage automatique, l'cybersécurité (pour le développement d'outils et l'exploitation de vulnérabilités), et bien plus encore.

## ⚙️ Configuration
* **Fichiers de configuration clés**:
  * `pip.ini` (Windows) ou `pip.conf` (Linux/macOS) : pour configurer le gestionnaire de paquets pip.
  * `.venv/` ou `env/` : répertoire typique pour les environnements virtuels isolant les dépendances de projet.
* **Modules importants**:
  * **Standard Library**: `os`, `sys`, `subprocess`, `json`, `re`.
  * **Librairies tierces courantes**: `requests` (HTTP), `Django` (web), `Flask` (web), `pandas` (données), `numpy` (calcul numérique), `scikit-learn` (ML).
* **Dépendances**: Nécessite un système d'exploitation (par exemple, Linux, Windows, MacOS).

## 🔒 Sécurisation (Durcissement / Hardening)
* **Pratiques de codage sécurisé**:
  * Valider et désinfecter toutes les entrées non validées pour prévenir les injections SQL, les XSS et autres vecteurs d'attaque.
  * Éviter l'utilisation de `eval()` avec des entrées utilisateur, qui peut mener à l'exécution de code à distance.
  * Gérer les erreurs de manière sécurisée pour éviter de divulguer des informations sensibles.
* **Gestion des dépendances**:
  * Maintenir les librairies et paquets Python à jour pour corriger les vulnérabilités logicielles connues.
  * Utiliser des outils comme `pip-audit` pour vérifier les dépendances par rapport aux bases de données de CVE.
  * Mettre en œuvre la sécurité de la chaîne d'approvisionnement logicielle pour les composants open source.
* **Principe du moindre privilège**: Exécuter les processus Python avec les permissions minimales nécessaires sur le système.
* **Environnements virtuels**: Isoler les dépendances de chaque projet pour éviter les conflits et limiter la surface d'attaque.
* **Revue de code**: Effectuer des revues de code régulières pour identifier les failles de sécurité et les bugs logiciels.

## 🔍 Audit et Surveillance
* **Logs importants**:
  * Les logs d'applications Python configurés (souvent dans `/var/log/` sur Linux ou des emplacements spécifiques pour les applications web).
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
* Programmation
* Script informatique
* Système d'exploitation
* Vulnérabilité Logicielle
* Bugs Logiciels
* Sécurité de la chaîne d'approvisionnement logicielle
* Exploit
* Logiciel malveillant
* Automatisation
* Acteur de menace (souvent utilise Python pour ses attaques)
* Pratiques de codage sécurisé (concept à créer si non existant)
* Environnement Virtuel (concept à créer si non existant)
* Pip (gestionnaire de paquets, concept à créer si non existant)
* Open Source
* Développement Web (concept à créer si non existant)
* Science des Données (concept à créer si non existant)
* Apprentissage Automatique
* Vulnérabilités connues (CVEs)
* Principe du moindre privilège
* Revue de Code
* Exécution de Code à Distance
* Injection SQL
* Scripting Inter-sites (XSS)
* Entrée Non Validée
* Gestion des Vulnérabilités
* Données Sensibles
* Vecteur d'attaque
* Surface d'attaque
* Linux
* Windows
* macOS