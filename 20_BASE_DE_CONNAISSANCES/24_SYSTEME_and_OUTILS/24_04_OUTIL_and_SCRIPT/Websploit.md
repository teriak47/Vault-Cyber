---
aliases:
  - Websploit
  - Web Exploitation Tool
  - Web Pentesting Tool
  - Outil d'exploitation web
  - Outil de pentesting web
  - Web exploitation framework
archetype: outil
site_web:
  - https://github.com/websploit/websploit
langage:
  - Python
cssclasses:
  - max
tags:
  - websploit
  - outil
  - pentesting
  - framework
  - exploitation
  - securite/web
  - reconnaissance
  - analyse/vulnerabilite
  - ingenierie-sociale
  - phishing
  - langage/bash
  - langage/python
  - attaque/deni-de-service
  - logiciel/apache
  - detection
  - detection/ids
  - detection/ips
  - outil/edr
  - protection/antivirus
  - processus
  - analyse/trafic-reseau
  - protocole/http
  - protocole/https
  - port
  - fichier
  - log/event-id
  - systeme-exploitation/windows
  - serveur/web
---

# Websploit

> [!abstract] Description
> Websploit est un **cadre d'exploitation web** et un outil de **pentesting** inspiré de Metasploit. Il fournit une collection de modules pour la *reconnaissance*, l'analyse de *vulnérabilités*, l'exploitation de *serveurs web*, ainsi que des attaques de *social engineering*, notamment le *phishing web*. Il est conçu pour simplifier les tâches d'évaluation de sécurité liées aux applications et infrastructures web.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales
> ```bash
> # Lancer le framework Websploit
> websploit
> 
> # Afficher tous les modules disponibles
> show modules
> 
> # Utiliser un module spécifique (ex: web/apache/mod_negotiation_dos)
> use [chemin/du/module]
> 
> # Afficher les options configurables du module sélectionné
> show options
> 
> # Définir une option (ex: set TARGET http://example.com)
> set [OPTION] [VALEUR]
> 
> # Exécuter le module
> run
> ```

## 📦 Installation
```bash
# Debian/Kali (souvent préinstallé ou disponible via git)
sudo apt update
sudo apt install websploit

# Installation via Git / Source (recommandé pour la dernière version ou si non disponible via apt)
git clone https://github.com/websploit/websploit.git
cd websploit
# Installer les dépendances Python (souvent pour Python 2.x, vérifier les besoins)
pip install -r requirements.txt
# Ou si vous rencontrez des problèmes, essayez `pip2 install -r requirements.txt`
```

## ⚙️ Cas d'usage Détaillés

### 1. Exploitation d'un serveur web (ex: DoS Apache)
Ce cas d'usage démontre comment utiliser Websploit pour tenter une attaque par déni de service (DoS) sur un serveur Apache vulnérable en exploitant le module `mod_negotiation`.

```bash
websploit
use web/apache/mod_negotiation_dos
show options
set TARGET http://192.168.1.100:80/
set THREADS 100
run
```

### 2. Création d'une page de phishing web
Websploit peut être utilisé pour cloner des pages web existantes et mettre en place un serveur de phishing local, pour des exercices de social engineering contrôlés.

```bash
websploit
use web/phishing/web_phisher
show options
set URL https://www.exemple-de-site.com/login
set OUTPUT_PATH /var/www/html/phish_page/
run
```

### 3. Scan de répertoires d'un site web
Cet exemple montre comment utiliser un module auxiliaire pour scanner les répertoires d'un site web à la recherche de fichiers et de chemins cachés ou intéressants.

```bash
websploit
use web/auxiliary/dir_scanner
show options
set TARGET http://192.168.1.101/
set WORDLIST /usr/share/wordlists/dirb/common.txt
run
```

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> *   **Bruit** : Les modules de scanning et d'exploitation actifs peuvent générer un trafic réseau significatif, rendant l'outil *bruyant* et facilement détectable par les IDS/IPS.
> *   **Détection** : L'usage de modules d'exploitation et de scripts de phishing peut être détecté par des solutions de sécurité (AV/EDR) basées sur des signatures ou des comportements anormaux.
> *   **Stabilité** : Certains modules d'exploitation de vulnérabilités peuvent entraîner des instabilités ou des *plantages* (crashs) sur les systèmes cibles, notamment lors d'attaques DoS. Utiliser avec prudence et uniquement sur des systèmes autorisés.

## 🕵️‍♂️ Détection & Chasse (Blue Team)
Comment repérer l'usage de cet outil dans les logs ?

> [!bug] Artefacts & Signatures
> *   **Processus** : Recherche de processus Python exécutant des scripts nommés `websploit.py` ou des scripts liés à ses modules (`phisher.py`, `scanner.py`, etc.).
> *   **Réseau** :
    *   **Requêtes HTTP/S** : Trafic suspect vers des répertoires sensibles (`admin/`, `backup/`) ou des tentatives répétées d'accès à des URL non existantes (404) si un scanner de répertoires est utilisé.
    *   **User-Agent** : Certains modules peuvent utiliser des User-Agents par défaut spécifiques, ou des User-Agents qui ne correspondent pas à des navigateurs légitimes.
    *   **Ports** : Activité sortante inhabituelle vers des ports spécifiques ou des schémas de connexion anormaux.
> *   **Fichiers** : Création de fichiers temporaires, de logs d'exploitation, ou de pages clonées (HTML, CSS, JS) sur des systèmes compromis ou sur la machine de l'attaquant si l'outil est mal configuré.
> *   **Logs Windows** :
    *   **Event ID 4688** (Création de processus) : Recherche de `python.exe` avec des arguments suspects ou des chemins de fichiers de Websploit.
    *   **Event ID 5156/5157** (Filtrage de plateforme) : Activité réseau bloquée ou autorisée vers des cibles inhabituelles.