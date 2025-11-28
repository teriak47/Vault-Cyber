---
aliases:
  - Greenbone Security Manager
  - GVM
  - OpenVAS
  - Scanner de Vulnérabilités
  - Plateforme de gestion des vulnérabilités
  - Vulnerability Management Platform
  - Vulnerability Scanner
archetype: outil
site_web:
  - https://www.greenbone.net
  - https://www.openvas.org
langage:
  - C
  - Python
  - Perl
cssclasses:
  - max
tags:
  - outil/greenbone
  - outil/openvas
  - analyse/vulnerabilite
  - vulnerabilite/gestion
  - audit-securite
  - conformite
  - commande
  - installation-logiciel
  - logiciel/docker
  - reseau/securite
  - detection
  - blue-team
  - gestion_des_risques
  - pentest/scanning
  - norme
---

# Greenbone

> [!abstract] Description
> **Greenbone** est une suite logicielle et une plateforme complète de gestion des vulnérabilités, incluant le scanner de vulnérabilités open-source **OpenVAS (Open Vulnerability Assessment System)**. Elle est conçue pour l'audit de sécurité, l'identification et l'évaluation des failles de sécurité sur les réseaux et systèmes. Greenbone est un outil essentiel pour les professionnels de la **cybersécurité** souhaitant réaliser des audits proactifs et maintenir une posture de sécurité robuste.

## ⚡ Cheat Sheet Express
> [!tip] Commandes Vitales (via `gvm-cli` pour interaction à distance/scripting)
> ```bash
> # Afficher les cibles existantes
> gvm-cli tls --gmp-username admin --gmp-password <password> --socketpath /run/gvmd/gvmd.sock get targets
> 
> # Créer une nouvelle cible de scan
> gvm-cli tls --gmp-username admin --gmp-password <password> --socketpath /run/gvmd/gvmd.sock \
>   create target --name "My Target" --hosts "192.168.1.10,192.168.1.20"
> 
> # Démarrer un scan avec une configuration par défaut (full and fast)
> # Nécessite l'ID de la cible, du scanner et de la configuration (récupérables via 'get targets', 'get scanners', 'get configs')
> # Exemple hypothétique : target_id='...', scanner_id='...', config_id='...'
> gvm-cli tls --gmp-username admin --gmp-password <password> --socketpath /run/gvmd/gvmd.sock \
>   create task --name "My First Scan" --target target_id --scanner scanner_id --config config_id
> ```

## 📦 Installation
```bash
# Debian/Kali (Installation de la suite Greenbone Vulnerability Management)
# Cette commande installe OpenVAS et les composants nécessaires
sudo apt update
sudo apt install openvas

# Initialiser et configurer Greenbone (peut prendre du temps pour les mises à jour des NVT)
sudo gvm-setup
sudo gvm-check-setup # Vérifier la configuration et l'état des services

# Utilisation via Docker (Greenbone Community Edition - GCE)
# Cette méthode est souvent plus simple pour une mise en place rapide
docker pull greenbone/gsa:stable
docker run -d -p 80:80 -p 443:443 -p 9390:9390 -p 9392:9392 --name greenbone-community-edition greenbone/gsa:stable
# Accéder à l'interface web via HTTPS (port 443 ou 9392 selon la configuration Docker)
```

## ⚙️ Cas d'usage Détaillés

### 1. Scan de Vulnérabilités Réseau Standard
Greenbone est principalement utilisé pour identifier les vulnérabilités sur les hôtes et services d'un réseau. Cela inclut les systèmes d'exploitation, les applications web, les bases de données et les périphériques réseau.

```bash
# Les actions sont généralement effectuées via l'interface web (Greenbone Security Assistant - GSA) :
# 1. Naviguer vers Scans -> Targets et créer une nouvelle cible (IPs, plages CIDR).
# 2. Naviguer vers Scans -> Tasks et créer une nouvelle tâche en sélectionnant la cible, le scanner et la configuration de scan (ex: "Full and fast").
# 3. Démarrer la tâche et consulter les rapports générés pour analyser les vulnérabilités détectées.
# (Pas de commande shell directe pour un scan complet depuis l'interface)
```

### 2. Audit de Conformité et Reporting
La plateforme Greenbone permet de réaliser des audits de conformité par rapport à des standards (PCI DSS, ISO 27001) et de générer des rapports détaillés pour prouver cette conformité ou identifier les écarts.

```bash
# Les actions sont généralement effectuées via l'interface web GSA :
# 1. Sélectionner une configuration de scan adaptée aux standards de conformité.
# 2. Exécuter un scan.
# 3. Générer des rapports personnalisés (ex: PDF, XML) en filtrant les résultats pour la conformité.
# 4. Exporter les rapports pour documentation et preuve d'audit.
# (Pas de commande shell directe ; l'export se fait depuis l'interface)
```

## ⚠️ Limitations & OPSEC
> [!warning] Attention
> *   **Bruit** : Un scan Greenbone est un processus **bruyant**. Il génère un volume important de trafic réseau et peut déclencher des alertes sur les IDS/IPS. Il est facilement identifiable comme une activité de scan.
> *   **Détection** : L'activité de Greenbone est très facilement **détectable** par les systèmes de défense (pare-feu, IDS/IPS, SIEM) en raison de la nature active et intrusive de ses contrôles.
> *   **Stabilité** : Les scans agressifs, en particulier sur des systèmes anciens, mal configurés ou à faible ressource, peuvent potentiellement provoquer des **ralentissements** ou des **plantages** de services. Il est crucial de tester les scans dans des environnements contrôlés avant de les appliquer à la production.

## 🕵️‍♂️ Détection & Chasse (Blue Team)
Comment repérer l'usage de cet outil dans les logs ?

> [!bug] Artefacts & Signatures
> *   **Processus** : Sur un système Linux hébergeant Greenbone, la présence de processus comme `gvmd` (Greenbone Vulnerability Management Daemon), `openvassd` (OpenVAS Scanner Daemon), `gsa` (Greenbone Security Assistant - l'interface web) est un indicateur clé.
> *   **Réseau** :
    *   Un grand nombre de connexions sortantes vers diverses applications (ports 21, 22, 23, 80, 443, 139, 445, etc.) initiées par l'adresse IP du scanner.
    *   Tentatives de connexion à des ports non standards.
    *   Paquets avec des User-Agents ou des en-têtes HTTP spécifiques liés à OpenVAS.
    *   Trafic de type "scan de ports" (SYN scans, TCP connect scans).
> *   **Fichiers** : Création de fichiers temporaires ou de logs dans `/var/lib/gvm/` ou `/var/log/gvm/`. Les rapports de scan sont stockés dans la base de données de Greenbone mais peuvent être exportés sous divers formats sur le système du client.
> *   **Logs Windows** :
    *   Événements de connexion/déconnexion multiples et rapides (Event ID 4624/4625 pour échecs d'authentification) provenant de l'IP du scanner.
    *   Augmentation de l'utilisation des ressources CPU/mémoire sur les machines cibles pendant les scans.
    *   Événements liés à l'activité de services spécifiques ciblés par les Network Vulnerability Tests (NVTs).